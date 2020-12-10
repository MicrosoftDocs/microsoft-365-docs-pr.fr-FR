---
title: Utiliser Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison
f1.keywords:
- NOCSH
keywords: intégration, Microsoft Defender, ATP
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/29/2020
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Utilisez Microsoft Defender pour Office 365 avec Microsoft Defender for Endpoint pour obtenir des informations plus détaillées sur les menaces pesant sur vos appareils et votre contenu de messagerie.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 8cc78e7d674facb371ea98125b6857502031d26e
ms.sourcegitcommit: ee39faf3507d0edc9497117b3b2854955c959c6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49616511"
---
# <a name="use-microsoft-defender-for-office-365-together-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="3636d-104">Utiliser Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3636d-104">Use Microsoft Defender for Office 365 together with Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="3636d-105">[Microsoft Defender pour Office 365](office-365-atp.md) peut être configuré pour fonctionner avec [Microsoft Defender pour le point de terminaison](https://docs.microsoft.com/windows/security/threat-protection).</span><span class="sxs-lookup"><span data-stu-id="3636d-105">[Microsoft Defender for Office 365](office-365-atp.md) can be configured to work with [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection).</span></span>

<span data-ttu-id="3636d-106">L’intégration de Microsoft Defender pour Office 365 avec Microsoft Defender for Endpoint peut aider votre surveillance d’équipe en matière de sécurité et prendre des mesures rapidement si les appareils des utilisateurs sont menacés.</span><span class="sxs-lookup"><span data-stu-id="3636d-106">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint can help your security operations team monitor and take action quickly if users' devices are at risk.</span></span> <span data-ttu-id="3636d-107">Par exemple, une fois l’intégration activée, votre équipe d’opérations de sécurité pourra voir les appareils potentiellement affectés par un message électronique détecté, ainsi que le nombre d’alertes récentes générées pour ces appareils dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3636d-107">For example, once integration is enabled, your security operations team will be able to see the devices that are potentially affected by a detected email message, as well as how many recent alerts were generated for those devices in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="3636d-108">L’image suivante montre à quoi ressemble l’onglet **appareils** comme qui est activé pour l’intégration de Microsoft Defender pour les points de terminaison :</span><span class="sxs-lookup"><span data-stu-id="3636d-108">The following image depicts what the **Devices** tab looks like have Microsoft Defender for Endpoint integration enabled:</span></span>

![Lorsque Microsoft Defender pour le point de terminaison est activé, vous pouvez voir une liste de périphériques avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)

<span data-ttu-id="3636d-110">Dans cet exemple, vous pouvez voir que les destinataires du message électronique détecté ont quatre appareils et que l’un d’entre eux comporte une alerte.</span><span class="sxs-lookup"><span data-stu-id="3636d-110">In this example, you can see that the recipients of the detected email message have four devices and one has an alert.</span></span> <span data-ttu-id="3636d-111">Si vous cliquez sur le lien d’un appareil, celui-ci s’ouvre dans le centre de sécurité Microsoft Defender ( <https://securitycenter.windows.com> ).</span><span class="sxs-lookup"><span data-stu-id="3636d-111">Clicking the link for a device opens its page in the Microsoft Defender Security Center (<https://securitycenter.windows.com>).</span></span>

> [!TIP]
> <span data-ttu-id="3636d-112">**[En savoir plus sur le centre de sécurité Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** (également appelé portail Microsoft Defender pour les points de terminaison).</span><span class="sxs-lookup"><span data-stu-id="3636d-112">**[Learn more about the Microsoft Defender Security Center](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** (also referred to as the Microsoft Defender for Endpoint portal.)</span></span>

## <a name="requirements"></a><span data-ttu-id="3636d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3636d-113">Requirements</span></span>

- <span data-ttu-id="3636d-114">Votre organisation doit avoir Microsoft Defender pour Office 365 (ou Office 365 E5) et Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="3636d-114">Your organization must have Microsoft Defender for Office 365 (or Office 365 E5) and Microsoft Defender for Endpoint.</span></span>

- <span data-ttu-id="3636d-115">Vous devez être un administrateur général ou disposer d’un rôle d’administrateur de sécurité (tel que administrateur de sécurité) affecté dans le [Centre de sécurité & conformité](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="3636d-115">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in the [Security & Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="3636d-116">(Consultez [la rubrique autorisations dans le centre de sécurité & conformité](permissions-in-the-security-and-compliance-center.md))</span><span class="sxs-lookup"><span data-stu-id="3636d-116">(See [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>

- <span data-ttu-id="3636d-117">Vous devez avoir accès à l' [Explorateur (ou aux détections en temps réel)](threat-explorer.md) dans le centre de sécurité & conformité et au centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="3636d-117">You must have access to both [Explorer (or real-time detections)](threat-explorer.md) in the Security & Compliance Center and the Microsoft Defender Security Center.</span></span>

## <a name="to-integrate-microsoft-defender-for-office-365-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="3636d-118">Pour intégrer Microsoft Defender pour Office 365 à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3636d-118">To integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="3636d-119">L’intégration de Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison est configurée à l’aide du centre de sécurité & de la sécurité et du centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="3636d-119">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint is set up by using both the Security & Compliance Center AND the Microsoft Defender Security Center.</span></span>

1. <span data-ttu-id="3636d-120">En tant qu’administrateur général ou administrateur de sécurité, accédez à <https://protection.office.com> et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="3636d-120">As a global administrator or a security administrator, go to <https://protection.office.com> and sign in.</span></span> <span data-ttu-id="3636d-121">(Vous accédez au centre de sécurité & conformité d’Office 365.)</span><span class="sxs-lookup"><span data-stu-id="3636d-121">(This takes you to the Office 365 Security & Compliance Center.)</span></span>

2. <span data-ttu-id="3636d-122">Dans le volet de navigation, sélectionnez Explorateur de **gestion des menaces** \> .</span><span class="sxs-lookup"><span data-stu-id="3636d-122">In the navigation pane, choose **Threat management** \> **Explorer**.</span></span>

   ![Explorateur dans le menu gestion des menaces](../../media/ThreatMgmt-Explorer-nav.png)

3. <span data-ttu-id="3636d-124">Dans le coin supérieur droit de l’écran, choisissez **Defender pour les paramètres de point de terminaison**.</span><span class="sxs-lookup"><span data-stu-id="3636d-124">In the upper right corner of the screen, choose **Defender for Endpoint Settings**.</span></span>

4. <span data-ttu-id="3636d-125">Dans la boîte de dialogue Microsoft Defender pour la connexion au point de terminaison, activez **connexion à Microsoft Defender pour le point de terminaison**.</span><span class="sxs-lookup"><span data-stu-id="3636d-125">In the Microsoft Defender for Endpoint connection dialog box, turn on **Connect to Microsoft Defender for Endpoint**.</span></span>

   ![Microsoft Defender pour la connexion au point de terminaison](../../media/Explorer-WDATPConnection-dialog.png)

5. <span data-ttu-id="3636d-127">Accédez au centre de sécurité Microsoft Defender ( <https://securitycenter.windows.com> ).</span><span class="sxs-lookup"><span data-stu-id="3636d-127">Go to the Microsoft Defender Security Center (<https://securitycenter.windows.com>).</span></span>

6. <span data-ttu-id="3636d-128">Dans la barre de navigation, sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="3636d-128">In the navigation bar, choose **Settings**.</span></span> <span data-ttu-id="3636d-129">Ensuite, sous **général**, choisissez **fonctionnalités avancées**.</span><span class="sxs-lookup"><span data-stu-id="3636d-129">Then, under **General**, choose **Advanced features**.</span></span>

7. <span data-ttu-id="3636d-130">Faites défiler vers le bas jusqu’à **Office 365 Threat Intelligence Connection** et activez la connexion.</span><span class="sxs-lookup"><span data-stu-id="3636d-130">Scroll down to **Office 365 Threat Intelligence connection**, and turn the connection on.</span></span>

   ![Connexion d’aide à la décision Office 365](../../media/mdatp-oatptoggle.png)

## <a name="related-articles"></a><span data-ttu-id="3636d-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="3636d-132">Related articles</span></span>

[<span data-ttu-id="3636d-133">Fonctionnalités d’enquête et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="3636d-133">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)

[<span data-ttu-id="3636d-134">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3636d-134">Microsoft Defender for Office 365</span></span>](office-365-atp.md)

[<span data-ttu-id="3636d-135">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3636d-135">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection)
