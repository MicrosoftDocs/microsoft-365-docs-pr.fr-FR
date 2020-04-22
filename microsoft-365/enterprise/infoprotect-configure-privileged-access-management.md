---
title: 'Étape 7 : configurer la gestion des accès privilégiés'
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.custom: ''
description: Comprenez et configurez la gestion des accès privilégiés.
ms.openlocfilehash: 4fed4daacc17a34563825bf0575880ce06ec6ebd
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43636987"
---
# <a name="step-7-configure-privileged-access-management"></a><span data-ttu-id="43694-103">Étape 7 : configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="43694-103">Step 7: Configure privileged access management</span></span>

<span data-ttu-id="43694-104">*Cette étape est facultative et s’applique uniquement à la version E5 et à la version Conformité avancée de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="43694-104">*This step is optional and applies only to the E5 and Advanced Compliance versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : Protection des informations](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="43694-106">La gestion des accès privilégiés est activée en configurant des stratégies qui spécifient un accès juste-à-temps pour les activités basées sur les tâches de votre client.</span><span class="sxs-lookup"><span data-stu-id="43694-106">Privileged access management is enabled by configuring policies that specify just-in-time access for task-based activities in your tenant.</span></span> <span data-ttu-id="43694-107">Il peut vous aider à protéger votre organisation contre les violations susceptibles d’utiliser des comptes administrateur avec privilèges existants avec un accès permanent aux données sensibles ou un accès aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="43694-107">It can help protect your organization from breaches that may use existing privileged administrator accounts with standing access to sensitive data or access to critical configuration settings.</span></span> <span data-ttu-id="43694-108">Par exemple, vous pouvez configurer une stratégie de gestion des accès privilégiés qui requiert une approbation explicite pour accéder aux paramètres de la boîte aux lettres de l’organisation et les modifier dans votre client.</span><span class="sxs-lookup"><span data-stu-id="43694-108">For example, you could configure a privileged access management policy that requires explicit approval to access and change organization mailbox settings in your tenant.</span></span>

<span data-ttu-id="43694-109">Dans cette étape, vous allez activer la gestion des accès privilégiés dans votre client et configurer des stratégies d’accès privilégié qui fournissent une sécurité supplémentaire pour l’accès basé sur les tâches aux paramètres de données et de configuration de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="43694-109">In this step, you'll enable privileged access management in your tenant and configure privileged access policies that provide additional security for task-based access to data and configuration settings for your organization.</span></span> <span data-ttu-id="43694-110">Il existe trois étapes de base pour commencer à utiliser l’accès privilégié dans votre organisation :</span><span class="sxs-lookup"><span data-stu-id="43694-110">There are three basic steps to get started with privileged access in your organization:</span></span>
- <span data-ttu-id="43694-111">Création d’un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="43694-111">Creating an approver's group</span></span>
- <span data-ttu-id="43694-112">Activation des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="43694-112">Enabling privileged access</span></span>
- <span data-ttu-id="43694-113">Création de stratégies d’approbation</span><span class="sxs-lookup"><span data-stu-id="43694-113">Creating approval policies</span></span>

<span data-ttu-id="43694-p103">Une fois configurée, la gestion des accès privilégiés permettra à votre organisation de fonctionner sans aucun privilège permanent et de fournir une sécurité renforcée contre les lacunes d’un accès administratif permanent comme celui-ci. L’accès privilégié requiert des approbations pour exécuter toute tâche pour laquelle une stratégie d’approbation associée a été définie. Les utilisateurs ayant besoin d’exécuter des tâches incluses dans la stratégie d’approbation doivent demander l’approbation de l’accès et l’obtenir afin de disposer des autorisations nécessaires pour exécuter les tâches définies dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="43694-p103">One configured, privileged access management will enable your organization to operate with zero standing privileges and provide a layer of defense against vulnerabilities arising because of such standing administrative access. Privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute tasks defined in the policy.</span></span>

<span data-ttu-id="43694-117">Pour activer la gestion des accès privilégiés, consultez la rubrique [configurer la gestion des accès privilégiés](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) .</span><span class="sxs-lookup"><span data-stu-id="43694-117">To enable privileged access management, see the [Configure privileged access management](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic.</span></span>

<span data-ttu-id="43694-118">Pour plus d’informations, consultez la rubrique [gestion des accès privilégiés](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview) .</span><span class="sxs-lookup"><span data-stu-id="43694-118">For more information, see the [Privileged access management](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview) topic.</span></span>


|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)|  <span data-ttu-id="43694-120">Pour tester cette configuration dans un environnement de laboratoire de test, consultez le [Guide de laboratoire de test Gestion des accès privilégiés](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="43694-120">To practice this configuration in a test lab environment, see the [Privileged access management Test Lab Guide](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span></span> |
|||

<span data-ttu-id="43694-121">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step7) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="43694-121">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step7) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="43694-122">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="43694-122">Next Step</span></span>

[<span data-ttu-id="43694-123">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="43694-123">Information protection infrastructure exit criteria</span></span>](infoprotect-exit-criteria.md)
