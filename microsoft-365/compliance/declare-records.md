---
title: Déclarer des enregistrements à l’aide d’étiquettes de rétention
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
ms.collection:
- M365-security-compliance
- SPO_Content
search.appverid:
- MOE150
- MET150
description: Déclarer des enregistrements à l’aide d’étiquettes de rétention.
ms.openlocfilehash: 841c5197addff704016e344ba7ae44355c872f72
ms.sourcegitcommit: 9f5b136b96b3af4db4cc6f5b1f35130ae60d6b12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "47817100"
---
# <a name="declare-records-by-using-retention-labels"></a><span data-ttu-id="1e663-103">Déclarer des enregistrements à l’aide d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="1e663-103">Declare records by using retention labels</span></span>

><span data-ttu-id="1e663-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="1e663-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="1e663-105">Pour déclarer des documents et courriers électroniques comme enregistrement, utilisez des [étiquettes de rétention](retention.md#retention-labels) qui servent à marquer des éléments comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e663-105">To declare documents and emails as a record, you use [retention labels](retention.md#retention-labels) that mark items as a record.</span></span> <span data-ttu-id="1e663-106">Vous pouvez soit publier ces étiquettes pour permettre aux utilisateurs et aux administrateurs de les appliquer manuellement au contenu, soit appliquer automatiquement ces étiquettes au contenu que vous voulez marquer comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e663-106">You can either publish those labels so that users and administrators can manually apply them to content, or auto-apply those labels to content that you want to mark as a record.</span></span>

## <a name="configuring-retention-labels-to-declare-records"></a><span data-ttu-id="1e663-107">Configuration d’étiquettes de rétention pour déclarer des enregistrements</span><span class="sxs-lookup"><span data-stu-id="1e663-107">Configuring retention labels to declare records</span></span>

<span data-ttu-id="1e663-108">Lors de la création ou la configuration d’une étiquette de rétention, sélectionnez l'option permettant de marquer le contenu comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1e663-108">When you create or configure a retention label, select the option to mark items as a record.</span></span>

>[!NOTE] 
> <span data-ttu-id="1e663-109">L’option de marquage du contenu en tant qu’enregistrement n’est pas disponible lorsque vous créez ou configurez des étiquettes de rétention depuis **Gouvernance des informations** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1e663-109">The option to mark the content as a record is not available when you create or configure retention labels from **Information Governance** in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="1e663-110">Au lieu de cela, vous devez utiliser**Gestion des enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="1e663-110">Instead, you must use **Records Management**.</span></span>

<span data-ttu-id="1e663-111">Créer un nouveau label de conservation qui marque le contenu comme un enregistrement :</span><span class="sxs-lookup"><span data-stu-id="1e663-111">To create a new retention label that marks the content as a record:</span></span>

1. <span data-ttu-id="1e663-112">Dans le [centre de conformité Microsoft 365](https://compliance.microsoft.com), accédez à **Gestion des enregistrements** \> **Plan de gestion de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="1e663-112">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Records Management** \> **File Plan**.</span></span> <span data-ttu-id="1e663-113">Dans la page **plan de fichiers**, cliquez **créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="1e663-113">On the **File plan** page, select **Create a label**.</span></span>

2. <span data-ttu-id="1e663-114">Dans la page **Définir les paramètres de rétention** de l’assistant, choisissez l’option permettant de marquer des éléments comme enregistrements :</span><span class="sxs-lookup"><span data-stu-id="1e663-114">On the **Define retention settings** page in the wizard, choose the option to mark items as records:</span></span>
    
   ![Sélectionnez paramètre de rétention pour marquer des éléments comme enregistrement](../media/recordversioning6.png)

3. <span data-ttu-id="1e663-116">Appliquez l’étiquette de rétention aux documents SharePoint ou OneDrive et aux messages électroniques Exchange, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1e663-116">Apply the retention label to SharePoint or OneDrive documents and Exchange emails, as needed.</span></span> <span data-ttu-id="1e663-117">Pour obtenir des instructions :</span><span class="sxs-lookup"><span data-stu-id="1e663-117">For instructions:</span></span>
    
    - [<span data-ttu-id="1e663-118">Créer des étiquettes de rétention et les appliquer dans les applications</span><span class="sxs-lookup"><span data-stu-id="1e663-118">Create retention labels and apply them in apps</span></span>](create-apply-retention-labels.md)
    
    - [<span data-ttu-id="1e663-119">Appliquer automatiquement une étiquette de rétention au contenu</span><span class="sxs-lookup"><span data-stu-id="1e663-119">Apply a retention label to content automatically</span></span>](apply-retention-labels-automatically.md)

## <a name="applying-the-configured-retention-label-to-content"></a><span data-ttu-id="1e663-120">Application de l’étiquette de rétention configurée au contenu</span><span class="sxs-lookup"><span data-stu-id="1e663-120">Applying the configured retention label to content</span></span>

<span data-ttu-id="1e663-121">Lorsque des étiquettes de rétention qui marquent le contenu en tant qu’enregistrement sont mises à la disposition des utilisateurs pour qu’ils les appliquent dans les applications :</span><span class="sxs-lookup"><span data-stu-id="1e663-121">When retention labels that mark content as a record are made available for users to apply them in apps:</span></span>

- <span data-ttu-id="1e663-122">Pour Exchange, tout utilisateur disposant d’un accès en écriture à la boîte aux lettres peut appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="1e663-122">For Exchange, any user with write-access to the mailbox can apply these labels.</span></span> 
- <span data-ttu-id="1e663-123">Pour SharePoint et OneDrive, tous les utilisateurs du groupe Membres par défaut (niveau d’autorisation Collaboration) peuvent appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="1e663-123">For SharePoint and OneDrive, any user in the default Members group (the Contribute permission level) can apply these labels.</span></span>

<span data-ttu-id="1e663-124">Exemple d’un document marqué en tant qu’enregistrement à l’aide d’une étiquette de rétention :</span><span class="sxs-lookup"><span data-stu-id="1e663-124">Example of a document marked as record by using a retention label:</span></span>

![Volet Détails pour le document marqué comme enregistrement](../media/recordversioning7.png)

## <a name="next-steps"></a><span data-ttu-id="1e663-126">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1e663-126">Next steps</span></span>

<span data-ttu-id="1e663-127">Pour une liste des scénarios pris en charge par la gestion des documents, voir [Scénarios communs pour la gestion des documents](get-started-with-records-management.md#common-scenarios-for-records-management).</span><span class="sxs-lookup"><span data-stu-id="1e663-127">For a list of scenarios supported by records management, see [Common scenarios for records management](get-started-with-records-management.md#common-scenarios-for-records-management).</span></span>
