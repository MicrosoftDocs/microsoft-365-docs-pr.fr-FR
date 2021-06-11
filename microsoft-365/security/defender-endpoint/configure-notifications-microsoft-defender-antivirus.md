---
title: Configurer les Antivirus Microsoft Defender notifications
description: Découvrez comment configurer et personnaliser des notifications standard et Antivirus Microsoft Defender supplémentaires sur les points de terminaison.
keywords: notifications, defender, antivirus, point de terminaison, gestion, administrateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 05/17/2021
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: f885b6d7991e4175cd14be5bbe9e0a7c96b1580f
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572344"
---
# <a name="configure-the-notifications-that-appear-on-endpoints"></a><span data-ttu-id="bf052-104">Configurer les notifications qui s’affichent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-104">Configure the notifications that appear on endpoints</span></span>

<span data-ttu-id="bf052-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="bf052-105">**Applies to:**</span></span>

- [<span data-ttu-id="bf052-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="bf052-107">Dans Windows 10, les notifications d’application concernant la détection et la correction des programmes malveillants sont plus robustes, cohérentes et concises.</span><span class="sxs-lookup"><span data-stu-id="bf052-107">In Windows 10, application notifications about malware detection and remediation are more robust, consistent, and concise.</span></span>

<span data-ttu-id="bf052-108">Les notifications apparaissent sur les points de terminaison lorsque des analyses déclenchées et programmées manuellement sont terminées et que des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="bf052-108">Notifications appear on endpoints when manually triggered and scheduled scans are completed and threats are detected.</span></span> <span data-ttu-id="bf052-109">Ces notifications apparaissent également dans le Centre de **notifications** et un résumé des analyses et des détections de menaces s’affiche à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="bf052-109">These notifications also appear in the **Notification Center**, and a summary of scans and threat detections appear at regular time intervals.</span></span>

<span data-ttu-id="bf052-110">Vous pouvez également configurer l’apparition des notifications standard sur les points de terminaison, telles que les notifications de redémarrage ou lorsqu’une menace a été détectée et corrigé.</span><span class="sxs-lookup"><span data-stu-id="bf052-110">You can also configure how standard notifications appear on endpoints, such as notifications for reboot or when a threat has been detected and remediated.</span></span>

## <a name="configure-the-additional-notifications-that-appear-on-endpoints"></a><span data-ttu-id="bf052-111">Configurer les notifications supplémentaires qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-111">Configure the additional notifications that appear on endpoints</span></span>

<span data-ttu-id="bf052-112">Vous pouvez configurer l’affichage de notifications supplémentaires, telles que des résumés récents de la détection des menaces, dans [l’application Sécurité Windows et](microsoft-defender-security-center-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bf052-112">You can configure the display of additional notifications, such as recent threat detection summaries, in the [Windows Security app](microsoft-defender-security-center-antivirus.md) and with Group Policy.</span></span>

> [!NOTE]
> <span data-ttu-id="bf052-113">Dans Windows 10 version 1607, la fonctionnalité était appelée **notifications améliorées** et pouvait être configurée sous Windows Paramètres mise à jour &   >  **sécurité**  >  **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="bf052-113">In Windows 10, version 1607 the feature was called **Enhanced notifications** and could be configured under **Windows Settings** > **Update & security** > **Windows Defender**.</span></span> <span data-ttu-id="bf052-114">Dans les paramètres de stratégie de groupe dans toutes les versions de Windows 10, il s’agit des **notifications améliorées.**</span><span class="sxs-lookup"><span data-stu-id="bf052-114">In Group Policy settings in all versions of Windows 10, it is called **Enhanced notifications**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bf052-115">La désactivation de notifications supplémentaires ne désactive pas les notifications critiques, telles que les alertes de détection et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="bf052-115">Disabling additional notifications will not disable critical notifications, such as threat detection and remediation alerts.</span></span>

<span data-ttu-id="bf052-116">**Utilisez l’Sécurité Windows pour désactiver des notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="bf052-116">**Use the Windows Security app to disable additional notifications:**</span></span>

1. <span data-ttu-id="bf052-117">Ouvrez l Sécurité Windows application en cliquant sur l’icône de bouclier dans la barre des tâches ou en recherchant sécurité dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="bf052-117">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="bf052-118">Sélectionnez **la vignette & protection** antivirus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez **Paramètres** de protection contre & virus</span><span class="sxs-lookup"><span data-stu-id="bf052-118">Select **Virus & threat protection** tile (or the shield icon on the left menu bar) and, then select **Virus & threat protection settings**</span></span>

3. <span data-ttu-id="bf052-119">Faites défiler la page **jusqu’à la** section Notifications et cliquez **sur Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="bf052-119">Scroll to the **Notifications** section and click **Change notification settings**.</span></span>

4. <span data-ttu-id="bf052-120">Faites glisser le commutateur **sur Désactivé** ou **Activé** pour désactiver ou activer des notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bf052-120">Slide the switch to **Off** or **On** to disable or enable additional notifications.</span></span>

<span data-ttu-id="bf052-121">**Utilisez la stratégie de groupe pour désactiver les notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="bf052-121">**Use Group Policy to disable additional notifications:**</span></span>

1. <span data-ttu-id="bf052-122">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="bf052-122">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="bf052-123">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="bf052-123">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="bf052-124">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="bf052-124">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="bf052-125">Développez l’arborescence **pour Windows composants > Antivirus Microsoft Defender > rapports.**</span><span class="sxs-lookup"><span data-stu-id="bf052-125">Expand the tree to **Windows components > Microsoft Defender Antivirus > Reporting**.</span></span>

5. <span data-ttu-id="bf052-126">Double-cliquez **sur Désactiver les notifications améliorées** et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="bf052-126">Double-click **Turn off enhanced notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="bf052-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf052-127">Click **OK**.</span></span> <span data-ttu-id="bf052-128">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bf052-128">This will prevent additional notifications from appearing.</span></span>

## <a name="configure-standard-notifications-on-endpoints"></a><span data-ttu-id="bf052-129">Configurer des notifications standard sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-129">Configure standard notifications on endpoints</span></span>

<span data-ttu-id="bf052-130">Vous pouvez utiliser la stratégie de groupe pour :</span><span class="sxs-lookup"><span data-stu-id="bf052-130">You can use Group Policy to:</span></span>

- <span data-ttu-id="bf052-131">Afficher du texte personnalisé supplémentaire sur les points de terminaison lorsque l’utilisateur doit effectuer une action</span><span class="sxs-lookup"><span data-stu-id="bf052-131">Display additional, customized text on endpoints when the user needs to perform an action</span></span>
- <span data-ttu-id="bf052-132">Masquer toutes les notifications sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-132">Hide all notifications on endpoints</span></span>
- <span data-ttu-id="bf052-133">Masquer les notifications de redémarrage sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="bf052-133">Hide reboot notifications on endpoints</span></span>

<span data-ttu-id="bf052-134">Masquer les notifications peut être utile dans les situations où vous ne pouvez pas masquer l’interface Antivirus Microsoft Defender complète.</span><span class="sxs-lookup"><span data-stu-id="bf052-134">Hiding notifications can be useful in situations where you can't hide the entire Microsoft Defender Antivirus interface.</span></span> <span data-ttu-id="bf052-135">Pour plus d’informations, voir Empêcher les utilisateurs de voir ou [d’interagir Antivirus Microsoft Defender’interface utilisateur.](prevent-end-user-interaction-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="bf052-135">See [Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface](prevent-end-user-interaction-microsoft-defender-antivirus.md) for more information.</span></span> 

> [!NOTE]
> <span data-ttu-id="bf052-136">Le masquation des notifications se produit uniquement sur les points de terminaison sur lesquels la stratégie a été déployée.</span><span class="sxs-lookup"><span data-stu-id="bf052-136">Hiding notifications will only occur on endpoints to which the policy has been deployed.</span></span> <span data-ttu-id="bf052-137">Les notifications liées aux actions qui doivent être prises (par exemple, un redémarrage) apparaissent toujours dans le tableau de bord de Microsoft Endpoint Manager Endpoint Protection de surveillance [et les rapports.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="bf052-137">Notifications related to actions that must be taken (such as a reboot) will still appear on the [Microsoft Endpoint Manager Endpoint Protection monitoring dashboard and reports](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span> 

<span data-ttu-id="bf052-138">Pour obtenir des instructions sur l’ajout [d’informations](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) de contact personnalisées aux notifications que les utilisateurs voient sur leurs ordinateurs, voir Personnaliser l’application Sécurité Windows pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="bf052-138">See [Customize the Windows Security app for your organization](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) for instructions to add custom contact information to the notifications that users see on their machines.</span></span>

<span data-ttu-id="bf052-139">**Utilisez la stratégie de groupe pour masquer les notifications :**</span><span class="sxs-lookup"><span data-stu-id="bf052-139">**Use Group Policy to hide notifications:**</span></span>

1. <span data-ttu-id="bf052-140">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="bf052-140">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and click **Edit**.</span></span>

2. <span data-ttu-id="bf052-141">Dans **l’Éditeur de gestion des stratégies de** groupe, cliquez sur **Configuration** ordinateur et cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="bf052-141">In the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="bf052-142">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender >'interface client.**</span><span class="sxs-lookup"><span data-stu-id="bf052-142">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span> 

4. <span data-ttu-id="bf052-143">Double-cliquez sur **Supprimer toutes les notifications et** définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="bf052-143">Double-click **Suppress all notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="bf052-144">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf052-144">Click **OK**.</span></span> <span data-ttu-id="bf052-145">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bf052-145">This will prevent additional notifications from appearing.</span></span>

<span data-ttu-id="bf052-146">**Utilisez la stratégie de groupe pour masquer les notifications de redémarrage :**</span><span class="sxs-lookup"><span data-stu-id="bf052-146">**Use Group Policy to hide reboot notifications:**</span></span>

1. <span data-ttu-id="bf052-147">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la [Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))de gestion des stratégies de groupe, cliquez avec le bouton droit sur l’objet de stratégie de groupe à configurer, puis cliquez sur **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="bf052-147">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="bf052-148">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="bf052-148">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="bf052-149">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="bf052-149">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="bf052-150">Développez l’arborescence **Windows composants > Antivirus Microsoft Defender >'interface client.**</span><span class="sxs-lookup"><span data-stu-id="bf052-150">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span>

5. <span data-ttu-id="bf052-151">Double-cliquez sur Supprimer les notifications de **redémarrage** et définir l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="bf052-151">Double-click **Suppresses reboot notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="bf052-152">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf052-152">Click **OK**.</span></span> <span data-ttu-id="bf052-153">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="bf052-153">This will prevent additional notifications from appearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf052-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf052-154">Related topics</span></span>

- [<span data-ttu-id="bf052-155">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="bf052-155">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="bf052-156">Configurer l’interaction de l’utilisateur final avec Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="bf052-156">Configure end-user interaction with Microsoft Defender Antivirus</span></span>](configure-end-user-interaction-microsoft-defender-antivirus.md)
