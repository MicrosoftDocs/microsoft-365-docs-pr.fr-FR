---
title: Fonctionnalités du score de sécurité Microsoft
description: Décrit les nouvelles modifications apportées à Microsoft Secure score dans le centre de sécurité Microsoft 365.
keywords: score de sécurité Microsoft, score de sécurisation, score de sécurité Office 365, score de sécurité Microsoft, centre de sécurité Microsoft 365, actions d’amélioration
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 82ec67cae86525c055b2232667cccb603830d15f
ms.sourcegitcommit: c51de5e1a4cb9c4a7a9854a4226b32453d9e73e0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "48779247"
---
# <a name="whats-coming-to-microsoft-secure-score"></a><span data-ttu-id="47bec-104">Fonctionnalités du score de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="47bec-104">What's coming to Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="47bec-105">Nous apportons des modifications à l’avenir proche pour faire en sorte que [Microsoft Secure](microsoft-secure-score.md) évalue un meilleur représentant de votre position de sécurité et améliore l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="47bec-105">We're making some changes in the near future to make [Microsoft Secure Score](microsoft-secure-score.md) a better representative of your security posture and improve usability.</span></span> <span data-ttu-id="47bec-106">Votre score et le score maximal possible peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="47bec-106">Your score and the maximum possible score may change.</span></span>

## <a name="proposed-changes"></a><span data-ttu-id="47bec-107">Proposed changes</span><span class="sxs-lookup"><span data-stu-id="47bec-107">Proposed changes</span></span>

### <a name="november-2020"></a><span data-ttu-id="47bec-108">Novembre 2020</span><span class="sxs-lookup"><span data-stu-id="47bec-108">November 2020</span></span>

<span data-ttu-id="47bec-109">Suppression de la possibilité de créer des tickets ServiceNow via le score de sécurité en accédant à **Share > ServiceNow** .</span><span class="sxs-lookup"><span data-stu-id="47bec-109">Removing the ability to create ServiceNow tickets through Secure Score by going to **Share > ServiceNow** .</span></span>

- <span data-ttu-id="47bec-110">La période d’aperçu du connecteur ServiceNow se termine.</span><span class="sxs-lookup"><span data-stu-id="47bec-110">The preview period for the ServiceNow connector is ending.</span></span> <span data-ttu-id="47bec-111">Cette fonctionnalité n’est plus disponible à la fin du 2020.</span><span class="sxs-lookup"><span data-stu-id="47bec-111">This capability will no longer available by the end of 2020.</span></span> <span data-ttu-id="47bec-112">Nous vous remercions pour vos commentaires et le support technique pendant que nous déterminons les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="47bec-112">Thank you for your feedback and continued support while we determine next steps.</span></span>

<span data-ttu-id="47bec-113">Ajout de 18 actions d’amélioration relatives à Microsoft Defender pour le point de terminaison (précédemment Microsoft Defender ATP) :</span><span class="sxs-lookup"><span data-stu-id="47bec-113">Adding 18 improvement actions related to Microsoft Defender for Endpoint (previously Microsoft Defender ATP):</span></span>

<span data-ttu-id="47bec-114">Recommandations relatives à la réduction de la surface d’attaque (ASR) :</span><span class="sxs-lookup"><span data-stu-id="47bec-114">Attack Surface Reduction (ASR) related recommendations:</span></span>
- <span data-ttu-id="47bec-115">Bloquer le contenu exécutable à partir du client de messagerie et de la messagerie Web</span><span class="sxs-lookup"><span data-stu-id="47bec-115">Block executable content from email client and webmail</span></span>
- <span data-ttu-id="47bec-116">Empêcher toutes les applications Office de créer des processus enfants</span><span class="sxs-lookup"><span data-stu-id="47bec-116">Block all Office applications from creating child processes</span></span>
- <span data-ttu-id="47bec-117">Empêcher les applications Office de créer du contenu exécutable</span><span class="sxs-lookup"><span data-stu-id="47bec-117">Block Office applications from creating executable content</span></span>
- <span data-ttu-id="47bec-118">Bloquer l’injection de code dans d’autres processus par les applications Office</span><span class="sxs-lookup"><span data-stu-id="47bec-118">Block Office applications from injecting code into other processes</span></span>
- <span data-ttu-id="47bec-119">Bloquer JavaScript ou VBScript pour lancer le téléchargement de contenu exécutable</span><span class="sxs-lookup"><span data-stu-id="47bec-119">Block JavaScript or VBScript from launching downloaded executable content</span></span>
- <span data-ttu-id="47bec-120">Bloquer l’exécution des scripts potentiellement brouillés</span><span class="sxs-lookup"><span data-stu-id="47bec-120">Block execution of potentially obfuscated scripts</span></span>
- <span data-ttu-id="47bec-121">Bloquer les appels d’API Win32 à partir de macros Office</span><span class="sxs-lookup"><span data-stu-id="47bec-121">Block Win32 API calls from Office macros</span></span>
- <span data-ttu-id="47bec-122">Bloquer l’exécution des fichiers exécutables sauf s’ils répondent à un critère de récurrence, d’âge ou de liste approuvée</span><span class="sxs-lookup"><span data-stu-id="47bec-122">Block executable files from running unless they meet a prevalence, age, or trusted list criterion</span></span>
- <span data-ttu-id="47bec-123">Utiliser la protection avancée contre les ransomware</span><span class="sxs-lookup"><span data-stu-id="47bec-123">Use advanced protection against ransomware</span></span>
- <span data-ttu-id="47bec-124">Bloquer le vol d’informations d’identification à partir du sous-système Windows local Security Authority (lsass.exe)</span><span class="sxs-lookup"><span data-stu-id="47bec-124">Block credential stealing from the Windows local security authority subsystem (lsass.exe)</span></span>
- <span data-ttu-id="47bec-125">Création de processus de bloc provenant de commandes PSExec et WMI</span><span class="sxs-lookup"><span data-stu-id="47bec-125">Block process creations originating from PSExec and WMI commands</span></span>
- <span data-ttu-id="47bec-126">Bloquer les processus non approuvés et non signés qui s’exécutent à partir de ports USB</span><span class="sxs-lookup"><span data-stu-id="47bec-126">Block untrusted and unsigned processes that run from USB</span></span>
- <span data-ttu-id="47bec-127">Bloquer l’application de communication Office de la création de processus enfants</span><span class="sxs-lookup"><span data-stu-id="47bec-127">Block Office communication application from creating child processes</span></span>
- <span data-ttu-id="47bec-128">Empêcher Adobe Reader de créer des processus enfants</span><span class="sxs-lookup"><span data-stu-id="47bec-128">Block Adobe Reader from creating child processes</span></span>
- <span data-ttu-id="47bec-129">Blocage de la persistance via l’abonnement aux événements WMI</span><span class="sxs-lookup"><span data-stu-id="47bec-129">Block persistence through WMI event subscription</span></span>

<span data-ttu-id="47bec-130">Recommandations relatives aux services :</span><span class="sxs-lookup"><span data-stu-id="47bec-130">Services related recommendations:</span></span>
- <span data-ttu-id="47bec-131">Corriger le chemin d’accès non quoted service pour les services Windows</span><span class="sxs-lookup"><span data-stu-id="47bec-131">Fix unquoted service path for Windows services</span></span>
- <span data-ttu-id="47bec-132">Modifier le chemin d’accès exécutable de service en un emplacement protégé courant</span><span class="sxs-lookup"><span data-stu-id="47bec-132">Change service executable path to a common protected location</span></span>
- <span data-ttu-id="47bec-133">Modifier le compte de service pour éviter le mot de passe mis en cache dans le Registre Windows</span><span class="sxs-lookup"><span data-stu-id="47bec-133">Change service account to avoid cached password in windows registry</span></span>

## <a name="related-resources"></a><span data-ttu-id="47bec-134">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="47bec-134">Related resources</span></span>

- [<span data-ttu-id="47bec-135">Présentation de Microsoft Secure score</span><span class="sxs-lookup"><span data-stu-id="47bec-135">Microsoft Secure Score overview</span></span>](microsoft-secure-score.md)
- [<span data-ttu-id="47bec-136">Évaluez votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="47bec-136">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="47bec-137">Suivi de votre historique de score sécurisé Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="47bec-137">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="47bec-138">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="47bec-138">What's new</span></span>](microsoft-secure-score-whats-new.md)
