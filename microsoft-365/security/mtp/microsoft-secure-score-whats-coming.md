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
ms.openlocfilehash: 1a5c5ae702f16bbf47be83837cf244cdd64278cd
ms.sourcegitcommit: 4988934836eee45c890b9bdd5ef73590656c78ba
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "43541106"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="a5ef9-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="a5ef9-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="a5ef9-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-105">To make Microsoft Secure Score a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="a5ef9-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="a5ef9-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="a5ef9-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="a5ef9-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="april-21st-2020"></a><span data-ttu-id="a5ef9-109">21 avril 2020</span><span class="sxs-lookup"><span data-stu-id="a5ef9-109">April 21st 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement-or-dont-provide-a-useful-representation-of-security-posture"></a><span data-ttu-id="a5ef9-110">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable ou ne fournissent pas une représentation utile de la position de la sécurité</span><span class="sxs-lookup"><span data-stu-id="a5ef9-110">Removing improvement actions that don't meet expectations for reliable measurement or don't provide a useful representation of security posture</span></span>

<span data-ttu-id="a5ef9-111">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="a5ef9-111">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="a5ef9-112">Appliquer des protections IRM aux documents</span><span class="sxs-lookup"><span data-stu-id="a5ef9-112">Apply IRM protections to documents</span></span>
- <span data-ttu-id="a5ef9-113">Appliquer des stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="a5ef9-113">Apply Data Loss Prevention policies</span></span>

### <a name="adding-azure-ad-improvement-action-in-the-preview-version"></a><span data-ttu-id="a5ef9-114">Ajout de l’action d’amélioration Azure AD dans la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="a5ef9-114">Adding Azure AD improvement action in the preview version</span></span>

- <span data-ttu-id="a5ef9-115">Ne pas autoriser les utilisateurs à accorder un consentement aux applications non gérées (actuellement disponible dans la version publiée)</span><span class="sxs-lookup"><span data-stu-id="a5ef9-115">Do not allow users to grant consent to unmanaged applications (currently available in released version)</span></span>

### <a name="adding-azure-atp-improvement-actions-in-the-preview-version"></a><span data-ttu-id="a5ef9-116">Ajout d’actions d’amélioration ATP ATP dans la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="a5ef9-116">Adding Azure ATP improvement actions in the preview version</span></span>

- <span data-ttu-id="a5ef9-117">Désactiver le service spouleur d’impression sur les contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="a5ef9-117">Disable Print spooler service on domain controllers</span></span>
- <span data-ttu-id="a5ef9-118">Modifier les délégations Kerberos non sécurisées pour empêcher l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="a5ef9-118">Modify unsecure Kerberos delegations to prevent impersonation</span></span>
- <span data-ttu-id="a5ef9-119">Protéger et gérer les mots de passe d’administrateur local avec Microsoft couvre</span><span class="sxs-lookup"><span data-stu-id="a5ef9-119">Protect and manage local admin passwords with Microsoft LAPS</span></span>
- <span data-ttu-id="a5ef9-120">Réduire le risque de trajet latéral vers les entités sensibles</span><span class="sxs-lookup"><span data-stu-id="a5ef9-120">Reduce lateral movement path risk to sensitive entities</span></span>
- <span data-ttu-id="a5ef9-121">Supprimer des comptes dormants de groupes sensibles</span><span class="sxs-lookup"><span data-stu-id="a5ef9-121">Remove dormant accounts from sensitive groups</span></span>
- <span data-ttu-id="a5ef9-122">Supprimer les attributs d’historique SID non sécurisé des entités</span><span class="sxs-lookup"><span data-stu-id="a5ef9-122">Remove unsecure SID history attributes from entities</span></span>
- <span data-ttu-id="a5ef9-123">Résoudre les attributs de compte non sécurisé</span><span class="sxs-lookup"><span data-stu-id="a5ef9-123">Resolve unsecure account attributes</span></span>
- <span data-ttu-id="a5ef9-124">Arrêter l’exposition en texte clair des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="a5ef9-124">Stop clear text credentials exposure</span></span>
- <span data-ttu-id="a5ef9-125">Arrêter la communication des protocoles hérités</span><span class="sxs-lookup"><span data-stu-id="a5ef9-125">Stop legacy protocols communication</span></span>
- <span data-ttu-id="a5ef9-126">Arrêter l’utilisation du chiffrement faible</span><span class="sxs-lookup"><span data-stu-id="a5ef9-126">Stop weak cipher usage</span></span>

### <a name="support-for-microsoft-defender-atp-threat--vulnerability-management-tvm-security-recommendations-in-the-preview-version"></a><span data-ttu-id="a5ef9-127">Prise en charge des recommandations de sécurité de la & la gestion des vulnérabilités de Microsoft Defender ATP (TVM) dans la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="a5ef9-127">Support for Microsoft Defender ATP Threat & Vulnerability Management (TVM) security recommendations in the preview version</span></span>

- <span data-ttu-id="a5ef9-128">Toutes les recommandations de sécurité fournies par la TVM seront désormais également disponibles dans Microsoft Secure score</span><span class="sxs-lookup"><span data-stu-id="a5ef9-128">All released security recommendations supplied by TVM will now also be available in Microsoft Secure Score</span></span>
