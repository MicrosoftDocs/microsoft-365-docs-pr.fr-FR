---
title: Intégrer Office 365 - Protection avancée contre les menaces avec Microsoft Defender ATP
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 07/08/2020
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 414fa693-d7b7-4a1d-a387-ebc3b6a52889
ms.collection:
- M365-security-compliance
description: Intégrer Office 365 Advanced Threat Protection avec Microsoft Defender Advanced Threat Protection pour consulter des informations plus détaillées sur la gestion des menaces.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: bfb87edd24a22033b3771ba0fd3c4f1afbbc988e
ms.sourcegitcommit: 41bc923bb31598cea8f02923792c1cd786e39616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2020
ms.locfileid: "45086707"
---
# <a name="integrate-office-365-advanced-threat-protection-with-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="ee94c-103">Intégrer Office 365 Advanced Threat Protection avec Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ee94c-103">Integrate Office 365 Advanced Threat Protection with Microsoft Defender Advanced Threat Protection</span></span>

<span data-ttu-id="ee94c-104">[Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide) (Office 365 ATP) peut être configuré pour fonctionner avec [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection) (Microsoft Defender ATP).</span><span class="sxs-lookup"><span data-stu-id="ee94c-104">[Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp?view=o365-worldwide) (Office 365 ATP) can be configured to work with [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection) (Microsoft Defender ATP).</span></span>

<span data-ttu-id="ee94c-105">L’intégration de la fonctionnalité ATP Office 365 à Microsoft Defender ATP peut aider votre surveillance d’équipe en matière de sécurité et prendre des mesures rapidement si les appareils des utilisateurs sont menacés.</span><span class="sxs-lookup"><span data-stu-id="ee94c-105">Integrating Office 365 ATP with Microsoft Defender ATP can help your security operations team monitor and take action quickly if users' devices are at risk.</span></span> <span data-ttu-id="ee94c-106">Par exemple, une fois l’intégration activée, votre équipe d’opérations de sécurité pourra voir les appareils potentiellement affectés par un message électronique détecté, ainsi que le nombre d’alertes récentes que ces appareils ont dans Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="ee94c-106">For example, once integration is enabled, your security operations team will be able to see the devices that are potentially affected by a detected email message, as well as how many recent alerts those devices have in Microsoft Defender ATP.</span></span> 

<span data-ttu-id="ee94c-107">L’image suivante montre l’apparence de l’onglet **appareils** comme l’activation de l’intégration de Microsoft Defender ATP :</span><span class="sxs-lookup"><span data-stu-id="ee94c-107">The following image depicts what the **Devices** tab looks like have Microsoft Defender ATP integration enabled:</span></span>
  
![Lorsque l’ATP Microsoft Defender est activé, vous pouvez voir une liste des périphériques avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="ee94c-109">Dans cet exemple, vous pouvez voir que les destinataires du message électronique détecté ont quatre appareils et que l’un d’entre eux comporte une alerte.</span><span class="sxs-lookup"><span data-stu-id="ee94c-109">In this example, you can see that the recipients of the detected email message have four devices and one has an alert.</span></span> <span data-ttu-id="ee94c-110">Si vous cliquez sur le lien d’un appareil, celui-ci s’ouvre dans le centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="ee94c-110">Clicking the link for a device opens its page in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

> [!TIP]
> <span data-ttu-id="ee94c-111">**[En savoir plus sur le centre de sécurité Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** (également appelé portail Microsoft Defender ATP).</span><span class="sxs-lookup"><span data-stu-id="ee94c-111">**[Learn more about the Microsoft Defender Security Center](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** (also referred to as the Microsoft Defender ATP portal.)</span></span>
  
## <a name="requirements"></a><span data-ttu-id="ee94c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee94c-112">Requirements</span></span>

- <span data-ttu-id="ee94c-113">Votre organisation doit disposer d’Office 365 ATP plan 2 (ou Office 365 E5) et de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="ee94c-113">Your organization must have Office 365 ATP Plan 2 (or Office 365 E5) and Microsoft Defender ATP.</span></span>
    
- <span data-ttu-id="ee94c-114">Vous devez être un administrateur général ou disposer d’un rôle d’administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [ &amp; Centre de sécurité](https://protection.office.com)et de conformité.</span><span class="sxs-lookup"><span data-stu-id="ee94c-114">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="ee94c-115">(Voir [Permissions in the Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="ee94c-115">(See [Permissions in the Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="ee94c-116">Vous devez avoir accès à l' [Explorateur (ou aux détections en temps réel)](threat-explorer.md) dans le centre de sécurité & conformité et au centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="ee94c-116">You must have access to both [Explorer (or real-time detections)](threat-explorer.md) in the Security & Compliance Center and the Microsoft Defender Security Center.</span></span>
    
## <a name="to-integrate-office-365-atp-with-microsoft-defender-atp"></a><span data-ttu-id="ee94c-117">Pour intégrer la protection avancée contre les menaces Office 365 à Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="ee94c-117">To integrate Office 365 ATP with Microsoft Defender ATP</span></span>

<span data-ttu-id="ee94c-118">L’intégration de la fonctionnalité ATP Office 365 à Microsoft Defender ATP est configurée à l’aide du centre de sécurité & de la sécurité et du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="ee94c-118">Integrating Office 365 ATP with Microsoft Defender ATP is set up by using both the Security & Compliance Center AND the Microsoft Defender Security Center.</span></span>
  
1. <span data-ttu-id="ee94c-119">En tant qu’administrateur général ou administrateur de sécurité, accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="ee94c-119">As a global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="ee94c-120">(Vous accédez au centre de sécurité & conformité d’Office 365.)</span><span class="sxs-lookup"><span data-stu-id="ee94c-120">(This takes you to the Office 365 Security & Compliance Center.)</span></span>
    
2. <span data-ttu-id="ee94c-121">Dans le volet de navigation, sélectionnez Explorateur de **gestion des menaces**  >  **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="ee94c-121">In the navigation pane, choose **Threat management** > **Explorer**.</span></span><br><span data-ttu-id="ee94c-122">![Explorateur dans le menu gestion des menaces](../../media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="ee94c-122">![Explorer in Threat Management menu](../../media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="ee94c-123">Dans le coin supérieur droit de l’écran, sélectionnez **paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="ee94c-123">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="ee94c-124">Dans la boîte de dialogue connexion Microsoft Defender ATP, activez **connexion à Windows ATP**.</span><span class="sxs-lookup"><span data-stu-id="ee94c-124">In the Microsoft Defender ATP connection dialog box, turn on **Connect to Windows ATP**.</span></span><br><span data-ttu-id="ee94c-125">![Connexion ATP Microsoft Defender](../../media/Explorer-WDATPConnection-dialog.png)</span><span class="sxs-lookup"><span data-stu-id="ee94c-125">![Microsoft Defender ATP connection](../../media/Explorer-WDATPConnection-dialog.png)</span></span><br>
    
5. <span data-ttu-id="ee94c-126">Accédez au centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ).</span><span class="sxs-lookup"><span data-stu-id="ee94c-126">Go to the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

6. <span data-ttu-id="ee94c-127">Dans la barre de navigation, sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="ee94c-127">In the navigation bar, choose **Settings**.</span></span> <span data-ttu-id="ee94c-128">Ensuite, sous **général**, choisissez **fonctionnalités avancées**.</span><span class="sxs-lookup"><span data-stu-id="ee94c-128">Then, under **General**, choose **Advanced features**.</span></span>

7. <span data-ttu-id="ee94c-129">Faites défiler vers le bas jusqu’à **Office 365 Threat Intelligence Connection**et activez la connexion.</span><span class="sxs-lookup"><span data-stu-id="ee94c-129">Scroll down to **Office 365 Threat Intelligence connection**, and turn the connection on.</span></span><br/><span data-ttu-id="ee94c-130">![Connexion d’aide à la décision Office 365](../../media/mdatp-oatptoggle.png)</span><span class="sxs-lookup"><span data-stu-id="ee94c-130">![Office 365 threat intelligence connection](../../media/mdatp-oatptoggle.png)</span></span><br>

## <a name="related-articles"></a><span data-ttu-id="ee94c-131">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="ee94c-131">Related articles</span></span>

[<span data-ttu-id="ee94c-132">Fonctionnalités d’enquête et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ee94c-132">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)
  
[<span data-ttu-id="ee94c-133">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="ee94c-133">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="ee94c-134">Microsoft Defender - PACM</span><span class="sxs-lookup"><span data-stu-id="ee94c-134">Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection)
