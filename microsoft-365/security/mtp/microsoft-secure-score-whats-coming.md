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
ms.openlocfilehash: 55c7cb34c5484eaf8f6693be0ce439e33a82550f
ms.sourcegitcommit: 59b006f8e82d1772cae2029f278a59ae8a106736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2020
ms.locfileid: "42266966"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="d192b-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="d192b-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="d192b-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="d192b-105">To make Microsoft Secure Score a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="d192b-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="d192b-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="d192b-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="d192b-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="d192b-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="d192b-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="march-2nd-2020"></a><span data-ttu-id="d192b-109">2nd mars 2020</span><span class="sxs-lookup"><span data-stu-id="d192b-109">March 2nd 2020</span></span>

### <a name="removing-improvement-actions-from-intune"></a><span data-ttu-id="d192b-110">Suppression des actions d’amélioration d’Intune</span><span class="sxs-lookup"><span data-stu-id="d192b-110">Removing improvement actions from Intune</span></span>

<span data-ttu-id="d192b-111">Après une évaluation des actions de Microsoft Secure scores improved fournies par Intune, il a été décidé de ne pas fournir une représentation utile de la position de sécurité des appareils dans les organisations.</span><span class="sxs-lookup"><span data-stu-id="d192b-111">After an evaluation of the Microsoft Secure Score improvement actions supplied from Intune, it was decided that they do not provide a useful representation of the security posture of devices in organizations.</span></span> <span data-ttu-id="d192b-112">Au lieu de se concentrer sur les stratégies, nous nous efforcerons de mettre en place des contrôles de sécurité qui évaluent directement l’état de configuration des appareils.</span><span class="sxs-lookup"><span data-stu-id="d192b-112">Instead of focusing on policies, we are working to bring in security controls that directly assess the configuration state of the devices.</span></span>

<span data-ttu-id="d192b-113">Les actions d’amélioration d’Intune suivantes seront supprimées :</span><span class="sxs-lookup"><span data-stu-id="d192b-113">The following Intune improvement actions will be removed:</span></span>

- <span data-ttu-id="d192b-114">Activer la gestion des appareils mobiles Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d192b-114">Enable Microsoft Intune Mobile Device Management</span></span>
- <span data-ttu-id="d192b-115">Créer une stratégie de conformité Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="d192b-115">Create a Microsoft Intune Compliance Policy for Android</span></span>
- <span data-ttu-id="d192b-116">Créer une stratégie de conformité Microsoft Intune pour Android pour le travail</span><span class="sxs-lookup"><span data-stu-id="d192b-116">Create a Microsoft Intune Compliance Policy for Android for Work</span></span>
- <span data-ttu-id="d192b-117">Créer une stratégie de protection des applications Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="d192b-117">Create a Microsoft Intune App Protection Policy for Android</span></span>
- <span data-ttu-id="d192b-118">Créer une stratégie de protection des applications Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="d192b-118">Create a Microsoft Intune App Protection Policy for iOS</span></span>
- <span data-ttu-id="d192b-119">Marquer les appareils sans aucune stratégie de conformité Microsoft Intune attribuée comme non conforme</span><span class="sxs-lookup"><span data-stu-id="d192b-119">Mark devices with no Microsoft Intune Compliance Policy assigned as not compliant</span></span>
- <span data-ttu-id="d192b-120">Créer une stratégie de conformité Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="d192b-120">Create a Microsoft Intune Compliance Policy for iOS</span></span>
- <span data-ttu-id="d192b-121">Créer une stratégie de conformité Microsoft Intune pour macOS</span><span class="sxs-lookup"><span data-stu-id="d192b-121">Create a Microsoft Intune Compliance Policy for macOS</span></span>
- <span data-ttu-id="d192b-122">Créer une stratégie de conformité Microsoft Intune pour Windows</span><span class="sxs-lookup"><span data-stu-id="d192b-122">Create a Microsoft Intune Compliance Policy for Windows</span></span>
- <span data-ttu-id="d192b-123">Créer un profil de configuration Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="d192b-123">Create a Microsoft Intune Configuration Profile for Android</span></span>
- <span data-ttu-id="d192b-124">Créer un profil de configuration Microsoft Intune pour Android pour le travail</span><span class="sxs-lookup"><span data-stu-id="d192b-124">Create a Microsoft Intune Configuration Profile for Android for Work</span></span>
- <span data-ttu-id="d192b-125">Créer un profil de configuration Microsoft Intune pour macOS</span><span class="sxs-lookup"><span data-stu-id="d192b-125">Create a Microsoft Intune Configuration Profile for macOS</span></span>
- <span data-ttu-id="d192b-126">Créer un profil de configuration Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="d192b-126">Create a Microsoft Intune Configuration Profile for iOS</span></span>
- <span data-ttu-id="d192b-127">Créer un profil de configuration Microsoft Intune pour Windows</span><span class="sxs-lookup"><span data-stu-id="d192b-127">Create a Microsoft Intune Configuration Profile for Windows</span></span>
- <span data-ttu-id="d192b-128">Activer la détection jailbreak améliorée dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d192b-128">Enable enhanced jailbreak detection in Microsoft Intune</span></span>
- <span data-ttu-id="d192b-129">Exiger l’application des correctifs sur tous les appareils, les antivirus et les pare-feu activés</span><span class="sxs-lookup"><span data-stu-id="d192b-129">Require all devices to be patched, have anti-virus, and firewalls enabled</span></span>
- <span data-ttu-id="d192b-130">Activer l’intégration de Windows Defender ATP dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d192b-130">Enable Windows Defender ATP integration into Microsoft Intune</span></span>
- <span data-ttu-id="d192b-131">Créer une stratégie de protection des informations Windows Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="d192b-131">Create a Microsoft Intune Windows Information Protection Policy</span></span>
- <span data-ttu-id="d192b-132">Exiger que tous les appareils disposent de configurations de sécurité avancées</span><span class="sxs-lookup"><span data-stu-id="d192b-132">Require all devices to have advanced security configurations</span></span>
- <span data-ttu-id="d192b-133">Vérifier toutes les semaines les périphériques bloqués</span><span class="sxs-lookup"><span data-stu-id="d192b-133">Review blocked devices report weekly</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement"></a><span data-ttu-id="d192b-134">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable</span><span class="sxs-lookup"><span data-stu-id="d192b-134">Removing improvement actions that don't meet expectations for reliable measurement</span></span>

<span data-ttu-id="d192b-135">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="d192b-135">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="d192b-136">Activer l’enregistrement des données d’audit</span><span class="sxs-lookup"><span data-stu-id="d192b-136">Turn on audit data recording</span></span>
- <span data-ttu-id="d192b-137">Découverte des applications informatiques de clichés instantanés risquées et non conformes</span><span class="sxs-lookup"><span data-stu-id="d192b-137">Discover risky and non-compliant shadow IT applications</span></span>
- <span data-ttu-id="d192b-138">Passer en revue les autorisations & bloquer les applications OAuth à risque connectées à votre environnement</span><span class="sxs-lookup"><span data-stu-id="d192b-138">Review permissions & block risky OAuth applications connected to your environment</span></span>
- <span data-ttu-id="d192b-139">Configurer le contrôle de version sur les bibliothèques de documents SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d192b-139">Set up versioning on SharePoint online document libraries</span></span>

### <a name="mfa-improvement-action-updates"></a><span data-ttu-id="d192b-140">Mises à jour de l’action d’amélioration MFA</span><span class="sxs-lookup"><span data-stu-id="d192b-140">MFA improvement action updates</span></span>

<span data-ttu-id="d192b-141">Pour refléter la nécessité pour les entreprises de garantir la sécurité maximale lors de l’application des stratégies qui fonctionnent avec leur entreprise, le score de sécurité Microsoft supprime trois actions d’amélioration axées sur l’authentification multifacteur et en ajoutant deux.</span><span class="sxs-lookup"><span data-stu-id="d192b-141">To reflect the need for businesses to ensure the upmost security while applying policies that work with their business, Microsoft Secure Score is removing three improvement actions centered around multi-factor authentication, and adding two.</span></span>

<span data-ttu-id="d192b-142">Les trois qui seront supprimés :</span><span class="sxs-lookup"><span data-stu-id="d192b-142">The three that will be removed:</span></span>

- <span data-ttu-id="d192b-143">Inscrire tous les utilisateurs pour l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="d192b-143">Register all users for multi-factor authentication</span></span>
- <span data-ttu-id="d192b-144">Exiger l’authentification multifacteur pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d192b-144">Require MFA for all users</span></span>
- <span data-ttu-id="d192b-145">Exiger l’authentification multifacteur pour les rôles privilège Azure AD</span><span class="sxs-lookup"><span data-stu-id="d192b-145">Require MFA for Azure AD privileged roles</span></span>

<span data-ttu-id="d192b-146">Nouvelles actions d’amélioration ajoutées :</span><span class="sxs-lookup"><span data-stu-id="d192b-146">New improvement actions added:</span></span>

- <span data-ttu-id="d192b-147">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé</span><span class="sxs-lookup"><span data-stu-id="d192b-147">Ensure all users can complete multi-factor authentication for secure access</span></span>
- <span data-ttu-id="d192b-148">Exiger MFA pour les rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="d192b-148">Require MFA for administrative roles</span></span>

 <span data-ttu-id="d192b-149">Ces nouvelles actions d’amélioration requièrent l’enregistrement de vos utilisateurs ou administrateurs pour l’authentification multifacteur (MFA) dans votre répertoire et l’établissement de l’ensemble approprié de stratégies répondant à vos besoins organisationnels.</span><span class="sxs-lookup"><span data-stu-id="d192b-149">These new improvement actions will require registering your users or admins for multi-factor authentication (MFA) across your directory and establishing the right set of policies that fit your organizational needs.</span></span> <span data-ttu-id="d192b-150">L’objectif principal est de la flexibilité tout en s’assurant que tous vos utilisateurs et administrateurs peuvent s’authentifier avec plusieurs facteurs ou des invites de vérification d’identité basées sur les risques.</span><span class="sxs-lookup"><span data-stu-id="d192b-150">The main goal is have flexibility while ensuring all your users and admins can authenticate with multiple factors or risk-based identity verification prompts.</span></span> <span data-ttu-id="d192b-151">Cela peut prendre la forme d’avoir plusieurs stratégies qui appliquent des décisions délimitées ou de définir des paramètres de sécurité par défaut (à venir le 16 mars) qui permettent à Microsoft de décider du défi des utilisateurs pour l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="d192b-151">That can take the form of having multiple policies that apply scoped decisions, or setting security defaults (coming March 16th) that let Microsoft decide when to challenge users for MFA.</span></span>

### <a name="removing-review-improvement-actions"></a><span data-ttu-id="d192b-152">Suppression des actions d’amélioration « révision »</span><span class="sxs-lookup"><span data-stu-id="d192b-152">Removing “review” improvement actions</span></span>

<span data-ttu-id="d192b-153">L’un des principes du score de sécurité est que le score doit être standardisé et facile à mettre en relation.</span><span class="sxs-lookup"><span data-stu-id="d192b-153">One of the principles of Secure Score is that the score should be standardized and easy to relate to.</span></span> <span data-ttu-id="d192b-154">Les actions d’amélioration qui ne sont pas mesurables ou exploitables provoquent des confusions.</span><span class="sxs-lookup"><span data-stu-id="d192b-154">Having improvement actions that are not measurable or actionable has been causing confusion.</span></span> <span data-ttu-id="d192b-155">Un score de sécurité Microsoft n’a de sens que si chaque recommandation peut avoir un effet clair sur le score.</span><span class="sxs-lookup"><span data-stu-id="d192b-155">One Microsoft Secure Score only makes sense when every recommendation can have a clear effect on the score.</span></span> <span data-ttu-id="d192b-156">Examiner les actions d’amélioration ne sont pas mesurées de la même façon que les autres actions d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="d192b-156">Review improvement actions are not measured to the same standard as other improvement actions.</span></span>  

<span data-ttu-id="d192b-157">Pour ces raisons, toutes les actions d’amélioration nécessitant une cadence de révision seront temporairement supprimées.</span><span class="sxs-lookup"><span data-stu-id="d192b-157">For these reasons, all improvement actions that required a review cadence will be temporarily removed.</span></span> <span data-ttu-id="d192b-158">Aucune action n’est nécessaire de votre part.</span><span class="sxs-lookup"><span data-stu-id="d192b-158">No action is needed on your part.</span></span>

## <a name="march-16th-2020"></a><span data-ttu-id="d192b-159">16 mars 2020</span><span class="sxs-lookup"><span data-stu-id="d192b-159">March 16th 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement"></a><span data-ttu-id="d192b-160">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable</span><span class="sxs-lookup"><span data-stu-id="d192b-160">Removing improvement actions that don't meet expectations for reliable measurement</span></span>

<span data-ttu-id="d192b-161">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="d192b-161">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="d192b-162">Stocker des documents utilisateur dans OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="d192b-162">Store user documents in OneDrive for Business</span></span>
- <span data-ttu-id="d192b-163">Configurer des stratégies de pièces jointes approuvées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="d192b-163">Set up Office 365 ATP Safe Attachment policies</span></span>
- <span data-ttu-id="d192b-164">Configurer les liens fiables Office 365 pour vérifier les URL</span><span class="sxs-lookup"><span data-stu-id="d192b-164">Set up Office 365 Safe Links to verify URLs</span></span>
- <span data-ttu-id="d192b-165">Ne pas autoriser la délégation de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="d192b-165">Do not allow mailbox delegation</span></span>
- <span data-ttu-id="d192b-166">Autoriser les liens de partage d’invités anonymes pour les sites et les documents</span><span class="sxs-lookup"><span data-stu-id="d192b-166">Allow anonymous guest sharing links for sites and docs</span></span>

### <a name="supporting-security-defaults-for-azure-ad-improvement-actions"></a><span data-ttu-id="d192b-167">Prise en charge des paramètres de sécurité par défaut pour les actions d’amélioration Azure AD</span><span class="sxs-lookup"><span data-stu-id="d192b-167">Supporting security defaults for Azure AD improvement actions</span></span>

<span data-ttu-id="d192b-168">Le score de sécurité Microsoft mettra à jour les actions d’amélioration afin de prendre en charge les paramètres de [sécurité par défaut dans Azure ad](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), ce qui facilite la protection de votre organisation à l’aide de paramètres de sécurité préconfigurés pour les attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="d192b-168">Microsoft Secure Score will be updating improvement actions to support [security defaults in Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), which make it easier to help protect your organization with pre-configured security settings for common attacks.</span></span>

<span data-ttu-id="d192b-169">Cela aura une incidence sur les actions d’amélioration suivantes :</span><span class="sxs-lookup"><span data-stu-id="d192b-169">It will affect the following improvement actions:</span></span>

- <span data-ttu-id="d192b-170">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé</span><span class="sxs-lookup"><span data-stu-id="d192b-170">Ensure all users can complete multi-factor authentication for secure access</span></span>
- <span data-ttu-id="d192b-171">Exiger MFA pour les rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="d192b-171">Require MFA for administrative roles</span></span>
- <span data-ttu-id="d192b-172">Activer la stratégie pour bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="d192b-172">Enable policy to block legacy authentication</span></span>
