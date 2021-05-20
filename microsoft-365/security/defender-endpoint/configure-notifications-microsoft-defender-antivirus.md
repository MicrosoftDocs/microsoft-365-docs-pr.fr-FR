---
title: Configurer Antivirus Microsoft Defender notifications
description: Découvrez comment configurer et personnaliser les notifications standard et Antivirus Microsoft Defender sur les points de terminaison.
keywords: notifications, défenseur, antivirus, point final, gestion, admin
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
# <a name="configure-the-notifications-that-appear-on-endpoints"></a><span data-ttu-id="37645-104">Configurer les notifications qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-104">Configure the notifications that appear on endpoints</span></span>

<span data-ttu-id="37645-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="37645-105">**Applies to:**</span></span>

- [<span data-ttu-id="37645-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="37645-107">En Windows 10, les notifications d’application sur la détection et l’assainissement des logiciels malveillants sont plus robustes, cohérentes et concises.</span><span class="sxs-lookup"><span data-stu-id="37645-107">In Windows 10, application notifications about malware detection and remediation are more robust, consistent, and concise.</span></span>

<span data-ttu-id="37645-108">Les notifications apparaissent sur les points de terminaison lorsque les analyses déclenchées manuellement et planifiées sont terminées et que les menaces sont détectées.</span><span class="sxs-lookup"><span data-stu-id="37645-108">Notifications appear on endpoints when manually triggered and scheduled scans are completed and threats are detected.</span></span> <span data-ttu-id="37645-109">Ces notifications apparaissent également dans le Centre **de notification,** et un résumé des analyses et des détections de menaces apparaissent à intervalles réguliers.</span><span class="sxs-lookup"><span data-stu-id="37645-109">These notifications also appear in the **Notification Center**, and a summary of scans and threat detections appear at regular time intervals.</span></span>

<span data-ttu-id="37645-110">Vous pouvez également configurer la façon dont les notifications standard s’apparaissent sur les paramètres, tels que les notifications de redémarrage ou lorsqu’une menace a été détectée et assainie.</span><span class="sxs-lookup"><span data-stu-id="37645-110">You can also configure how standard notifications appear on endpoints, such as notifications for reboot or when a threat has been detected and remediated.</span></span>

## <a name="configure-the-additional-notifications-that-appear-on-endpoints"></a><span data-ttu-id="37645-111">Configurer les notifications supplémentaires qui apparaissent sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-111">Configure the additional notifications that appear on endpoints</span></span>

<span data-ttu-id="37645-112">Vous pouvez configurer l’affichage de notifications supplémentaires, telles que des résumés récents de détection de menaces, [dans l’application Sécurité Windows et](microsoft-defender-security-center-antivirus.md) avec la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="37645-112">You can configure the display of additional notifications, such as recent threat detection summaries, in the [Windows Security app](microsoft-defender-security-center-antivirus.md) and with Group Policy.</span></span>

> [!NOTE]
> <span data-ttu-id="37645-113">Dans Windows 10, version 1607 la fonctionnalité a été appelée **notifications améliorées** et pourrait être **configuré sous Windows Paramètres** mise à jour &  >  **sécurité**  >  **Windows Defender**.</span><span class="sxs-lookup"><span data-stu-id="37645-113">In Windows 10, version 1607 the feature was called **Enhanced notifications** and could be configured under **Windows Settings** > **Update & security** > **Windows Defender**.</span></span> <span data-ttu-id="37645-114">Dans les paramètres de stratégie de groupe dans toutes les versions Windows 10, il est appelé **notifications améliorées**.</span><span class="sxs-lookup"><span data-stu-id="37645-114">In Group Policy settings in all versions of Windows 10, it is called **Enhanced notifications**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="37645-115">La désactivation de notifications supplémentaires ne désactivera pas les notifications critiques, telles que les alertes de détection et d’assainissement des menaces.</span><span class="sxs-lookup"><span data-stu-id="37645-115">Disabling additional notifications will not disable critical notifications, such as threat detection and remediation alerts.</span></span>

<span data-ttu-id="37645-116">**Utilisez l Sécurité Windows apprable pour désactiver les notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="37645-116">**Use the Windows Security app to disable additional notifications:**</span></span>

1. <span data-ttu-id="37645-117">Ouvrez l Sécurité Windows application en cliquant sur l’icône bouclier dans la barre des tâches ou en recherchant le menu de démarrage pour **la sécurité**.</span><span class="sxs-lookup"><span data-stu-id="37645-117">Open the Windows Security app by clicking the shield icon in the task bar or searching the start menu for **Security**.</span></span>

2. <span data-ttu-id="37645-118">Sélectionnez **la vignette de protection contre & virus** (ou l’icône du bouclier sur la barre de menu gauche) et sélectionnez ensuite les paramètres de protection contre les menaces & virus ou les paramètres de protection contre les **menaces**</span><span class="sxs-lookup"><span data-stu-id="37645-118">Select **Virus & threat protection** tile (or the shield icon on the left menu bar) and, then select **Virus & threat protection settings**</span></span>

3. <span data-ttu-id="37645-119">Faites défiler vers la section **Notifications** et cliquez sur **Paramètres de notification de modification**.</span><span class="sxs-lookup"><span data-stu-id="37645-119">Scroll to the **Notifications** section and click **Change notification settings**.</span></span>

4. <span data-ttu-id="37645-120">Faites glisser le commutateur vers **Off** ou **On** pour désactiver ou activer des notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="37645-120">Slide the switch to **Off** or **On** to disable or enable additional notifications.</span></span>

<span data-ttu-id="37645-121">**Utilisez la stratégie de groupe pour désactiver des notifications supplémentaires :**</span><span class="sxs-lookup"><span data-stu-id="37645-121">**Use Group Policy to disable additional notifications:**</span></span>

1. <span data-ttu-id="37645-122">Sur votre ordinateur de gestion de stratégie de groupe, ouvrez [la console de gestion de stratégie de](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))groupe, cliquez à droite sur l’objet de stratégie de groupe que vous souhaitez configurer et cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="37645-122">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="37645-123">Dans le **groupe Policy Management Editor aller** à la configuration de **l’ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="37645-123">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="37645-124">Cliquez **sur Modèles administratifs**.</span><span class="sxs-lookup"><span data-stu-id="37645-124">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="37645-125">Étendre l’arbre **aux Windows composants > Antivirus Microsoft Defender > Reporting**.</span><span class="sxs-lookup"><span data-stu-id="37645-125">Expand the tree to **Windows components > Microsoft Defender Antivirus > Reporting**.</span></span>

5. <span data-ttu-id="37645-126">Double-cliquez Désactiver **les notifications améliorées et** définir l’option **activée**.</span><span class="sxs-lookup"><span data-stu-id="37645-126">Double-click **Turn off enhanced notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="37645-127">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="37645-127">Click **OK**.</span></span> <span data-ttu-id="37645-128">Cela empêchera l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="37645-128">This will prevent additional notifications from appearing.</span></span>

## <a name="configure-standard-notifications-on-endpoints"></a><span data-ttu-id="37645-129">Configurer les notifications standard sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-129">Configure standard notifications on endpoints</span></span>

<span data-ttu-id="37645-130">Vous pouvez utiliser la stratégie de groupe pour :</span><span class="sxs-lookup"><span data-stu-id="37645-130">You can use Group Policy to:</span></span>

- <span data-ttu-id="37645-131">Affichez du texte supplémentaire personnalisé sur les points de terminaison lorsque l’utilisateur a besoin d’effectuer une action</span><span class="sxs-lookup"><span data-stu-id="37645-131">Display additional, customized text on endpoints when the user needs to perform an action</span></span>
- <span data-ttu-id="37645-132">Masquer toutes les notifications sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-132">Hide all notifications on endpoints</span></span>
- <span data-ttu-id="37645-133">Masquer les notifications de redémarrage sur les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37645-133">Hide reboot notifications on endpoints</span></span>

<span data-ttu-id="37645-134">Masquer les notifications peut être utile dans les situations où vous ne pouvez pas masquer l’ensemble Antivirus Microsoft Defender interface.</span><span class="sxs-lookup"><span data-stu-id="37645-134">Hiding notifications can be useful in situations where you can't hide the entire Microsoft Defender Antivirus interface.</span></span> <span data-ttu-id="37645-135">Voir [Empêcher les utilisateurs de voir ou d’interagir avec l’interface Antivirus Microsoft Defender utilisation pour](prevent-end-user-interaction-microsoft-defender-antivirus.md) plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="37645-135">See [Prevent users from seeing or interacting with the Microsoft Defender Antivirus user interface](prevent-end-user-interaction-microsoft-defender-antivirus.md) for more information.</span></span> 

> [!NOTE]
> <span data-ttu-id="37645-136">La dissimulation des notifications ne se produira que sur les points de terminaison auxquels la stratégie a été déployée.</span><span class="sxs-lookup"><span data-stu-id="37645-136">Hiding notifications will only occur on endpoints to which the policy has been deployed.</span></span> <span data-ttu-id="37645-137">Les notifications relatives aux mesures à prendre (comme un redémarrage) apparaîtront toujours sur le [tableau de bord et les rapports Microsoft Endpoint Manager Endpoint Protection surveillance des données.](/configmgr/protect/deploy-use/monitor-endpoint-protection)</span><span class="sxs-lookup"><span data-stu-id="37645-137">Notifications related to actions that must be taken (such as a reboot) will still appear on the [Microsoft Endpoint Manager Endpoint Protection monitoring dashboard and reports](/configmgr/protect/deploy-use/monitor-endpoint-protection).</span></span> 

<span data-ttu-id="37645-138">Consultez [personnaliser l’application Sécurité Windows pour votre organisation pour obtenir](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) des instructions pour ajouter des coordonnées personnalisées aux notifications que les utilisateurs voient sur leurs machines.</span><span class="sxs-lookup"><span data-stu-id="37645-138">See [Customize the Windows Security app for your organization](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) for instructions to add custom contact information to the notifications that users see on their machines.</span></span>

<span data-ttu-id="37645-139">**Utilisez la stratégie de groupe pour masquer les notifications :**</span><span class="sxs-lookup"><span data-stu-id="37645-139">**Use Group Policy to hide notifications:**</span></span>

1. <span data-ttu-id="37645-140">Sur votre ordinateur de gestion de stratégie de groupe, ouvrez [la console de gestion de stratégie de](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))groupe, cliquez à droite sur l’objet de stratégie de groupe que vous souhaitez configurer et cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="37645-140">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure, and click **Edit**.</span></span>

2. <span data-ttu-id="37645-141">Dans le **groupe Policy Management Editor aller** à la configuration de **l’ordinateur** et **cliquez sur modèles administratifs**.</span><span class="sxs-lookup"><span data-stu-id="37645-141">In the **Group Policy Management Editor** go to **Computer configuration** and click **Administrative templates**.</span></span>

3. <span data-ttu-id="37645-142">Élargissez l’arbre **Windows composants > Antivirus Microsoft Defender > interface client.**</span><span class="sxs-lookup"><span data-stu-id="37645-142">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span> 

4. <span data-ttu-id="37645-143">Double-cliquez supprimer **toutes les notifications et** définir l’option activé **.**</span><span class="sxs-lookup"><span data-stu-id="37645-143">Double-click **Suppress all notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="37645-144">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="37645-144">Click **OK**.</span></span> <span data-ttu-id="37645-145">Cela empêchera l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="37645-145">This will prevent additional notifications from appearing.</span></span>

<span data-ttu-id="37645-146">**Utilisez la stratégie de groupe pour masquer les notifications de redémarrage :**</span><span class="sxs-lookup"><span data-stu-id="37645-146">**Use Group Policy to hide reboot notifications:**</span></span>

1. <span data-ttu-id="37645-147">Sur votre ordinateur de gestion de stratégie de groupe, ouvrez [la console de gestion de stratégie de](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11))groupe, cliquez à droite sur l’objet de stratégie de groupe que vous souhaitez configurer et cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="37645-147">On your Group Policy management computer, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)), right-click the Group Policy Object you want to configure and click **Edit**.</span></span>

2. <span data-ttu-id="37645-148">Dans le **groupe Policy Management Editor aller** à la configuration de **l’ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="37645-148">In the **Group Policy Management Editor** go to **Computer configuration**.</span></span>

3. <span data-ttu-id="37645-149">Cliquez **sur Modèles administratifs**.</span><span class="sxs-lookup"><span data-stu-id="37645-149">Click **Administrative templates**.</span></span>

4. <span data-ttu-id="37645-150">Élargissez l’arbre **Windows composants > Antivirus Microsoft Defender > interface client.**</span><span class="sxs-lookup"><span data-stu-id="37645-150">Expand the tree to **Windows components > Microsoft Defender Antivirus > Client interface**.</span></span>

5. <span data-ttu-id="37645-151">Double-click **supprime les notifications de redémarrage et** définir l’option **activée**.</span><span class="sxs-lookup"><span data-stu-id="37645-151">Double-click **Suppresses reboot notifications** and set the option to **Enabled**.</span></span> <span data-ttu-id="37645-152">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="37645-152">Click **OK**.</span></span> <span data-ttu-id="37645-153">Cela empêchera l’apparition de notifications supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="37645-153">This will prevent additional notifications from appearing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37645-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37645-154">Related topics</span></span>

- [<span data-ttu-id="37645-155">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="37645-155">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="37645-156">Configurer l’interaction utilisateur final avec Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="37645-156">Configure end-user interaction with Microsoft Defender Antivirus</span></span>](configure-end-user-interaction-microsoft-defender-antivirus.md)
