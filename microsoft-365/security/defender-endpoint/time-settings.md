---
title: Centre de sécurité Microsoft Defender de fuseau horaire
description: Utilisez les informations contenues ici pour configurer les paramètres de fuseau Centre de sécurité Microsoft Defender et afficher les informations de licence.
keywords: paramètres, Microsoft Defender, veille contre les menaces de cybersécurité, Microsoft Defender pour le point de terminaison, fuseau horaire, utc, heure locale, licence
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: df55a1b0e92c24b5f52032330ef95bf19aeb8cb3
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51932630"
---
# <a name="microsoft-defender-security-center-time-zone-settings"></a><span data-ttu-id="eee1f-104">Centre de sécurité Microsoft Defender de fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="eee1f-104">Microsoft Defender Security Center time zone settings</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="eee1f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="eee1f-105">**Applies to:**</span></span>
- [<span data-ttu-id="eee1f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="eee1f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)


><span data-ttu-id="eee1f-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="eee1f-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="eee1f-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="eee1f-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-settings-abovefoldlink)

<span data-ttu-id="eee1f-109">Utilisez **l’icône 1** des paramètres de fuseau horaire du menu Fuseau horaire pour configurer le fuseau horaire et ![ afficher les informations de ](images/atp-time-zone.png) licence.</span><span class="sxs-lookup"><span data-stu-id="eee1f-109">Use the **Time zone** menu ![Time zone settings icon1](images/atp-time-zone.png) to configure the time zone and view license information.</span></span>

## <a name="time-zone-settings"></a><span data-ttu-id="eee1f-110">Paramètres de fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="eee1f-110">Time zone settings</span></span>
<span data-ttu-id="eee1f-111">L’aspect du temps est important dans l’évaluation et l’analyse des cyberattaques perçues et réelles.</span><span class="sxs-lookup"><span data-stu-id="eee1f-111">The aspect of time is important in the assessment and analysis of perceived and actual cyberattacks.</span></span>

<span data-ttu-id="eee1f-112">Les enquêtes cyberforensiques s’appuient souvent sur des horodatés pour rassembler la séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="eee1f-112">Cyberforensic investigations often rely on time stamps to piece together the sequence of events.</span></span> <span data-ttu-id="eee1f-113">Il est important que votre système reflète les paramètres de fuseau horaire corrects.</span><span class="sxs-lookup"><span data-stu-id="eee1f-113">It’s important that your system reflects the correct time zone settings.</span></span>

<span data-ttu-id="eee1f-114">Microsoft Defender pour le point de terminaison peut afficher le temps universel coordonné (UTC) ou l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="eee1f-114">Microsoft Defender for Endpoint can display either Coordinated Universal Time (UTC) or local time.</span></span>

<span data-ttu-id="eee1f-115">Votre paramètre de fuseau horaire actuel s’affiche dans le menu Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eee1f-115">Your current time zone setting is shown in the Microsoft Defender for Endpoint menu.</span></span> <span data-ttu-id="eee1f-116">Vous pouvez modifier le fuseau horaire affiché dans le menu **Fuseau** horaire.</span><span class="sxs-lookup"><span data-stu-id="eee1f-116">You can change the displayed time zone in the **Time zone** menu.</span></span>

![Paramètres de fuseau horaire icône2](images/atp-time-zone-menu.png)<span data-ttu-id="eee1f-118">.</span><span class="sxs-lookup"><span data-stu-id="eee1f-118">.</span></span>

### <a name="utc-time-zone"></a><span data-ttu-id="eee1f-119">Fuseau horaire UTC</span><span class="sxs-lookup"><span data-stu-id="eee1f-119">UTC time zone</span></span>
<span data-ttu-id="eee1f-120">Microsoft Defender pour le point de terminaison utilise l’heure UTC par défaut.</span><span class="sxs-lookup"><span data-stu-id="eee1f-120">Microsoft Defender for Endpoint uses UTC time by default.</span></span>

<span data-ttu-id="eee1f-121">La définition du fuseau horaire De Microsoft Defender pour le point de terminaison sur UTC affiche tous les timestamps système (alertes, événements, etc.) en UTC pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="eee1f-121">Setting the Microsoft Defender for Endpoint time zone to UTC will display all system timestamps (alerts, events, and others) in UTC for all users.</span></span> <span data-ttu-id="eee1f-122">Cela peut aider les analystes de sécurité travaillant à différents endroits dans le monde à utiliser les mêmes horodatés lors de l’étude des événements.</span><span class="sxs-lookup"><span data-stu-id="eee1f-122">This can help security analysts working in different locations across the globe to use the same time stamps while investigating events.</span></span>

### <a name="local-time-zone"></a><span data-ttu-id="eee1f-123">Fuseau horaire local</span><span class="sxs-lookup"><span data-stu-id="eee1f-123">Local time zone</span></span>
<span data-ttu-id="eee1f-124">Vous pouvez choisir que Microsoft Defender pour le point de terminaison utilise les paramètres de fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="eee1f-124">You can choose to have Microsoft Defender for Endpoint use local time zone settings.</span></span> <span data-ttu-id="eee1f-125">Toutes les alertes et événements s’affichent à l’aide de votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="eee1f-125">All alerts and events will be displayed using your local time zone.</span></span>

<span data-ttu-id="eee1f-126">Le fuseau horaire local est pris à partir des paramètres régionaux de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="eee1f-126">The local time zone is taken from your device’s regional settings.</span></span> <span data-ttu-id="eee1f-127">Si vous modifiez vos paramètres régionaux, le fuseau horaire de Microsoft Defender for Endpoint change également.</span><span class="sxs-lookup"><span data-stu-id="eee1f-127">If you change your regional settings, the Microsoft Defender for Endpoint time zone will also change.</span></span> <span data-ttu-id="eee1f-128">Le choix de ce paramètre signifie que les timestamps affichés dans Microsoft Defender pour Endpoint seront alignés sur l’heure locale pour tous les utilisateurs de Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="eee1f-128">Choosing this setting means that the timestamps displayed in Microsoft Defender for Endpoint will be aligned to local time for all Microsoft Defender for Endpoint users.</span></span> <span data-ttu-id="eee1f-129">Les analystes situés dans différents emplacements globaux voient désormais les alertes De Microsoft Defender pour point de terminaison en fonction de leurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="eee1f-129">Analysts located in different global locations will now see the Microsoft Defender for Endpoint alerts according to their regional settings.</span></span>

<span data-ttu-id="eee1f-130">Choisir d’utiliser l’heure locale peut être utile si les analystes se trouvent dans un emplacement unique.</span><span class="sxs-lookup"><span data-stu-id="eee1f-130">Choosing to use local time can be useful if the analysts are located in a single location.</span></span> <span data-ttu-id="eee1f-131">Dans ce cas, il peut être plus facile de mettre en corrélation les événements avec l’heure locale, par exemple, lorsqu’un utilisateur local clique sur un lien de courrier suspect.</span><span class="sxs-lookup"><span data-stu-id="eee1f-131">In this case it might be easier to correlate events to local time, for example – when a local user clicked on a suspicious email link.</span></span>

### <a name="set-the-time-zone"></a><span data-ttu-id="eee1f-132">Définir le fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="eee1f-132">Set the time zone</span></span>
<span data-ttu-id="eee1f-133">Le fuseau horaire De Microsoft Defender pour le point de terminaison est définie par défaut sur UTC.</span><span class="sxs-lookup"><span data-stu-id="eee1f-133">The Microsoft Defender for Endpoint time zone is set by default to UTC.</span></span>
<span data-ttu-id="eee1f-134">La définition du fuseau horaire modifie également les heures de tous les affichages de Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="eee1f-134">Setting the time zone also changes the times for all Microsoft Defender for Endpoint views.</span></span>
<span data-ttu-id="eee1f-135">Pour définir le fuseau horaire :</span><span class="sxs-lookup"><span data-stu-id="eee1f-135">To set the time zone:</span></span>

1. <span data-ttu-id="eee1f-136">Cliquez sur **l’icône 3** des paramètres de fuseau horaire du menu ![ Fuseau ](images/atp-time-zone.png) horaire.</span><span class="sxs-lookup"><span data-stu-id="eee1f-136">Click the **Time zone** menu ![Time zone settings icon3](images/atp-time-zone.png).</span></span>
2. <span data-ttu-id="eee1f-137">Sélectionnez **l’indicateur UTC** de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="eee1f-137">Select the **Timezone UTC** indicator.</span></span>
3. <span data-ttu-id="eee1f-138">Sélectionnez **le fuseau horaire UTC** ou votre fuseau horaire local, par exemple -7:00.</span><span class="sxs-lookup"><span data-stu-id="eee1f-138">Select **Timezone UTC** or your local time zone, for example -7:00.</span></span>

### <a name="regional-settings"></a><span data-ttu-id="eee1f-139">Paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="eee1f-139">Regional settings</span></span>
<span data-ttu-id="eee1f-140">Pour appliquer différents formats de date pour Microsoft Defender pour le point de terminaison, utilisez les paramètres régionaux pour Internet Explorer (IE) et Microsoft Edge (Edge).</span><span class="sxs-lookup"><span data-stu-id="eee1f-140">To apply different date formats for Microsoft Defender for Endpoint, use regional settings for Internet Explorer (IE) and Microsoft Edge (Edge).</span></span> <span data-ttu-id="eee1f-141">Si vous utilisez un autre navigateur tel que Google Chrome, suivez les étapes requises pour modifier les paramètres d’heure et de date de ce navigateur.</span><span class="sxs-lookup"><span data-stu-id="eee1f-141">If you're using another browser such as Google Chrome, follow the required steps to change the time and date settings for that browser.</span></span> 


<span data-ttu-id="eee1f-142">**Internet Explorer (IE) et Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="eee1f-142">**Internet Explorer (IE) and Microsoft Edge**</span></span>

<span data-ttu-id="eee1f-143">IE et Microsoft Edge utiliser  les paramètres de région configurés dans l’option **Horloges,** Langue et Région du Panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="eee1f-143">IE and Microsoft Edge use the **Region** settings configured in the **Clocks, Language, and Region** option in the Control panel.</span></span> 


#### <a name="known-issues-with-regional-formats"></a><span data-ttu-id="eee1f-144">Problèmes connus avec les formats régionaux</span><span class="sxs-lookup"><span data-stu-id="eee1f-144">Known issues with regional formats</span></span>

<span data-ttu-id="eee1f-145">**Formats de date et d’heure**</span><span class="sxs-lookup"><span data-stu-id="eee1f-145">**Date and time formats**</span></span><br>
<span data-ttu-id="eee1f-146">Il existe des problèmes connus avec les formats d’heure et de date.</span><span class="sxs-lookup"><span data-stu-id="eee1f-146">There are some known issues with the time and date formats.</span></span> <span data-ttu-id="eee1f-147">Si vous configurez vos paramètres régionaux dans d’autres formats que les formats pris en charge, le portail risque de ne pas refléter correctement vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="eee1f-147">If you configure your regional settings to anything other than the supported formats, the portal may not correctly reflect your settings.</span></span>

<span data-ttu-id="eee1f-148">Les formats de date et d’heure suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="eee1f-148">The following date and time formats are supported:</span></span>
- <span data-ttu-id="eee1f-149">Format de date MM/j j/aaie</span><span class="sxs-lookup"><span data-stu-id="eee1f-149">Date format MM/dd/yyyy</span></span>
- <span data-ttu-id="eee1f-150">Date format jd/MM/aaa</span><span class="sxs-lookup"><span data-stu-id="eee1f-150">Date format dd/MM/yyyy</span></span>
- <span data-ttu-id="eee1f-151">Format d’heure hh:mm:ss (format 12 heures)</span><span class="sxs-lookup"><span data-stu-id="eee1f-151">Time format hh:mm:ss (12 hour format)</span></span>

<span data-ttu-id="eee1f-152">Les formats de date et d’heure suivants ne sont actuellement pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="eee1f-152">The following date and time formats are currently not supported:</span></span>
- <span data-ttu-id="eee1f-153">Format de date aay-MM-j j j</span><span class="sxs-lookup"><span data-stu-id="eee1f-153">Date format yyyy-MM-dd</span></span>
- <span data-ttu-id="eee1f-154">Date format dd-MMM-yy</span><span class="sxs-lookup"><span data-stu-id="eee1f-154">Date format dd-MMM-yy</span></span>
- <span data-ttu-id="eee1f-155">Format de date j/MM/aa</span><span class="sxs-lookup"><span data-stu-id="eee1f-155">Date format dd/MM/yy</span></span>
- <span data-ttu-id="eee1f-156">Format de date MM/j j/j/aa</span><span class="sxs-lookup"><span data-stu-id="eee1f-156">Date format MM/dd/yy</span></span>
- <span data-ttu-id="eee1f-157">Format de date avec aa.</span><span class="sxs-lookup"><span data-stu-id="eee1f-157">Date format with yy.</span></span> <span data-ttu-id="eee1f-158">Affiche uniquement yyyy.</span><span class="sxs-lookup"><span data-stu-id="eee1f-158">Will only show yyyy.</span></span>
- <span data-ttu-id="eee1f-159">Format d’heure HH:mm:ss (format 24 heures)</span><span class="sxs-lookup"><span data-stu-id="eee1f-159">Time format HH:mm:ss (24 hour format)</span></span>

<span data-ttu-id="eee1f-160">**Symbole décimal utilisé dans les nombres**</span><span class="sxs-lookup"><span data-stu-id="eee1f-160">**Decimal symbol used in numbers**</span></span><br>
<span data-ttu-id="eee1f-161">Le symbole décimal utilisé est toujours un point, même si une virgule est sélectionnée dans les paramètres de **format** Nombres dans les **paramètres** de région.</span><span class="sxs-lookup"><span data-stu-id="eee1f-161">Decimal symbol used is always a dot, even if a comma is selected in  the **Numbers** format settings in **Region** settings.</span></span> <span data-ttu-id="eee1f-162">Par exemple, 15 500 000 sont affichés en tant que 15,5 000.</span><span class="sxs-lookup"><span data-stu-id="eee1f-162">For example, 15,5K is displayed as 15.5K.</span></span>


