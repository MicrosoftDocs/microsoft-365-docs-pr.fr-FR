---
title: Rediriger les utilisateurs du centre Office 365 sécurité et conformité vers le centre Microsoft 365 conformité de l’application
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
ms.service: O365-seccomp
audience: ITPro
ms.topic: article
localization_priority: Normal
description: Découvrez comment rediriger automatiquement Office 365 utilisateurs du Centre de sécurité et conformité vers le centre Microsoft 365 conformité.
ms.collection: M365-security-compliance
ms.openlocfilehash: fb667e8f19b26cbe229b3aceffe194a86133c261
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52772479"
---
# <a name="redirect-users-from-the-office-365-security-and-compliance-center-to-the-microsoft-365-compliance-center"></a><span data-ttu-id="7e801-103">Rediriger les utilisateurs du centre Office 365 sécurité et conformité vers le centre Microsoft 365 conformité de l’application</span><span class="sxs-lookup"><span data-stu-id="7e801-103">Redirect users from the Office 365 Security and Compliance center to the Microsoft 365 compliance center</span></span>

<span data-ttu-id="7e801-104">Cet article explique comment fonctionne la redirection automatique pour les utilisateurs accédant à des solutions de conformité à partir du Centre de sécurité et conformité Office 365 (protection.office.com) vers le Centre de conformité Microsoft 365 (compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7e801-104">This article explains how automatic redirection works for users accessing compliance solutions from the Office 365 Security and Compliance Center (protection.office.com) to the Microsoft 365 compliance center (compliance.microsoft.com).</span></span>

## <a name="what-to-expect"></a><span data-ttu-id="7e801-105">À quoi s’attendre</span><span class="sxs-lookup"><span data-stu-id="7e801-105">What to expect</span></span>

<span data-ttu-id="7e801-106">La redirection automatique est activée par défaut pour tous les utilisateurs accédant aux solutions de conformité suivantes dans Office 365 Security and Compliance (protection.office.com) :</span><span class="sxs-lookup"><span data-stu-id="7e801-106">Automatic redirection is enabled by default for all users accessing the following compliance-related solutions in Office 365 Security and Compliance (protection.office.com):</span></span>

- <span data-ttu-id="7e801-107">Protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="7e801-107">Data loss prevention (DLP)</span></span>
- <span data-ttu-id="7e801-108">Classification</span><span class="sxs-lookup"><span data-stu-id="7e801-108">Classification</span></span>
- <span data-ttu-id="7e801-109">Gouvernance des informations</span><span class="sxs-lookup"><span data-stu-id="7e801-109">Information governance</span></span>
- <span data-ttu-id="7e801-110">Gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="7e801-110">Records management</span></span>
- <span data-ttu-id="7e801-111">Conformité des communications (anciennement « Supervision » )</span><span class="sxs-lookup"><span data-stu-id="7e801-111">Communication compliance (formerly 'Supervision')</span></span>

<span data-ttu-id="7e801-112">Les utilisateurs sont automatiquement acheminés vers les mêmes solutions de conformité dans le centre Microsoft 365 conformité (compliance.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7e801-112">Users are automatically routed to the same compliance solutions in the Microsoft 365 compliance center (compliance.microsoft.com).</span></span>

>[!NOTE]
><span data-ttu-id="7e801-113">Pour les autres solutions de conformité incluses dans le Centre de sécurité et conformité Office 365, les utilisateurs continueront à gérer ces solutions dans le Centre de conformité Microsoft 365 ou le Centre de sécurité et conformité Office 365.</span><span class="sxs-lookup"><span data-stu-id="7e801-113">For other compliance solutions included in the Office 365 Security and Compliance Center, users will continue to manage these solutions in either the Microsoft 365 compliance center or the Office 365 Security and Compliance Center.</span></span> <span data-ttu-id="7e801-114">La redirection automatique pour ces solutions de conformité sera bientôt disponible.\*</span><span class="sxs-lookup"><span data-stu-id="7e801-114">The automatic redirection for these compliance solutions will be available soon.\*</span></span>

<span data-ttu-id="7e801-115">Cette fonctionnalité et les contrôles associés n’activent pas la redirection automatique des fonctionnalités de sécurité pour Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="7e801-115">This feature and associated controls does not enable the automatic redirection of Security features for Microsoft Defender for Office 365.</span></span> <span data-ttu-id="7e801-116">Pour activer la redirection pour les [fonctionnalités](/microsoft-365/security/defender/microsoft-365-security-mdo-redirection) de sécurité, consultez La redirection des comptes de Microsoft Defender Office 365 vers le centre de sécurité Microsoft 365 pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="7e801-116">To enable the redirection for security features, see [Redirecting accounts from Microsoft Defender for Office 365 to the Microsoft 365 security center](/microsoft-365/security/defender/microsoft-365-security-mdo-redirection) for details.</span></span>

## <a name="can-i-go-back-to-using-the-former-portal"></a><span data-ttu-id="7e801-117">Puis-je revenir à l’ancien portail ?</span><span class="sxs-lookup"><span data-stu-id="7e801-117">Can I go back to using the former portal?</span></span>

<span data-ttu-id="7e801-118">Si quelque chose ne fonctionne pas pour vous ou s’il y a quelque chose que vous ne parvenez pas à effectuer via le portail du Centre de conformité Microsoft 365, vous pouvez désactiver temporairement la redirection automatique pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7e801-118">If something isn't working for you or if there's anything you're unable to complete through the Microsoft 365 compliance center portal, you can temporarily disable the automatic redirection for all users.</span></span>

>[!IMPORTANT]
><span data-ttu-id="7e801-119">Le centre Microsoft 365 conformité est le portail de gestion des remplacements pour les solutions de conformité actuellement gérées dans le centre de sécurité Office 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="7e801-119">The Microsoft 365 compliance center is the replacement management portal for compliance solutions currently managed in the Office 365 Security and Compliance center.</span></span> <span data-ttu-id="7e801-120">Toutes Microsoft 365 solutions de conformité seront gérées uniquement dans le centre Microsoft 365 conformité.</span><span class="sxs-lookup"><span data-stu-id="7e801-120">All Microsoft 365 compliance solutions will be managed solely in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="7e801-121">La désactivation de la redirection vers le centre Microsoft 365 conformité doit être une solution à court terme.\*</span><span class="sxs-lookup"><span data-stu-id="7e801-121">Disabling redirection to the Microsoft 365 compliance center should be a short-term solution.\*</span></span>

<span data-ttu-id="7e801-122">Pour revenir au Centre Office 365 sécurité et conformité (protection.microsoft.com) pour tous les utilisateurs, passez aux étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7e801-122">To switch back to the Office 365 Security and Compliance center (protection.microsoft.com) for all users, complete the following steps:</span></span>

1. <span data-ttu-id="7e801-123">Connectez-vous au [centre Microsoft 365](https://compliance.microsoft.com) conformité en tant qu’administrateur général ou en utilisant n’importe quel compte ayant des autorisations d’administrateur de conformité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7e801-123">Sign in to the [Microsoft 365 compliance center](https://compliance.microsoft.com) as a global administrator or using any account with compliance administrator permissions in Azure Active directory.</span></span>
2. <span data-ttu-id="7e801-124">Accédez à **Paramètres**  >  **redirection du Centre de conformité.**</span><span class="sxs-lookup"><span data-stu-id="7e801-124">Navigate to **Settings** > **Compliance center redirection**.</span></span>
3. <span data-ttu-id="7e801-125">Basculez le paramètre de redirection automatique sur **Désintégation.**</span><span class="sxs-lookup"><span data-stu-id="7e801-125">Toggle the Automatic redirection setting to **Off**.</span></span>
4. <span data-ttu-id="7e801-126">Sélectionnez **Désactiver et** partager des commentaires lorsque vous y sont invités.</span><span class="sxs-lookup"><span data-stu-id="7e801-126">Select **Disable** and share feedback when prompted.</span></span>

<span data-ttu-id="7e801-127">Une fois désactivés, les utilisateurs ne sont plus acheminés vers compliance.microsoft.com et ils sont dirigés vers le Centre de sécurité et conformité Office 365 (protection.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7e801-127">Once disabled, users will no longer be routed to compliance.microsoft.com and they will be directed to the Office 365 Security and Compliance center (protection.microsoft.com).</span></span> <span data-ttu-id="7e801-128">Ce paramètre peut être à nouveau activé à tout moment par les administrateurs globaux ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="7e801-128">This setting can be enabled again at any time by Global or Compliance admins.</span></span>

## <a name="related-information"></a><span data-ttu-id="7e801-129">Informations connexes</span><span class="sxs-lookup"><span data-stu-id="7e801-129">Related information</span></span>

- [<span data-ttu-id="7e801-130">vue d Microsoft 365 du centre de conformité de l’application</span><span class="sxs-lookup"><span data-stu-id="7e801-130">Microsoft 365 compliance center overview</span></span>](/microsoft-365/compliance/microsoft-365-compliance-center)
