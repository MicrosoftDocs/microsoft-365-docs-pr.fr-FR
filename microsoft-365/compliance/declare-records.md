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
ms.openlocfilehash: c8024cf08be2259ffa8b6747bebf4943e11e4d60
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46695246"
---
# <a name="declare-records-by-using-retention-labels"></a><span data-ttu-id="18486-103">Déclarer des enregistrements à l’aide d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="18486-103">Declare records by using retention labels</span></span>

><span data-ttu-id="18486-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="18486-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="18486-105">Vous utilisez les [étiquettes de rétention](retention.md#retention-labels) pour marquer du contenu sous la forme d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="18486-105">You use [retention labels](retention.md#retention-labels) to mark content as a record.</span></span> <span data-ttu-id="18486-106">Vous pouvez soit publier ces étiquettes pour permettre aux utilisateurs et aux administrateurs de les appliquer manuellement au contenu, soit appliquer automatiquement ces étiquettes au contenu que vous voulez marquer comme enregistrement.</span><span class="sxs-lookup"><span data-stu-id="18486-106">You can either publish those labels so that users and administrators can manually apply them to content, or auto-apply those labels to content that you want to mark as a record.</span></span>

## <a name="configuring-retention-labels-to-declare-records"></a><span data-ttu-id="18486-107">Configuration d’étiquettes de rétention pour déclarer des enregistrements</span><span class="sxs-lookup"><span data-stu-id="18486-107">Configuring retention labels to declare records</span></span>

<span data-ttu-id="18486-108">Lorsque vous créez une [étiquette de rétention](retention.md#retention-labels), sélectionnez l’option permettant de marquer le contenu en tant qu’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="18486-108">When you create a [retention label](retention.md#retention-labels), select the option to mark the content as a record.</span></span>

>[!NOTE] 
> <span data-ttu-id="18486-109">L’option de marquage du contenu en tant qu’enregistrement n’est pas disponible lorsque vous créez ou configurez des étiquettes de rétention depuis **Gouvernance des informations** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="18486-109">The option to mark the content as a record is not available when you create or configure retention labels from **Information Governance** in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="18486-110">Au lieu de cela, vous devez utiliser**Gestion des enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="18486-110">Instead, you must use **Records Management**.</span></span>

1. <span data-ttu-id="18486-111">Dans le [centre de conformité Microsoft 365](https://compliance.microsoft.com), accédez à **Gestion des enregistrements** \> **Plan de gestion de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="18486-111">In the [Microsoft 365 compliance center](https://compliance.microsoft.com), go to **Records Management** \> **File Plan**.</span></span> <span data-ttu-id="18486-112">Dans la page **plan de fichiers**, cliquez **créer une étiquette**.</span><span class="sxs-lookup"><span data-stu-id="18486-112">On the **File plan** page, select **Create a label**.</span></span>

2. <span data-ttu-id="18486-113">Sur la page **Paramètres d’étiquette** de l’Assistant, choisissez l’option permettant de classifier du contenu sous la forme d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="18486-113">On the **Label settings** page in the wizard, choose the option to classify content as a record.</span></span>
    
   ![Cliquez sur Utiliser l’étiquette pour classifier du contenu en tant que case à cocher d’Enregistrement](../media/recordversioning6.png)

3. <span data-ttu-id="18486-115">Appliquez l’étiquette de rétention aux documents SharePoint ou OneDrive et aux messages électroniques Exchange, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="18486-115">Apply the retention label to SharePoint or OneDrive documents and Exchange emails, as needed.</span></span> <span data-ttu-id="18486-116">Pour obtenir des instructions :</span><span class="sxs-lookup"><span data-stu-id="18486-116">For instructions:</span></span>
    
    - [<span data-ttu-id="18486-117">Créer des étiquettes de rétention et les appliquer dans les applications</span><span class="sxs-lookup"><span data-stu-id="18486-117">Create retention labels and apply them in apps</span></span>](create-apply-retention-labels.md)
    
    - [<span data-ttu-id="18486-118">Appliquer automatiquement une étiquette de rétention au contenu</span><span class="sxs-lookup"><span data-stu-id="18486-118">Apply a retention label to content automatically</span></span>](apply-retention-labels-automatically.md)

## <a name="applying-the-configured-retention-label-to-content"></a><span data-ttu-id="18486-119">Application de l’étiquette de rétention configurée au contenu</span><span class="sxs-lookup"><span data-stu-id="18486-119">Applying the configured retention label to content</span></span>

<span data-ttu-id="18486-120">Lorsque des étiquettes de rétention qui marquent le contenu en tant qu’enregistrement sont mises à la disposition des utilisateurs pour qu’ils les appliquent dans les applications :</span><span class="sxs-lookup"><span data-stu-id="18486-120">When retention labels that mark content as a record are made available for users to apply them in apps:</span></span>

- <span data-ttu-id="18486-121">Pour Exchange, tout utilisateur disposant d’un accès en écriture à la boîte aux lettres peut appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="18486-121">For Exchange, any user with write-access to the mailbox can apply these labels.</span></span> 
- <span data-ttu-id="18486-122">Pour SharePoint et OneDrive, tous les utilisateurs du groupe Membres par défaut (niveau d’autorisation Collaboration) peuvent appliquer ces étiquettes.</span><span class="sxs-lookup"><span data-stu-id="18486-122">For SharePoint and OneDrive, any user in the default Members group (the Contribute permission level) can apply these labels.</span></span>

<span data-ttu-id="18486-123">Exemple d’un document marqué en tant qu’enregistrement à l’aide d’une étiquette de rétention :</span><span class="sxs-lookup"><span data-stu-id="18486-123">Example of a document marked as record by using a retention label:</span></span>

![Volet Détails pour le document marqué comme enregistrement](../media/recordversioning7.png)

## <a name="next-steps"></a><span data-ttu-id="18486-125">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="18486-125">Next steps</span></span>

<span data-ttu-id="18486-126">Si vous devez mettre à jour des enregistrements, consultez [Utiliser le contrôle de version des enregistrements pour mettre à jour les enregistrements stockés dans SharePoint ou OneDrive](record-versioning.md).</span><span class="sxs-lookup"><span data-stu-id="18486-126">If you need to update documents that are records, see [Use record versioning to update records stored in SharePoint or OneDrive](record-versioning.md).</span></span>

<span data-ttu-id="18486-127">Si vous souhaitez en savoir plus sur la destruction des enregistrements, consultez [Disposition de contenu](disposition.md).</span><span class="sxs-lookup"><span data-stu-id="18486-127">To learn about the disposition of records, see [Disposing of content](disposition.md).</span></span>
