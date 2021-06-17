---
title: Configurer les Antivirus Microsoft Defender notifications
description: Découvrez comment configurer et personnaliser les notifications standard et autres Antivirus Microsoft Defender sur les points de terminaison.
keywords: notifications, defender, antivirus, point de terminaison, gestion, administrateur
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.technology: mde
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: Normal
author: denisebmsft
ms.topic: article
ms.author: deniseb
ms.custom: nextgen
ms.date: 06/16/2021
ms.reviewer: ''
manager: dansimp
ms.openlocfilehash: a7a838bb15cd011b750fbfa3d6df100ddf9f713c
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985407"
---
# <a name="configure-microsoft-defender-antivirus-notifications-that-appear-on-endpoints"></a><span data-ttu-id="3e1d2-104">Configurer les notifications Antivirus Microsoft Defender qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e1d2-104">Configure Microsoft Defender Antivirus notifications that appear on endpoints</span></span>

<span data-ttu-id="3e1d2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-105">**Applies to:**</span></span>

- [<span data-ttu-id="3e1d2-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e1d2-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="3e1d2-107">Dans Windows 10, les notifications d’application concernant la détection et la correction des programmes malveillants sont plus robustes, cohérentes et concises.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-107">In Windows 10, application notifications about malware detection and remediation are more robust, consistent, and concise.</span></span> <span data-ttu-id="3e1d2-108">Antivirus Microsoft Defender notifications apparaissent sur les points de terminaison lorsque des analyses sont terminées et que des menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-108">Microsoft Defender Antivirus notifications appear on endpoints when scans are completed and threats are detected.</span></span> <span data-ttu-id="3e1d2-109">Les notifications suivent les analyses programmées et déclenchées manuellement.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-109">Notifications follow both scheduled and manually triggered scans.</span></span> <span data-ttu-id="3e1d2-110">Ces notifications apparaissent également dans le Centre de **notifications** et un résumé des analyses et des détections de menaces s’affiche à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-110">These notifications also appear in the **Notification Center**, and a summary of scans and threat detections appear at regular time intervals.</span></span>

<span data-ttu-id="3e1d2-111">Si vous faites partie de l’équipe de sécurité de votre organisation, vous pouvez configurer l’apparition des notifications sur les points de terminaison, telles que les notifications qui invitent à un redémarrage du système ou qui indiquent qu’une menace a été détectée et corrigé.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-111">If you're part of your organization's security team, you can configure how notifications appear on endpoints, such as notifications that prompt for a system reboot or that indicate a threat has been detected and remediated.</span></span>

## <a name="configure-antivirus-notifications-using-group-policy-or-the-windows-security-app"></a><span data-ttu-id="3e1d2-112">Configurer les notifications antivirus à l’aide de la stratégie de groupe ou de l Sécurité Windows appl</span><span class="sxs-lookup"><span data-stu-id="3e1d2-112">Configure antivirus notifications using Group Policy or the Windows Security app</span></span>

<span data-ttu-id="3e1d2-113">Vous pouvez configurer l’affichage de notifications supplémentaires, telles que des résumés récents de détection des menaces, dans [l’application Sécurité Windows et](microsoft-defender-security-center-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-113">You can configure the display of additional notifications, such as recent threat detection summaries, in the [Windows Security app](microsoft-defender-security-center-antivirus.md) and with Group Policy.</span></span>

> [!NOTE]
> <span data-ttu-id="3e1d2-114">Dans Windows 10 version 1607, la fonctionnalité s’appelait **notifications améliorées** et a été configurée sous Windows Paramètres mise à jour &   >  **sécurité**  >  **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-114">In Windows 10, version 1607 the feature was called **Enhanced notifications** and was configured under **Windows Settings** > **Update & security** > **Windows Defender**.</span></span> <span data-ttu-id="3e1d2-115">Dans les paramètres de stratégie de groupe pour toutes les versions de Windows 10, la fonctionnalité de notification est appelée **notifications améliorées.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-115">In Group Policy settings for all versions of Windows 10, the notification feature is called **Enhanced notifications**.</span></span>

### <a name="use-group-policy-to-disable-additional-notifications"></a><span data-ttu-id="3e1d2-116">Utiliser une stratégie de groupe pour désactiver des notifications supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3e1d2-116">Use Group Policy to disable additional notifications</span></span>

1. <span data-ttu-id="3e1d2-117">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la[Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="3e1d2-117">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="3e1d2-118">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-118">Right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

3. <span data-ttu-id="3e1d2-119">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-119">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

4. <span data-ttu-id="3e1d2-120">Sélectionnez **modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-120">Select **Administrative templates**.</span></span>

5. <span data-ttu-id="3e1d2-121">Développez l’arborescence **Windows composants Antivirus Microsoft Defender**>  >   Reporting\*\*.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-121">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > Reporting\*\*.</span></span>

6. <span data-ttu-id="3e1d2-122">Double-cliquez **sur Désactiver les notifications améliorées** et définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-122">Double-click **Turn off enhanced notifications**, and set the option to **Enabled**.</span></span> <span data-ttu-id="3e1d2-123">Puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-123">Then select **OK**.</span></span> <span data-ttu-id="3e1d2-124">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-124">This will prevent additional notifications from appearing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e1d2-125">La désactivation de notifications supplémentaires ne désactive pas les notifications critiques, telles que les alertes de détection et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-125">Disabling additional notifications will not disable critical notifications, such as threat detection and remediation alerts.</span></span>

### <a name="use-the-windows-security-app-to-disable-additional-notifications"></a><span data-ttu-id="3e1d2-126">Utiliser l’application Sécurité Windows pour désactiver des notifications supplémentaires</span><span class="sxs-lookup"><span data-stu-id="3e1d2-126">Use the Windows Security app to disable additional notifications</span></span>

1. <span data-ttu-id="3e1d2-127">Ouvrez l Sécurité Windows application en cliquant sur l’icône de bouclier dans la barre des tâches ou en recherchant sécurité dans le menu **Démarrer.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-127">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="3e1d2-128">Sélectionnez **la vignette & protection** antivirus contre les menaces (ou l’icône de bouclier dans la barre de menus de gauche), puis sélectionnez **Paramètres** de protection contre & virus</span><span class="sxs-lookup"><span data-stu-id="3e1d2-128">Select **Virus & threat protection** tile (or the shield icon on the left menu bar) and, then select **Virus & threat protection settings**</span></span>

3. <span data-ttu-id="3e1d2-129">Faites défiler la page **jusqu’à la** section Notifications et sélectionnez **Modifier les paramètres de notification.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-129">Scroll to the **Notifications** section and select **Change notification settings**.</span></span>

4. <span data-ttu-id="3e1d2-130">Faites glisser le commutateur **sur Désactivé** ou **Activé** pour désactiver ou activer des notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-130">Slide the switch to **Off** or **On** to disable or enable additional notifications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e1d2-131">La désactivation de notifications supplémentaires ne désactive pas les notifications critiques, telles que les alertes de détection et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-131">Disabling additional notifications will not disable critical notifications, such as threat detection and remediation alerts.</span></span>

## <a name="configure-standard-notifications-on-endpoints-using-group-policy"></a><span data-ttu-id="3e1d2-132">Configurer des notifications standard sur les points de terminaison à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3e1d2-132">Configure standard notifications on endpoints using Group Policy</span></span>

<span data-ttu-id="3e1d2-133">Vous pouvez utiliser la stratégie de groupe pour :</span><span class="sxs-lookup"><span data-stu-id="3e1d2-133">You can use Group Policy to:</span></span>

- <span data-ttu-id="3e1d2-134">Afficher du texte personnalisé supplémentaire sur les points de terminaison lorsque l’utilisateur doit effectuer une action</span><span class="sxs-lookup"><span data-stu-id="3e1d2-134">Display additional, customized text on endpoints when the user needs to perform an action</span></span>
- <span data-ttu-id="3e1d2-135">Masquer toutes les notifications sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e1d2-135">Hide all notifications on endpoints</span></span>
- <span data-ttu-id="3e1d2-136">Masquer les notifications de redémarrage sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="3e1d2-136">Hide reboot notifications on endpoints</span></span>

<span data-ttu-id="3e1d2-137">Masquer les notifications peut être utile dans les situations où vous ne pouvez pas masquer l’interface Antivirus Microsoft Defender complète.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-137">Hiding notifications can be useful in situations where you can't hide the entire Microsoft Defender Antivirus interface.</span></span> <span data-ttu-id="3e1d2-138">Pour plus d’informations, voir Empêcher les utilisateurs de voir ou [d’interagir Antivirus Microsoft Defender’interface utilisateur.](prevent-end-user-interaction-microsoft-defender-antivirus.md)</span><span class="sxs-lookup"><span data-stu-id="3e1d2-138">See [Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface](prevent-end-user-interaction-microsoft-defender-antivirus.md) for more information.</span></span> <span data-ttu-id="3e1d2-139">Le masquation des notifications se produit uniquement sur les points de terminaison sur lesquels la stratégie a été déployée.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-139">Hiding notifications will only occur on endpoints to which the policy has been deployed.</span></span> <span data-ttu-id="3e1d2-140">Les notifications liées aux actions qui doivent être prises (par exemple, un redémarrage) apparaissent toujours dans le tableau de bord de Microsoft Endpoint Manager Endpoint Protection de surveillance [et les rapports.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="3e1d2-140">Notifications related to actions that must be taken (such as a reboot) will still appear on the [Microsoft Endpoint Manager Endpoint Protection monitoring dashboard and reports](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span> 

<span data-ttu-id="3e1d2-141">Pour ajouter des informations de contact personnalisées aux notifications de point de terminaison, voir [Personnaliser l’application Sécurité Windows pour votre organisation.](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center)</span><span class="sxs-lookup"><span data-stu-id="3e1d2-141">To add custom contact information to endpoint notifications, see [Customize the Windows Security app for your organization](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center).</span></span>

### <a name="use-group-policy-to-hide-notifications"></a><span data-ttu-id="3e1d2-142">Utiliser la stratégie de groupe pour masquer les notifications</span><span class="sxs-lookup"><span data-stu-id="3e1d2-142">Use Group Policy to hide notifications</span></span>

1. <span data-ttu-id="3e1d2-143">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la[Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="3e1d2-143">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="3e1d2-144">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-144">Right-click the Group Policy Object you want to configure, and then select **Edit**.</span></span>

3. <span data-ttu-id="3e1d2-145">Dans **l’Éditeur de gestion des stratégies de** groupe, sélectionnez **Configuration** ordinateur, puis sélectionnez **Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-145">In the **Group Policy Management Editor** go to **Computer configuration** and then select **Administrative templates**.</span></span>

4. <span data-ttu-id="3e1d2-146">Développez l’arborescence **Windows composants**  >    >  **Antivirus Microsoft Defender’interface client.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-146">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Client interface**.</span></span> 

5. <span data-ttu-id="3e1d2-147">Double-cliquez sur **Supprimer toutes les notifications et** définissez l’option sur **Activé.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-147">Double-click **Suppress all notifications** and set the option to **Enabled**.</span></span> 

6. <span data-ttu-id="3e1d2-148">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-148">Select **OK**.</span></span> <span data-ttu-id="3e1d2-149">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-149">This will prevent additional notifications from appearing.</span></span>

### <a name="use-group-policy-to-hide-reboot-notifications"></a><span data-ttu-id="3e1d2-150">Utiliser la stratégie de groupe pour masquer les notifications de redémarrage</span><span class="sxs-lookup"><span data-stu-id="3e1d2-150">Use Group Policy to hide reboot notifications</span></span>

1. <span data-ttu-id="3e1d2-151">Sur votre ordinateur de gestion des stratégies de groupe, ouvrez la[Console de gestion des stratégies de groupe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="3e1d2-151">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).</span></span>

2. <span data-ttu-id="3e1d2-152">Cliquez avec le bouton droit sur l’objet de stratégie de groupe que vous souhaitez configurer, puis sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-152">Right-click the Group Policy Object you want to configure and then select **Edit**.</span></span>

2. <span data-ttu-id="3e1d2-153">Dans **l’Éditeur de gestion des stratégies de** groupe, allez à **Configuration ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-153">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="3e1d2-154">Cliquez **sur Modèles d’administration.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-154">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="3e1d2-155">Développez l’arborescence **Windows composants**  >    >  **Antivirus Microsoft Defender’interface client.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-155">Expand the tree to **Windows components** > **Microsoft Defender Antivirus** > **Client interface**.</span></span>

5. <span data-ttu-id="3e1d2-156">Double-cliquez **sur Supprimer les notifications** de redémarrage et définir l’option **sur Activé.**</span><span class="sxs-lookup"><span data-stu-id="3e1d2-156">Double-click **Suppresses reboot notifications** and set the option to **Enabled**.</span></span> 

5. <span data-ttu-id="3e1d2-157">Sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-157">Select **OK**.</span></span> <span data-ttu-id="3e1d2-158">Cela empêche l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="3e1d2-158">This will prevent additional notifications from appearing.</span></span>

