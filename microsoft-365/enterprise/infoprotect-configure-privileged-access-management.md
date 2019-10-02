---
title: 'Étape 7 : Configurer la gestion des accès privilégiés pour Office 365'
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
description: Familiarisez-vous avec la gestion des accès privilégiés pour Office 365 et apprenez à la configurer.
ms.openlocfilehash: e9c68e4fafb1e9537b403965b4360806938c6a6f
ms.sourcegitcommit: 8bcd76e5c8749a5670fbc3356957a089454c03d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2019
ms.locfileid: "37370421"
---
# <a name="step-7-configure-privileged-access-management-for-office-365"></a><span data-ttu-id="202fb-103">Étape 7 : Configurer la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="202fb-103">Step 7: Configure privileged access management for Office 365</span></span>

<span data-ttu-id="202fb-104">*Cette étape est facultative et s’applique uniquement à la version E5 et à la version Conformité avancée de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="202fb-104">*This step is optional and applies only to the E5 and Advanced Compliance versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : protection des informations](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="202fb-p101">Vous activez la gestion des accès privilégiés en configurant des stratégies qui indiquent l’accès juste-à-temps pour les activités basées sur des tâches dans votre client Office 365. Elle peut vous aider à protéger votre organisation contre les violations qui pourraient survenir par le biais de comptes d’administrateur privilégiés existants qui donnent un accès permanent à des données sensibles ou à des paramètres de configuration critiques. Par exemple, vous pouvez configurer une stratégie de gestion des accès privilégiés qui requiert une approbation explicite pour pouvoir accéder aux paramètres de boîte aux lettres de votre organisation dans votre client Office 365 et les modifier.</span><span class="sxs-lookup"><span data-stu-id="202fb-p101">Privileged access management is enabled by configuring policies that specify just-in-time access for task-based activities in your Office 365 tenant. It can help protect your organization from breaches that may use existing privileged administrator accounts with standing access to sensitive data or access to critical configuration settings. For example, you could configure a privileged access management policy that requires explicit approval to access and change organization mailbox settings in your Office 365 tenant.</span></span>

<span data-ttu-id="202fb-p102">Pour cette étape, vous allez activer la gestion des accès privilégiés dans votre client Office 365 et configurer les stratégies d’accès privilégiés qui permettent de renforcer la sécurité des accès basés sur les tâches à vos paramètres de configuration et à vos données Office 365 pour votre organisation. Il existe trois étapes simples pour commencer à utiliser les accès privilégiés dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="202fb-p102">In this step, you'll enable privileged access management in your Office 365 tenant and configure privileged access policies that provide additional security for task-based access to Office 365 data and configuration settings for your organization. There are three basic steps to get started with privileged access in your Office 365 organization:</span></span>
- <span data-ttu-id="202fb-111">Création d’un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="202fb-111">Creating an approver's group</span></span>
- <span data-ttu-id="202fb-112">Activation des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="202fb-112">Enabling privileged access</span></span>
- <span data-ttu-id="202fb-113">Création de stratégies d’approbation</span><span class="sxs-lookup"><span data-stu-id="202fb-113">Creating approval policies</span></span>

<span data-ttu-id="202fb-p103">Une fois configurée, la gestion des accès privilégiés permettra à votre organisation de fonctionner sans aucun privilège permanent et de fournir une sécurité renforcée contre les lacunes d’un accès administratif permanent comme celui-ci. L’accès privilégié requiert des approbations pour exécuter toute tâche pour laquelle une stratégie d’approbation associée a été définie. Les utilisateurs ayant besoin d’exécuter des tâches incluses dans la stratégie d’approbation doivent demander l’approbation de l’accès et l’obtenir afin de disposer des autorisations nécessaires pour exécuter les tâches définies dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="202fb-p103">One configured, privileged access management will enable your organization to operate with zero standing privileges and provide a layer of defense against vulnerabilities arising because of such standing administrative access. Privileged access requires approvals for executing any task that has an associated approval policy defined. Users needing to execute tasks included in the an approval policy must request and be granted access approval in order to have permissions necessary to execute tasks defined in the policy.</span></span>

<span data-ttu-id="202fb-117">Pour activer la gestion des accès privilégiés d’Office 365, consultez la rubrique relative à la [configuration de la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration).</span><span class="sxs-lookup"><span data-stu-id="202fb-117">To enable Office 365 privileged access management, see the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic.</span></span>

<span data-ttu-id="202fb-118">Pour plus d’informations, reportez-vous à la rubrique relative à la [gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview).</span><span class="sxs-lookup"><span data-stu-id="202fb-118">For more information, see the [Privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-overview) topic.</span></span>


|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)|  <span data-ttu-id="202fb-120">Pour vous exercer à cette configuration dans un environnement de laboratoire de test, consultez le [Guide de laboratoire de test de gestion des accès privilégiés](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="202fb-120">To practice this configuration in a test lab environment, see the [Privileged access management Test Lab Guide](privileged-access-microsoft-365-enterprise-dev-test-environment.md).</span></span> |
|||

<span data-ttu-id="202fb-121">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step7) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="202fb-121">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step7) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="202fb-122">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="202fb-122">Next Step</span></span>

[<span data-ttu-id="202fb-123">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="202fb-123">Information protection infrastructure exit criteria</span></span>](infoprotect-exit-criteria.md)
