---
title: Configurer les notifications de l'Antivirus Microsoft Defender
description: Découvrez comment configurer et personnaliser les notifications standard et supplémentaires de l'Antivirus Microsoft Defender sur les points de terminaison.
keywords: notifications, defender, antivirus, point de terminaison, gestion, administrateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.openlocfilehash: a91da48f27450d6f4a6fd2b9607aa979458ccf71
ms.sourcegitcommit: 7a339c9f7039825d131b39481ddf54c57b021b11
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51765094"
---
# <a name="configure-the-notifications-that-appear-on-endpoints"></a><span data-ttu-id="8dbe9-104">Configurer les notifications qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-104">Configure the notifications that appear on endpoints</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="8dbe9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-105">**Applies to:**</span></span>

- [<span data-ttu-id="8dbe9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="8dbe9-107">Dans Windows 10, les notifications d'application concernant la détection et la correction des programmes malveillants sont plus robustes, cohérentes et concises.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-107">In Windows 10, application notifications about malware detection and remediation are more robust, consistent, and concise.</span></span>

<span data-ttu-id="8dbe9-108">Les notifications apparaissent sur les points de terminaison lorsque des analyses déclenchées et programmées manuellement sont terminées et que des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-108">Notifications appear on endpoints when manually triggered and scheduled scans are completed and threats are detected.</span></span> <span data-ttu-id="8dbe9-109">Ces notifications apparaissent également dans le Centre de **notifications** et un résumé des analyses et des détections de menaces s'affiche à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-109">These notifications also appear in the **Notification Center**, and a summary of scans and threat detections appear at regular time intervals.</span></span>

<span data-ttu-id="8dbe9-110">Vous pouvez également configurer l'apparition des notifications standard sur les points de terminaison, telles que les notifications de redémarrage ou lorsqu'une menace a été détectée et corrigé.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-110">You can also configure how standard notifications appear on endpoints, such as notifications for reboot or when a threat has been detected and remediated.</span></span>

## <a name="configure-the-additional-notifications-that-appear-on-endpoints"></a><span data-ttu-id="8dbe9-111">Configurer les notifications supplémentaires qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-111">Configure the additional notifications that appear on endpoints</span></span>

<span data-ttu-id="8dbe9-112">Vous pouvez configurer l'affichage de notifications supplémentaires, telles que des résumés récents de la détection des menaces, dans l'application Sécurité [Windows](microsoft-defender-security-center-antivirus.md) et avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-112">You can configure the display of additional notifications, such as recent threat detection summaries, in the [Windows Security app](microsoft-defender-security-center-antivirus.md) and with Group Policy.</span></span>

> [!NOTE]
> <span data-ttu-id="8dbe9-113">Dans Windows 10, version 1607, la fonctionnalité était appelée **notifications améliorées** et pouvait être configurée sous La mise à jour des **paramètres Windows**&  >  **sécurité**  >  **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-113">In Windows 10, version 1607 the feature was called **Enhanced notifications** and could be configured under **Windows Settings** > **Update & security** > **Windows Defender**.</span></span> <span data-ttu-id="8dbe9-114">Dans les paramètres de stratégie de groupe dans toutes les versions de Windows 10, il s'agit des **notifications améliorées.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-114">In Group Policy settings in all versions of Windows 10, it is called **Enhanced notifications**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8dbe9-115">La désactivation de notifications supplémentaires ne désactive pas les notifications critiques, telles que les alertes de détection et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-115">Disabling additional notifications will not disable critical notifications, such as threat detection and remediation alerts.</span></span>

<span data-ttu-id="8dbe9-116">**Utilisez l'application sécurité Windows pour désactiver les notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-116">**Use the Windows Security app to disable additional notifications:**</span></span>

1. <span data-ttu-id="8dbe9-117">Ouvrez l'application Sécurité Windows en cliquant sur l'icône de bouclier dans la barre des tâches ou en recherchant Defender dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-117">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Defender**.</span></span>

2. <span data-ttu-id="8dbe9-118">Cliquez sur la **vignette & protection** contre les virus contre les menaces (ou sur l'icône de bouclier dans la barre de menus de gauche), puis sur l'étiquette **paramètres** de protection contre & virus :</span><span class="sxs-lookup"><span data-stu-id="8dbe9-118">Click the **Virus & threat protection** tile (or the shield icon on the left menu bar) and then the **Virus & threat protection settings** label:</span></span>

    ![Capture d'écran de l'étiquette & protection contre les virus dans l'application Sécurité Windows](images/defender/wdav-protection-settings-wdsc.png)

3. <span data-ttu-id="8dbe9-120">Faites défiler la page **jusqu'à la** section Notifications et cliquez **sur Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-120">Scroll to the **Notifications** section and click **Change notification settings**.</span></span>

4. <span data-ttu-id="8dbe9-121">Faites glisser le commutateur **sur Désactivé** ou **Activé** pour désactiver ou activer des notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-121">Slide the switch to **Off** or **On** to disable or enable additional notifications.</span></span>

<span data-ttu-id="8dbe9-122">**Utilisez la stratégie de groupe pour désactiver les notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-122">**Use Group Policy to disable additional notifications:**</span></span>

1. <span data-ttu-id="8dbe9-123">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-123">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="8dbe9-124">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-124">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="8dbe9-125">Cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-125">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="8dbe9-126">Développez l'arborescence **des composants Windows >'antivirus Microsoft Defender > rapports.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-126">Expand the tree to **Windows components > Microsoft Defender Antivirus > Reporting**.</span></span>

5. <span data-ttu-id="8dbe9-127">Double-cliquez **sur Désactiver les notifications améliorées** et définissez l'option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-127">Double-click **Turn off enhanced notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="8dbe9-128">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-128">Click **OK**.</span></span> <span data-ttu-id="8dbe9-129">Cela empêche l'apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-129">This will prevent additional notifications from appearing.</span></span>

## <a name="configure-standard-notifications-on-endpoints"></a><span data-ttu-id="8dbe9-130">Configurer des notifications standard sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-130">Configure standard notifications on endpoints</span></span>

<span data-ttu-id="8dbe9-131">Vous pouvez utiliser la stratégie de groupe pour :</span><span class="sxs-lookup"><span data-stu-id="8dbe9-131">You can use Group Policy to:</span></span>

- <span data-ttu-id="8dbe9-132">Afficher du texte personnalisé supplémentaire sur les points de terminaison lorsque l'utilisateur doit effectuer une action</span><span class="sxs-lookup"><span data-stu-id="8dbe9-132">Display additional, customized text on endpoints when the user needs to perform an action</span></span>
- <span data-ttu-id="8dbe9-133">Masquer toutes les notifications sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-133">Hide all notifications on endpoints</span></span>
- <span data-ttu-id="8dbe9-134">Masquer les notifications de redémarrage sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="8dbe9-134">Hide reboot notifications on endpoints</span></span>

<span data-ttu-id="8dbe9-135">Masquer les notifications peut être utile dans les situations où vous ne pouvez pas masquer l'intégralité de l'interface antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-135">Hiding notifications can be useful in situations where you can't hide the entire Microsoft Defender Antivirus interface.</span></span> <span data-ttu-id="8dbe9-136">Pour [plus d'informations,](prevent-end-user-interaction-microsoft-defender-antivirus.md) voir Empêcher les utilisateurs de voir ou d'interagir avec l'interface utilisateur de l'Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-136">See [Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface](prevent-end-user-interaction-microsoft-defender-antivirus.md) for more information.</span></span> 

> [!NOTE]
> <span data-ttu-id="8dbe9-137">Le masquation des notifications se produit uniquement sur les points de terminaison sur lesquels la stratégie a été déployée.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-137">Hiding notifications will only occur on endpoints to which the policy has been deployed.</span></span> <span data-ttu-id="8dbe9-138">Les notifications liées aux actions qui doivent être prises (par exemple, un redémarrage) apparaissent toujours dans le tableau de bord et les rapports de surveillance de [Microsoft Endpoint Manager Endpoint Protection.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="8dbe9-138">Notifications related to actions that must be taken (such as a reboot) will still appear on the [Microsoft Endpoint Manager Endpoint Protection monitoring dashboard and reports](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span> 

<span data-ttu-id="8dbe9-139">Voir [Personnaliser l'application sécurité Windows](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) pour votre organisation pour obtenir des instructions pour ajouter des informations de contact personnalisées aux notifications que les utilisateurs voient sur leurs ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-139">See [Customize the Windows Security app for your organization](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) for instructions to add custom contact information to the notifications that users see on their machines.</span></span>

<span data-ttu-id="8dbe9-140">**Utilisez la stratégie de groupe pour masquer les notifications :**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-140">**Use Group Policy to hide notifications:**</span></span>

1. <span data-ttu-id="8dbe9-141">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-141">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and click **Edit**.</span></span>

2. <span data-ttu-id="8dbe9-142">Dans **l'Éditeur de gestion des stratégies de** groupe, cliquez sur **Configuration** ordinateur et cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-142">In the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="8dbe9-143">Développez l'arborescence **des composants Windows >'interface > client antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-143">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span> 

4. <span data-ttu-id="8dbe9-144">Double-cliquez sur **Supprimer toutes les notifications et** définissez l'option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-144">Double-click **Suppress all notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="8dbe9-145">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-145">Click **OK**.</span></span> <span data-ttu-id="8dbe9-146">Cela empêche l'apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-146">This will prevent additional notifications from appearing.</span></span>

<span data-ttu-id="8dbe9-147">**Utilisez la stratégie de groupe pour masquer les notifications de redémarrage :**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-147">**Use Group Policy to hide reboot notifications:**</span></span>

1. <span data-ttu-id="8dbe9-148">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l'objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-148">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="8dbe9-149">Dans **l'Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-149">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="8dbe9-150">Cliquez **sur Modèles d'administration.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-150">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="8dbe9-151">Développez l'arborescence **des composants Windows >'interface > client antivirus Microsoft Defender.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-151">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span>

5. <span data-ttu-id="8dbe9-152">Double-cliquez **sur Supprimer les notifications** de redémarrage et définir l'option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="8dbe9-152">Double-click **Suppresses reboot notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="8dbe9-153">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-153">Click **OK**.</span></span> <span data-ttu-id="8dbe9-154">Cela empêche l'apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8dbe9-154">This will prevent additional notifications from appearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dbe9-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dbe9-155">Related topics</span></span>

- [<span data-ttu-id="8dbe9-156">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="8dbe9-156">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="8dbe9-157">Configurer l'interaction de l'utilisateur final avec l'Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="8dbe9-157">Configure end-user interaction with Microsoft Defender Antivirus</span></span>](configure-end-user-interaction-microsoft-defender-antivirus.md)