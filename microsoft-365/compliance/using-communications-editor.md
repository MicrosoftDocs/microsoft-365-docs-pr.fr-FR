---
title: Utiliser l’éditeur de communications
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez l’Éditeur de communications pour modifier le texte et fusionner des variables de champ lors de la mise en forme de votre contenu.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 6dcfb58dff3a3acf99340895872bb2da9795d9c8
ms.sourcegitcommit: 5ba0015c1554048f817fdfdc85359eee1368da64
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "49769159"
---
# <a name="use-the-communications-editor"></a><span data-ttu-id="4616e-103">Utiliser l’éditeur de communications</span><span class="sxs-lookup"><span data-stu-id="4616e-103">Use the communications editor</span></span>

<span data-ttu-id="4616e-104">Lorsque vous définissez le contenu de votre portail, les notifications de mise en attente légale et les rappels/escalades connexes, vous pouvez utiliser l’Éditeur de communications pour mettre en forme et personnaliser dynamiquement votre contenu.</span><span class="sxs-lookup"><span data-stu-id="4616e-104">As you define the content of your portal content, legal hold notifications, and related reminders/escalations, you can use the Communications Editor to format and dynamically customize your content.</span></span>

## <a name="rich-text-editor"></a><span data-ttu-id="4616e-105">Éditeur de texte enrichi</span><span class="sxs-lookup"><span data-stu-id="4616e-105">Rich text editor</span></span>

<span data-ttu-id="4616e-106">L’Éditeur de communications permet à l’utilisateur de personnaliser le texte à l’aide des options de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="4616e-106">The Communications Editor allows user to customize the text using the editor options.</span></span> <span data-ttu-id="4616e-107">Par exemple, les utilisateurs peuvent modifier des types de polices, créer des listes à puces, mettre en surbrillez du contenu, etc.</span><span class="sxs-lookup"><span data-stu-id="4616e-107">For example, users can change font types, create bulleted lists, highlight content, and more.</span></span>

## <a name="merge-field-variables"></a><span data-ttu-id="4616e-108">Fusionner des variables de champ</span><span class="sxs-lookup"><span data-stu-id="4616e-108">Merge field variables</span></span>

<span data-ttu-id="4616e-109">Vous pouvez utiliser des variables de fusion et de messagerie de l’Éditeur de communications pour incorporer des attributs de dépositaire personnalisés dans le corps du texte d’une communication.</span><span class="sxs-lookup"><span data-stu-id="4616e-109">You can use email merge variables from the Communications Editor to embed customized custodian attributes into a communication's body text.</span></span> <span data-ttu-id="4616e-110">Lorsqu’il est envoyé au dépositaire, le champ de fusion est rempli avec le champ correspondant.</span><span class="sxs-lookup"><span data-stu-id="4616e-110">When sent to the custodian, the merge field will be populated with the corresponding field.</span></span> <span data-ttu-id="4616e-111">Par exemple, lorsqu’il est envoyé au dépositaire John Smith, le champ de fusion [Nom du dépositaire] est traduit par le nom correspondant.</span><span class="sxs-lookup"><span data-stu-id="4616e-111">For example, when sent to custodian John Smith, the merge field [Custodian Name] would be translated with the corresponding name.</span></span>

<span data-ttu-id="4616e-112">Vous pouvez utiliser des champs  de fusion et de fusion en sélectionnant les icônes de champ Fusionner en haut du contrôle d’éditeur de texte enrichi.</span><span class="sxs-lookup"><span data-stu-id="4616e-112">You can use email merge fields by selecting the **Merge field** icons on the top of the rich-text editor control.</span></span> <span data-ttu-id="4616e-113">L’espace réservé est ajouté en fonction de l’emplacement du curseur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4616e-113">The placeholder will be added based off the location of the users' cursor.</span></span>

### <a name="list-of-merge-field-variables"></a><span data-ttu-id="4616e-114">Liste des variables de champ de fusion</span><span class="sxs-lookup"><span data-stu-id="4616e-114">List of merge field variables</span></span>

| <span data-ttu-id="4616e-115">Nom du champ</span><span class="sxs-lookup"><span data-stu-id="4616e-115">Field name</span></span>                  | <span data-ttu-id="4616e-116">Détails du champ</span><span class="sxs-lookup"><span data-stu-id="4616e-116">Field details</span></span> |
| :------------------- | :------------------- |
| <span data-ttu-id="4616e-117">Nom d’affichage</span><span class="sxs-lookup"><span data-stu-id="4616e-117">Display Name</span></span>  | <span data-ttu-id="4616e-118">Prénom et nom du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="4616e-118">The custodian's first and last name.</span></span> | 
| <span data-ttu-id="4616e-119">Lien d’accusé de réception</span><span class="sxs-lookup"><span data-stu-id="4616e-119">Acknowledgment Link</span></span> | <span data-ttu-id="4616e-120">Lien personnalisé pour enregistrer l’accusé de réception de chaque dépositaire.</span><span class="sxs-lookup"><span data-stu-id="4616e-120">A customized link to record each custodian's acknowledgment.</span></span>|                 |
| <span data-ttu-id="4616e-121">Lien portail</span><span class="sxs-lookup"><span data-stu-id="4616e-121">Portal Link</span></span>     | <span data-ttu-id="4616e-122">Lien personnalisé pour le portail de conformité du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="4616e-122">A customized link for the custodian's Compliance Portal.</span></span>|                |
| <span data-ttu-id="4616e-123">Responsable de l’émission</span><span class="sxs-lookup"><span data-stu-id="4616e-123">Issuing Officer</span></span>                   | <span data-ttu-id="4616e-124">Adresse de messagerie du responsable de l’émission spécifié.</span><span class="sxs-lookup"><span data-stu-id="4616e-124">The email address of the specified issuing officer.</span></span>|                   |
| <span data-ttu-id="4616e-125">Date d’émission</span><span class="sxs-lookup"><span data-stu-id="4616e-125">Issuing Date</span></span>                   | <span data-ttu-id="4616e-126">Date à laquelle l’avis a été émis (UTC).</span><span class="sxs-lookup"><span data-stu-id="4616e-126">The date that the notice was issued (UTC).</span></span>              |
|||
