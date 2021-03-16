---
title: En savoir plus sur la stratégie de protection contre la perte de données par défaut dans Microsoft Teams (aperçu)
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: En savoir plus sur la stratégie de protection contre la perte de données par défaut dans Microsoft Teams
ms.openlocfilehash: 3992daf9431dbd87ed5e947a1e5a2b0acd20edce
ms.sourcegitcommit: 450661071e44854f0a0a92af648f76d907767b71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "50826232"
---
# <a name="learn-about-the-default-data-loss-prevention-policy-in-microsoft-teams-preview"></a><span data-ttu-id="22881-103">En savoir plus sur la stratégie de protection contre la perte de données par défaut dans Microsoft Teams (aperçu)</span><span class="sxs-lookup"><span data-stu-id="22881-103">Learn about the default data loss prevention policy in Microsoft Teams (preview)</span></span>

<span data-ttu-id="22881-104">[Les](data-loss-prevention-policies.md) fonctionnalités de protection contre la perte de données (DLP) ont été étendues pour inclure les messages de conversation et de canal Microsoft Teams, y compris les messages de canal privé.</span><span class="sxs-lookup"><span data-stu-id="22881-104">[Data loss prevention](data-loss-prevention-policies.md) (DLP) capabilities have been extended to include Microsoft Teams chat and channel messages, including private channel messages.</span></span> <span data-ttu-id="22881-105">Dans le cadre de cette version, nous avons créé une stratégie DLP par défaut pour les nouveaux clients dans le Centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="22881-105">As a part of this release, we created a default DLP policy for first-time customers to Compliance center.</span></span>

## <a name="applies-to"></a><span data-ttu-id="22881-106">S’applique à</span><span class="sxs-lookup"><span data-stu-id="22881-106">Applies to</span></span>

<span data-ttu-id="22881-107">Tout client titulaire d’une licence avec une ou plusieurs des licences ci-dessous et ayant des utilisateurs Teams actifs</span><span class="sxs-lookup"><span data-stu-id="22881-107">Any tenant who is licensed with one or more of the below licenses and have active Teams users</span></span>
 
- <span data-ttu-id="22881-108">ME5,</span><span class="sxs-lookup"><span data-stu-id="22881-108">ME5,</span></span> 
- <span data-ttu-id="22881-109">MA5,</span><span class="sxs-lookup"><span data-stu-id="22881-109">MA5,</span></span> 
- <span data-ttu-id="22881-110">Conformité E5/A5,</span><span class="sxs-lookup"><span data-stu-id="22881-110">E5/A5 Compliance,</span></span> 
- <span data-ttu-id="22881-111">IP+G,</span><span class="sxs-lookup"><span data-stu-id="22881-111">IP+G,</span></span> 
- <span data-ttu-id="22881-112">OE5,</span><span class="sxs-lookup"><span data-stu-id="22881-112">OE5,</span></span> 
- <span data-ttu-id="22881-113">Conformité avancée O365</span><span class="sxs-lookup"><span data-stu-id="22881-113">O365 Advanced Compliance</span></span> 
- <span data-ttu-id="22881-114">EMS E5</span><span class="sxs-lookup"><span data-stu-id="22881-114">EMS E5</span></span>


## <a name="what-does-the-default-policy-do"></a><span data-ttu-id="22881-115">Que fait la stratégie par défaut ?</span><span class="sxs-lookup"><span data-stu-id="22881-115">What does the default policy do?</span></span>

<span data-ttu-id="22881-116">La stratégie DLP par défaut suit tous les numéros de carte de crédit partagés en interne et en externe dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="22881-116">The default DLP policy tracks all the credit card numbers shared internally and externally to the organization.</span></span> <span data-ttu-id="22881-117">Cette stratégie est en cours d’utilisation par défaut pour tous les utilisateurs du client.</span><span class="sxs-lookup"><span data-stu-id="22881-117">This policy is on by default for all users of the tenant.</span></span> <span data-ttu-id="22881-118">Il ne génère aucun conseil de stratégie pour les utilisateurs finaux, mais génère un événement d’alerte et déclenche également un e-mail de faible gravité à l’administrateur (ajouté dans la stratégie).</span><span class="sxs-lookup"><span data-stu-id="22881-118">It does not generate any policy tips for end users but does generate an Alert event and also triggers a low severity email to the admin (added in the policy).</span></span> <span data-ttu-id="22881-119">L’administrateur peut afficher les activités et modifier les détails des stratégies en se connectant au Centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="22881-119">Administrator can view the activities and edit the policies details by logging into the Compliance center.</span></span>

<span data-ttu-id="22881-120">Les administrateurs peuvent afficher [](https://compliance.microsoft.com/compliancesettings) cette stratégie dans le Centre de conformité et > stratégies de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="22881-120">Admins can view this policy in the [Compliance center](https://compliance.microsoft.com/compliancesettings) > Data Loss prevention policies page.</span></span>


> [!div class="mx-imgBorder"]
> <span data-ttu-id="22881-121">![Stratégie DLP Teams par défaut](../media/default-teams-dlp-policy.png)</span><span class="sxs-lookup"><span data-stu-id="22881-121">![default Teams DLP policy](../media/default-teams-dlp-policy.png)</span></span>

## <a name="edit-or-delete-the-default-policy"></a><span data-ttu-id="22881-122">Modifier ou supprimer la stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="22881-122">Edit or delete the default policy</span></span>

<span data-ttu-id="22881-123">Pour [modifier la stratégie par défaut afin d’améliorer les performances](create-test-tune-dlp-policy.md#tune-a-dlp-policy)ou pour la supprimer, utilisez simplement un compte avec les autorisations de gestion de la conformité **DLP.**</span><span class="sxs-lookup"><span data-stu-id="22881-123">To [edit the default policy for better performance or to delete it](create-test-tune-dlp-policy.md#tune-a-dlp-policy), just use an account with **DLP Compliance Management** permissions.</span></span> <span data-ttu-id="22881-124">Pour plus d’informations, voir [Autorisations.](create-test-tune-dlp-policy.md#permissions)</span><span class="sxs-lookup"><span data-stu-id="22881-124">For more information, see, [Permissions](create-test-tune-dlp-policy.md#permissions).</span></span>

