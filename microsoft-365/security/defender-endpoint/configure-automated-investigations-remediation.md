---
title: Configurer des fonctionnalités automatisées d’examen et de correction
description: Configurer vos fonctionnalités automatisées d’examen et de correction dans Microsoft Defender pour le point de terminaison.
keywords: configurer, configurer, automatisé, examen, détection, alertes, correction, réponse
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.technology: mde
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: JoeDavies-MSFT
ms.author: josephd
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: how-to
ms.date: 01/27/2021
ms.reviewer: ramarom, evaldm, isco, mabraitm, chriggs
ms.openlocfilehash: bd86458749db4019bb247a3664748b9891965754
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841329"
---
# <a name="configure-automated-investigation-and-remediation-capabilities-in-microsoft-defender-for-endpoint"></a><span data-ttu-id="70598-104">Configurer les fonctionnalités automatisées d’examen et de correction dans Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="70598-104">Configure automated investigation and remediation capabilities in Microsoft Defender for Endpoint</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="70598-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="70598-105">**Applies to:**</span></span>
- [<span data-ttu-id="70598-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="70598-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="70598-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="70598-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="70598-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="70598-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="70598-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="70598-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="70598-110">Si votre organisation utilise [Microsoft Defender pour le](/windows/security/threat-protection/) point de terminaison (Defender pour point de terminaison), les fonctionnalités d’examen et de correction automatisées peuvent économiser du temps et des efforts de votre équipe en matière d’opérations de sécurité. [](/microsoft-365/security/defender-endpoint/automated-investigations)</span><span class="sxs-lookup"><span data-stu-id="70598-110">If your organization is using [Microsoft Defender for Endpoint](/windows/security/threat-protection/) (Defender for Endpoint), [automated investigation and remediation capabilities](/microsoft-365/security/defender-endpoint/automated-investigations) can save your security operations team time and effort.</span></span> <span data-ttu-id="70598-111">Comme indiqué dans ce [billet de blog,](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/enhance-your-soc-with-microsoft-defender-atp-automatic/ba-p/848946)ces fonctionnalités imitent les étapes idéales qu’un analyste de sécurité prend pour examiner et corriger les menaces.</span><span class="sxs-lookup"><span data-stu-id="70598-111">As outlined in [this blog post](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/enhance-your-soc-with-microsoft-defender-atp-automatic/ba-p/848946), these capabilities mimic the ideal steps that a security analyst takes to investigate and remediate threats.</span></span> <span data-ttu-id="70598-112">[En savoir plus sur l’examen et la correction automatisés.](/microsoft-365/security/defender-endpoint/automated-investigations)</span><span class="sxs-lookup"><span data-stu-id="70598-112">[Learn more about automated investigation and remediation](/microsoft-365/security/defender-endpoint/automated-investigations).</span></span> 

<span data-ttu-id="70598-113">Pour configurer l’examen et la correction automatisés,</span><span class="sxs-lookup"><span data-stu-id="70598-113">To configure automated investigation and remediation,</span></span>
1. <span data-ttu-id="70598-114">[Activer les fonctionnalités](#turn-on-automated-investigation-and-remediation); et</span><span class="sxs-lookup"><span data-stu-id="70598-114">[Turn on the features](#turn-on-automated-investigation-and-remediation); and</span></span> 
2. <span data-ttu-id="70598-115">[Configurer des groupes d’appareils.](#set-up-device-groups)</span><span class="sxs-lookup"><span data-stu-id="70598-115">[Set up device groups](#set-up-device-groups).</span></span>

## <a name="turn-on-automated-investigation-and-remediation"></a><span data-ttu-id="70598-116">Activer l’examen et la correction automatisés</span><span class="sxs-lookup"><span data-stu-id="70598-116">Turn on automated investigation and remediation</span></span>

1. <span data-ttu-id="70598-117">En tant qu’administrateur général ou administrateur de sécurité, Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="70598-117">As a global administrator or security administrator, go to the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)) and sign in.</span></span>
2. <span data-ttu-id="70598-118">Dans le volet de navigation, choisissez **Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="70598-118">In the navigation pane, choose **Settings**.</span></span>
3. <span data-ttu-id="70598-119">Dans la section **Général,** sélectionnez **Fonctionnalités avancées.**</span><span class="sxs-lookup"><span data-stu-id="70598-119">In the **General** section, select **Advanced features**.</span></span>
4. <span data-ttu-id="70598-120">Activer **l’examen automatisé et** résoudre automatiquement les **alertes.**</span><span class="sxs-lookup"><span data-stu-id="70598-120">Turn on both **Automated Investigation** and **Automatically resolve alerts**.</span></span>

## <a name="set-up-device-groups"></a><span data-ttu-id="70598-121">Configurer des groupes d’appareils</span><span class="sxs-lookup"><span data-stu-id="70598-121">Set up device groups</span></span>

1. <span data-ttu-id="70598-122">In the Centre de sécurité Microsoft Defender ( [https://securitycenter.windows.com](https://securitycenter.windows.com) ), on the **Paramètres** page, under **Permissions**, select **Device groups**.</span><span class="sxs-lookup"><span data-stu-id="70598-122">In the Microsoft Defender Security Center ([https://securitycenter.windows.com](https://securitycenter.windows.com)), on the **Settings** page, under **Permissions**, select **Device groups**.</span></span>
2. <span data-ttu-id="70598-123">Sélectionnez **+ Ajouter un groupe d’appareils.**</span><span class="sxs-lookup"><span data-stu-id="70598-123">Select **+ Add device group**.</span></span>
3. <span data-ttu-id="70598-124">Créez au moins un groupe d’appareils, comme suit :</span><span class="sxs-lookup"><span data-stu-id="70598-124">Create at least one device group, as follows:</span></span>
   - <span data-ttu-id="70598-125">Spécifiez un nom et une description pour le groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="70598-125">Specify a name and description for the device group.</span></span>
   - <span data-ttu-id="70598-126">Dans la liste **des niveaux Automation,** sélectionnez un niveau, tel que Complet , pour corriger automatiquement **les menaces.**</span><span class="sxs-lookup"><span data-stu-id="70598-126">In the **Automation level list**, select a level, such as **Full – remediate threats automatically**.</span></span> <span data-ttu-id="70598-127">Le niveau d’automatisation détermine si des actions de correction sont prises automatiquement, ou uniquement après approbation.</span><span class="sxs-lookup"><span data-stu-id="70598-127">The automation level determines whether remediation actions are taken automatically, or only upon approval.</span></span> <span data-ttu-id="70598-128">Pour en savoir plus, consultez [Les niveaux Automation dans l’examen et la correction automatisés.](automation-levels.md)</span><span class="sxs-lookup"><span data-stu-id="70598-128">To learn more, see [Automation levels in automated investigation and remediation](automation-levels.md).</span></span>
   - <span data-ttu-id="70598-129">Dans la section **Membres,** utilisez une ou plusieurs conditions pour identifier et inclure des appareils.</span><span class="sxs-lookup"><span data-stu-id="70598-129">In the **Members** section, use one or more conditions to identify and include devices.</span></span>
   - <span data-ttu-id="70598-130">Sous **l’onglet** Accès utilisateur, sélectionnez [les groupes Azure Active Directory qui](/azure/active-directory/fundamentals/active-directory-manage-groups?context=azure/active-directory/users-groups-roles/context/ugr-context) doivent avoir accès au groupe d’appareils que vous créez.</span><span class="sxs-lookup"><span data-stu-id="70598-130">On the **User access** tab, select the [Azure Active Directory groups](/azure/active-directory/fundamentals/active-directory-manage-groups?context=azure/active-directory/users-groups-roles/context/ugr-context) who should have access to the device group you're creating.</span></span>
4. <span data-ttu-id="70598-131">Sélectionnez **Terminé** lorsque vous avez terminé la configuration de votre groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="70598-131">Select **Done** when you're finished setting up your device group.</span></span>

## <a name="next-steps"></a><span data-ttu-id="70598-132">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="70598-132">Next steps</span></span>

- [<span data-ttu-id="70598-133">Visitez le centre de mise en œuvre pour afficher les actions de correction en attente et terminées</span><span class="sxs-lookup"><span data-stu-id="70598-133">Visit the Action Center to view pending and completed remediation actions</span></span>](/microsoft-365/security/defender-endpoint/auto-investigation-action-center#the-action-center)
- [<span data-ttu-id="70598-134">Examiner et approuver les actions en attente</span><span class="sxs-lookup"><span data-stu-id="70598-134">Review and approve pending actions</span></span>](/microsoft-365/security/defender-endpoint/manage-auto-investigation)

## <a name="see-also"></a><span data-ttu-id="70598-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70598-135">See also</span></span>

- [<span data-ttu-id="70598-136">Résoudre des faux négatifs/positifs dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="70598-136">Address false positives/negatives in Microsoft Defender for Endpoint</span></span>](defender-endpoint-false-positives-negatives.md)
