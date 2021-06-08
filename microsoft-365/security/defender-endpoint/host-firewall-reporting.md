---
title: Rapports de pare-feu d’hôte dans Microsoft Defender pour le point de terminaison
description: Hébergez et affichez les rapports de pare-feu dans Microsoft 365 de sécurité.
keywords: windows defender, pare-feu
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
ms.pagetype: security
localization_priority: normal
audience: ITPro
ms.topic: article
author: dansimp
ms.author: dansimp
manager: dansimp
ms.technology: mde
ms.openlocfilehash: 0289d6f920fd6ff35fd446f9c2b8c5516883a4d2
ms.sourcegitcommit: e1e275eb88153bafddf93327adf8f82318913a8d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52809251"
---
# <a name="host-firewall-reporting-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="469d3-104">Rapports de pare-feu d’hôte dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="469d3-104">Host firewall reporting in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="469d3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="469d3-105">**Applies to:**</span></span>
- [<span data-ttu-id="469d3-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="469d3-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="469d3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="469d3-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="469d3-108">Si vous êtes un administrateur, vous pouvez désormais héberger des rapports de pare-feu [Microsoft 365 centre de sécurité.](https://security.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="469d3-108">If you are an admin, you can now host firewall reporting to [Microsoft 365 security center](https://security.microsoft.com).</span></span> <span data-ttu-id="469d3-109">Cette fonctionnalité vous permet d’afficher les Windows 10 et Windows de pare-feu Server 2019 à partir d’un emplacement centralisé.</span><span class="sxs-lookup"><span data-stu-id="469d3-109">This feature enables you to view Windows 10 and Windows Server 2019 firewall reporting from a centralized location.</span></span> 

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="469d3-110">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="469d3-110">What do you need to know before you begin?</span></span> 

- <span data-ttu-id="469d3-111">Vous devez être en cours Windows 10 ou Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="469d3-111">You must be running Windows 10 or Windows Server 2019.</span></span>
- <span data-ttu-id="469d3-112">Pour intégrer des appareils au service Microsoft Defender for Endpoint, voir [ici.](onboard-configure.md)</span><span class="sxs-lookup"><span data-stu-id="469d3-112">To onboard devices to the Microsoft Defender for Endpoint service, see [here](onboard-configure.md).</span></span> 
- <span data-ttu-id="469d3-113">Pour que Microsoft 365 centre de sécurité commence à recevoir les données, vous devez activer les événements **d’audit** Pare-feu Windows Defender avec Fonctions avancées de sécurité :</span><span class="sxs-lookup"><span data-stu-id="469d3-113">For Microsoft 365 security center to start receiving the data, you must enable **Audit Events** for Windows Defender Firewall with Advanced Security:</span></span> 
    - [<span data-ttu-id="469d3-114">Auditer le drop de paquets de plateforme de filtrage</span><span class="sxs-lookup"><span data-stu-id="469d3-114">Audit Filtering Platform Packet Drop</span></span>](/windows/security/threat-protection/auditing/audit-filtering-platform-packet-drop)
    - [<span data-ttu-id="469d3-115">Auditer la connexion à la plateforme de filtrage</span><span class="sxs-lookup"><span data-stu-id="469d3-115">Audit Filtering Platform Connection</span></span>](/windows/security/threat-protection/auditing/audit-filtering-platform-connection) 
- <span data-ttu-id="469d3-116">Activez ces événements à l’aide de l’Éditeur d’objets de stratégie de groupe, de la stratégie de sécurité locale ou auditpol.exe commandes.</span><span class="sxs-lookup"><span data-stu-id="469d3-116">Enable these events by using Group Policy Object Editor, Local Security Policy, or the auditpol.exe commands.</span></span> <span data-ttu-id="469d3-117">Pour plus d’informations, voir [ici.](/windows/win32/fwp/auditing-and-logging)</span><span class="sxs-lookup"><span data-stu-id="469d3-117">For more information, see [here](/windows/win32/fwp/auditing-and-logging).</span></span> 
    - <span data-ttu-id="469d3-118">Les deux commandes PowerShell sont :</span><span class="sxs-lookup"><span data-stu-id="469d3-118">The two PowerShell commands are:</span></span>
        - <span data-ttu-id="469d3-119">**auditpol /set /subcategory:"Filtering Platform Packet Drop » /failure:enable**</span><span class="sxs-lookup"><span data-stu-id="469d3-119">**auditpol /set /subcategory:"Filtering Platform Packet Drop" /failure:enable**</span></span> 
        - <span data-ttu-id="469d3-120">**auditpol /set /subcategory:"Filtering Platform Connection » /failure:enable**</span><span class="sxs-lookup"><span data-stu-id="469d3-120">**auditpol /set /subcategory:"Filtering Platform Connection" /failure:enable**</span></span> 

## <a name="the-process"></a><span data-ttu-id="469d3-121">Processus</span><span class="sxs-lookup"><span data-stu-id="469d3-121">The process</span></span>
> [!NOTE]
> <span data-ttu-id="469d3-122">Veillez à suivre les instructions de la section ci-dessus et à configurer correctement vos appareils pour la participation à la prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="469d3-122">Make sure to follow the instructions from the section above and properly configure your devices for the early preview participation.</span></span>

- <span data-ttu-id="469d3-123">Une fois les événements Microsoft 365, le centre de sécurité commence à surveiller les données.</span><span class="sxs-lookup"><span data-stu-id="469d3-123">After enabling the events, Microsoft 365 security center will start to monitor the data.</span></span>
    - <span data-ttu-id="469d3-124">Adresse IP distante, port distant, port local, adresse IP locale, nom de l’ordinateur, processus entre les connexions entrantes et sortantes.</span><span class="sxs-lookup"><span data-stu-id="469d3-124">Remote IP, Remote Port, Local Port, Local IP, Computer Name, Process across inbound and outbound connections.</span></span>
- <span data-ttu-id="469d3-125">Les administrateurs peuvent désormais voir Windows activité de pare-feu [hôte ici.](https://security.microsoft.com/firewall)</span><span class="sxs-lookup"><span data-stu-id="469d3-125">Admins can now see Windows host firewall activity [here](https://security.microsoft.com/firewall).</span></span>
    - <span data-ttu-id="469d3-126">La création de rapports supplémentaires peut être facilitée en téléchargeant le [script](https://github.com/microsoft/MDATP-PowerBI-Templates/tree/master/Firewall) de création de rapports personnalisé pour surveiller les activités Pare-feu Windows Defender à l’aide Power BI.</span><span class="sxs-lookup"><span data-stu-id="469d3-126">Additional reporting can be facilitated by downloading the [Custom Reporting script](https://github.com/microsoft/MDATP-PowerBI-Templates/tree/master/Firewall) to monitor the Windows Defender Firewall activities using Power BI.</span></span> 
    - <span data-ttu-id="469d3-127">La réflexion des données peut prendre jusqu’à 12 heures.</span><span class="sxs-lookup"><span data-stu-id="469d3-127">It can take up to 12 hours before the data is reflected.</span></span>

## <a name="supported-scenarios"></a><span data-ttu-id="469d3-128">Scénarios pris en charge</span><span class="sxs-lookup"><span data-stu-id="469d3-128">Supported scenarios</span></span>
<span data-ttu-id="469d3-129">Les scénarios suivants sont pris en charge pendant ring0 Preview.</span><span class="sxs-lookup"><span data-stu-id="469d3-129">The following scenarios are supported during Ring0 Preview.</span></span> 

### <a name="firewall-reporting-in-security-center"></a><span data-ttu-id="469d3-130">Rapports de pare-feu dans le centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="469d3-130">Firewall reporting in security center</span></span>

<span data-ttu-id="469d3-131">Voici quelques exemples de pages de rapport de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="469d3-131">Here is a couple of examples of the firewall report pages.</span></span> <span data-ttu-id="469d3-132">Vous trouverez ici un résumé de l’activité des applications entrantes, sortantes et sortantes.</span><span class="sxs-lookup"><span data-stu-id="469d3-132">Here you will find a summary of inbound, outbound, and application activity.</span></span> <span data-ttu-id="469d3-133">Vous pouvez accéder à cette page directement en accédant à https://security.microsoft.com/firewall .</span><span class="sxs-lookup"><span data-stu-id="469d3-133">You can access this page directly by going to https://security.microsoft.com/firewall.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="469d3-134">![Page de rapports du pare-feu hôte](\images\host-firewall-reporting-page.png)</span><span class="sxs-lookup"><span data-stu-id="469d3-134">![Host firewall reporting page](\images\host-firewall-reporting-page.png)</span></span>

<span data-ttu-id="469d3-135">Ces rapports sont également accessibles en accédant à la section Périphériques de rapport de sécurité des rapports située en bas de la carte Connexions entrantes bloquées du  >    >   **pare-feu.**</span><span class="sxs-lookup"><span data-stu-id="469d3-135">These reports can also be accessed by going to **Reports** > **Security Report** > **Devices** (section) located at the bottom of the **Firewall Blocked Inbound Connections** card.</span></span>

### <a name="from-computers-with-a-blocked-connection-to-device"></a><span data-ttu-id="469d3-136">De « Ordinateurs avec une connexion bloquée » à l’appareil</span><span class="sxs-lookup"><span data-stu-id="469d3-136">From "Computers with a blocked connection" to device</span></span>

<span data-ttu-id="469d3-137">Les cartes supportent les objets interactifs.</span><span class="sxs-lookup"><span data-stu-id="469d3-137">Cards support interactive objects.</span></span> <span data-ttu-id="469d3-138">Vous pouvez consulter l’activité d’un appareil en cliquant sur le nom de l’appareil, qui sera lancé dans un nouvel onglet, et vous diriger directement vers l’onglet Chronologie de https://securitycenter.microsoft.com l’appareil. </span><span class="sxs-lookup"><span data-stu-id="469d3-138">You can drill into the activity of a device by clicking on the device name, which will launch https://securitycenter.microsoft.com in a new tab, and take you directly to the **Device Timeline** tab.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="469d3-139">![Ordinateurs avec une connexion bloquée](\images\firewall-reporting-blocked-connection.png)</span><span class="sxs-lookup"><span data-stu-id="469d3-139">![Computers with a blocked connection](\images\firewall-reporting-blocked-connection.png)</span></span>

<span data-ttu-id="469d3-140">Vous pouvez maintenant sélectionner **l’onglet** Chronologie, qui vous donne la liste des événements associés à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="469d3-140">You can now select the **Timeline** tab, which will give you a list of events associated with that device.</span></span> 

<span data-ttu-id="469d3-141">Après avoir cliqué sur le bouton **Filtres** dans le coin supérieur droit du volet d’affichage, sélectionnez le type d’événement de votre choix.</span><span class="sxs-lookup"><span data-stu-id="469d3-141">After clicking on the **Filters** button on the upper right-hand corner of the viewing pane, select the type of event you want.</span></span> <span data-ttu-id="469d3-142">Dans ce cas, sélectionnez **événements de** pare-feu et le volet sera filtré en événements de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="469d3-142">In this case, select **Firewall events** and the pane will be filtered to Firewall events.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="469d3-143">![Bouton Filtres](\images\firewall-reporting-filters-button.png)</span><span class="sxs-lookup"><span data-stu-id="469d3-143">![Filters button](\images\firewall-reporting-filters-button.png)</span></span>

### <a name="drill-into-advanced-hunting-preview-refresh"></a><span data-ttu-id="469d3-144">Recherche avancée (actualisation de l’aperçu)</span><span class="sxs-lookup"><span data-stu-id="469d3-144">Drill into advanced hunting (preview refresh)</span></span>

<span data-ttu-id="469d3-145">Les rapports de pare-feu  prendre en charge l’exploration à partir de la carte directement dans la recherche avancée en cliquant sur le **bouton Ouvrir le chasse** avancé.</span><span class="sxs-lookup"><span data-stu-id="469d3-145">Firewall reports support drilling from the card directly into **Advanced Hunting** by clicking the **Open Advanced hunting** button.</span></span> <span data-ttu-id="469d3-146">La requête sera pré-remplie.</span><span class="sxs-lookup"><span data-stu-id="469d3-146">The query will be pre-populated.</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="469d3-147">![Bouton Ouvrir le point de recherche avancé](\images\firewall-reporting-advanced-hunting.png)</span><span class="sxs-lookup"><span data-stu-id="469d3-147">![Open Advanced hunting button](\images\firewall-reporting-advanced-hunting.png)</span></span>

<span data-ttu-id="469d3-148">La requête peut maintenant être exécutée et tous les événements de pare-feu associés des 30 derniers jours peuvent être explorer.</span><span class="sxs-lookup"><span data-stu-id="469d3-148">The query can now be executed, and all related Firewall events from the last 30 days can be explored.</span></span> 

<span data-ttu-id="469d3-149">Pour des rapports supplémentaires ou des modifications personnalisées, la requête peut être exportée dans Power BI pour une analyse plus approfondie.</span><span class="sxs-lookup"><span data-stu-id="469d3-149">For additional reporting, or custom changes, the query can be exported into Power BI for further analysis.</span></span> <span data-ttu-id="469d3-150">La création de rapports personnalisés peut être facilitée en téléchargeant le [script](https://github.com/microsoft/MDATP-PowerBI-Templates/tree/master/Firewall) de création de rapports personnalisés pour surveiller les activités Pare-feu Windows Defender l’aide Power BI.</span><span class="sxs-lookup"><span data-stu-id="469d3-150">Custom reporting can be facilitated by downloading the [Custom Reporting script](https://github.com/microsoft/MDATP-PowerBI-Templates/tree/master/Firewall) to monitor the Windows Defender Firewall activities using Power BI.</span></span> 

 