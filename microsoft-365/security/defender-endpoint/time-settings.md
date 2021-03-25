---
title: Paramètres de fuseau horaire du Centre de sécurité Microsoft Defender
description: Utilisez les informations contenues ici pour configurer les paramètres de fuseau horaire du Centre de sécurité Microsoft Defender et afficher les informations de licence.
keywords: paramètres, Microsoft Defender, veille contre les menaces de cybersécurité, protection avancée contre les menaces, fuseau horaire, utc, heure locale, licence
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
ms.openlocfilehash: 25f2fc979cd6ffe82ba16e1ab870c97cdf4fcfe9
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51066073"
---
# <a name="microsoft-defender-security-center-time-zone-settings"></a><span data-ttu-id="b35cb-104">Paramètres de fuseau horaire du Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="b35cb-104">Microsoft Defender Security Center time zone settings</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b35cb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b35cb-105">**Applies to:**</span></span>
- [<span data-ttu-id="b35cb-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b35cb-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="b35cb-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b35cb-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)




><span data-ttu-id="b35cb-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b35cb-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b35cb-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b35cb-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-settings-abovefoldlink)

<span data-ttu-id="b35cb-110">Utilisez **l’icône 1** des paramètres de fuseau horaire du menu Fuseau horaire pour configurer le fuseau horaire et ![ afficher les informations de ](images/atp-time-zone.png) licence.</span><span class="sxs-lookup"><span data-stu-id="b35cb-110">Use the **Time zone** menu ![Time zone settings icon1](images/atp-time-zone.png) to configure the time zone and view license information.</span></span>

## <a name="time-zone-settings"></a><span data-ttu-id="b35cb-111">Paramètres de fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="b35cb-111">Time zone settings</span></span>
<span data-ttu-id="b35cb-112">L’aspect du temps est important dans l’évaluation et l’analyse des cyberattaques perçues et réelles.</span><span class="sxs-lookup"><span data-stu-id="b35cb-112">The aspect of time is important in the assessment and analysis of perceived and actual cyberattacks.</span></span>

<span data-ttu-id="b35cb-113">Les enquêtes cyberforensiques s’appuient souvent sur des horodatés pour rassembler la séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="b35cb-113">Cyberforensic investigations often rely on time stamps to piece together the sequence of events.</span></span> <span data-ttu-id="b35cb-114">Il est important que votre système reflète les paramètres de fuseau horaire corrects.</span><span class="sxs-lookup"><span data-stu-id="b35cb-114">It’s important that your system reflects the correct time zone settings.</span></span>

<span data-ttu-id="b35cb-115">Microsoft Defender pour le point de terminaison peut afficher le temps universel coordonné (UTC) ou l’heure locale.</span><span class="sxs-lookup"><span data-stu-id="b35cb-115">Microsoft Defender for Endpoint can display either Coordinated Universal Time (UTC) or local time.</span></span>

<span data-ttu-id="b35cb-116">Votre paramètre de fuseau horaire actuel s’affiche dans le menu Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b35cb-116">Your current time zone setting is shown in the Microsoft Defender for Endpoint menu.</span></span> <span data-ttu-id="b35cb-117">Vous pouvez modifier le fuseau horaire affiché dans le menu **Fuseau** horaire.</span><span class="sxs-lookup"><span data-stu-id="b35cb-117">You can change the displayed time zone in the **Time zone** menu.</span></span>

![Paramètres de fuseau horaire icône2](images/atp-time-zone-menu.png)<span data-ttu-id="b35cb-119">.</span><span class="sxs-lookup"><span data-stu-id="b35cb-119">.</span></span>

### <a name="utc-time-zone"></a><span data-ttu-id="b35cb-120">Fuseau horaire UTC</span><span class="sxs-lookup"><span data-stu-id="b35cb-120">UTC time zone</span></span>
<span data-ttu-id="b35cb-121">Microsoft Defender pour le point de terminaison utilise l’heure UTC par défaut.</span><span class="sxs-lookup"><span data-stu-id="b35cb-121">Microsoft Defender for Endpoint uses UTC time by default.</span></span>

<span data-ttu-id="b35cb-122">La définition du fuseau horaire De Microsoft Defender pour le point de terminaison sur UTC affiche tous les timestamps système (alertes, événements, etc.) en UTC pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b35cb-122">Setting the Microsoft Defender for Endpoint time zone to UTC will display all system timestamps (alerts, events, and others) in UTC for all users.</span></span> <span data-ttu-id="b35cb-123">Cela peut aider les analystes de sécurité travaillant à différents endroits dans le monde à utiliser les mêmes horodatés lors de l’étude des événements.</span><span class="sxs-lookup"><span data-stu-id="b35cb-123">This can help security analysts working in different locations across the globe to use the same time stamps while investigating events.</span></span>

### <a name="local-time-zone"></a><span data-ttu-id="b35cb-124">Fuseau horaire local</span><span class="sxs-lookup"><span data-stu-id="b35cb-124">Local time zone</span></span>
<span data-ttu-id="b35cb-125">Vous pouvez choisir que Microsoft Defender pour le point de terminaison utilise les paramètres de fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="b35cb-125">You can choose to have Microsoft Defender for Endpoint use local time zone settings.</span></span> <span data-ttu-id="b35cb-126">Toutes les alertes et événements s’affichent à l’aide de votre fuseau horaire local.</span><span class="sxs-lookup"><span data-stu-id="b35cb-126">All alerts and events will be displayed using your local time zone.</span></span>

<span data-ttu-id="b35cb-127">Le fuseau horaire local est pris à partir des paramètres régionaux de votre appareil.</span><span class="sxs-lookup"><span data-stu-id="b35cb-127">The local time zone is taken from your device’s regional settings.</span></span> <span data-ttu-id="b35cb-128">Si vous modifiez vos paramètres régionaux, le fuseau horaire de Microsoft Defender for Endpoint change également.</span><span class="sxs-lookup"><span data-stu-id="b35cb-128">If you change your regional settings, the Microsoft Defender for Endpoint time zone will also change.</span></span> <span data-ttu-id="b35cb-129">Le choix de ce paramètre signifie que les timestamps affichés dans Microsoft Defender pour Endpoint seront alignés sur l’heure locale pour tous les utilisateurs de Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="b35cb-129">Choosing this setting means that the timestamps displayed in Microsoft Defender for Endpoint will be aligned to local time for all Microsoft Defender for Endpoint users.</span></span> <span data-ttu-id="b35cb-130">Les analystes situés dans différents emplacements globaux voient désormais les alertes De Microsoft Defender pour point de terminaison en fonction de leurs paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b35cb-130">Analysts located in different global locations will now see the Microsoft Defender for Endpoint alerts according to their regional settings.</span></span>

<span data-ttu-id="b35cb-131">Choisir d’utiliser l’heure locale peut être utile si les analystes se trouvent dans un emplacement unique.</span><span class="sxs-lookup"><span data-stu-id="b35cb-131">Choosing to use local time can be useful if the analysts are located in a single location.</span></span> <span data-ttu-id="b35cb-132">Dans ce cas, il peut être plus facile de mettre en corrélation les événements avec l’heure locale, par exemple, lorsqu’un utilisateur local clique sur un lien de courrier suspect.</span><span class="sxs-lookup"><span data-stu-id="b35cb-132">In this case it might be easier to correlate events to local time, for example – when a local user clicked on a suspicious email link.</span></span>

### <a name="set-the-time-zone"></a><span data-ttu-id="b35cb-133">Définir le fuseau horaire</span><span class="sxs-lookup"><span data-stu-id="b35cb-133">Set the time zone</span></span>
<span data-ttu-id="b35cb-134">Le fuseau horaire De Microsoft Defender pour le point de terminaison est définie par défaut sur UTC.</span><span class="sxs-lookup"><span data-stu-id="b35cb-134">The Microsoft Defender for Endpoint time zone is set by default to UTC.</span></span>
<span data-ttu-id="b35cb-135">La définition du fuseau horaire modifie également les heures de tous les affichages de Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b35cb-135">Setting the time zone also changes the times for all Microsoft Defender for Endpoint views.</span></span>
<span data-ttu-id="b35cb-136">Pour définir le fuseau horaire :</span><span class="sxs-lookup"><span data-stu-id="b35cb-136">To set the time zone:</span></span>

1. <span data-ttu-id="b35cb-137">Cliquez sur **l’icône 3** des paramètres de fuseau horaire du menu ![ Fuseau ](images/atp-time-zone.png) horaire.</span><span class="sxs-lookup"><span data-stu-id="b35cb-137">Click the **Time zone** menu ![Time zone settings icon3](images/atp-time-zone.png).</span></span>
2. <span data-ttu-id="b35cb-138">Sélectionnez **l’indicateur UTC** de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="b35cb-138">Select the **Timezone UTC** indicator.</span></span>
3. <span data-ttu-id="b35cb-139">Sélectionnez **le fuseau horaire UTC** ou votre fuseau horaire local, par exemple -7:00.</span><span class="sxs-lookup"><span data-stu-id="b35cb-139">Select **Timezone UTC** or your local time zone, for example -7:00.</span></span>

### <a name="regional-settings"></a><span data-ttu-id="b35cb-140">Paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="b35cb-140">Regional settings</span></span>
<span data-ttu-id="b35cb-141">Pour appliquer différents formats de date pour Microsoft Defender pour le point de terminaison, utilisez les paramètres régionaux pour Internet Explorer (IE) et Microsoft Edge (Edge).</span><span class="sxs-lookup"><span data-stu-id="b35cb-141">To apply different date formats for Microsoft Defender for Endpoint, use regional settings for Internet Explorer (IE) and Microsoft Edge (Edge).</span></span> <span data-ttu-id="b35cb-142">Si vous utilisez un autre navigateur tel que Google Chrome, suivez les étapes requises pour modifier les paramètres d’heure et de date de ce navigateur.</span><span class="sxs-lookup"><span data-stu-id="b35cb-142">If you're using another browser such as Google Chrome, follow the required steps to change the time and date settings for that browser.</span></span> 


<span data-ttu-id="b35cb-143">**Internet Explorer (IE) et Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="b35cb-143">**Internet Explorer (IE) and Microsoft Edge**</span></span>

<span data-ttu-id="b35cb-144">IE et Microsoft  Edge utilisent les paramètres de région configurés dans l’option **Horloges,** Langue et Région du Panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="b35cb-144">IE and Microsoft Edge use the **Region** settings configured in the **Clocks, Language, and Region** option in the Control panel.</span></span> 


#### <a name="known-issues-with-regional-formats"></a><span data-ttu-id="b35cb-145">Problèmes connus avec les formats régionaux</span><span class="sxs-lookup"><span data-stu-id="b35cb-145">Known issues with regional formats</span></span>

<span data-ttu-id="b35cb-146">**Formats de date et d’heure**</span><span class="sxs-lookup"><span data-stu-id="b35cb-146">**Date and time formats**</span></span><br>
<span data-ttu-id="b35cb-147">Il existe des problèmes connus avec les formats d’heure et de date.</span><span class="sxs-lookup"><span data-stu-id="b35cb-147">There are some known issues with the time and date formats.</span></span> <span data-ttu-id="b35cb-148">Si vous configurez vos paramètres régionaux dans d’autres formats que les formats pris en charge, le portail risque de ne pas refléter correctement vos paramètres.</span><span class="sxs-lookup"><span data-stu-id="b35cb-148">If you configure your regional settings to anything other than the supported formats, the portal may not correctly reflect your settings.</span></span>

<span data-ttu-id="b35cb-149">Les formats de date et d’heure suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="b35cb-149">The following date and time formats are supported:</span></span>
- <span data-ttu-id="b35cb-150">Format de date MM/j j/aaie</span><span class="sxs-lookup"><span data-stu-id="b35cb-150">Date format MM/dd/yyyy</span></span>
- <span data-ttu-id="b35cb-151">Date format jd/MM/aaa</span><span class="sxs-lookup"><span data-stu-id="b35cb-151">Date format dd/MM/yyyy</span></span>
- <span data-ttu-id="b35cb-152">Format d’heure hh:mm:ss (format 12 heures)</span><span class="sxs-lookup"><span data-stu-id="b35cb-152">Time format hh:mm:ss (12 hour format)</span></span>

<span data-ttu-id="b35cb-153">Les formats de date et d’heure suivants ne sont actuellement pas pris en charge :</span><span class="sxs-lookup"><span data-stu-id="b35cb-153">The following date and time formats are currently not supported:</span></span>
- <span data-ttu-id="b35cb-154">Format de date aay-MM-j j j</span><span class="sxs-lookup"><span data-stu-id="b35cb-154">Date format yyyy-MM-dd</span></span>
- <span data-ttu-id="b35cb-155">Date format dd-MMM-yy</span><span class="sxs-lookup"><span data-stu-id="b35cb-155">Date format dd-MMM-yy</span></span>
- <span data-ttu-id="b35cb-156">Format de date j/MM/aa</span><span class="sxs-lookup"><span data-stu-id="b35cb-156">Date format dd/MM/yy</span></span>
- <span data-ttu-id="b35cb-157">Format de date MM/j j/j/aa</span><span class="sxs-lookup"><span data-stu-id="b35cb-157">Date format MM/dd/yy</span></span>
- <span data-ttu-id="b35cb-158">Format de date avec aa.</span><span class="sxs-lookup"><span data-stu-id="b35cb-158">Date format with yy.</span></span> <span data-ttu-id="b35cb-159">Affiche uniquement yyyy.</span><span class="sxs-lookup"><span data-stu-id="b35cb-159">Will only show yyyy.</span></span>
- <span data-ttu-id="b35cb-160">Format d’heure HH:mm:ss (format 24 heures)</span><span class="sxs-lookup"><span data-stu-id="b35cb-160">Time format HH:mm:ss (24 hour format)</span></span>

<span data-ttu-id="b35cb-161">**Symbole décimal utilisé dans les nombres**</span><span class="sxs-lookup"><span data-stu-id="b35cb-161">**Decimal symbol used in numbers**</span></span><br>
<span data-ttu-id="b35cb-162">Le symbole décimal utilisé est toujours un point, même si une virgule est sélectionnée dans les paramètres de **format** Nombres dans les **paramètres** de région.</span><span class="sxs-lookup"><span data-stu-id="b35cb-162">Decimal symbol used is always a dot, even if a comma is selected in  the **Numbers** format settings in **Region** settings.</span></span> <span data-ttu-id="b35cb-163">Par exemple, 15 500 000 sont affichés en tant que 15,5 000.</span><span class="sxs-lookup"><span data-stu-id="b35cb-163">For example, 15,5K is displayed as 15.5K.</span></span>


