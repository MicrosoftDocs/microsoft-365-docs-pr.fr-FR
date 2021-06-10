---
title: Configurer le délai d’Antivirus Microsoft Defender cloud
description: Vous pouvez configurer la durée pendant Antivirus Microsoft Defender’exécution d’un fichier en attendant une détermination du cloud.
keywords: Antivirus Microsoft Defender, logiciel anti-programme malveillant, sécurité, defender, cloud, délai d’attente, bloc, période, secondes
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.date: 06/04/2021
ms.openlocfilehash: dfb75b77119d9550931c3e476323bde67a3b148f
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789086"
---
# <a name="configure-the-cloud-block-timeout-period"></a><span data-ttu-id="64851-104">Configurer le délai de blocage du cloud</span><span class="sxs-lookup"><span data-stu-id="64851-104">Configure the cloud block timeout period</span></span>

<span data-ttu-id="64851-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="64851-105">**Applies to:**</span></span>

- [<span data-ttu-id="64851-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="64851-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="64851-107">Lorsque Antivirus Microsoft Defender trouve un fichier suspect, il peut empêcher l’exécution du fichier pendant qu’il interroge [Antivirus Microsoft Defender service cloud.](cloud-protection-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="64851-107">When Microsoft Defender Antivirus finds a suspicious file, it can prevent the file from running while it queries the [Microsoft Defender Antivirus cloud service](cloud-protection-microsoft-defender-antivirus.md).</span></span>

<span data-ttu-id="64851-108">La période par défaut de blocage [du](configure-block-at-first-sight-microsoft-defender-antivirus.md) fichier est de 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="64851-108">The default period that the file is [blocked](configure-block-at-first-sight-microsoft-defender-antivirus.md) is 10 seconds.</span></span> <span data-ttu-id="64851-109">Si vous êtes administrateur de sécurité, vous pouvez spécifier plus de temps d’attente avant que le fichier ne soit autorisé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="64851-109">If you're a security administrator, you can specify more time to wait before the file is allowed to run.</span></span> <span data-ttu-id="64851-110">L’extension du délai d’attente du blocage du cloud permet de s’assurer qu’il y a suffisamment de temps pour recevoir une détermination appropriée du service cloud Antivirus Microsoft Defender cloud.</span><span class="sxs-lookup"><span data-stu-id="64851-110">Extending the cloud block timeout period can help ensure there is enough time to receive a proper determination from the Microsoft Defender Antivirus cloud service.</span></span>

## <a name="prerequisites-to-use-the-extended-cloud-block-timeout"></a><span data-ttu-id="64851-111">Conditions préalables à l’utilisation du délai d’accès au blocage étendu du cloud</span><span class="sxs-lookup"><span data-stu-id="64851-111">Prerequisites to use the extended cloud block timeout</span></span>

<span data-ttu-id="64851-112">[Bloquer à la première vue](configure-block-at-first-sight-microsoft-defender-antivirus.md) et ses conditions préalables doivent être activées avant de pouvoir spécifier un délai d’attente étendu.</span><span class="sxs-lookup"><span data-stu-id="64851-112">[Block at first sight](configure-block-at-first-sight-microsoft-defender-antivirus.md) and its prerequisites must be enabled before you can specify an extended timeout period.</span></span>

## <a name="specify-the-extended-timeout-period-using-microsoft-endpoint-manager"></a><span data-ttu-id="64851-113">Spécifier le délai d’attente étendu à l’aide Microsoft Endpoint Manager</span><span class="sxs-lookup"><span data-stu-id="64851-113">Specify the extended timeout period using Microsoft Endpoint Manager</span></span>

<span data-ttu-id="64851-114">Vous pouvez spécifier le délai d’attente de blocage du cloud avec une stratégie de sécurité de point de terminaison [dans Microsoft Endpoint Manager](/mem/intune/protect/endpoint-security-policy).</span><span class="sxs-lookup"><span data-stu-id="64851-114">You can specify the cloud block timeout period with an [endpoint security policy in Microsoft Endpoint Manager](/mem/intune/protect/endpoint-security-policy).</span></span>

1. <span data-ttu-id="64851-115">Go to the Endpoint Manager admin center ( [https://endpoint.microsoft.com/](https://endpoint.microsoft.com/) ) and sign in.</span><span class="sxs-lookup"><span data-stu-id="64851-115">Go to the Endpoint Manager admin center ([https://endpoint.microsoft.com/](https://endpoint.microsoft.com/)) and sign in.</span></span>

2. <span data-ttu-id="64851-116">Sélectionnez **Sécurité du point de** terminaison, puis sous **Gérer**, choisissez **Antivirus**.</span><span class="sxs-lookup"><span data-stu-id="64851-116">Select **Endpoint security**, and then under **Manage**, choose **Antivirus**.</span></span>

3. <span data-ttu-id="64851-117">Sélectionnez (ou créez) une stratégie antivirus.</span><span class="sxs-lookup"><span data-stu-id="64851-117">Select (or create) an antivirus policy.</span></span>

4. <span data-ttu-id="64851-118">Dans la **section Paramètres de** configuration, développez **Protection cloud.**</span><span class="sxs-lookup"><span data-stu-id="64851-118">In the **Configuration settings** section, expand **Cloud protection**.</span></span> <span data-ttu-id="64851-119">Ensuite, dans la zone Délai d’out étendu de **Defender Cloud** en secondes, spécifiez la durée, en secondes, entre 1 seconde et 50 secondes.</span><span class="sxs-lookup"><span data-stu-id="64851-119">Then, in the **Defender Cloud Extended Timeout In Seconds** box, specify the more time, in seconds, from 1 second to 50 seconds.</span></span> <span data-ttu-id="64851-120">Tout ce que vous spécifiez est ajouté aux 10 secondes par défaut.</span><span class="sxs-lookup"><span data-stu-id="64851-120">Whatever you specify is added to the default 10 seconds.</span></span>

5. <span data-ttu-id="64851-121">(Cette étape est facultative) A apporter d’autres modifications à votre stratégie antivirus.</span><span class="sxs-lookup"><span data-stu-id="64851-121">(This step is optional) Make any other changes to your antivirus policy.</span></span> <span data-ttu-id="64851-122">(Vous avez besoin d’aide ?</span><span class="sxs-lookup"><span data-stu-id="64851-122">(Need help?</span></span> <span data-ttu-id="64851-123">Voir [Paramètres la stratégie Antivirus Microsoft Defender dans Microsoft Intune.)](/mem/intune/protect/antivirus-microsoft-defender-settings-windows)</span><span class="sxs-lookup"><span data-stu-id="64851-123">See [Settings for Microsoft Defender Antivirus policy in Microsoft Intune](/mem/intune/protect/antivirus-microsoft-defender-settings-windows).)</span></span>

6. <span data-ttu-id="64851-124">Choisissez **Suivant** et terminez la configuration de votre stratégie.</span><span class="sxs-lookup"><span data-stu-id="64851-124">Choose **Next**, and finish configuring your policy.</span></span>

## <a name="specify-the-extended-timeout-period-using-group-policy"></a><span data-ttu-id="64851-125">Spécifier le délai d’attente étendu à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="64851-125">Specify the extended timeout period using Group Policy</span></span>

<span data-ttu-id="64851-126">Vous pouvez utiliser la stratégie de groupe pour spécifier un délai d’accès étendu pour les vérifications dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="64851-126">You can use Group Policy to specify an extended timeout for cloud checks.</span></span>

1. <span data-ttu-id="64851-127">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [console de gestion des stratégies de groupe.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="64851-127">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))</span></span>

2. <span data-ttu-id="64851-128">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="64851-128">Right-click the Group Policy Object you want to configure and then select **Edit**.</span></span>

3. <span data-ttu-id="64851-129">Dans **l’Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur, puis sélectionnez **Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="64851-129">In the **Group Policy Management Editor**, go to **Computer configuration**, and then select **Administrative templates**.</span></span>

3. <span data-ttu-id="64851-130">Développez l’arborescence **Windows composants**  >  **Antivirus Microsoft Defender**  >  **MpEngine**.</span><span class="sxs-lookup"><span data-stu-id="64851-130">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **MpEngine**.</span></span>

4. <span data-ttu-id="64851-131">Double-cliquez **sur Configurer la vérification cloud étendue** et assurez-vous que l’option est activée.</span><span class="sxs-lookup"><span data-stu-id="64851-131">Double-click **Configure extended cloud check** and ensure the option is enabled.</span></span> 

   <span data-ttu-id="64851-132">Spécifiez la durée supplémentaire pour empêcher l’exécution du fichier en attendant une détermination du cloud.</span><span class="sxs-lookup"><span data-stu-id="64851-132">Specify the extra amount of time to prevent the file from running while waiting for a cloud determination.</span></span> <span data-ttu-id="64851-133">Spécifiez le temps supplémentaire, en secondes, entre 1 seconde et 50 secondes.</span><span class="sxs-lookup"><span data-stu-id="64851-133">Specify the extra time, in seconds, from 1 second to 50 seconds.</span></span> <span data-ttu-id="64851-134">Tout ce que vous spécifiez est ajouté aux 10 secondes par défaut.</span><span class="sxs-lookup"><span data-stu-id="64851-134">Whatever you specify is added to the default 10 seconds.</span></span>

5. <span data-ttu-id="64851-135">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="64851-135">Select **OK**.</span></span>

 