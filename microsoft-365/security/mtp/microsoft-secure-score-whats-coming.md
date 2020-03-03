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
ms.openlocfilehash: efb75f26d66258880c9defa94869f27e18685052
ms.sourcegitcommit: 9224a7a5886c0c5fa0bc12bd9f7234a0eba90023
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/02/2020
ms.locfileid: "42372002"
---
# <a name="whats-coming-in-microsoft-secure-score"></a><span data-ttu-id="35d42-104">Qu’est-ce qui arrive dans le score de sécurité Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="35d42-104">What's coming in Microsoft Secure Score?</span></span>

<span data-ttu-id="35d42-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité et améliore la convivialité, nous apportons des modifications dans le futur proche.</span><span class="sxs-lookup"><span data-stu-id="35d42-105">To make Microsoft Secure Score a better representative of your security posture and improve usability, we are making some changes in the near future.</span></span> <span data-ttu-id="35d42-106">Votre score et le score maximal possible seront modifiés.</span><span class="sxs-lookup"><span data-stu-id="35d42-106">Your score and the maximum possible score will change.</span></span> <span data-ttu-id="35d42-107">Toutefois, cela n’implique pas de modification de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="35d42-107">However, this does not imply a change in your security posture.</span></span>

<span data-ttu-id="35d42-108">Pour en savoir plus sur les modifications récentes, consultez [la rubrique what’s New in Microsoft Secure score ?](microsoft-secure-score.md#whats-new)</span><span class="sxs-lookup"><span data-stu-id="35d42-108">To learn about recent changes, see [What's new in Microsoft Secure Score?](microsoft-secure-score.md#whats-new)</span></span>

## <a name="march-16th-2020"></a><span data-ttu-id="35d42-109">16 mars 2020</span><span class="sxs-lookup"><span data-stu-id="35d42-109">March 16th 2020</span></span>

### <a name="removing-improvement-actions-that-dont-meet-expectations-for-reliable-measurement-or-dont-provide-a-useful-representation-of-security-posture"></a><span data-ttu-id="35d42-110">Suppression des actions d’amélioration qui ne répondent pas aux attentes en matière de mesure fiable ou ne fournissent pas une représentation utile de la position de la sécurité</span><span class="sxs-lookup"><span data-stu-id="35d42-110">Removing improvement actions that don't meet expectations for reliable measurement or don't provide a useful representation of security posture</span></span>

<span data-ttu-id="35d42-111">Pour vous assurer que le score de sécurité de Microsoft est significatif et que chaque action d’amélioration est mesurable et fiable, nous supprimons les actions d’amélioration suivantes.</span><span class="sxs-lookup"><span data-stu-id="35d42-111">To ensure that the Microsoft Secure Score is meaningful and that every improvement action is measurable and reliable, we are removing the following improvement actions.</span></span>

- <span data-ttu-id="35d42-112">Stocker des documents utilisateur dans OneDrive entreprise</span><span class="sxs-lookup"><span data-stu-id="35d42-112">Store user documents in OneDrive for Business</span></span>
- <span data-ttu-id="35d42-113">Configurer des stratégies de pièces jointes approuvées ATP Office 365</span><span class="sxs-lookup"><span data-stu-id="35d42-113">Set up Office 365 ATP Safe Attachment policies</span></span>
- <span data-ttu-id="35d42-114">Configurer les liens fiables Office 365 pour vérifier les URL</span><span class="sxs-lookup"><span data-stu-id="35d42-114">Set up Office 365 Safe Links to verify URLs</span></span>
- <span data-ttu-id="35d42-115">Ne pas autoriser la délégation de boîte aux lettres</span><span class="sxs-lookup"><span data-stu-id="35d42-115">Do not allow mailbox delegation</span></span>
- <span data-ttu-id="35d42-116">Autoriser les liens de partage d’invités anonymes pour les sites et les documents</span><span class="sxs-lookup"><span data-stu-id="35d42-116">Allow anonymous guest sharing links for sites and docs</span></span>
- <span data-ttu-id="35d42-117">Activer la console de sécurité des applications Cloud</span><span class="sxs-lookup"><span data-stu-id="35d42-117">Turn on Cloud App Security Console</span></span>
- <span data-ttu-id="35d42-118">Configurer le délai d’expiration pour les liens de partage externe</span><span class="sxs-lookup"><span data-stu-id="35d42-118">Configure expiration time for external sharing links</span></span>

### <a name="supporting-security-defaults-for-azure-ad-improvement-actions"></a><span data-ttu-id="35d42-119">Prise en charge des paramètres de sécurité par défaut pour les actions d’amélioration Azure AD</span><span class="sxs-lookup"><span data-stu-id="35d42-119">Supporting security defaults for Azure AD improvement actions</span></span>

<span data-ttu-id="35d42-120">Le score de sécurité Microsoft mettra à jour les actions d’amélioration afin de prendre en charge les paramètres de [sécurité par défaut dans Azure ad](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), ce qui facilite la protection de votre organisation à l’aide de paramètres de sécurité préconfigurés pour les attaques courantes.</span><span class="sxs-lookup"><span data-stu-id="35d42-120">Microsoft Secure Score will be updating improvement actions to support [security defaults in Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults), which make it easier to help protect your organization with pre-configured security settings for common attacks.</span></span>

<span data-ttu-id="35d42-121">Cela aura une incidence sur les actions d’amélioration suivantes :</span><span class="sxs-lookup"><span data-stu-id="35d42-121">It will affect the following improvement actions:</span></span>

- <span data-ttu-id="35d42-122">S’assurer que tous les utilisateurs peuvent effectuer l’authentification multifacteur pour un accès sécurisé</span><span class="sxs-lookup"><span data-stu-id="35d42-122">Ensure all users can complete multi-factor authentication for secure access</span></span>
- <span data-ttu-id="35d42-123">Exiger MFA pour les rôles d’administration</span><span class="sxs-lookup"><span data-stu-id="35d42-123">Require MFA for administrative roles</span></span>
- <span data-ttu-id="35d42-124">Activer la stratégie pour bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="35d42-124">Enable policy to block legacy authentication</span></span>
