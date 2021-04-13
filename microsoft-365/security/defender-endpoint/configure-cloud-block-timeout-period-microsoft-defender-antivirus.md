---
title: Configurer le délai d'attente du blocage du cloud de l'Antivirus Microsoft Defender
description: Vous pouvez configurer la durée pendant combien de temps l'Antivirus Microsoft Defender bloquera l'exécution d'un fichier en attendant une détermination du cloud.
keywords: Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, defender, cloud, délai d'attente, bloc, période, secondes
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
ms.localizationpriority: medium
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 7ec134c2861b0185f66a08257fbc410b7a475b5a
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51690451"
---
# <a name="configure-the-cloud-block-timeout-period"></a><span data-ttu-id="1f9f8-104">Configurer le délai d'attente du blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="1f9f8-104">Configure the cloud block timeout period</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1f9f8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1f9f8-105">**Applies to:**</span></span>

- [<span data-ttu-id="1f9f8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1f9f8-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="1f9f8-107">Lorsque l'Antivirus Microsoft Defender trouve un fichier suspect, il peut empêcher l'exécution du fichier pendant qu'il interroge le service cloud de [l'Antivirus Microsoft Defender.](cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="1f9f8-107">When Microsoft Defender Antivirus finds a suspicious file, it can prevent the file from running while it queries the [Microsoft Defender Antivirus cloud service](cloud-protection-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="1f9f8-108">La période par défaut de blocage [du](configure-block-at-first-sight-microsoft-defender-antivirus.md) fichier est de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-108">The default period that the file will be [blocked](configure-block-at-first-sight-microsoft-defender-antivirus.md) is 10 seconds.</span></span> <span data-ttu-id="1f9f8-109">Vous pouvez spécifier une période supplémentaire d'attente avant que le fichier ne soit autorisé à s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-109">You can specify an additional period of time to wait before the file is allowed to run.</span></span> <span data-ttu-id="1f9f8-110">Cela permet de s'assurer qu'il y a suffisamment de temps pour recevoir une détermination appropriée du service cloud de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-110">This can help ensure there is enough time to receive a proper determination from the Microsoft Defender Antivirus cloud service.</span></span>

## <a name="prerequisites-to-use-the-extended-cloud-block-timeout"></a><span data-ttu-id="1f9f8-111">Conditions préalables à l'utilisation du délai d'accès au blocage étendu du cloud</span><span class="sxs-lookup"><span data-stu-id="1f9f8-111">Prerequisites to use the extended cloud block timeout</span></span>

<span data-ttu-id="1f9f8-112">[Bloquer à la première vue](configure-block-at-first-sight-microsoft-defender-antivirus.md) et ses conditions préalables doivent être activées avant de pouvoir spécifier un délai d'attente étendu.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-112">[Block at first sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) and its prerequisites must be enabled before you can specify an extended timeout period.</span></span>

## <a name="specify-the-extended-timeout-period"></a><span data-ttu-id="1f9f8-113">Spécifier le délai d'attente étendu</span><span class="sxs-lookup"><span data-stu-id="1f9f8-113">Specify the extended timeout period</span></span>

<span data-ttu-id="1f9f8-114">Vous pouvez utiliser la stratégie de groupe pour spécifier un délai d'accès étendu pour les vérifications dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-114">You can use Group Policy to specify an extended timeout for cloud checks.</span></span>

1. <span data-ttu-id="1f9f8-115">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="1f9f8-115">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="1f9f8-116">Dans **l'Éditeur de gestion des stratégies de** groupe, cliquez sur **Configuration** ordinateur et cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="1f9f8-116">In the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="1f9f8-117">Développez l'arborescence **des composants Windows > l'Antivirus Microsoft Defender > MpEngine**</span><span class="sxs-lookup"><span data-stu-id="1f9f8-117">Expand the tree to **Windows components > Microsoft Defender Antivirus > MpEngine**</span></span>

4. <span data-ttu-id="1f9f8-118">Double-cliquez **sur Configurer la vérification cloud étendue** et assurez-vous que l'option est activée.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-118">Double-click **Configure extended cloud check** and ensure the option is enabled.</span></span> <span data-ttu-id="1f9f8-119">Spécifiez la durée supplémentaire pour empêcher l'exécution du fichier en attendant une détermination du cloud.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-119">Specify the additional amount of time to prevent the file from running while waiting for a cloud determination.</span></span> <span data-ttu-id="1f9f8-120">Vous pouvez spécifier la durée supplémentaire, en secondes, entre 1 seconde et 50 secondes.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-120">You can specify the additional time, in seconds, from 1 second to 50 seconds.</span></span> <span data-ttu-id="1f9f8-121">Cette durée est ajoutée aux 10 secondes par défaut.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-121">This time will be added to the default 10 seconds.</span></span>

5. <span data-ttu-id="1f9f8-122">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f9f8-122">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f9f8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f9f8-123">Related topics</span></span>

- [<span data-ttu-id="1f9f8-124">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="1f9f8-124">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="1f9f8-125">Utiliser les technologies antivirus de nouvelle génération par le biais d'une protection cloud</span><span class="sxs-lookup"><span data-stu-id="1f9f8-125">Use next-generation antivirus technologies through cloud-delivered protection</span></span>](cloud-protection-microsoft-defender-antivirus.md)
- [<span data-ttu-id="1f9f8-126">Configurer bloquer à la première vue</span><span class="sxs-lookup"><span data-stu-id="1f9f8-126">Configure block at first sight</span></span>](configure-block-at-first-sight-microsoft-defender-antivirus.md)
- [<span data-ttu-id="1f9f8-127">Activer la protection cloud</span><span class="sxs-lookup"><span data-stu-id="1f9f8-127">Enable cloud-delivered protection</span></span>](enable-cloud-protection-microsoft-defender-antivirus.md)