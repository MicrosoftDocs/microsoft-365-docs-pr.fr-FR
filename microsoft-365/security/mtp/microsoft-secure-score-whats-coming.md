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
ms.openlocfilehash: 4d445d4c917a46b12592308f599570725ace8e9d
ms.sourcegitcommit: 6c7f6ef98c321c80a9254c10bbbb917895b5c156
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2020
ms.locfileid: "42322563"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="c9097-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="c9097-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="c9097-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="c9097-105">To make Microsoft Secure Score a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="c9097-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="c9097-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="c9097-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c9097-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="c9097-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="c9097-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="march-2nd-2020"></a><span data-ttu-id="c9097-109">2nd mars 2020</span><span class="sxs-lookup"><span data-stu-id="c9097-109">March 2nd 2020</span></span>

### <a name="removing-improvement-actions-from-intune"></a><span data-ttu-id="c9097-110">Suppression des actions d’amélioration d’Intune</span><span class="sxs-lookup"><span data-stu-id="c9097-110">Removing improvement actions from Intune</span></span>

<span data-ttu-id="c9097-111">Après une évaluation des actions de Microsoft Secure scores improved fournies par Intune, il a été décidé de ne pas fournir une représentation utile de la position de sécurité des appareils dans les organisations.</span><span class="sxs-lookup"><span data-stu-id="c9097-111">After an evaluation of the Microsoft Secure Score improvement actions supplied from Intune, it was decided that they do not provide a useful representation of the security posture of devices in organizations.</span></span> <span data-ttu-id="c9097-112">Au lieu de se concentrer sur les stratégies, nous nous efforcerons de mettre en place des contrôles de sécurité qui évaluent directement l’état de configuration des appareils.</span><span class="sxs-lookup"><span data-stu-id="c9097-112">Instead of focusing on policies, we are working to bring in security controls that directly assess the configuration state of the devices.</span></span>

<span data-ttu-id="c9097-113">Les actions d’amélioration d’Intune suivantes seront supprimées :</span><span class="sxs-lookup"><span data-stu-id="c9097-113">The following Intune improvement actions will be removed:</span></span>

- <span data-ttu-id="c9097-114">Activer la gestion des appareils mobiles Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c9097-114">Enable Microsoft Intune Mobile Device Management</span></span>
- <span data-ttu-id="c9097-115">Créer une stratégie de conformité Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="c9097-115">Create a Microsoft Intune Compliance Policy for Android</span></span>
- <span data-ttu-id="c9097-116">Créer une stratégie de conformité Microsoft Intune pour Android pour le travail</span><span class="sxs-lookup"><span data-stu-id="c9097-116">Create a Microsoft Intune Compliance Policy for Android for Work</span></span>
- <span data-ttu-id="c9097-117">Créer une stratégie de protection des applications Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="c9097-117">Create a Microsoft Intune App Protection Policy for Android</span></span>
- <span data-ttu-id="c9097-118">Créer une stratégie de protection des applications Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="c9097-118">Create a Microsoft Intune App Protection Policy for iOS</span></span>
- <span data-ttu-id="c9097-119">Marquer les appareils sans aucune stratégie de conformité Microsoft Intune attribuée comme non conforme</span><span class="sxs-lookup"><span data-stu-id="c9097-119">Mark devices with no Microsoft Intune Compliance Policy assigned as not compliant</span></span>
- <span data-ttu-id="c9097-120">Créer une stratégie de conformité Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="c9097-120">Create a Microsoft Intune Compliance Policy for iOS</span></span>
- <span data-ttu-id="c9097-121">Créer une stratégie de conformité Microsoft Intune pour macOS</span><span class="sxs-lookup"><span data-stu-id="c9097-121">Create a Microsoft Intune Compliance Policy for macOS</span></span>
- <span data-ttu-id="c9097-122">Créer une stratégie de conformité Microsoft Intune pour Windows</span><span class="sxs-lookup"><span data-stu-id="c9097-122">Create a Microsoft Intune Compliance Policy for Windows</span></span>
- <span data-ttu-id="c9097-123">Créer un profil de configuration Microsoft Intune pour Android</span><span class="sxs-lookup"><span data-stu-id="c9097-123">Create a Microsoft Intune Configuration Profile for Android</span></span>
- <span data-ttu-id="c9097-124">Créer un profil de configuration Microsoft Intune pour Android pour le travail</span><span class="sxs-lookup"><span data-stu-id="c9097-124">Create a Microsoft Intune Configuration Profile for Android for Work</span></span>
- <span data-ttu-id="c9097-125">Créer un profil de configuration Microsoft Intune pour macOS</span><span class="sxs-lookup"><span data-stu-id="c9097-125">Create a Microsoft Intune Configuration Profile for macOS</span></span>
- <span data-ttu-id="c9097-126">Créer un profil de configuration Microsoft Intune pour iOS</span><span class="sxs-lookup"><span data-stu-id="c9097-126">Create a Microsoft Intune Configuration Profile for iOS</span></span>
- <span data-ttu-id="c9097-127">Créer un profil de configuration Microsoft Intune pour Windows</span><span class="sxs-lookup"><span data-stu-id="c9097-127">Create a Microsoft Intune Configuration Profile for Windows</span></span>
- <span data-ttu-id="c9097-128">Activer la détection jailbreak améliorée dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c9097-128">Enable enhanced jailbreak detection in Microsoft Intune</span></span>
- <span data-ttu-id="c9097-129">Exiger l’application des correctifs sur tous les appareils, les antivirus et les pare-feu activés</span><span class="sxs-lookup"><span data-stu-id="c9097-129">Require all devices to be patched, have anti-virus, and firewalls enabled</span></span>
- <span data-ttu-id="c9097-130">Activer l’intégration de Windows Defender ATP dans Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c9097-130">Enable Windows Defender ATP integration into Microsoft Intune</span></span>
- <span data-ttu-id="c9097-131">Créer une stratégie de protection des informations Windows Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="c9097-131">Create a Microsoft Intune Windows Information Protection Policy</span></span>
- <span data-ttu-id="c9097-132">Exiger que tous les appareils disposent de configurations de sécurité avancées</span><span class="sxs-lookup"><span data-stu-id="c9097-132">Require all devices to have advanced security configurations</span></span>
- <span data-ttu-id="c9097-133">Vérifier toutes les semaines les périphériques bloqués</span><span class="sxs-lookup"><span data-stu-id="c9097-133">Review blocked devices report weekly</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement"></a><span data-ttu-id="c9097-134">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable</span><span class="sxs-lookup"><span data-stu-id="c9097-134">Removing improvement actions that don't meet expectations for reliable measurement</span></span> 

<span data-ttu-id="c9097-135">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9097-135">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="c9097-136">Activer l’enregistrement des données d’audit</span><span class="sxs-lookup"><span data-stu-id="c9097-136">Turn on audit data recording</span></span>
- <span data-ttu-id="c9097-137">Découverte des applications informatiques de clichés instantanés risquées et non conformes</span><span class="sxs-lookup"><span data-stu-id="c9097-137">Discover risky and non-compliant shadow IT applications</span></span>
- <span data-ttu-id="c9097-138">Passer en revue les autorisations & bloquer les applications OAuth à risque connectées à votre environnement</span><span class="sxs-lookup"><span data-stu-id="c9097-138">Review permissions & block risky OAuth applications connected to your environment</span></span>
- <span data-ttu-id="c9097-139">Configurer le contrôle de version sur les bibliothèques de documents SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="c9097-139">Set up versioning on SharePoint online document libraries</span></span>

### <a name="mfa-improvement-action-updates"></a><span data-ttu-id="c9097-140">Mises à jour de l’action d’amélioration MFA</span><span class="sxs-lookup"><span data-stu-id="c9097-140">MFA improvement action updates</span></span>

<span data-ttu-id="c9097-141">Pour refléter la nécessité pour les entreprises de garantir la sécurité maximale lors de l’application des stratégies qui fonctionnent avec leur entreprise, le score de sécurité Microsoft supprime trois actions d’amélioration axées sur l’authentification multifacteur et en ajoutant deux.</span><span class="sxs-lookup"><span data-stu-id="c9097-141">To reflect the need for businesses to ensure the upmost security while applying policies that work with their business, Microsoft Secure Score is removing three improvement actions centered around multi-factor authentication, and adding two.</span></span>

<span data-ttu-id="c9097-142">Les trois qui seront supprimés :</span><span class="sxs-lookup"><span data-stu-id="c9097-142">The three that will be removed:</span></span>

- <span data-ttu-id="c9097-143">Inscrire tous les utilisateurs pour l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="c9097-143">Register all users for multi-factor authentication</span></span>
- <span data-ttu-id="c9097-144">Exiger l’authentification multifacteur pour tous les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="c9097-144">Require MFA for all users</span></span>
- <span data-ttu-id="c9097-145">Exiger l’authentification multifacteur pour les rôles privilège Azure AD</span><span class="sxs-lookup"><span data-stu-id="c9097-145">Require MFA for Azure AD privileged roles</span></span>

<span data-ttu-id="c9097-146">Nouvelles actions d’amélioration ajoutées :</span><span class="sxs-lookup"><span data-stu-id="c9097-146">New improvement actions added:</span></span>

- <span data-ttu-id="c9097-147">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé</span><span class="sxs-lookup"><span data-stu-id="c9097-147">Ensure all users can complete multi-factor authentication for secure access</span></span>
- <span data-ttu-id="c9097-148">Exiger MFA pour les rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="c9097-148">Require MFA for administrative roles</span></span>

 <span data-ttu-id="c9097-149">Ces nouvelles actions d’amélioration requièrent l’enregistrement de vos utilisateurs ou administrateurs pour l’authentification multifacteur (MFA) dans votre répertoire et l’établissement de l’ensemble approprié de stratégies répondant à vos besoins organisationnels.</span><span class="sxs-lookup"><span data-stu-id="c9097-149">These new improvement actions will require registering your users or admins for multi-factor authentication (MFA) across your directory and establishing the right set of policies that fit your organizational needs.</span></span> <span data-ttu-id="c9097-150">L’objectif principal est de la flexibilité tout en s’assurant que tous vos utilisateurs et administrateurs peuvent s’authentifier avec plusieurs facteurs ou des invites de vérification d’identité basées sur les risques.</span><span class="sxs-lookup"><span data-stu-id="c9097-150">The main goal is have flexibility while ensuring all your users and admins can authenticate with multiple factors or risk-based identity verification prompts.</span></span> <span data-ttu-id="c9097-151">Cela peut prendre la forme d’avoir plusieurs stratégies qui appliquent des décisions délimitées ou de définir des paramètres de sécurité par défaut (à venir le 16 mars) qui permettent à Microsoft de décider du défi des utilisateurs pour l’authentification multifacteur.</span><span class="sxs-lookup"><span data-stu-id="c9097-151">That can take the form of having multiple policies that apply scoped decisions, or setting security defaults (coming March 16th) that let Microsoft decide when to challenge users for MFA.</span></span>

### <a name="removing-review-improvement-actions"></a><span data-ttu-id="c9097-152">Suppression des actions d’amélioration « révision »</span><span class="sxs-lookup"><span data-stu-id="c9097-152">Removing “review” improvement actions</span></span>

<span data-ttu-id="c9097-153">L’un des principes du score de sécurité est que le score doit être standardisé et facile à mettre en relation.</span><span class="sxs-lookup"><span data-stu-id="c9097-153">One of the principles of Secure Score is that the score should be standardized and easy to relate to.</span></span> <span data-ttu-id="c9097-154">Les actions d’amélioration qui ne sont pas mesurables ou exploitables provoquent des confusions.</span><span class="sxs-lookup"><span data-stu-id="c9097-154">Having improvement actions that are not measurable or actionable has been causing confusion.</span></span> <span data-ttu-id="c9097-155">Un score de sécurité Microsoft n’a de sens que si chaque recommandation peut avoir un effet clair sur le score.</span><span class="sxs-lookup"><span data-stu-id="c9097-155">One Microsoft Secure Score only makes sense when every recommendation can have a clear effect on the score.</span></span> <span data-ttu-id="c9097-156">Examiner les actions d’amélioration ne sont pas mesurées de la même façon que les autres actions d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="c9097-156">Review improvement actions are not measured to the same standard as other improvement actions.</span></span>  

<span data-ttu-id="c9097-157">Pour ces raisons, toutes les actions d’amélioration nécessitant une cadence de révision seront temporairement supprimées.</span><span class="sxs-lookup"><span data-stu-id="c9097-157">For these reasons, all improvement actions that required a review cadence will be temporarily removed.</span></span> <span data-ttu-id="c9097-158">Aucune action n’est nécessaire de votre part.</span><span class="sxs-lookup"><span data-stu-id="c9097-158">No action is needed on your part.</span></span>

## <a name="march-16th-2020"></a><span data-ttu-id="c9097-159">16 mars 2020</span><span class="sxs-lookup"><span data-stu-id="c9097-159">March 16th 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement-or-dont-provide-a-useful-representation-of-security-posture"></a><span data-ttu-id="c9097-160">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable ou ne fournissent pas une représentation utile de la position de la sécurité</span><span class="sxs-lookup"><span data-stu-id="c9097-160">Removing improvement actions that don't meet expectations for reliable measurement or don't provide a useful representation of security posture</span></span>

<span data-ttu-id="c9097-161">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="c9097-161">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="c9097-162">Stocker des documents utilisateur dans OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="c9097-162">Store user documents in OneDrive for Business</span></span>
- <span data-ttu-id="c9097-163">Configurer des stratégies de pièces jointes approuvées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="c9097-163">Set up Office 365 ATP Safe Attachment policies</span></span>
- <span data-ttu-id="c9097-164">Configurer les liens fiables Office 365 pour vérifier les URL</span><span class="sxs-lookup"><span data-stu-id="c9097-164">Set up Office 365 Safe Links to verify URLs</span></span>
- <span data-ttu-id="c9097-165">Ne pas autoriser la délégation de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="c9097-165">Do not allow mailbox delegation</span></span>
- <span data-ttu-id="c9097-166">Autoriser les liens de partage d’invités anonymes pour les sites et les documents</span><span class="sxs-lookup"><span data-stu-id="c9097-166">Allow anonymous guest sharing links for sites and docs</span></span>
- <span data-ttu-id="c9097-167">Activer la console de sécurité des applications Cloud</span><span class="sxs-lookup"><span data-stu-id="c9097-167">Turn on Cloud App Security Console</span></span>

### <a name="supporting-security-defaults-for-azure-ad-improvement-actions"></a><span data-ttu-id="c9097-168">Prise en charge des paramètres de sécurité par défaut pour les actions d’amélioration Azure AD</span><span class="sxs-lookup"><span data-stu-id="c9097-168">Supporting security defaults for Azure AD improvement actions</span></span>

<span data-ttu-id="c9097-169">Le score de sécurité Microsoft mettra à jour les actions d’amélioration afin de prendre en charge les paramètres de [sécurité par défaut dans Azure ad](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), ce qui facilite la protection de votre organisation à l’aide de paramètres de sécurité préconfigurés pour les attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="c9097-169">Microsoft Secure Score will be updating improvement actions to support [security defaults in Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), which make it easier to help protect your organization with pre-configured security settings for common attacks.</span></span>

<span data-ttu-id="c9097-170">Cela aura une incidence sur les actions d’amélioration suivantes :</span><span class="sxs-lookup"><span data-stu-id="c9097-170">It will affect the following improvement actions:</span></span>

- <span data-ttu-id="c9097-171">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé</span><span class="sxs-lookup"><span data-stu-id="c9097-171">Ensure all users can complete multi-factor authentication for secure access</span></span>
- <span data-ttu-id="c9097-172">Exiger MFA pour les rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="c9097-172">Require MFA for administrative roles</span></span>
- <span data-ttu-id="c9097-173">Activer la stratégie pour bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="c9097-173">Enable policy to block legacy authentication</span></span>
