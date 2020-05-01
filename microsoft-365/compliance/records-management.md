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
ms.openlocfilehash: e4454ba5940d9a67d9f160d90d0a9db14563bcf7
ms.sourcegitcommit: f5cecd77e63ae8b47743d4f6dc3135f5decaf28b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "43949247"
---
# <a name="records-management-in-microsoft-365"></a><span data-ttu-id="23a8f-103">Gestion des enregistrements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="23a8f-103">Records management in Microsoft 365</span></span>

><span data-ttu-id="23a8f-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="23a8f-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="23a8f-105">Les organisations de tous types ont besoin d’une solution de gestion des enregistrements pour gérer les documents réglementaires, juridiques et commerciaux critiques dans l'ensemble de leurs données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="23a8f-105">Organizations of all types require a records-management solution to manage regulatory, legal, and business-critical records across their corporate data.</span></span> <span data-ttu-id="23a8f-106">La gestion des enregistrements dans Microsoft 365 aide les organisations à gérer leurs obligations juridiques ainsi qu’à démontrer leur conformité avec les réglementations, et renforce leur efficacité grâce à la destruction régulière d’éléments dont la conservation n'est plus requise, qui n’ont plus de valeur ou qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="23a8f-106">Records management in Microsoft 365 helps an organization manage their legal obligations, provides the ability to demonstrate compliance with regulations, and increases efficiency with regular disposition of items that are no longer required to be retained, no longer of value, or no longer required for business purposes.</span></span>

<span data-ttu-id="23a8f-107">La solution de gestion des enregistrements prend en charge les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="23a8f-107">The records-management solution supports the following elements:</span></span>

- <span data-ttu-id="23a8f-108">**Étiqueter du contenu comme enregistrement**</span><span class="sxs-lookup"><span data-stu-id="23a8f-108">**Label content as a record**.</span></span> <span data-ttu-id="23a8f-109">Créez et publiez des étiquettes de rétention qui déclarent du contenu sous la forme d’un [enregistrement](records.md) qui peut ensuite être appliquées par des utilisateurs finaux ou [appliquées automatiquement](labels.md#applying-a-retention-label-automatically-based-on-conditions) en identifiant les informations sensibles, les mots clés ou les types de contenu.</span><span class="sxs-lookup"><span data-stu-id="23a8f-109">Create and publish retention labels that declare content as a [record](records.md) that can then be applied by end users or [auto-applied](labels.md#applying-a-retention-label-automatically-based-on-conditions) by identifying sensitive information, keywords, or content types.</span></span>

- <span data-ttu-id="23a8f-110">**Migrer et gérer votre plan de rétention avec le plan de gestion de fichiers**, et utiliser le [gestionnaire du plan de gestion de fichiers](file-plan-manager.md) pour incorporer votre plan de rétention existant ou en créer un avec des descripteurs de fichiers et des hiérarchies en expansion.</span><span class="sxs-lookup"><span data-stu-id="23a8f-110">**Migrate and manage your retention plan with file plan** and use [file plan manager](file-plan-manager.md) to bring in your existing retention plan, or build new with file descriptors and expanding hierarchies.</span></span>

- <span data-ttu-id="23a8f-111">**Établir des stratégies de rétention et de suppression**.</span><span class="sxs-lookup"><span data-stu-id="23a8f-111">**Establish retention and deletion policies**.</span></span> <span data-ttu-id="23a8f-112">Définir des périodes de [rétention](retention-policies.md#retaining-content-for-a-specific-period-of-time) et de [destruction](retention-policies.md#deleting-content-thats-older-than-a-specific-age) en fonction de divers facteurs qui incluent la date de création ou de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="23a8f-112">Define [retention](retention-policies.md#retaining-content-for-a-specific-period-of-time) and [disposition](retention-policies.md#deleting-content-thats-older-than-a-specific-age) periods based on various factors that include the date last modified or created.</span></span>

- <span data-ttu-id="23a8f-113">**Déclencher une rétention basée sur les événements** avec un [destruction basée sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="23a8f-113">**Trigger event-based retention** with [event-based retention](event-driven-retention.md).</span></span>

- <span data-ttu-id="23a8f-114">**Vérifier et valider la destruction** en effectuant une [révision avant destruction](disposition.md#disposition-reviews) et la preuve de la [suppression d’enregistrements](disposition.md#disposition-of-records).</span><span class="sxs-lookup"><span data-stu-id="23a8f-114">**Review and validate disposition** with [disposition reviews](disposition.md#disposition-reviews) and proof of [records deletion](disposition.md#disposition-of-records).</span></span>

- <span data-ttu-id="23a8f-115">**Exporter des informations sur tous les éléments supprimés** avec l’[option exporter](disposition.md#filter-and-export-the-views).</span><span class="sxs-lookup"><span data-stu-id="23a8f-115">**Export information about all disposed items** with the [export option](disposition.md#filter-and-export-the-views).</span></span>

- <span data-ttu-id="23a8f-116">**Définir des autorisations spécifiques** afin que les fonctions de gestionnaire d’enregistrements au sein de votre organisation [disposent du droit d’accès](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="23a8f-116">**Set specific permissions** for records manager functions in your organization to [have the right access](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="23a8f-117">La solution de gestion des enregistrements dans Microsoft 365 vous permet d’incorporer des planifications de rétention de votre organisation dans le plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction afin de prendre en charge le cycle de vie complet de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="23a8f-117">With the records-management solution in Microsoft 365, you can incorporate your organization’s retention schedules into the file plan to manage retention, records declaration, and disposition to support the full lifecycle of your content.</span></span>
