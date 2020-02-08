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
ms.openlocfilehash: dcc3e5666bcd438a046d535cf9fce88910b85ad7
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41597651"
---
# <a name="records-management-in-microsoft-365"></a><span data-ttu-id="fe215-103">Gestion des enregistrements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="fe215-103">Records management in Microsoft 365</span></span>

<span data-ttu-id="fe215-104">Les organisations de tous types ont besoin d’une solution de gestion des enregistrements pour gérer les documents réglementaires, juridiques et commerciaux critiques dans l'ensemble de leurs données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="fe215-104">Organizations of all types require a records-management solution to manage regulatory, legal, and business-critical records across their corporate data.</span></span> <span data-ttu-id="fe215-105">La gestion des enregistrements dans Microsoft 365 aide les organisations à gérer leurs obligations juridiques ainsi qu’à démontrer leur conformité avec les réglementations, et renforce leur efficacité grâce à la destruction régulière d’éléments dont la conservation n'est plus requise, qui n’ont plus de valeur ou qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="fe215-105">Records management in Microsoft 365 helps an organization manage their legal obligations, provides the ability to demonstrate compliance with regulations, and increases efficiency with regular disposition of items that are no longer required to be retained, no longer of value, or no longer required for business purposes.</span></span>

<span data-ttu-id="fe215-106">La solution de gestion des enregistrements prend en charge les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe215-106">The records-management solution supports the following elements:</span></span>

- <span data-ttu-id="fe215-107">**Étiqueter du contenu comme enregistrement**</span><span class="sxs-lookup"><span data-stu-id="fe215-107">**Label content as a record**.</span></span> <span data-ttu-id="fe215-108">Publier des [étiquettes d’enregistrement](records.md) à appliquer par les utilisateurs finaux ou [appliquées automatiquement](labels.md#applying-a-retention-label-automatically-based-on-conditions) aux éléments contenant des informations sensibles, des mots clés ou certaines types de contenus.</span><span class="sxs-lookup"><span data-stu-id="fe215-108">Publish [record labels](records.md) to be applied by end users or [auto-apply](labels.md#applying-a-retention-label-automatically-based-on-conditions) record labels to items containing specific sensitive information, keywords, or content types.</span></span>

- <span data-ttu-id="fe215-109">**Migrer et gérer votre plan de rétention avec le plan de gestion de fichiers**, et utiliser le [gestionnaire du plan de gestion de fichiers](file-plan-manager.md) pour incorporer votre plan de rétention existant ou en créer un avec des descripteurs de fichiers et des hiérarchies en expansion.</span><span class="sxs-lookup"><span data-stu-id="fe215-109">**Migrate and manage your retention plan with file plan** and use [file plan manager](file-plan-manager.md) to bring in your existing retention plan, or build new with file descriptors and expanding hierarchies.</span></span>

- <span data-ttu-id="fe215-110">**Établir des stratégies de rétention et de suppression à l’intérieur de l’étiquette d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="fe215-110">**Establish retention and deletion policies within the record label**.</span></span> <span data-ttu-id="fe215-111">Définir des périodes de [rétention](retention-policies.md#retaining-content-for-a-specific-period-of-time) et de [destruction](retention-policies.md#deleting-content-thats-older-than-a-specific-age) en fonction de divers facteurs, dont la date de création ou de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="fe215-111">Define [retention](retention-policies.md#retaining-content-for-a-specific-period-of-time) and [disposition](retention-policies.md#deleting-content-thats-older-than-a-specific-age) periods based on various factors including the date last modified or created.</span></span>

- <span data-ttu-id="fe215-112">**Déclencher une rétention basée sur les événements** avec un [destruction basée sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="fe215-112">**Trigger event-based retention** with [event-based retention](event-driven-retention.md).</span></span>

- <span data-ttu-id="fe215-113">**Vérifier et valider la destruction** en effectuant une [révision avant destruction](disposition-reviews.md).</span><span class="sxs-lookup"><span data-stu-id="fe215-113">**Review and validate disposition** with [disposition review](disposition-reviews.md).</span></span>

- <span data-ttu-id="fe215-114">**Passer en revue les éléments détruits en effectuant une révision avant destruction**, puis [exporter un rapport d’actions](disposition-reviews.md#export-the-disposition-items) afin d’approfondir la validation et de générer un rapport.</span><span class="sxs-lookup"><span data-stu-id="fe215-114">**Review disposed items with disposition review** and [export a disposition report](disposition-reviews.md#export-the-disposition-items) for further validation and reporting.</span></span>

- <span data-ttu-id="fe215-115">**Définir des autorisations spécifiques** afin que les fonctions de gestionnaire d’enregistrements au sein de votre organisation [disposent du droit d’accès](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fe215-115">**Set specific permissions** for records manager functions in your organization to [have the right access](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="fe215-116">La solution de gestion des enregistrements dans Microsoft 365 vous permet d’incorporer des planifications de rétention de votre organisation dans le plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction de ceux-ci à l’appui du cycle de vie complet du contenu.</span><span class="sxs-lookup"><span data-stu-id="fe215-116">With the records-management solution in Microsoft 365, you can incorporate your organization’s retention schedules into the file plan to manage retention, records declaration, and disposition in support of the full content lifecycle.</span></span>
