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
ms.openlocfilehash: 61f066b2fff2798e78e6379bbca46e48e93ff017
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895440"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="db47a-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="db47a-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="db47a-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="db47a-105">To make Microsoft Secure Score a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="db47a-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="db47a-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="db47a-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="db47a-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="db47a-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="db47a-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="april-21st-2020"></a><span data-ttu-id="db47a-109">21 avril 2020</span><span class="sxs-lookup"><span data-stu-id="db47a-109">April 21st 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement-or-dont-provide-a-useful-representation-of-security-posture"></a><span data-ttu-id="db47a-110">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable ou ne fournissent pas une représentation utile de la position de la sécurité</span><span class="sxs-lookup"><span data-stu-id="db47a-110">Removing improvement actions that don't meet expectations for reliable measurement or don't provide a useful representation of security posture</span></span>

<span data-ttu-id="db47a-111">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="db47a-111">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="db47a-112">Supprimer/bloquer les comptes non utilisés au cours des 30 derniers jours</span><span class="sxs-lookup"><span data-stu-id="db47a-112">Delete/block accounts not used in last 30 days</span></span>
- <span data-ttu-id="db47a-113">Désigner moins de 5 administrateurs globaux</span><span class="sxs-lookup"><span data-stu-id="db47a-113">Designate fewer than 5 global admins</span></span>
- <span data-ttu-id="db47a-114">Appliquer des protections IRM aux documents</span><span class="sxs-lookup"><span data-stu-id="db47a-114">Apply IRM protections to documents</span></span>
- <span data-ttu-id="db47a-115">Appliquer des stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="db47a-115">Apply Data Loss Prevention policies</span></span>

### <a name="adding-additional-control-support-in-the-preview-version"></a><span data-ttu-id="db47a-116">Ajout de la prise en charge de contrôles supplémentaires dans la version d’évaluation</span><span class="sxs-lookup"><span data-stu-id="db47a-116">Adding additional control support in the preview version</span></span>
- <span data-ttu-id="db47a-117">Ne pas autoriser les utilisateurs à accorder un consentement aux applications non gérées (actuellement disponible dans la version publiée)</span><span class="sxs-lookup"><span data-stu-id="db47a-117">Do not allow users to grant consent to unmanaged applications (currently available in released version)</span></span>

#### <a name="support-for-additional-microsoft-cloud-app-security-improvement-actions"></a><span data-ttu-id="db47a-118">Prise en charge d’autres actions d’amélioration de la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="db47a-118">Support for additional Microsoft Cloud App Security improvement actions</span></span>
- <span data-ttu-id="db47a-119">Désactiver le service spouleur d’impression sur les contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="db47a-119">Disable Print spooler service on domain controllers</span></span>
- <span data-ttu-id="db47a-120">Modifier les délégations Kerberos non sécurisées pour empêcher l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="db47a-120">Modify unsecure Kerberos delegations to prevent impersonation</span></span>
- <span data-ttu-id="db47a-121">Protéger et gérer les mots de passe d’administrateur local avec Microsoft couvre</span><span class="sxs-lookup"><span data-stu-id="db47a-121">Protect and manage local admin passwords with Microsoft LAPS</span></span>
- <span data-ttu-id="db47a-122">Réduire le risque de trajet latéral vers les entités sensibles</span><span class="sxs-lookup"><span data-stu-id="db47a-122">Reduce lateral movement path risk to sensitive entities</span></span>
- <span data-ttu-id="db47a-123">Supprimer des comptes dormants de groupes sensibles</span><span class="sxs-lookup"><span data-stu-id="db47a-123">Remove dormant accounts from sensitive groups</span></span>
- <span data-ttu-id="db47a-124">Supprimer les attributs d’historique SID non sécurisé des entités</span><span class="sxs-lookup"><span data-stu-id="db47a-124">Remove unsecure SID history attributes from entities</span></span>
- <span data-ttu-id="db47a-125">Résoudre les attributs de compte non sécurisé</span><span class="sxs-lookup"><span data-stu-id="db47a-125">Resolve unsecure account attributes</span></span>
- <span data-ttu-id="db47a-126">Arrêter l’exposition en texte clair des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="db47a-126">Stop clear text credentials exposure</span></span>
- <span data-ttu-id="db47a-127">Arrêter la communication des protocoles hérités</span><span class="sxs-lookup"><span data-stu-id="db47a-127">Stop legacy protocols communication</span></span>
- <span data-ttu-id="db47a-128">Arrêter l’utilisation du chiffrement faible</span><span class="sxs-lookup"><span data-stu-id="db47a-128">Stop weak cipher usage</span></span>

#### <a name="support-for-microsoft-defender-atp-threat--vulnerability-management-tvm-security-recommendations"></a><span data-ttu-id="db47a-129">Prise en charge des recommandations de sécurité de la & la gestion des vulnérabilités de Microsoft Defender ATP (TVM)</span><span class="sxs-lookup"><span data-stu-id="db47a-129">Support for Microsoft Defender ATP Threat & Vulnerability Management (TVM) security recommendations</span></span>
- <span data-ttu-id="db47a-130">Toutes les recommandations de sécurité fournies par la TVM seront désormais également disponibles dans Microsoft Secure score</span><span class="sxs-lookup"><span data-stu-id="db47a-130">All released security recommendations supplied by TVM will now also be available in Microsoft Secure Score</span></span>
