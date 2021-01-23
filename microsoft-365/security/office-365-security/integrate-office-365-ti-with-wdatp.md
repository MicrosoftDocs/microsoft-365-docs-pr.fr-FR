---
title: Utiliser Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison
f1.keywords:
- NOCSH
keywords: integrate, Microsoft Defender, ATP
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 01/21/2021
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
ms.openlocfilehash: 24b81bb4c445c44d7c0228fa1c4440faff642816
ms.sourcegitcommit: ba830e85899f247e5a1e117d63e09e4d5b8a8020
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49939331"
---
# <a name="use-microsoft-defender-for-office-365-together-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="40b1a-104">Utiliser Microsoft Defender pour Office 365 avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40b1a-104">Use Microsoft Defender for Office 365 together with Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="40b1a-105">[Microsoft Defender pour Office 365](office-365-atp.md) peut être configuré pour fonctionner avec [Microsoft Defender pour point de terminaison.](https://docs.microsoft.com/windows/security/threat-protection)</span><span class="sxs-lookup"><span data-stu-id="40b1a-105">[Microsoft Defender for Office 365](office-365-atp.md) can be configured to work with [Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection).</span></span>

<span data-ttu-id="40b1a-106">L’intégration de Microsoft Defender pour Office 365 à Microsoft Defender pour endpoint peut aider votre équipe en charge des opérations de sécurité à surveiller et à prendre des mesures rapidement si les appareils des utilisateurs sont exposés.</span><span class="sxs-lookup"><span data-stu-id="40b1a-106">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint can help your security operations team monitor and take action quickly if users' devices are at risk.</span></span> <span data-ttu-id="40b1a-107">Par exemple, une fois l’intégration activée, votre équipe des opérations de sécurité pourra voir les appareils potentiellement affectés par un message électronique détecté, ainsi que le nombre d’alertes récentes générées pour ces appareils dans Microsoft Defender pour Endpoint.</span><span class="sxs-lookup"><span data-stu-id="40b1a-107">For example, once integration is enabled, your security operations team will be able to see the devices that are potentially affected by a detected email message, as well as how many recent alerts were generated for those devices in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="40b1a-108">L’image suivante illustre à quoi ressemble l’onglet **Appareils** pour que l’intégration de Microsoft Defender for Endpoint soit activée :</span><span class="sxs-lookup"><span data-stu-id="40b1a-108">The following image depicts what the **Devices** tab looks like have Microsoft Defender for Endpoint integration enabled:</span></span>

![Lorsque Microsoft Defender pour le point de terminaison est activé, vous pouvez voir une liste d’appareils avec des alertes.](../../media/fec928ea-8f0c-44d7-80b9-a2e0a8cd4e89.PNG)

<span data-ttu-id="40b1a-110">Dans cet exemple, vous pouvez voir que les destinataires du message électronique détecté ont quatre appareils et un a une alerte.</span><span class="sxs-lookup"><span data-stu-id="40b1a-110">In this example, you can see that the recipients of the detected email message have four devices and one has an alert.</span></span> <span data-ttu-id="40b1a-111">Le fait de cliquer sur le lien d’un appareil ouvre sa page dans le Centre de sécurité Microsoft Defender ( <https://securitycenter.windows.com> ).</span><span class="sxs-lookup"><span data-stu-id="40b1a-111">Clicking the link for a device opens its page in the Microsoft Defender Security Center (<https://securitycenter.windows.com>).</span></span>

> [!TIP]
> <span data-ttu-id="40b1a-112">**[En savoir plus sur le Centre de](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** sécurité Microsoft Defender (également appelé portail Microsoft Defender pour points de terminaison).)</span><span class="sxs-lookup"><span data-stu-id="40b1a-112">**[Learn more about the Microsoft Defender Security Center](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/use)** (also referred to as the Microsoft Defender for Endpoint portal.)</span></span>

## <a name="requirements"></a><span data-ttu-id="40b1a-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="40b1a-113">Requirements</span></span>

- <span data-ttu-id="40b1a-114">Votre organisation doit avoir Microsoft Defender pour Office 365 (ou Office 365 E5) et Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="40b1a-114">Your organization must have Microsoft Defender for Office 365 (or Office 365 E5) and Microsoft Defender for Endpoint.</span></span>

- <span data-ttu-id="40b1a-115">Vous devez être un administrateur général ou avoir un rôle d’administrateur de sécurité (par exemple, Administrateur de la sécurité) affecté dans le Centre de sécurité [& conformité.](https://protection.office.com)</span><span class="sxs-lookup"><span data-stu-id="40b1a-115">You must be a global administrator or have a security administrator role (such as Security Administrator) assigned in the [Security & Compliance Center](https://protection.office.com).</span></span> <span data-ttu-id="40b1a-116">(Voir [autorisations dans le Centre de sécurité & conformité)](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="40b1a-116">(See [Permissions in the Security & Compliance Center](permissions-in-the-security-and-compliance-center.md))</span></span>

- <span data-ttu-id="40b1a-117">Vous devez avoir accès à [l’Explorateur (ou](threat-explorer.md) aux détections en temps réel) dans le Centre de sécurité & conformité et le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="40b1a-117">You must have access to both [Explorer (or real-time detections)](threat-explorer.md) in the Security & Compliance Center and the Microsoft Defender Security Center.</span></span>

## <a name="to-integrate-microsoft-defender-for-office-365-with-microsoft-defender-for-endpoint"></a><span data-ttu-id="40b1a-118">Pour intégrer Microsoft Defender pour Office 365 à Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40b1a-118">To integrate Microsoft Defender for Office 365 with Microsoft Defender for Endpoint</span></span>

<span data-ttu-id="40b1a-119">L’intégration de Microsoft Defender pour Office 365 à Microsoft Defender pour endpoint est définie à l’aide du Centre de sécurité & conformité et du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="40b1a-119">Integrating Microsoft Defender for Office 365 with Microsoft Defender for Endpoint is set up by using both the Security & Compliance Center AND the Microsoft Defender Security Center.</span></span>

1. <span data-ttu-id="40b1a-120">En tant qu’administrateur général ou administrateur de sécurité, <https://protection.office.com> connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="40b1a-120">As a global administrator or a security administrator, go to <https://protection.office.com> and sign in.</span></span> <span data-ttu-id="40b1a-121">(Cette action vous place dans le Centre de sécurité et conformité Office 365&.)</span><span class="sxs-lookup"><span data-stu-id="40b1a-121">(This takes you to the Office 365 Security & Compliance Center.)</span></span>

2. <span data-ttu-id="40b1a-122">Dans le volet de navigation, choisissez **l’Explorateur de gestion** \> **des menaces.**</span><span class="sxs-lookup"><span data-stu-id="40b1a-122">In the navigation pane, choose **Threat management** \> **Explorer**.</span></span>

   ![Explorateur dans le menu Gestion des menaces](../../media/ThreatMgmt-Explorer-nav.png)

3. <span data-ttu-id="40b1a-124">Dans le coin supérieur droit de l’écran, choisissez Defender pour les paramètres de point de terminaison **(paramètres MDE).**</span><span class="sxs-lookup"><span data-stu-id="40b1a-124">In the upper right corner of the screen, choose **Defender for Endpoint Settings (MDE Settings)**.</span></span>

4. <span data-ttu-id="40b1a-125">Dans la boîte de dialogue connexion Microsoft Defender pour point de terminaison, activer la connexion **à Microsoft Defender pour le point de terminaison.**</span><span class="sxs-lookup"><span data-stu-id="40b1a-125">In the Microsoft Defender for Endpoint connection dialog box, turn on **Connect to Microsoft Defender for Endpoint**.</span></span>

   ![Connexion microsoft Defender pour point de terminaison](../../media/Explorer-WDATPConnection-dialog.png)

5. <span data-ttu-id="40b1a-127">Go to the Microsoft Defender Security Center ( <https://securitycenter.windows.com> ).</span><span class="sxs-lookup"><span data-stu-id="40b1a-127">Go to the Microsoft Defender Security Center (<https://securitycenter.windows.com>).</span></span>

6. <span data-ttu-id="40b1a-128">Dans la barre de navigation, choisissez **Paramètres.**</span><span class="sxs-lookup"><span data-stu-id="40b1a-128">In the navigation bar, choose **Settings**.</span></span> <span data-ttu-id="40b1a-129">Ensuite, sous **Général,** choisissez **Fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="40b1a-129">Then, under **General**, choose **Advanced features**.</span></span>

7. <span data-ttu-id="40b1a-130">Faites défiler vers le bas jusqu’à la connexion **Office 365 Threat Intelligence** et allumez la connexion.</span><span class="sxs-lookup"><span data-stu-id="40b1a-130">Scroll down to **Office 365 Threat Intelligence connection**, and turn the connection on.</span></span>

   ![Connexion à l’intelligence des menaces Office 365](../../media/mdatp-oatptoggle.png)

## <a name="related-articles"></a><span data-ttu-id="40b1a-132">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="40b1a-132">Related articles</span></span>

[<span data-ttu-id="40b1a-133">Fonctionnalités d’examen et de réponse aux menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="40b1a-133">Threat investigation and response capabilities in Office 365</span></span>](office-365-ti.md)

[<span data-ttu-id="40b1a-134">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="40b1a-134">Microsoft Defender for Office 365</span></span>](office-365-atp.md)

[<span data-ttu-id="40b1a-135">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="40b1a-135">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection)
