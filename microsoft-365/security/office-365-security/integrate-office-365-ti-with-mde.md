---
title: Utiliser Microsoft Defender pour les Office 365 avec Microsoft Defender pour le point de terminaison
f1.keywords:
- NOCSH
keywords: intégrer, Microsoft Defender, Microsoft Defender pour point de terminaison
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 06/10/2021
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Utilisez Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison pour obtenir des informations plus détaillées sur les menaces contre vos appareils et le contenu de votre courrier électronique.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 1d54e4ec40c636b8b3ea319e79cbad5005850952
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029262"
---
# <a name="use-microsoft-defender-for-office-365-together-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="b2206-104">Utiliser Microsoft Defender pour les Office 365 avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b2206-104">Use Microsoft Defender for Office 365 together with Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="b2206-105">[Microsoft Defender pour Office 365](defender-for-office-365.md) peut être configuré pour fonctionner avec [Microsoft Defender pour endpoint](/windows/security/threat-protection).</span><span class="sxs-lookup"><span data-stu-id="b2206-105">[Microsoft Defender for Office 365](defender-for-office-365.md) can be configured to work with [Microsoft Defender for Endpoint](/windows/security/threat-protection).</span></span>

<span data-ttu-id="b2206-106">L’intégration de Microsoft Defender pour Office 365 avec Microsoft Defender for Endpoint peut aider votre équipe des opérations de sécurité à surveiller et à prendre des mesures rapidement si les appareils des utilisateurs sont exposés.</span><span class="sxs-lookup"><span data-stu-id="b2206-106">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint can help your security operations team monitor and take action quickly if users' devices are at risk.</span></span> <span data-ttu-id="b2206-107">Par exemple, une fois l’intégration activée, votre équipe des opérations de sécurité pourra voir les appareils potentiellement affectés par un message électronique détecté, ainsi que le nombre d’alertes récentes générées pour ces appareils dans Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="b2206-107">For example, once integration is enabled, your security operations team will be able to see the devices that are potentially affected by a detected email message, as well as how many recent alerts were generated for those devices in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="b2206-108">L’image suivante illustre l’apparence de l’onglet **Appareils** lorsque l’intégration de Microsoft Defender for Endpoint est activée :</span><span class="sxs-lookup"><span data-stu-id="b2206-108">The following image depicts what the **Devices** tab looks like when you have Microsoft Defender for Endpoint integration enabled:</span></span>

![Lorsque Microsoft Defender pour le point de terminaison est activé, vous pouvez voir une liste d’appareils avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)

<span data-ttu-id="b2206-110">Dans cet exemple, vous pouvez voir que les destinataires du message électronique détecté ont quatre appareils et un a une alerte.</span><span class="sxs-lookup"><span data-stu-id="b2206-110">In this example, you can see that the recipients of the detected email message have four devices and one has an alert.</span></span> <span data-ttu-id="b2206-111">Cliquer sur le lien d’un appareil ouvre sa page [dans Microsoft 365 Defender](../defender-endpoint/microsoft-defender-security-center.md) (anciennement centre de sécurité Microsoft Defender).</span><span class="sxs-lookup"><span data-stu-id="b2206-111">Clicking the link for a device opens its page in [Microsoft 365 Defender](../defender-endpoint/microsoft-defender-security-center.md) (formerly the Microsoft Defender security center).</span></span>

> [!TIP]
> <span data-ttu-id="b2206-112">Le Microsoft 365 Defender de l’entreprise remplace le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b2206-112">The Microsoft 365 Defender portal replaces the Microsoft Defender Security Center.</span></span> <span data-ttu-id="b2206-113">Voir [Microsoft Defender pour le point de terminaison dans Microsoft 365 Defender](../defender/microsoft-365-security-center-mde.md).</span><span class="sxs-lookup"><span data-stu-id="b2206-113">See [Microsoft Defender for Endpoint in Microsoft 365 Defender](../defender/microsoft-365-security-center-mde.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2206-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b2206-114">Requirements</span></span>

- <span data-ttu-id="b2206-115">Votre organisation doit avoir Microsoft Defender pour Office 365 (ou Office 365 E5) et Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b2206-115">Your organization must have Microsoft Defender for Office 365 (or Office 365 E5) and Microsoft Defender for Endpoint.</span></span>

- <span data-ttu-id="b2206-116">Vous devez être un administrateur général ou avoir un rôle d’administrateur de sécurité (par exemple, Administrateur de la sécurité) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b2206-116">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in Microsoft 365.</span></span> <span data-ttu-id="b2206-117">Pour plus d’informations, [voir Autorisations dans le portail Microsoft 365 Defender.](permissions-microsoft-365-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="b2206-117">For more information, see [Permissions in the Microsoft 365 Defender portal](permissions-microsoft-365-security-center.md).</span></span>

- <span data-ttu-id="b2206-118">Vous devez avoir accès à [l’Explorateur (ou aux détections en temps réel).](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="b2206-118">You must have access to [Explorer (or real-time detections)](threat-explorer.md).</span></span>

## <a name="to-integrate-microsoft-defender-for-office-365-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="b2206-119">Pour intégrer Microsoft Defender for Office 365 avec Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="b2206-119">To integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="b2206-120">L’intégration de Microsoft Defender pour Office 365 microsoft Defender pour le point de terminaison est définie dans Defender pour Point de terminaison et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="b2206-120">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint is set up in both Defender for Endpoint and Defender for Office 365.</span></span>

1. <span data-ttu-id="b2206-121">En tant qu’administrateur général ou administrateur de sécurité, <https://security.microsoft.com/threatexplorer> .</span><span class="sxs-lookup"><span data-stu-id="b2206-121">As a global administrator or a security administrator,<https://security.microsoft.com/threatexplorer>.</span></span>

2. <span data-ttu-id="b2206-122">Dans le volet de navigation, sélectionnez **Email & Collaboration** \> **Explorer.**</span><span class="sxs-lookup"><span data-stu-id="b2206-122">In the navigation pane, choose **Email & collaboration** \> **Explorer**.</span></span>

3. <span data-ttu-id="b2206-123">Dans la page **Explorateur,** dans le coin supérieur droit de l’écran, cliquez sur **MDE Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="b2206-123">On the **Explorer** page, in the upper right corner of the screen, click **MDE Settings**.</span></span>

4. <span data-ttu-id="b2206-124">Dans le volant de connexion **Microsoft Defender** pour point de terminaison qui s’affiche, Connecter à **Microsoft Defender** pour le point de terminaison ( Activer/ Activer), puis cliquez sur Fermer l’icône ![ ](../../media/scc-toggle-on.png) ![ ](../../media/m365-cc-sc-close-icon.png) **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b2206-124">In the **Microsoft Defender for Endpoint connection** flyout that appears, turn on **Connect to Microsoft Defender for Endpoint** (![Toggle on](../../media/scc-toggle-on.png)) and then click ![Close icon](../../media/m365-cc-sc-close-icon.png) **Close**.</span></span>

    :::image type="content" source="../../media/explorer-mdeconnection-dialognew.png" alt-text="Connexion MDE":::

5. <span data-ttu-id="b2206-126">De retour dans le volet de navigation, choisissez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="b2206-126">Back in the navigation pane, choose **Settings**.</span></span> <span data-ttu-id="b2206-127">Dans la **page Paramètres,** choisissez **Points de terminaison**</span><span class="sxs-lookup"><span data-stu-id="b2206-127">On the **Settings** page, choose **Endpoints**</span></span>

6. <span data-ttu-id="b2206-128">Dans la page **Points de terminaison** qui s’ouvre, choisissez **Fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="b2206-128">On the **Endpoints** page that opens, choose **Advanced features**.</span></span>

7. <span data-ttu-id="b2206-129">Faites défiler vers le **bas Office 365 la connexion Threat Intelligence,** puis allumez-la ![ (activer). ](../../media/scc-toggle-on.png)</span><span class="sxs-lookup"><span data-stu-id="b2206-129">Scroll down to **Office 365 Threat Intelligence connection**, and turn it on (![Toggle on](../../media/scc-toggle-on.png)).</span></span>

   <span data-ttu-id="b2206-130">Lorsque vous avez terminé, cliquez sur **Enregistrer les préférences.**</span><span class="sxs-lookup"><span data-stu-id="b2206-130">When you're finished, click **Save preferences**.</span></span>

## <a name="related-articles"></a><span data-ttu-id="b2206-131">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="b2206-131">Related articles</span></span>

[<span data-ttu-id="b2206-132">Fonctionnalités d’examen et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b2206-132">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)

[<span data-ttu-id="b2206-133">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="b2206-133">Microsoft Defender for Office 365</span></span>](defender-for-office-365.md)

[<span data-ttu-id="b2206-134">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b2206-134">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection)
