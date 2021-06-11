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
ms.openlocfilehash: 63ae9f8c1136a973e4fccb63ecfbaee2639c3f6f
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904079"
---
# <a name="use-microsoft-defender-for-office-365-together-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="46be1-104">Utiliser Microsoft Defender pour les Office 365 avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="46be1-104">Use Microsoft Defender for Office 365 together with Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="46be1-105">[Microsoft Defender pour Office 365](defender-for-office-365.md) peut être configuré pour fonctionner avec [Microsoft Defender pour le point de terminaison.](/windows/security/threat-protection)</span><span class="sxs-lookup"><span data-stu-id="46be1-105">[Microsoft Defender for Office 365](defender-for-office-365.md) can be configured to work with [Microsoft Defender for Endpoint](/windows/security/threat-protection).</span></span>

<span data-ttu-id="46be1-106">L’intégration de Microsoft Defender pour Office 365 Microsoft Defender pour Endpoint peut aider votre équipe en matière d’opérations de sécurité à surveiller et à prendre des mesures rapidement si les appareils des utilisateurs sont exposés.</span><span class="sxs-lookup"><span data-stu-id="46be1-106">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint can help your security operations team monitor and take action quickly if users' devices are at risk.</span></span> <span data-ttu-id="46be1-107">Par exemple, une fois l’intégration activée, votre équipe des opérations de sécurité pourra voir les appareils potentiellement affectés par un message électronique détecté, ainsi que le nombre d’alertes récentes générées pour ces appareils dans Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="46be1-107">For example, once integration is enabled, your security operations team will be able to see the devices that are potentially affected by a detected email message, as well as how many recent alerts were generated for those devices in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="46be1-108">L’image suivante illustre l’apparence de l’onglet **Appareils** lorsque l’intégration de Microsoft Defender for Endpoint est activée :</span><span class="sxs-lookup"><span data-stu-id="46be1-108">The following image depicts what the **Devices** tab looks like when you have Microsoft Defender for Endpoint integration enabled:</span></span>

![Lorsque Microsoft Defender pour le point de terminaison est activé, vous pouvez voir une liste d’appareils avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)

<span data-ttu-id="46be1-110">Dans cet exemple, vous pouvez voir que les destinataires du message électronique détecté ont quatre appareils et un a une alerte.</span><span class="sxs-lookup"><span data-stu-id="46be1-110">In this example, you can see that the recipients of the detected email message have four devices and one has an alert.</span></span> <span data-ttu-id="46be1-111">Le fait de cliquer sur le lien d’un appareil ouvre sa page [dans Microsoft 365 Defender](../defender-endpoint/microsoft-defender-security-center.md) (anciennement Centre de sécurité Microsoft Defender).</span><span class="sxs-lookup"><span data-stu-id="46be1-111">Clicking the link for a device opens its page in [Microsoft 365 Defender](../defender-endpoint/microsoft-defender-security-center.md) (formerly the Microsoft Defender Security Center).</span></span>

> [!TIP]
> <span data-ttu-id="46be1-112">Le Microsoft 365 Defender remplace le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="46be1-112">The Microsoft 365 Defender portal replaces the Microsoft Defender Security Center.</span></span> <span data-ttu-id="46be1-113">Voir [Microsoft Defender pour le point de terminaison dans Microsoft 365 Defender.](../defender/microsoft-365-security-center-mde.md)</span><span class="sxs-lookup"><span data-stu-id="46be1-113">See [Microsoft Defender for Endpoint in Microsoft 365 Defender](../defender/microsoft-365-security-center-mde.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46be1-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="46be1-114">Requirements</span></span>

- <span data-ttu-id="46be1-115">Votre organisation doit avoir Microsoft Defender pour Office 365 (ou Office 365 E5) et Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="46be1-115">Your organization must have Microsoft Defender for Office 365 (or Office 365 E5) and Microsoft Defender for Endpoint.</span></span>

- <span data-ttu-id="46be1-116">Vous devez être un administrateur général ou avoir un rôle d’administrateur de sécurité (par exemple, Administrateur de la sécurité) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="46be1-116">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in Microsoft 365.</span></span> <span data-ttu-id="46be1-117">(Voir [Autorisations dans le Centre de sécurité & conformité)](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="46be1-117">(See [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>

- <span data-ttu-id="46be1-118">Vous devez avoir accès à [l’Explorateur (ou aux détections en temps réel).](threat-explorer.md)</span><span class="sxs-lookup"><span data-stu-id="46be1-118">You must have access to [Explorer (or real-time detections)](threat-explorer.md).</span></span>

## <a name="to-integrate-microsoft-defender-for-office-365-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="46be1-119">Pour intégrer Microsoft Defender for Office 365 avec Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="46be1-119">To integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="46be1-120">L’intégration de Microsoft Defender pour Office 365 microsoft Defender pour le point de terminaison est définie dans Defender pour Point de terminaison et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="46be1-120">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint is set up in both Defender for Endpoint and Defender for Office 365.</span></span>

1. <span data-ttu-id="46be1-121">En tant qu’administrateur général ou administrateur de sécurité, [https://protection.office.com](https://protection.office.com) connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="46be1-121">As a global administrator or a security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="46be1-122">(Vous êtes alors Office 365 centre de sécurité & conformité.)</span><span class="sxs-lookup"><span data-stu-id="46be1-122">(This takes you to the Office 365 Security & Compliance Center.)</span></span>

2. <span data-ttu-id="46be1-123">Dans le volet de navigation, choisissez **l’Explorateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="46be1-123">In the navigation pane, choose **Threat management** \> **Explorer**.</span></span>

   ![Explorateur dans le menu Gestion des menaces](../../media/ThreatMgmt-Explorer-nav.png)

3. <span data-ttu-id="46be1-125">Dans le coin supérieur droit de l’écran, choisissez Defender pour le point de **terminaison Paramètres (MDE Paramètres).**</span><span class="sxs-lookup"><span data-stu-id="46be1-125">In the upper right corner of the screen, choose **Defender for Endpoint Settings (MDE Settings)**.</span></span>

4. <span data-ttu-id="46be1-126">Dans la boîte de dialogue connexion Microsoft Defender pour point de terminaison, **Connecter à Microsoft Defender pour point de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="46be1-126">In the Microsoft Defender for Endpoint connection dialog box, turn on **Connect to Microsoft Defender for Endpoint**.</span></span>

   ![Connexion microsoft Defender pour point de terminaison](../../media/Explorer-WDATPConnection-dialog.png)

5. <span data-ttu-id="46be1-128">Go to the Microsoft 365 Defender portal ( [https://security.microsoft.com](https://security.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="46be1-128">Go to the Microsoft 365 Defender portal ([https://security.microsoft.com](https://security.microsoft.com).</span></span>

6. <span data-ttu-id="46be1-129">Dans la barre de navigation, choisissez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="46be1-129">In the navigation bar, choose **Settings**.</span></span> <span data-ttu-id="46be1-130">Ensuite, sous **Général,** choisissez **Fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="46be1-130">Then, under **General**, choose **Advanced features**.</span></span>

7. <span data-ttu-id="46be1-131">Faites défiler vers le **bas Office 365 la connexion Threat Intelligence,** puis allumez la connexion.</span><span class="sxs-lookup"><span data-stu-id="46be1-131">Scroll down to **Office 365 Threat Intelligence connection**, and turn the connection on.</span></span>

   ![Office 365 d’intelligence contre les menaces](../../media/mdatp-oatptoggle.png)

## <a name="related-articles"></a><span data-ttu-id="46be1-133">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="46be1-133">Related articles</span></span>

[<span data-ttu-id="46be1-134">Fonctionnalités d’examen et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="46be1-134">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)

[<span data-ttu-id="46be1-135">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="46be1-135">Microsoft Defender for Office 365</span></span>](defender-for-office-365.md)

[<span data-ttu-id="46be1-136">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="46be1-136">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection)
