---
title: Qu’est-ce qui arrive dans le score de sécurité Microsoft ?
description: Décrit Microsoft Secure score dans le centre de sécurité Microsoft 365, la façon dont les détails sont calculés et les administrateurs de la sécurité qui peuvent s’y attendre.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, Secure score, centre de sécurité, actions d’amélioration
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
ms.openlocfilehash: f9bca47c6a47468d0a5a37b77e4f587745bf619d
ms.sourcegitcommit: c696852da06d057dba4f5147bbf46521910de3ab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2020
ms.locfileid: "44545933"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="addab-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="addab-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="addab-105">Pour faire en sorte que [Microsoft Secure score](microsoft-secure-score-new.md) un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="addab-105">To make [Microsoft Secure Score](microsoft-secure-score-new.md) a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="addab-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="addab-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="addab-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="addab-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="addab-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score-new.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="addab-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score-new.md#whats-new)</span></span>

## <a name="june-2020"></a><span data-ttu-id="addab-109">2020 juin</span><span class="sxs-lookup"><span data-stu-id="addab-109">June 2020</span></span>

### <a name="remove-improvement-action-for-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="addab-110">Supprimer l’action d’amélioration pour la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="addab-110">Remove improvement action for Microsoft Defender Advanced Threat Protection</span></span>

* <span data-ttu-id="addab-111">Activer les règles de réduction de la surface d’attaque</span><span class="sxs-lookup"><span data-stu-id="addab-111">Turn on Attack Surface Reduction rules</span></span>

### <a name="add-improvement-actions-for-microsoft-defender-advanced-threat-protection"></a><span data-ttu-id="addab-112">Ajouter des actions d’amélioration pour la protection avancée contre les menaces Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="addab-112">Add improvement actions for Microsoft Defender Advanced Threat Protection</span></span>

* <span data-ttu-id="addab-113">Empêcher Adobe Reader de créer des processus enfants</span><span class="sxs-lookup"><span data-stu-id="addab-113">Block Adobe Reader from creating child processes</span></span>
* <span data-ttu-id="addab-114">Utiliser la protection avancée contre les ransomware</span><span class="sxs-lookup"><span data-stu-id="addab-114">Use advanced protection against ransomware</span></span>
* <span data-ttu-id="addab-115">Empêcher toutes les applications Office de créer des processus enfants</span><span class="sxs-lookup"><span data-stu-id="addab-115">Block all Office applications from creating child processes</span></span>
* <span data-ttu-id="addab-116">Empêcher les applications Office de créer du contenu exécutable</span><span class="sxs-lookup"><span data-stu-id="addab-116">Block Office applications from creating executable content</span></span>
* <span data-ttu-id="addab-117">Bloquer JavaScript ou VBScript pour lancer le téléchargement de contenu exécutable</span><span class="sxs-lookup"><span data-stu-id="addab-117">Block JavaScript or VBScript from launching downloaded executable content</span></span>
* <span data-ttu-id="addab-118">Bloquer l’exécution des scripts potentiellement brouillés</span><span class="sxs-lookup"><span data-stu-id="addab-118">Block execution of potentially obfuscated scripts</span></span>
* <span data-ttu-id="addab-119">Bloquer le contenu exécutable à partir du client de messagerie et de la messagerie Web</span><span class="sxs-lookup"><span data-stu-id="addab-119">Block executable content from email client and webmail</span></span>
* <span data-ttu-id="addab-120">Bloquer l’application de communication Office de la création de processus enfants</span><span class="sxs-lookup"><span data-stu-id="addab-120">Block Office communication application from creating child processes</span></span>
* <span data-ttu-id="addab-121">Bloquer les processus non approuvés et non signés qui s’exécutent à partir de ports USB</span><span class="sxs-lookup"><span data-stu-id="addab-121">Block untrusted and unsigned processes that run from USB</span></span>
* <span data-ttu-id="addab-122">Blocage de la persistance via l’abonnement aux événements WMI</span><span class="sxs-lookup"><span data-stu-id="addab-122">Block persistence through WMI event subscription</span></span>
* <span data-ttu-id="addab-123">Bloquer l’injection de code dans d’autres processus par les applications Office</span><span class="sxs-lookup"><span data-stu-id="addab-123">Block Office applications from injecting code into other processes</span></span>
* <span data-ttu-id="addab-124">Bloquer l’exécution des fichiers exécutables sauf s’ils répondent à un critère de récurrence, d’âge ou de liste approuvée</span><span class="sxs-lookup"><span data-stu-id="addab-124">Block executable files from running unless they meet a prevalence, age, or trusted list criterion</span></span>
* <span data-ttu-id="addab-125">Création de processus de bloc provenant de commandes PSExec et WMI</span><span class="sxs-lookup"><span data-stu-id="addab-125">Block process creations originating from PSExec and WMI commands</span></span>
* <span data-ttu-id="addab-126">Bloquer le vol d’informations d’identification à partir du sous-système Windows local Security Authority (lsass. exe)</span><span class="sxs-lookup"><span data-stu-id="addab-126">Block credential stealing from the Windows local security authority subsystem (lsass.exe)</span></span>
* <span data-ttu-id="addab-127">Bloquer les appels d’API Win32 à partir de macros Office</span><span class="sxs-lookup"><span data-stu-id="addab-127">Block Win32 API calls from Office macros</span></span>
