---
title: Intégrer Office 365 Advanced Threat Protection avec Microsoft Defender Advanced Threat Protection
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 04/13/2020
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
ms.openlocfilehash: e416d70baf7498b0163d5bd8aa8e923585a5e5a4
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633808"
---
# <a name="integrate-office-365-advanced-threat-protection-with-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="0aa74-103">Intégrer Office 365 Advanced Threat Protection avec Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0aa74-103">Integrate Office 365 Advanced Threat Protection with Microsoft Defender Advanced Threat Protection</span></span>

<span data-ttu-id="0aa74-104">Si vous êtes membre de l’équipe de sécurité de votre organisation, vous pouvez intégrer [Office 365 Advanced Threat Protection](office-365-atp.md) et les fonctionnalités d’enquête et de réponse associées avec [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="0aa74-104">If you are part of your organization's security team, you can integrate [Office 365 Advanced Threat Protection](office-365-atp.md) and related investigation and response features with [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection).</span></span> <span data-ttu-id="0aa74-105">Cela peut vous aider à comprendre rapidement si les ordinateurs des utilisateurs sont exposés lorsque vous étudiez les menaces dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="0aa74-105">This can help you quickly understand if users' machines are at risk when you are investigating threats in Office 365.</span></span> <span data-ttu-id="0aa74-106">Par exemple, une fois l’intégration activée, vous pouvez voir la liste des ordinateurs utilisés par les destinataires d’un message électronique détecté, ainsi que le nombre d’alertes récentes de la protection avancée contre les menaces de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0aa74-106">For example, once integration is enabled, you will be able to see a list of machines that are used by the recipients of a detected email message, as well as how many recent alerts those machines have in Microsoft Defender Advanced Threat Protection.</span></span>
  
<span data-ttu-id="0aa74-107">L’image suivante montre l’onglet **appareils** qui apparaît lorsque l’intégration de Microsoft Defender ATP est activée :</span><span class="sxs-lookup"><span data-stu-id="0aa74-107">The following image shows the **Devices** tab that you'll see when have Microsoft Defender ATP integration enabled:</span></span>
  
![Lorsque l’ATP Microsoft Defender est activé, vous pouvez voir une liste des périphériques avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)
  
<span data-ttu-id="0aa74-109">Dans cet exemple, vous pouvez voir que les destinataires du message électronique ont quatre appareils et que l’un d’entre eux comporte une alerte.</span><span class="sxs-lookup"><span data-stu-id="0aa74-109">In this example, you can see that the recipients of the email message have four devices and one has an alert.</span></span> <span data-ttu-id="0aa74-110">Si vous cliquez sur le lien d’un appareil, celui-ci s’ouvre dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0aa74-110">Clicking the link for a device opens its page in the Microsoft Defender Security Center.</span></span>
  
## <a name="requirements"></a><span data-ttu-id="0aa74-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aa74-111">Requirements</span></span>

- <span data-ttu-id="0aa74-112">Votre organisation doit disposer d’Office 365 ATP plan 2 (ou Office 365 E5) et de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="0aa74-112">Your organization must have Office 365 ATP Plan 2 (or Office 365 E5) and Microsoft Defender ATP.</span></span>
    
- <span data-ttu-id="0aa74-113">Vous devez être un administrateur général ou disposer d’un rôle d’administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [Centre de sécurité &amp; ](https://protection.office.com)et de conformité.</span><span class="sxs-lookup"><span data-stu-id="0aa74-113">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in the [Security &amp; Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="0aa74-114">(Voir [Permissions in &amp; the Security Compliance Center](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="0aa74-114">(See [Permissions in the Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>
    
- <span data-ttu-id="0aa74-115">Vous devez avoir accès à l' [Explorateur (ou aux détections en temps réel)](threat-explorer.md) dans le centre de sécurité & conformité et au centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0aa74-115">You must have access to both [Explorer (or real-time detections)](threat-explorer.md) in the Security & Compliance Center and the Microsoft Defender Security Center.</span></span>
    
## <a name="to-integrate-office-365-atp-with-microsoft-defender-atp"></a><span data-ttu-id="0aa74-116">Pour intégrer la protection avancée contre les menaces Office 365 à Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="0aa74-116">To integrate Office 365 ATP with Microsoft Defender ATP</span></span>

<span data-ttu-id="0aa74-117">L’intégration de la fonctionnalité ATP Office 365 à Microsoft Defender ATP est configurée à l’aide du centre de sécurité & de la sécurité et du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="0aa74-117">Integrating Office 365 ATP with Microsoft Defender ATP is set up by using both the Security & Compliance Center AND the Microsoft Defender Security Center.</span></span>
  
1. <span data-ttu-id="0aa74-118">En tant qu’administrateur général ou administrateur de la sécurité, [https://protection.office.com](https://protection.office.com) accédez à et connectez-vous avec votre compte professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="0aa74-118">As a global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in with your work or school account.</span></span>
    
2. <span data-ttu-id="0aa74-119">Choisissez **Threat management** \> **Explorateur**de gestion des menaces.</span><span class="sxs-lookup"><span data-stu-id="0aa74-119">Choose **Threat management** \> **Explorer**.</span></span><br><span data-ttu-id="0aa74-120">![Explorateur dans le menu gestion des menaces](../../media/ThreatMgmt-Explorer-nav.png)</span><span class="sxs-lookup"><span data-stu-id="0aa74-120">![Explorer in Threat Management menu](../../media/ThreatMgmt-Explorer-nav.png)</span></span><br>
    
3. <span data-ttu-id="0aa74-121">Dans le coin supérieur droit de l’écran, sélectionnez **paramètres WDATP**.</span><span class="sxs-lookup"><span data-stu-id="0aa74-121">In the upper right corner of the screen, choose **WDATP Settings**.</span></span>
    
4. <span data-ttu-id="0aa74-122">Dans la boîte de dialogue connexion Microsoft Defender ATP, activez **connexion à Windows ATP**.</span><span class="sxs-lookup"><span data-stu-id="0aa74-122">In the Microsoft Defender ATP connection dialog box, turn on **Connect to Windows ATP**.</span></span><br><span data-ttu-id="0aa74-123">![Connexion ATP Microsoft Defender](../../media/Explorer-WDATPConnection-dialog.png)</span><span class="sxs-lookup"><span data-stu-id="0aa74-123">![Microsoft Defender ATP connection](../../media/Explorer-WDATPConnection-dialog.png)</span></span><br>
    
5. <span data-ttu-id="0aa74-124">Activez la connexion dans le centre de sécurité Microsoft Defender ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span><span class="sxs-lookup"><span data-stu-id="0aa74-124">Enable the connection in the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aa74-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa74-125">Related topics</span></span>

[<span data-ttu-id="0aa74-126">Fonctionnalités d’enquête et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0aa74-126">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)
  
[<span data-ttu-id="0aa74-127">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0aa74-127">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  

