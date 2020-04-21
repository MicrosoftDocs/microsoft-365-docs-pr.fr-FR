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
ms.openlocfilehash: 234ae17ab31d56d1bbd65f1aa8ed29475e9cd155
ms.sourcegitcommit: d818828c66cf98b0b0037ba8b3cb790c940281b7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43583714"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="8e919-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="8e919-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="8e919-105">Pour faire en sorte que [Microsoft Secure score](microsoft-secure-score.md) un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="8e919-105">To make [Microsoft Secure Score](microsoft-secure-score.md) a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="8e919-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="8e919-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="8e919-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8e919-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="8e919-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="8e919-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="april-21st-2020"></a><span data-ttu-id="8e919-109">21 avril 2020</span><span class="sxs-lookup"><span data-stu-id="8e919-109">April 21st 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement-or-dont-provide-a-useful-representation-of-security-posture"></a><span data-ttu-id="8e919-110">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable ou ne fournissent pas une représentation utile de la position de la sécurité</span><span class="sxs-lookup"><span data-stu-id="8e919-110">Removing improvement actions that don't meet expectations for reliable measurement or don't provide a useful representation of security posture</span></span>

<span data-ttu-id="8e919-111">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="8e919-111">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="8e919-112">Appliquer des protections IRM aux documents</span><span class="sxs-lookup"><span data-stu-id="8e919-112">Apply IRM protections to documents</span></span>
- <span data-ttu-id="8e919-113">Appliquer des stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="8e919-113">Apply Data Loss Prevention policies</span></span>

### <a name="adding-azure-ad-improvement-action-to-preview"></a><span data-ttu-id="8e919-114">Ajout de l’action d’amélioration Azure AD à l’aperçu</span><span class="sxs-lookup"><span data-stu-id="8e919-114">Adding Azure AD improvement action to preview</span></span>

<span data-ttu-id="8e919-115">Ajout de l’action d’amélioration Azure Active Directory suivante à la [version préliminaire de Microsoft Secure score](microsoft-secure-score-preview.md):</span><span class="sxs-lookup"><span data-stu-id="8e919-115">Adding the following Azure Active Directory improvement action to the [preview release of Microsoft Secure Score](microsoft-secure-score-preview.md):</span></span>

- <span data-ttu-id="8e919-116">Ne pas autoriser les utilisateurs à accorder un consentement aux applications non gérées (actuellement disponible dans la version publiée)</span><span class="sxs-lookup"><span data-stu-id="8e919-116">Do not allow users to grant consent to unmanaged applications (currently available in released version)</span></span>

### <a name="adding-azure-atp-improvement-actions-to-preview"></a><span data-ttu-id="8e919-117">Ajout d’actions d’amélioration ATP DAV à l’aperçu</span><span class="sxs-lookup"><span data-stu-id="8e919-117">Adding Azure ATP improvement actions to preview</span></span>

<span data-ttu-id="8e919-118">Ajout des actions d’amélioration d’Azure protection avancée contre les menaces suivantes à la [version préliminaire de Microsoft Secure score](microsoft-secure-score-preview.md):</span><span class="sxs-lookup"><span data-stu-id="8e919-118">Adding the following Azure Advanced Threat Protection improvement actions to the [preview release of Microsoft Secure Score](microsoft-secure-score-preview.md):</span></span>

- <span data-ttu-id="8e919-119">Désactiver le service spouleur d’impression sur les contrôleurs de domaine</span><span class="sxs-lookup"><span data-stu-id="8e919-119">Disable Print spooler service on domain controllers</span></span>
- <span data-ttu-id="8e919-120">Modifier les délégations Kerberos non sécurisées pour empêcher l’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="8e919-120">Modify unsecure Kerberos delegations to prevent impersonation</span></span>
- <span data-ttu-id="8e919-121">Protéger et gérer les mots de passe d’administrateur local avec Microsoft couvre</span><span class="sxs-lookup"><span data-stu-id="8e919-121">Protect and manage local admin passwords with Microsoft LAPS</span></span>
- <span data-ttu-id="8e919-122">Réduire le risque de trajet latéral vers les entités sensibles</span><span class="sxs-lookup"><span data-stu-id="8e919-122">Reduce lateral movement path risk to sensitive entities</span></span>
- <span data-ttu-id="8e919-123">Supprimer des comptes dormants de groupes sensibles</span><span class="sxs-lookup"><span data-stu-id="8e919-123">Remove dormant accounts from sensitive groups</span></span>
- <span data-ttu-id="8e919-124">Supprimer les attributs d’historique SID non sécurisé des entités</span><span class="sxs-lookup"><span data-stu-id="8e919-124">Remove unsecure SID history attributes from entities</span></span>
- <span data-ttu-id="8e919-125">Résoudre les attributs de compte non sécurisé</span><span class="sxs-lookup"><span data-stu-id="8e919-125">Resolve unsecure account attributes</span></span>
- <span data-ttu-id="8e919-126">Arrêter l’exposition en texte clair des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="8e919-126">Stop clear text credentials exposure</span></span>
- <span data-ttu-id="8e919-127">Arrêter la communication des protocoles hérités</span><span class="sxs-lookup"><span data-stu-id="8e919-127">Stop legacy protocols communication</span></span>
- <span data-ttu-id="8e919-128">Arrêter l’utilisation du chiffrement faible</span><span class="sxs-lookup"><span data-stu-id="8e919-128">Stop weak cipher usage</span></span>

### <a name="support-for-microsoft-defender-atp-threat--vulnerability-management-tvm-security-recommendations-in-preview"></a><span data-ttu-id="8e919-129">Prise en charge de la protection contre les vulnérabilités de la & Microsoft Defender ATP (TVM) en aperçu</span><span class="sxs-lookup"><span data-stu-id="8e919-129">Support for Microsoft Defender ATP Threat & Vulnerability Management (TVM) security recommendations in preview</span></span>

<span data-ttu-id="8e919-130">Toutes les recommandations de sécurité fournies par TVM seront également disponibles dans la [version preview de Microsoft Secure score](microsoft-secure-score-preview.md).</span><span class="sxs-lookup"><span data-stu-id="8e919-130">All released security recommendations supplied by TVM will now also be available the [preview release of Microsoft Secure Score](microsoft-secure-score-preview.md).</span></span>
