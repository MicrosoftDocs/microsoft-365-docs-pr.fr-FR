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
ms.openlocfilehash: 08b028bbd28c06684245321e09f8ef3252098956
ms.sourcegitcommit: a53af7a228bb1f58cb8128a69a19da49f9e28700
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "45372487"
---
# <a name="records-management-in-microsoft-365"></a><span data-ttu-id="4e667-103">Gestion des enregistrements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4e667-103">Records management in Microsoft 365</span></span>

><span data-ttu-id="4e667-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="4e667-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="4e667-105">Les organisations de tous types ont besoin d’une solution de gestion des enregistrements pour gérer les documents réglementaires, juridiques et commerciaux critiques dans l'ensemble de leurs données d'entreprise.</span><span class="sxs-lookup"><span data-stu-id="4e667-105">Organizations of all types require a records-management solution to manage regulatory, legal, and business-critical records across their corporate data.</span></span> <span data-ttu-id="4e667-106">La gestion des enregistrements dans Microsoft 365 aide les organisations à gérer leurs obligations juridiques ainsi qu’à démontrer leur conformité avec les réglementations, et renforce leur efficacité grâce à la destruction régulière d’éléments dont la conservation n'est plus requise, qui n’ont plus de valeur ou qui ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4e667-106">Records management in Microsoft 365 helps an organization manage their legal obligations, provides the ability to demonstrate compliance with regulations, and increases efficiency with regular disposition of items that are no longer required to be retained, no longer of value, or no longer required for business purposes.</span></span>

<span data-ttu-id="4e667-107">La gestion des enregistrements dans Microsoft 365 offre les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="4e667-107">Records management in Microsoft 365 provides the following capabilities:</span></span>

- <span data-ttu-id="4e667-108">**Étiqueter du contenu comme enregistrement**</span><span class="sxs-lookup"><span data-stu-id="4e667-108">**Label content as a record**.</span></span> <span data-ttu-id="4e667-109">Créez et configurez des étiquettes de rétention pour marquer du contenu sous la forme d’un [enregistrement](records.md) qui peut ensuite être appliquées par des utilisateurs ou [appliquées automatiquement](apply-retention-labels-automatically.md) en identifiant les informations sensibles, les mots clés ou les types de contenu.</span><span class="sxs-lookup"><span data-stu-id="4e667-109">Create and configure retention labels to mark content as a [record](records.md) that can then be applied by users or [auto-applied](apply-retention-labels-automatically.md) by identifying sensitive information, keywords, or content types.</span></span>

- <span data-ttu-id="4e667-110">**Migrer et gérer vos exigences de conservation avec le plan de classement**.</span><span class="sxs-lookup"><span data-stu-id="4e667-110">**Migrate and manage your retention requirements with file plan**.</span></span> <span data-ttu-id="4e667-111">L’utilisation d’un [plan de gestion des fichiers ](file-plan-manager.md)vous permet de mettre en place un plan de rétention existante à Microsoft 365 ou d’en créer une nouvelle pour les fonctionnalités de gestion améliorées.</span><span class="sxs-lookup"><span data-stu-id="4e667-111">By using a [file plan](file-plan-manager.md), you can bring in an existing retention plan to Microsoft 365, or build a new one for enhanced management capabilities.</span></span>

- <span data-ttu-id="4e667-112">**Configurer les paramètres de rétention et de suppression avec l’étiquette de rétention**.</span><span class="sxs-lookup"><span data-stu-id="4e667-112">**Configure retention and deletion settings with the retention label**.</span></span> <span data-ttu-id="4e667-113">Définir des actions et des périodes de rétention en fonction de divers facteurs qui incluent la date de création ou de dernière modification.</span><span class="sxs-lookup"><span data-stu-id="4e667-113">Define retention periods and actions based on various factors that include the date last modified or created.</span></span>

- <span data-ttu-id="4e667-114">**Démarrer différentes périodes de rétention lorsqu’un événement se produit**avec[rétention basée sur des événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="4e667-114">**Start different retention periods when an event occurs** with [event-based retention](event-driven-retention.md).</span></span>

- <span data-ttu-id="4e667-115">**Vérifier et valider la destruction** en effectuant une [révision avant destruction](disposition.md#disposition-reviews) et la preuve de la [suppression d’enregistrements](disposition.md#disposition-of-records).</span><span class="sxs-lookup"><span data-stu-id="4e667-115">**Review and validate disposition** with [disposition reviews](disposition.md#disposition-reviews) and proof of [records deletion](disposition.md#disposition-of-records).</span></span>

- <span data-ttu-id="4e667-116">**Exporter des informations sur tous les éléments supprimés** avec l’[option exporter](disposition.md#filter-and-export-the-views).</span><span class="sxs-lookup"><span data-stu-id="4e667-116">**Export information about all disposed items** with the [export option](disposition.md#filter-and-export-the-views).</span></span>

- <span data-ttu-id="4e667-117">**Définir des autorisations spécifiques** afin que les fonctions de gestionnaire d’enregistrements au sein de votre organisation [disposent du droit d’accès](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="4e667-117">**Set specific permissions** for records manager functions in your organization to [have the right access](../security/office-365-security/permissions-in-the-security-and-compliance-center.md).</span></span>

<span data-ttu-id="4e667-118">La solution de gestion des enregistrements dans Microsoft 365 vous permet d’incorporer des planifications et exigences de rétention de votre organisation dans le plan de gestion de fichiers qui gère la rétention, la déclaration d’enregistrements et la destruction afin de prendre en charge le cycle de vie complet de votre contenu.</span><span class="sxs-lookup"><span data-stu-id="4e667-118">With the records-management solution in Microsoft 365, you can incorporate your organization's retention schedules and requirements into a file plan that manages retention, records declaration, and disposition to support the full lifecycle of your content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e667-119">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="4e667-119">Additional resources</span></span>

<span data-ttu-id="4e667-120">Consultez l’[enregistrement du webinaire](https://aka.ms/MIPC/Video-RecordsManagementWebinar) et le [support de présentation avec FAQ](https://aka.ms/MIPC/Blog-RecordsManagementWebinar) pour la gestion des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="4e667-120">See the [webinar recording](https://aka.ms/MIPC/Video-RecordsManagementWebinar) and [deck with FAQs](https://aka.ms/MIPC/Blog-RecordsManagementWebinar) for records management.</span></span>

## <a name="next-steps"></a><span data-ttu-id="4e667-121">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="4e667-121">Next steps</span></span>

<span data-ttu-id="4e667-122">Si vous êtes prêt à prendre en main la gestion des enregistrements dans Microsoft 365, consultez [en savoir plus sur les enregistrements](records.md).</span><span class="sxs-lookup"><span data-stu-id="4e667-122">If you are ready to get started with records management in Microsoft 365, see [Learn about records](records.md).</span></span>
