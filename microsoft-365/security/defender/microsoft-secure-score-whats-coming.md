---
title: Qu’arrive-t-il à Microsoft Secure Score ?
description: Décrit les nouvelles modifications apportées au Niveau de sécurité Microsoft dans le centre Microsoft 365 sécurité microsoft.
keywords: score de sécurité Microsoft, score sécurisé, score de sécurité Office 365, score de sécurité Microsoft, centre de sécurité Microsoft 365, actions d’amélioration
ms.prod: m365-security
ms.mktglfcycl: deploy
localization_priority: Normal
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 910eb16ad33555ca61875a346b50cea7e63b2220
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53338552"
---
# <a name="whats-coming-to-microsoft-secure-score"></a><span data-ttu-id="c300a-104">Qu’arrive-t-il à Microsoft Secure Score ?</span><span class="sxs-lookup"><span data-stu-id="c300a-104">What's coming to Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="c300a-105">Microsoft Secure Score se trouve dans https://security.microsoft.com/securescore le centre de sécurité [Microsoft 365.](overview-security-center.md)</span><span class="sxs-lookup"><span data-stu-id="c300a-105">Microsoft Secure Score can be found at https://security.microsoft.com/securescore in the [Microsoft 365 security center](overview-security-center.md).</span></span>

## <a name="proposed-changes"></a><span data-ttu-id="c300a-106">Proposed changes</span><span class="sxs-lookup"><span data-stu-id="c300a-106">Proposed changes</span></span>

<span data-ttu-id="c300a-107">Nous apporterons prochainement des modifications pour faire de [Microsoft Secure Score](microsoft-secure-score.md) un meilleur représentant de votre posture de sécurité et améliorer l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c300a-107">We're making some changes in the near future to make [Microsoft Secure Score](microsoft-secure-score.md) a better representative of your security posture and improve usability.</span></span> <span data-ttu-id="c300a-108">Votre score et le score maximal possible peuvent changer.</span><span class="sxs-lookup"><span data-stu-id="c300a-108">Your score and the maximum possible score may change.</span></span>

### <a name="july-2021"></a><span data-ttu-id="c300a-109">Juillet 2021</span><span class="sxs-lookup"><span data-stu-id="c300a-109">July 2021</span></span>

#### <a name="add-improvement-action-related-to-microsoft-teams"></a><span data-ttu-id="c300a-110">Ajouter une action d’amélioration liée à Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c300a-110">Add improvement action related to Microsoft Teams</span></span>

- <span data-ttu-id="c300a-111">Empêcher les utilisateurs d’appels d’appeler de contourner une salle d’accueil de réunion.</span><span class="sxs-lookup"><span data-stu-id="c300a-111">Restrict dial-in users from bypassing a meeting lobby.</span></span>
- <span data-ttu-id="c300a-112">Limitez le contrôle des participants externes à une Teams réunion.</span><span class="sxs-lookup"><span data-stu-id="c300a-112">Limit external participants from having control in a Teams meeting.</span></span>
- <span data-ttu-id="c300a-113">Empêcher les utilisateurs anonymes de commencer Teams réunions.</span><span class="sxs-lookup"><span data-stu-id="c300a-113">Restrict anonymous users from starting Teams meetings.</span></span>
- <span data-ttu-id="c300a-114">Exiger la mise en place de halls d’Teams réunions.</span><span class="sxs-lookup"><span data-stu-id="c300a-114">Require lobbies to be set up for Teams meetings.</span></span>
- <span data-ttu-id="c300a-115">Configurez les utilisateurs autorisés à être présents dans Teams réunions.</span><span class="sxs-lookup"><span data-stu-id="c300a-115">Configure which users are allowed to be present in Teams meetings.</span></span>

#### <a name="add-improvement-action-related-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="c300a-116">Ajouter une action d’amélioration liée à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c300a-116">Add improvement action related to Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="c300a-117">Corriger la collecte de données du capteur Microsoft Defender pour les points de terminaison pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-117">Fix Microsoft Defender for Endpoint sensor data collection for macOS</span></span>
- <span data-ttu-id="c300a-118">Résoudre les problèmes de communications de Microsoft Defender pour les points de terminaison pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-118">Fix Microsoft Defender for Endpoint impaired communications for macOS</span></span>
- <span data-ttu-id="c300a-119">Définir la longueur minimale du mot de passe sur 15 caractères ou plus dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-119">Set minimum password length to 15 or more characters in macOS</span></span>
- <span data-ttu-id="c300a-120">Définir « Appliquer l’historique des mots de passe » sur « 24 mots de passe ou plus » dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-120">Set 'Enforce password history' to '24 or more password(s)' in macOS</span></span>
- <span data-ttu-id="c300a-121">Définir « Âge maximal du mot de passe » sur « 90 jours ou moins, mais pas 0 » dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-121">Set 'Maximum password age' to '90 or fewer days, but not 0' in macOS</span></span>
- <span data-ttu-id="c300a-122">Définir le seuil de verrouillage du compte sur 5 ou moins dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-122">Set account lockout threshold to 5 or lower in macOS</span></span>
- <span data-ttu-id="c300a-123">Activer le pare-feu sur macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-123">Turn on Firewall on macOS</span></span>
- <span data-ttu-id="c300a-124">Activer Gatekeeper</span><span class="sxs-lookup"><span data-stu-id="c300a-124">Enable Gatekeeper</span></span>
- <span data-ttu-id="c300a-125">Activer la Protection de l’intégrité du système (SIP)</span><span class="sxs-lookup"><span data-stu-id="c300a-125">Enable System Integrity Protection (SIP)</span></span>
- <span data-ttu-id="c300a-126">Activer le chiffrement de disque FileVault</span><span class="sxs-lookup"><span data-stu-id="c300a-126">Enable FileVault Disk Encryption</span></span>
- <span data-ttu-id="c300a-127">Définir l’écran pour le verrouillage lorsque le sériaver démarre dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-127">Set screen to lock when screensaver starts in macOS</span></span>
- <span data-ttu-id="c300a-128">S’assurer que le écran de veille est prêt à démarrer dans 20 minutes ou moins dans macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-128">Ensure screensaver is set to start in 20 minutes or less in macOS</span></span>
- <span data-ttu-id="c300a-129">Dossiers d’accueil sécurisés</span><span class="sxs-lookup"><span data-stu-id="c300a-129">Secure Home Folders</span></span>
- <span data-ttu-id="c300a-130">Activer la Antivirus Microsoft Defender protection en temps réel pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-130">Turn on Microsoft Defender Antivirus real-time protection for macOS</span></span>
- <span data-ttu-id="c300a-131">Activer Antivirus Microsoft Defender protection PUA en mode bloc pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-131">Turn on Microsoft Defender Antivirus PUA protection in block mode for macOS</span></span>
- <span data-ttu-id="c300a-132">Activer Antivirus Microsoft Defender protection cloud pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-132">Enable Microsoft Defender Antivirus cloud-delivered protection for macOS</span></span>
- <span data-ttu-id="c300a-133">Mettre à jour Antivirus Microsoft Defender définitions de données pour macOS</span><span class="sxs-lookup"><span data-stu-id="c300a-133">Update Microsoft Defender Antivirus definitions for macOS</span></span>
- <span data-ttu-id="c300a-134">Corriger la collecte de données du capteur Microsoft Defender pour les points de terminaison pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-134">Fix Microsoft Defender for Endpoint sensor data collection for Linux</span></span>
- <span data-ttu-id="c300a-135">Résoudre les problèmes de communications de Microsoft Defender pour les points de terminaison pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-135">Fix Microsoft Defender for Endpoint impaired communications for Linux</span></span>
- <span data-ttu-id="c300a-136">Comptes d’accès non restreint</span><span class="sxs-lookup"><span data-stu-id="c300a-136">Unrestricted Access Accounts</span></span>
- <span data-ttu-id="c300a-137">Activer Antivirus Microsoft Defender protection en temps réel pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-137">Turn on Microsoft Defender Antivirus real-time protection for Linux</span></span>
- <span data-ttu-id="c300a-138">Activer Antivirus Microsoft Defender protection PUA en mode bloc pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-138">Turn on Microsoft Defender Antivirus PUA protection in block mode for Linux</span></span>
- <span data-ttu-id="c300a-139">Activer Antivirus Microsoft Defender protection cloud pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-139">Enable Microsoft Defender Antivirus cloud-delivered protection for Linux</span></span>
- <span data-ttu-id="c300a-140">Mettre à jour Antivirus Microsoft Defender définitions d’utilisateurs pour Linux</span><span class="sxs-lookup"><span data-stu-id="c300a-140">Update Microsoft Defender Antivirus definitions for Linux</span></span>



## <a name="related-resources"></a><span data-ttu-id="c300a-141">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c300a-141">Related resources</span></span>

- [<span data-ttu-id="c300a-142">Vue d’ensemble du score de sécurisation Microsoft</span><span class="sxs-lookup"><span data-stu-id="c300a-142">Microsoft Secure Score overview</span></span>](microsoft-secure-score.md)
- [<span data-ttu-id="c300a-143">Évaluer votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="c300a-143">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="c300a-144">Suivre votre historique du Score de sécurisation Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="c300a-144">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="c300a-145">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="c300a-145">What's new</span></span>](microsoft-secure-score-whats-new.md)
