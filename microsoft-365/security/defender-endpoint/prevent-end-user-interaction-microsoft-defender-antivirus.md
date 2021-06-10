---
title: Masquer l’interface Antivirus Microsoft Defender de données
description: Vous pouvez masquer la vignette de protection contre les virus et les menaces dans Sécurité Windows application.
keywords: Verrouillage de l’interface utilisateur, mode sans tête, masquer l’application, masquer les paramètres, masquer l’interface
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 06ee2f1cb68df0a957818e1fccb45628487c39fd
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274915"
---
# <a name="prevent-users-from-seeing-or-interacting-with-the-microsoft-defender-antivirus-user-interface"></a><span data-ttu-id="20c6d-104">Empêcher les utilisateurs de voir ou d’interagir avec l Antivirus Microsoft Defender’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="20c6d-104">Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="20c6d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="20c6d-105">**Applies to:**</span></span>

- [<span data-ttu-id="20c6d-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="20c6d-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="20c6d-107">Vous pouvez utiliser la stratégie de groupe pour empêcher les utilisateurs sur les points de terminaison de voir Antivirus Microsoft Defender interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="20c6d-107">You can use Group Policy to prevent users on endpoints from seeing the Microsoft Defender Antivirus interface.</span></span> <span data-ttu-id="20c6d-108">Vous pouvez également les empêcher de mettre en pause les analyses.</span><span class="sxs-lookup"><span data-stu-id="20c6d-108">You can also prevent them from pausing scans.</span></span>

## <a name="hide-the-microsoft-defender-antivirus-interface"></a><span data-ttu-id="20c6d-109">Masquer l’interface Antivirus Microsoft Defender de données</span><span class="sxs-lookup"><span data-stu-id="20c6d-109">Hide the Microsoft Defender Antivirus interface</span></span>

<span data-ttu-id="20c6d-110">Dans Windows 10 versions 1703, le masquage de l’interface masquera les notifications Antivirus Microsoft Defender et empêchera l’apparition de la vignette de protection contre les menaces & virus dans l’application Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="20c6d-110">In Windows 10, versions 1703, hiding the interface will hide Microsoft Defender Antivirus notifications and prevent the Virus & threat protection tile from appearing in the Windows Security app.</span></span>

<span data-ttu-id="20c6d-111">Avec le paramètre activé **:**</span><span class="sxs-lookup"><span data-stu-id="20c6d-111">With the setting set to **Enabled**:</span></span>

![Capture d’écran Sécurité Windows sans l’icône de bouclier et la section protection contre les virus et menaces](images/defender/wdav-headless-mode-1703.png)

<span data-ttu-id="20c6d-113">Avec le paramètre désactivé **ou** non configuré :</span><span class="sxs-lookup"><span data-stu-id="20c6d-113">With the setting set to **Disabled** or not configured:</span></span>

![Capture d’écran Sécurité Windows l’icône de bouclier et la section protection contre les virus et menaces](images/defender/wdav-headless-mode-off-1703.png)

>[!NOTE]
><span data-ttu-id="20c6d-115">Le masquage de l’interface empêchera Antivirus Microsoft Defender notifications d’apparaître sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="20c6d-115">Hiding the interface will also prevent Microsoft Defender Antivirus notifications from appearing on the endpoint.</span></span> <span data-ttu-id="20c6d-116">Les notifications de Microsoft Defender pour point de terminaison s’affichent toujours.</span><span class="sxs-lookup"><span data-stu-id="20c6d-116">Microsoft Defender for Endpoint notifications will still appear.</span></span> <span data-ttu-id="20c6d-117">Vous pouvez également configurer individuellement [les notifications qui apparaissent sur les points de terminaison](configure-notifications-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="20c6d-117">You can also individually [configure the notifications that appear on endpoints](configure-notifications-microsoft-defender-antivirus.md)</span></span>

<span data-ttu-id="20c6d-118">Dans les versions antérieures de Windows 10, le paramètre masque l’interface Windows Defender client.</span><span class="sxs-lookup"><span data-stu-id="20c6d-118">In earlier versions of Windows 10, the setting will hide the Windows Defender client interface.</span></span> <span data-ttu-id="20c6d-119">Si l’utilisateur tente de l’ouvrir, il reçoit un avertissement signalant que l’administrateur système a un accès restreint à cette application.</span><span class="sxs-lookup"><span data-stu-id="20c6d-119">If the user attempts to open it, they will receive a warning that says, "Your system administrator has restricted access to this app."</span></span>

![Message d’avertissement lorsque le mode sans Windows 10, versions antérieures à 1703](images/defender/wdav-headless-mode-1607.png)

## <a name="use-group-policy-to-hide-the-microsoft-defender-av-interface-from-users"></a><span data-ttu-id="20c6d-121">Utiliser une stratégie de groupe pour masquer l’interface de Microsoft Defender AV aux utilisateurs</span><span class="sxs-lookup"><span data-stu-id="20c6d-121">Use Group Policy to hide the Microsoft Defender AV interface from users</span></span>

1. <span data-ttu-id="20c6d-122">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-122">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="20c6d-123">À **l’aide de l’Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-123">Using the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="20c6d-124">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-124">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="20c6d-125">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender >'interface client.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-125">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span>

5. <span data-ttu-id="20c6d-126">Double-cliquez sur le **paramètre Activer le mode d’interface** utilisateur sans en-tête et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-126">Double-click the **Enable headless UI mode** setting and set the option to **Enabled**.</span></span> <span data-ttu-id="20c6d-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-127">Click **OK**.</span></span> 

<span data-ttu-id="20c6d-128">Voir [Empêcher les utilisateurs de modifier localement](configure-local-policy-overrides-microsoft-defender-antivirus.md) les paramètres de stratégie pour plus d’options pour empêcher les utilisateurs de modifier la protection sur leur PC.</span><span class="sxs-lookup"><span data-stu-id="20c6d-128">See [Prevent users from locally modifying policy settings](configure-local-policy-overrides-microsoft-defender-antivirus.md) for more options on preventing users form modifying protection on their PCs.</span></span>

## <a name="prevent-users-from-pausing-a-scan"></a><span data-ttu-id="20c6d-129">Empêcher les utilisateurs de mettre une analyse en pause</span><span class="sxs-lookup"><span data-stu-id="20c6d-129">Prevent users from pausing a scan</span></span>

<span data-ttu-id="20c6d-130">Vous pouvez empêcher les utilisateurs de mettre en pause les analyses, ce qui peut être utile pour vous assurer que les analyses programmées ou à la demande ne sont pas interrompues par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="20c6d-130">You can prevent users from pausing scans, which can be helpful to ensure scheduled or on-demand scans are not interrupted by users.</span></span>

> [!NOTE]
> <span data-ttu-id="20c6d-131">Ce paramètre n’est pas pris en charge Windows 10.</span><span class="sxs-lookup"><span data-stu-id="20c6d-131">This setting is not supported on Windows 10.</span></span>

### <a name="use-group-policy-to-prevent-users-from-pausing-a-scan"></a><span data-ttu-id="20c6d-132">Utiliser la stratégie de groupe pour empêcher les utilisateurs de mettre une analyse en pause</span><span class="sxs-lookup"><span data-stu-id="20c6d-132">Use Group Policy to prevent users from pausing a scan</span></span>

1. <span data-ttu-id="20c6d-133">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal)de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-133">On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="20c6d-134">À **l’aide de l’Éditeur de gestion des stratégies de** groupe, go to **Computer configuration**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-134">Using the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="20c6d-135">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-135">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="20c6d-136">Développez l’arborescence **Windows composants**  >  **Antivirus Microsoft Defender**  >  **Scan**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-136">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Scan**.</span></span>

5. <span data-ttu-id="20c6d-137">Double-cliquez sur le **paramètre Autoriser les utilisateurs à suspendre** l’analyse et définissez l’option **sur Désactivé.**</span><span class="sxs-lookup"><span data-stu-id="20c6d-137">Double-click the **Allow users to pause scan** setting and set the option to **Disabled**.</span></span> <span data-ttu-id="20c6d-138">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="20c6d-138">Click **OK**.</span></span> 

## <a name="related-articles"></a><span data-ttu-id="20c6d-139">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="20c6d-139">Related articles</span></span>

- [<span data-ttu-id="20c6d-140">Configurer les notifications qui s’affichent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="20c6d-140">Configure the notifications that appear on endpoints</span></span>](configure-notifications-microsoft-defender-antivirus.md)

- [<span data-ttu-id="20c6d-141">Configurer l’interaction de l’utilisateur final avec Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="20c6d-141">Configure end-user interaction with Microsoft Defender Antivirus</span></span>](configure-end-user-interaction-microsoft-defender-antivirus.md)

- [<span data-ttu-id="20c6d-142">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="20c6d-142">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)