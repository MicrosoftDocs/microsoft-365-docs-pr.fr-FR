---
title: Gestion des accès privilégiés dans Microsoft 365
description: Découvrez comment configurer les fonctionnalités de risque internes au sein Microsoft 365.
keywords: Microsoft 365, risques internes, conformité
localization_priority: Normal
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- m365-security-compliance
- m365solution-insiderrisk
- m365initiative-compliance
- m365solution-scenario
ms.openlocfilehash: a5cd9d62670b35f7093a3d38cf9e499df407de97
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50423807"
---
# <a name="privileged-access-management-in-microsoft-365"></a><span data-ttu-id="f35da-104">Gestion des accès privilégiés dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35da-104">Privileged access management in Microsoft 365</span></span>

<span data-ttu-id="f35da-105">L’accès permanent par certains utilisateurs aux informations sensibles ou aux paramètres de configuration réseau critiques dans Microsoft Exchange Online est un parcours potentiel pour les comptes compromis ou les activités de menace internes.</span><span class="sxs-lookup"><span data-stu-id="f35da-105">Having standing access by some users to sensitive information or critical network configuration settings in Microsoft Exchange Online is a potential pathway for compromised accounts or internal threat activities.</span></span> <span data-ttu-id="f35da-106">La gestion des accès privilégiés permet de protéger votre organisation contre les violations et de respecter les meilleures pratiques de conformité en limitant l’accès permanent aux données sensibles ou l’accès aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="f35da-106">Privileged access management helps protect your organization from breaches and helps to meet compliance best practices by limiting standing access to sensitive data or access to critical configuration settings.</span></span> <span data-ttu-id="f35da-107">Au lieu d’avoir un accès constant aux administrateurs, des règles d’accès juste-à-temps sont implémentées pour les tâches qui ont besoin d’autorisations élevées.</span><span class="sxs-lookup"><span data-stu-id="f35da-107">Instead of administrators having constant access, just-in-time access rules are implemented for tasks that need elevated permissions.</span></span> <span data-ttu-id="f35da-108">L’activation de la gestion des accès privilégiés pour Exchange Online dans Microsoft 365 permet à votre organisation de fonctionner avec zéro privilège permanent et de fournir une couche de défense contre les vulnérabilités d’accès administratifs.</span><span class="sxs-lookup"><span data-stu-id="f35da-108">Enabling privileged access management for Exchange Online in Microsoft 365 allows your organization to operate with zero standing privileges and provide a layer of defense against standing administrative access vulnerabilities.</span></span>

## <a name="configure-privileged-access-management-for-microsoft-365"></a><span data-ttu-id="f35da-109">Configurer la gestion des accès privilégiés pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35da-109">Configure privileged access management for Microsoft 365</span></span>

<span data-ttu-id="f35da-110">Pour configurer la gestion des accès privilégiés pour votre organisation, utilisez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f35da-110">Use the following steps to configure privileged access management for your organization:</span></span>

![Étapes de gestion des accès privilégiés de la solution à risque interne](../media/ir-solution-pam-steps.png)

1. <span data-ttu-id="f35da-112">En savoir plus [sur la gestion des accès privilégiés](privileged-access-management-overview.md) dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f35da-112">Learn about [privileged access management](privileged-access-management-overview.md) in Microsoft 365</span></span>
2. <span data-ttu-id="f35da-113">Créer un [groupe d’approbation](privileged-access-management-configuration.md#step-1-create-an-approvers-group)</span><span class="sxs-lookup"><span data-stu-id="f35da-113">Create an [approver's group](privileged-access-management-configuration.md#step-1-create-an-approvers-group)</span></span>
3. <span data-ttu-id="f35da-114">Activer la [gestion des accès privilégiés](privileged-access-management-configuration.md#step-2-enable-privileged-access)</span><span class="sxs-lookup"><span data-stu-id="f35da-114">Enable [privileged access management](privileged-access-management-configuration.md#step-2-enable-privileged-access)</span></span>
4. <span data-ttu-id="f35da-115">Créer une stratégie [d’accès](privileged-access-management-configuration.md#step-3-create-an-access-policy)</span><span class="sxs-lookup"><span data-stu-id="f35da-115">Create an [access policy](privileged-access-management-configuration.md#step-3-create-an-access-policy)</span></span>
5. <span data-ttu-id="f35da-116">Envoyer/approuver [des demandes d’accès privilégié](privileged-access-management-configuration.md#step-4-submitapprove-privileged-access-requests)</span><span class="sxs-lookup"><span data-stu-id="f35da-116">Submit/approve [privileged access requests](privileged-access-management-configuration.md#step-4-submitapprove-privileged-access-requests)</span></span>

## <a name="more-information-about-privileged-access-management"></a><span data-ttu-id="f35da-117">Plus d’informations sur la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="f35da-117">More information about privileged access management</span></span>

- [<span data-ttu-id="f35da-118">Questions fréquemment posées sur la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="f35da-118">Frequently asked questions about privileged access management</span></span>](privileged-access-management-overview.md#frequently-asked-questions)