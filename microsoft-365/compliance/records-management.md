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
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
description: La gestion des enregistrements dans Microsoft 365 vous permet d’appliquer des planifications de rétention dans un plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction de ceux-ci.
ms.openlocfilehash: 0179f208f10921293c164516b26440f5bd043517
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45127481"
---
# <a name="records-management-in-microsoft-365"></a><span data-ttu-id="4f1a0-103">Gestion des enregistrements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4f1a0-103">Records management in Microsoft 365</span></span>

><span data-ttu-id="4f1a0-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="4f1a0-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="4f1a0-105">Les organisations de tous types ont besoin d’une solution de gestion des enregistrements pour gérer les documents réglementaires, juridiques et commerciaux critiques dans l'ensemble de leurs données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-105">Organizations of all types require a records-management solution to manage regulatory, legal, and business-critical records across their corporate data.</span></span> <span data-ttu-id="4f1a0-106">La gestion des enregistrements dans Microsoft 365 aide les organisations à gérer leurs obligations juridiques ainsi qu’à démontrer leur conformité avec les réglementations, et renforce leur efficacité grâce à la destruction régulière d’éléments dont la conservation n'est plus requise, qui n’ont plus de valeur ou qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-106">Records management in Microsoft 365 helps an organization manage their legal obligations, provides the ability to demonstrate compliance with regulations, and increases efficiency with regular disposition of items that are no longer required to be retained, no longer of value, or no longer required for business purposes.</span></span>

<span data-ttu-id="4f1a0-107">La gestion des enregistrements dans Microsoft 365 offre les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f1a0-107">Records management in Microsoft 365 provides the following capabilities:</span></span>

- <span data-ttu-id="4f1a0-108">**Étiqueter du contenu comme enregistrement**</span><span class="sxs-lookup"><span data-stu-id="4f1a0-108">**Label content as a record**.</span></span> <span data-ttu-id="4f1a0-109">Créez et publiez des étiquettes de rétention qui marquent du contenu sous la forme d’un [enregistrement](records.md) qui peut ensuite être appliquées par des utilisateurs finaux ou [appliquées automatiquement](apply-retention-labels-automatically.md) en identifiant les informations sensibles, les mots clés ou les types de contenu.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-109">Create and publish retention labels that mark content as a [record](records.md) that can then be applied by end users or [auto-applied](apply-retention-labels-automatically.md) by identifying sensitive information, keywords, or content types.</span></span>

- <span data-ttu-id="4f1a0-110">**Migrer et gérer vos exigences de conservation avec le plan de classement**.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-110">**Migrate and manage your retention requirements with file plan**.</span></span> <span data-ttu-id="4f1a0-111">L’utilisation d’un [plan de gestion des fichiers ](file-plan-manager.md)vous permet de mettre en place un plan de rétention existante à Microsoft 365 ou d’en créer une nouvelle pour les fonctionnalités de gestion améliorées.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-111">By using a [file plan](file-plan-manager.md), you can bring in an existing retention plan to Microsoft 365, or build a new one for enhanced management capabilities.</span></span>

- <span data-ttu-id="4f1a0-112">**Configurer les paramètres de rétention et de suppression avec l’étiquette de rétention**.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-112">**Configure retention and deletion settings with the retention label**.</span></span> <span data-ttu-id="4f1a0-113">Définir des actions et des périodes de rétention en fonction de divers facteurs qui incluent la date de création ou de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-113">Define retention periods and actions based on various factors that include the date last modified or created.</span></span>

- <span data-ttu-id="4f1a0-114">**Déclencher une rétention basée sur les événements** avec un [destruction basée sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a0-114">**Trigger event-based retention** with [event-based retention](event-driven-retention.md).</span></span>

- <span data-ttu-id="4f1a0-115">**Vérifier et valider la destruction** en effectuant une [révision avant destruction](disposition.md#disposition-reviews) et la preuve de la [suppression d’enregistrements](disposition.md#disposition-of-records).</span><span class="sxs-lookup"><span data-stu-id="4f1a0-115">**Review and validate disposition** with [disposition reviews](disposition.md#disposition-reviews) and proof of [records deletion](disposition.md#disposition-of-records).</span></span>

- <span data-ttu-id="4f1a0-116">**Exporter des informations sur tous les éléments supprimés** avec l’[option exporter](disposition.md#filter-and-export-the-views).</span><span class="sxs-lookup"><span data-stu-id="4f1a0-116">**Export information about all disposed items** with the [export option](disposition.md#filter-and-export-the-views).</span></span>

- <span data-ttu-id="4f1a0-117">**Définir des autorisations spécifiques** afin que les fonctions de gestionnaire d’enregistrements au sein de votre organisation [disposent du droit d’accès](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a0-117">**Set specific permissions** for records manager functions in your organization to [have the right access](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="4f1a0-118">La solution de gestion des enregistrements dans Microsoft 365 vous permet d’incorporer des planifications de rétention de votre organisation dans le plan de gestion de fichiers afin de gérer la rétention, la déclaration d’enregistrements et la destruction afin de prendre en charge le cycle de vie complet de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-118">With the records-management solution in Microsoft 365, you can incorporate your organization’s retention schedules into the file plan to manage retention, records declaration, and disposition to support the full lifecycle of your content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f1a0-119">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4f1a0-119">Additional resources</span></span>

<span data-ttu-id="4f1a0-120">Consultez l’[enregistrement du webinaire](https://aka.ms/MIPC/Video-RecordsManagementWebinar) et le [support de présentation avec FAQ](https://aka.ms/MIPC/Blog-RecordsManagementWebinar) pour la gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4f1a0-120">See the [webinar recording](https://aka.ms/MIPC/Video-RecordsManagementWebinar) and [deck with FAQs](https://aka.ms/MIPC/Blog-RecordsManagementWebinar) for records management.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4f1a0-121">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4f1a0-121">Next steps</span></span>

<span data-ttu-id="4f1a0-122">Si vous êtes prêt à prendre en main la gestion des enregistrements dans Microsoft 365, consultez [en savoir plus sur les enregistrements](records.md).</span><span class="sxs-lookup"><span data-stu-id="4f1a0-122">If you are ready to get started with records management in Microsoft 365, see [Learn about records](records.md).</span></span>
