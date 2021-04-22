---
title: Déployer les mises à jour de Microsoft Defender pour Endpoint sur Linux
ms.reviewer: ''
description: Décrit comment déployer des mises à jour pour Microsoft Defender pour Endpoint sur Linux dans les environnements d'entreprise.
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, linux, mises à jour, déployer
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
ms.openlocfilehash: 9cb0c7375b538f502cf6165f13c68fd4b2fdcc64
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934752"
---
# <a name="deploy-updates-for-microsoft-defender-for-endpoint-on-linux"></a><span data-ttu-id="34973-104">Déployer les mises à jour de Microsoft Defender pour Endpoint sur Linux</span><span class="sxs-lookup"><span data-stu-id="34973-104">Deploy updates for Microsoft Defender for Endpoint on Linux</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="34973-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="34973-105">**Applies to:**</span></span>
- [<span data-ttu-id="34973-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="34973-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="34973-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="34973-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="34973-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="34973-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="34973-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="34973-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigateip-abovefoldlink)

<span data-ttu-id="34973-110">Microsoft publie régulièrement des mises à jour logicielles pour améliorer les performances, la sécurité et fournir de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="34973-110">Microsoft regularly publishes software updates to improve performance, security, and to deliver new features.</span></span>

> [!WARNING]
> <span data-ttu-id="34973-111">Chaque version de Defender pour Endpoint sur Linux a une date d'expiration, après laquelle elle ne continuera plus à protéger votre appareil.</span><span class="sxs-lookup"><span data-stu-id="34973-111">Each version of Defender for Endpoint on Linux has an expiration date, after which it will no longer continue to protect your device.</span></span> <span data-ttu-id="34973-112">Vous devez mettre à jour le produit avant cette date.</span><span class="sxs-lookup"><span data-stu-id="34973-112">You must update the product prior to this date.</span></span> <span data-ttu-id="34973-113">Pour vérifier la date d'expiration, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="34973-113">To check the expiration date, run the following command:</span></span>
> ```bash
> mdatp health --field product_expiration
> ```

<span data-ttu-id="34973-114">Pour mettre à jour Defender pour Endpoint sur Linux manuellement, exécutez l'une des commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="34973-114">To update Defender for Endpoint on Linux manually, execute one of the following commands:</span></span>

## <a name="rhel-and-variants-centos-and-oracle-linux"></a><span data-ttu-id="34973-115">RHEL et variantes (CentOS et Oracle Linux)</span><span class="sxs-lookup"><span data-stu-id="34973-115">RHEL and variants (CentOS and Oracle Linux)</span></span>

```bash
sudo yum update mdatp
```

## <a name="sles-and-variants"></a><span data-ttu-id="34973-116">SLES et variantes</span><span class="sxs-lookup"><span data-stu-id="34973-116">SLES and variants</span></span>

```bash
sudo zypper update mdatp
```

## <a name="ubuntu-and-debian-systems"></a><span data-ttu-id="34973-117">Systèmes Ubuntu et Debian</span><span class="sxs-lookup"><span data-stu-id="34973-117">Ubuntu and Debian systems</span></span>

```bash
sudo apt-get install --only-upgrade mdatp
```
