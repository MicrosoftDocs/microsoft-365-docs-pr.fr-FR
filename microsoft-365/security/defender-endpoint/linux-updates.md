---
title: Déployer les mises à jour de Microsoft Defender ATP pour Linux
ms.reviewer: ''
description: Décrit comment déployer des mises à jour pour Microsoft Defender ATP pour Linux dans les environnements d’entreprise.
keywords: microsoft, defender, atp, linux, mises à jour, déployer
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
ms.openlocfilehash: ad37427e8134c574690c3b3553d7fb9b8507593c
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187720"
---
# <a name="deploy-updates-for-microsoft-defender-for-endpoint-for-linux"></a><span data-ttu-id="7d4e7-104">Déployer les mises à jour de Microsoft Defender pour endpoint pour Linux</span><span class="sxs-lookup"><span data-stu-id="7d4e7-104">Deploy updates for Microsoft Defender for Endpoint for Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="7d4e7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7d4e7-105">**Applies to:**</span></span>
- [<span data-ttu-id="7d4e7-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7d4e7-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="7d4e7-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="7d4e7-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="7d4e7-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="7d4e7-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="7d4e7-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="7d4e7-110">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-110">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span>

> [!WARNING]
> <span data-ttu-id="7d4e7-111">Chaque version de Defender pour Endpoint pour Linux a une date d’expiration, après laquelle elle ne continuera plus à protéger votre appareil.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-111">Each version of Defender for Endpoint for Linux has an expiration date, after which it will no longer continue to protect your device.</span></span> <span data-ttu-id="7d4e7-112">Vous devez mettre à jour le produit avant cette date.</span><span class="sxs-lookup"><span data-stu-id="7d4e7-112">You must update the product prior to this date.</span></span> <span data-ttu-id="7d4e7-113">Pour vérifier la date d’expiration, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="7d4e7-113">To check the expiration date, run the following command:</span></span>
> ```bash
> mdatp health --field product_expiration
> ```

<span data-ttu-id="7d4e7-114">Pour mettre à jour Defender pour Endpoint pour Linux manuellement, exécutez l’une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d4e7-114">To update Defender for Endpoint for Linux manually, execute one of the following commands:</span></span>

## <a name="rhel-and-variants-centos-and-oracle-linux"></a><span data-ttu-id="7d4e7-115">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="7d4e7-115">RHEL and variants (CentOS and Oracle Linux)</span></span>

```bash
sudo yum update mdatp
```

## <a name="sles-and-variants"></a><span data-ttu-id="7d4e7-116">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="7d4e7-116">SLES and variants</span></span>

```bash
sudo zypper update mdatp
```

## <a name="ubuntu-and-debian-systems"></a><span data-ttu-id="7d4e7-117">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="7d4e7-117">Ubuntu and Debian systems</span></span>

```bash
sudo apt-get install --only-upgrade mdatp
```
