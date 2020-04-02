---
title: Gestion des enregistrements
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: La gestion des enregistrements dans Microsoft 365 vous permet d’appliquer des planifications de rétention spécifiques de votre organisation dans un plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction de ceux-ci à l’appui du cycle de vie complet du contenu.
ms.openlocfilehash: e74c7d9e5f01b49805fccdfac2c719835354b97a
ms.sourcegitcommit: e695bcfc69203da5d3d96f3d6a891664a0e27ae2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43106080"
---
# <a name="records-management-in-microsoft-365"></a><span data-ttu-id="331dd-103">Gestion des enregistrements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="331dd-103">Records management in Microsoft 365</span></span>

><span data-ttu-id="331dd-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="331dd-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="331dd-105">Les organisations de tous types ont besoin d’une solution de gestion des enregistrements pour gérer les documents réglementaires, juridiques et commerciaux critiques dans l'ensemble de leurs données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="331dd-105">Organizations of all types require a records-management solution to manage regulatory, legal, and business-critical records across their corporate data.</span></span> <span data-ttu-id="331dd-106">La gestion des enregistrements dans Microsoft 365 aide les organisations à gérer leurs obligations juridiques ainsi qu’à démontrer leur conformité avec les réglementations, et renforce leur efficacité grâce à la destruction régulière d’éléments dont la conservation n'est plus requise, qui n’ont plus de valeur ou qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="331dd-106">Records management in Microsoft 365 helps an organization manage their legal obligations, provides the ability to demonstrate compliance with regulations, and increases efficiency with regular disposition of items that are no longer required to be retained, no longer of value, or no longer required for business purposes.</span></span>

<span data-ttu-id="331dd-107">La solution de gestion des enregistrements prend en charge les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="331dd-107">The records-management solution supports the following elements:</span></span>

- <span data-ttu-id="331dd-108">**Étiqueter du contenu comme enregistrement**</span><span class="sxs-lookup"><span data-stu-id="331dd-108">**Label content as a record**.</span></span> <span data-ttu-id="331dd-109">Publier des [étiquettes d’enregistrement](records.md) à appliquer par les utilisateurs finaux ou [appliquées automatiquement](labels.md#applying-a-retention-label-automatically-based-on-conditions) aux éléments contenant des informations sensibles, des mots clés ou certaines types de contenus.</span><span class="sxs-lookup"><span data-stu-id="331dd-109">Publish [record labels](records.md) to be applied by end users or [auto-apply](labels.md#applying-a-retention-label-automatically-based-on-conditions) record labels to items containing specific sensitive information, keywords, or content types.</span></span>

- <span data-ttu-id="331dd-110">**Migrer et gérer votre plan de rétention avec le plan de gestion de fichiers**, et utiliser le [gestionnaire du plan de gestion de fichiers](file-plan-manager.md) pour incorporer votre plan de rétention existant ou en créer un avec des descripteurs de fichiers et des hiérarchies en expansion.</span><span class="sxs-lookup"><span data-stu-id="331dd-110">**Migrate and manage your retention plan with file plan** and use [file plan manager](file-plan-manager.md) to bring in your existing retention plan, or build new with file descriptors and expanding hierarchies.</span></span>

- <span data-ttu-id="331dd-111">**Établir des stratégies de rétention et de suppression à l’intérieur de l’étiquette d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="331dd-111">**Establish retention and deletion policies within the record label**.</span></span> <span data-ttu-id="331dd-112">Définir des périodes de [rétention](retention-policies.md#retaining-content-for-a-specific-period-of-time) et de [destruction](retention-policies.md#deleting-content-thats-older-than-a-specific-age) en fonction de divers facteurs, dont la date de création ou de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="331dd-112">Define [retention](retention-policies.md#retaining-content-for-a-specific-period-of-time) and [disposition](retention-policies.md#deleting-content-thats-older-than-a-specific-age) periods based on various factors including the date last modified or created.</span></span>

- <span data-ttu-id="331dd-113">**Déclencher une rétention basée sur les événements** avec un [destruction basée sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="331dd-113">**Trigger event-based retention** with [event-based retention](event-driven-retention.md).</span></span>

- <span data-ttu-id="331dd-114">**Vérifier et valider la destruction** en effectuant une [révision avant destruction](disposition-reviews.md).</span><span class="sxs-lookup"><span data-stu-id="331dd-114">**Review and validate disposition** with [disposition review](disposition-reviews.md).</span></span>

- <span data-ttu-id="331dd-115">**Passer en revue les éléments détruits en effectuant une révision avant destruction**, puis [exporter un rapport d’actions](disposition-reviews.md#export-the-disposition-items) afin d’approfondir la validation et de générer un rapport.</span><span class="sxs-lookup"><span data-stu-id="331dd-115">**Review disposed items with disposition review** and [export a disposition report](disposition-reviews.md#export-the-disposition-items) for further validation and reporting.</span></span>

- <span data-ttu-id="331dd-116">**Définir des autorisations spécifiques** afin que les fonctions de gestionnaire d’enregistrements au sein de votre organisation [disposent du droit d’accès](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="331dd-116">**Set specific permissions** for records manager functions in your organization to [have the right access](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="331dd-117">La solution de gestion des enregistrements dans Microsoft 365 vous permet d’incorporer des planifications de rétention de votre organisation dans le plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction de ceux-ci à l’appui du cycle de vie complet du contenu.</span><span class="sxs-lookup"><span data-stu-id="331dd-117">With the records-management solution in Microsoft 365, you can incorporate your organization’s retention schedules into the file plan to manage retention, records declaration, and disposition in support of the full content lifecycle.</span></span>
