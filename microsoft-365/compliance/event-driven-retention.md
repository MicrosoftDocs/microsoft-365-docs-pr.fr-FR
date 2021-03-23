---
title: Débuter la rétention lorsqu’un événement se produit
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
- seo-marvel-may2020
- seo-marvel-jun2020
description: Dans une solution de gestion des enregistrements, vous pouvez généralement configurer une étiquette de rétention pour démarrer la période de rétention sur la base d’un événement que vous identifiez.
ms.openlocfilehash: ee828b6852440f5be07fdf34df2fb6a11253ae1c
ms.sourcegitcommit: 8998f70d3f7bd673f93f8d1cf12ce981b1b771c3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51034245"
---
# <a name="start-retention-when-an-event-occurs"></a><span data-ttu-id="3b85b-103">Débuter la rétention lorsqu’un événement se produit</span><span class="sxs-lookup"><span data-stu-id="3b85b-103">Start retention when an event occurs</span></span>

><span data-ttu-id="3b85b-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).*</span><span class="sxs-lookup"><span data-stu-id="3b85b-104">*[Microsoft 365 licensing guidance for security & compliance](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance).*</span></span>

<span data-ttu-id="3b85b-p101">Lorsque vous conservez du contenu, la période de rétention est souvent basée sur l’ancienneté du contenu. Par exemple, vous pouvez conserver des documents pendant sept ans à compter de leur création, puis les supprimer. Cependant, lorsque vous configurez [étiquettes de rétention](retention.md#retention-labels), vous pouvez baser une période de rétention sur l’occurrence d’un type spécifique d’événement. L’événement déclenche le début de la période de rétention, et les actions de rétention d’une étiquette sont appliquées sur tout le contenu portant l’étiquette en question pour ce type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-p101">When you retain content, the retention period is often based on the age of the content. For example, you might retain documents for seven years after they're created and then delete them. But when you configure [retention labels](retention.md#retention-labels), you can also base a retention period on when a specific type of event occurs. The event triggers the start of the retention period, and all content with a retention label applied for that type of event get the label's retention actions enforced on them.</span></span>
  
<span data-ttu-id="3b85b-109">Exemples d'utilisation de la rétention basée sur les événements :</span><span class="sxs-lookup"><span data-stu-id="3b85b-109">Examples for using event-based retention:</span></span>
  
- <span data-ttu-id="3b85b-110">**Employés quittant l'organisation** Supposons que les enregistrements d’un employé doivent être conservés 10 ans à compter de son départ de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3b85b-110">**Employees leaving the organization** Suppose that employee records must be retained for 10 years from the time an employee leaves the organization.</span></span> <span data-ttu-id="3b85b-111">Une fois les 10 ans écoulés, tous les documents concernant l’embauche, les résultats et le départ de cet employé doivent être supprimés.</span><span class="sxs-lookup"><span data-stu-id="3b85b-111">After 10 years elapse, all documents related to the hiring, performance, and termination of that employee must be disposed.</span></span> <span data-ttu-id="3b85b-112">L’événement qui déclenche la période de rétention de 10 ans est le départ de l’employé de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3b85b-112">The event that triggers the 10-year retention period is the employee leaving the organization.</span></span> 
    
- <span data-ttu-id="3b85b-113">**Expiration du contrat** Supposons que tous les enregistrements liés aux contrats doivent être conservés pendant cinq ans après l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="3b85b-113">**Contract expiration** Suppose that all records related to contracts must be retained for five years from the time the contract expires.</span></span> <span data-ttu-id="3b85b-114">L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="3b85b-114">The event that triggers the five-year retention period is the expiration of the contract.</span></span> 
    
- <span data-ttu-id="3b85b-p104">**Durée de vie des produits** Votre organisation a peut-être des exigences de rétention liées à la dernière date de fabrication de produits pour le contenu tel que des spécifications techniques. Dans ce cas, la dernière date de fabrication est l’événement qui déclenche la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-p104">**Product lifetime** Your organization might have retention requirements related to the last manufacturing date of products for content such as technical specifications. In this case, the last manufacturing date is the event that triggers the retention period.</span></span> 
    
<span data-ttu-id="3b85b-p105">La rétention basée sur les événements est généralement utilisée dans le cadre d'un processus de gestion des documents. Cela signifie que :</span><span class="sxs-lookup"><span data-stu-id="3b85b-p105">Event-based retention is typically used as part of a records-management process. This means that:</span></span>
  
- <span data-ttu-id="3b85b-119">Les étiquettes de rétention basées sur les événements marquent aussi généralement les articles comme un enregistrement, dans le cadre d'une solution de gestion des documents.</span><span class="sxs-lookup"><span data-stu-id="3b85b-119">Retention labels based on events also usually mark items as a record, as a part of a records management solution.</span></span> <span data-ttu-id="3b85b-120">Pour plus d’informations, consultez [En savoir plus sur la gestion des enregistrements](records-management.md).</span><span class="sxs-lookup"><span data-stu-id="3b85b-120">For more information, see [Learn about records management](records-management.md).</span></span>

- <span data-ttu-id="3b85b-121">Un document qui a été déclaré comme un enregistrement mais dont l'événement déclencheur n'a pas encore eu lieu est conservé indéfiniment (les enregistrements ne peuvent pas être supprimés définitivement), jusqu'à ce qu'un événement déclenche la période de rétention de ce document.</span><span class="sxs-lookup"><span data-stu-id="3b85b-121">A document that's been declared a record but whose event trigger has not yet happened is retained indefinitely (records can't be permanently deleted), until an event triggers that document's retention period.</span></span>
    
- <span data-ttu-id="3b85b-122">Les étiquettes de rétention basées sur des événements déclenchent généralement une révision avant destruction à la fin de la période de rétention, ce qui permet à un gestionnaire d’enregistrements de manuellement passer en revue puis supprimer le contenu.</span><span class="sxs-lookup"><span data-stu-id="3b85b-122">Retention labels based on events usually trigger a disposition review at the end of the retention period, so that a records manager can manually review and dispose of the content.</span></span> <span data-ttu-id="3b85b-123">Si vous souhaitez en savoir plus, consultez la page [Destruction de contenu](disposition.md).</span><span class="sxs-lookup"><span data-stu-id="3b85b-123">For more information, see [Disposition of content](disposition.md).</span></span>
    

<span data-ttu-id="3b85b-124">Les étiquettes de rétention basées sur un événement possèdent les mêmes fonctionnalités que les étiquettes de rétention dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3b85b-124">A retention label based on an event has the same capabilities as any retention label in Microsoft 365.</span></span> <span data-ttu-id="3b85b-125">Pour plus d’informations, voir [En savoir plus sur les stratégies et les étiquettes de rétention](retention.md).</span><span class="sxs-lookup"><span data-stu-id="3b85b-125">For more information, see [Learn about retention policies and retention labels](retention.md).</span></span>

## <a name="understanding-the-relationship-between-event-types-labels-events-and-asset-ids"></a><span data-ttu-id="3b85b-126">Compréhension de la relation entre les types d’événements, les étiquettes, les événements et les ID d’élément</span><span class="sxs-lookup"><span data-stu-id="3b85b-126">Understanding the relationship between event types, labels, events, and asset IDs</span></span>

<span data-ttu-id="3b85b-127">Pour utiliser avec succès la rétention basée sur les événements, il est important de comprendre la relation entre les types d'événements, les étiquettes de rétention, les événements et les identifications d'actifs comme l'illustrent les diagrammes et l'explication qui suit :</span><span class="sxs-lookup"><span data-stu-id="3b85b-127">To successfully use event-based retention, it's important to understand the relationship between event types, retention labels, events, and asset IDs as illustrated in the diagrams and the explanation that follows:</span></span> 
  
![Diagramme 1 de 2 : Type d'événement, étiquettes, événements et identification des actifs](../media/a5141a6b-61ca-4a60-9ab0-24e6bb45bbdb.png)
  
![Diagramme 2 de 2 : Type d'événement, étiquettes, événements et identification des actifs](../media/ce89a91f-49aa-4b5a-933c-ac3a13dccd5d.png)
  
1. <span data-ttu-id="3b85b-130">Vous créez des étiquettes de rétention pour différents types de contenu et vous les associez à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-130">You create retention labels for different types of content and then associate them with a type of event.</span></span> <span data-ttu-id="3b85b-131">Par exemple, les étiquettes pour différents types de fichiers et d’enregistrements de produit sont associées à un type d’événement nommé Durée de vie des produits, car ces enregistrements doivent être conservés pendant 10 ans à compter de la fin de vie du produit.</span><span class="sxs-lookup"><span data-stu-id="3b85b-131">For example, retention labels for different types of product files and records are associated with an event type named Product Lifetime because those records must be retained for 10 years from the time the product reaches its end of life.</span></span>
    
2. <span data-ttu-id="3b85b-132">Les utilisateurs (généralement les gestionnaires de documents) appliquent ces étiquettes de rétention au contenu et (pour les documents dans SharePoint et OneDrive) saisissent un identifiant d'actif pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="3b85b-132">Users (typically records managers) apply those retention labels to content and (for documents in SharePoint and OneDrive) enter an asset ID for each item.</span></span> <span data-ttu-id="3b85b-133">Dans cet exemple, l’ID d’actif est un nom de produit ou un code utilisé par l’organisation.</span><span class="sxs-lookup"><span data-stu-id="3b85b-133">In this example, the asset ID is a product name or code used by the organization.</span></span> <span data-ttu-id="3b85b-134">Ensuite, une étiquette de rétention est attribuée aux enregistrements de chaque produit, et chaque enregistrement possède une propriété qui contient un numéro d'identification de l'actif.</span><span class="sxs-lookup"><span data-stu-id="3b85b-134">Then, each product's records are assigned a retention label, and each record has a property that contains an asset ID.</span></span> <span data-ttu-id="3b85b-135">Le diagramme représente **l'ensemble du contenu** de tous les enregistrements de produits dans une organisation, et chaque article porte l'ID de l'actif du produit dont il est l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-135">The diagram represents **all the content** for all product records in an organization, and each item bears the asset ID of the product whose record it is.</span></span> 
    
3. <span data-ttu-id="3b85b-p111">La fin de vie d’un produit est un « événement ». La durée de vie de ce produit est un « type d’événement ». Lorsqu’un événement (« fin de vie ») se produit pour un type d’événement (« durée de vie du produit »), vous devez créer un événement qui spécifie :</span><span class="sxs-lookup"><span data-stu-id="3b85b-p111">Product Lifetime is the event type; a specific product reaching end of life is an event. When an event of that event type occurs—in this case, when a product reaches its end of life—you create an event that specifies:</span></span>
    
   - <span data-ttu-id="3b85b-138">Un ID d’élément (pour les documents SharePoint et OneDrive).</span><span class="sxs-lookup"><span data-stu-id="3b85b-138">An asset ID (for SharePoint and OneDrive documents)</span></span>
    
   - <span data-ttu-id="3b85b-p112">Mots-clés (pour les articles d'échange). Dans cet exemple, l'organisation utilise un code produit dans les messages contenant des fiches produits, de sorte que le mot clé pour les articles Exchange est fonctionnellement le même que l'ID d'actif pour les documents SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="3b85b-p112">Keywords (for Exchange items). In this example, the organization uses a product code in messages containing product records, so the keyword for Exchange items is functionally the same as the asset ID for SharePoint and OneDrive documents.</span></span>
    
   - <span data-ttu-id="3b85b-p113">La date à laquelle l’événement s'est produit. Cette date est utilisée comme point de départ de la période de rétention. Cette date peut être la date actuelle, passée ou une date future.</span><span class="sxs-lookup"><span data-stu-id="3b85b-p113">The date when the event occurred. This date is used as the start of the retention period. This date can be the current, a past, or a future date.</span></span>

4. <span data-ttu-id="3b85b-144">Lorsque vous avez créé un événement, sa date est synchronisée avec tout le contenu portant l’étiquette de rétention du type d’événement correspondant et contenant l’ID d’élément ou le mot clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="3b85b-144">After you create an event, that event date is synchronized to all the content that has a retention label of that event type and that contains the specified asset ID or keyword.</span></span> <span data-ttu-id="3b85b-145">Comme pour toute étiquette de rétention, cette synchronisation peut prendre jusqu’à 7 jours.</span><span class="sxs-lookup"><span data-stu-id="3b85b-145">Like any retention label, this synchronization can take up to seven days.</span></span> <span data-ttu-id="3b85b-146">Dans le diagramme précédent, la période de rétention de tous les éléments encerclés en rouge est déclenchée par cet événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-146">In the previous diagram, all the items circled in red have their retention period triggered by this event.</span></span> <span data-ttu-id="3b85b-147">En d’autres termes, lorsque ce produit atteint sa fin de vie, cet événement déclenche la période de rétention pour les enregistrements de ce produit.</span><span class="sxs-lookup"><span data-stu-id="3b85b-147">In other words, when this product reaches its end of life, that event triggers the retention period for that product's records.</span></span>

<span data-ttu-id="3b85b-148">Il est important de comprendre que si vous ne spécifiez pas d'identifiant ou de mots clés pour un événement, **tout contenu** avec une étiquette de rétention de ce type d'événement aura sa période de rétention déclenchée par l'événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-148">It's important to understand that if you don't specify an asset ID or keywords for an event, **all content** with a retention label of that event type will have its retention period triggered by the event.</span></span> <span data-ttu-id="3b85b-149">Cela signifie que, dans le diagramme précédent, tout le contenu commencera à être conservé.</span><span class="sxs-lookup"><span data-stu-id="3b85b-149">This means that in the previous diagram, all content would start being retained.</span></span> <span data-ttu-id="3b85b-150">Ce n’est peut-être pas ce que vous voulez faire.</span><span class="sxs-lookup"><span data-stu-id="3b85b-150">This might not be what you intend.</span></span>

<span data-ttu-id="3b85b-151">Enfin, rappelez-vous que chaque étiquette de rétention possède ses propres paramètres de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-151">Finally, remember that each retention label has its own retention settings.</span></span> <span data-ttu-id="3b85b-152">Dans cet exemple, ils indiquent tous 10 ans, mais un événement peut très bien déclencher des étiquettes de rétention dont chacune possède sa propre période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-152">In this example, they all specify 10 years, but it's possible for an event to trigger retention labels where each label has a different retention period.</span></span>
  
## <a name="how-to-set-up-event-driven-retention"></a><span data-ttu-id="3b85b-153">Configuration des rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="3b85b-153">How to set up event-driven retention</span></span>

<span data-ttu-id="3b85b-154">Flux de travail général pour la rétention basée sur un événement :</span><span class="sxs-lookup"><span data-stu-id="3b85b-154">High-level workflow for event-driven retention:</span></span>
  
![Diagramme du flux de travail de la configuration des rétentions basées sur des événements](../media/event-based-retention-process.png)
  
> [!TIP]
> <span data-ttu-id="3b85b-156">Consultez [Gérer le cycle de vie des documents sauvegardés sur SharePoint avec des étiquettes de rétention](auto-apply-retention-labels-scenario.md) pour un scénario détaillé sur l’utilisation de propriétés gérées dans SharePoint afin d'appliquer automatiquement des étiquettes de rétention et exécuter la rétention basée sur un événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-156">See [Use retention labels to manage the lifecycle of documents stored in SharePoint](auto-apply-retention-labels-scenario.md) for a detailed scenario about using managed properties in SharePoint to auto-apply retention labels and implement event-driven retention.</span></span>

### <a name="step-1-create-a-label-whose-retention-period-is-based-on-an-event"></a><span data-ttu-id="3b85b-157">Étape 1 : créer une étiquette dont la période de rétention est basée sur des événements</span><span class="sxs-lookup"><span data-stu-id="3b85b-157">Step 1: Create a label whose retention period is based on an event</span></span>

<span data-ttu-id="3b85b-158">Pour créer et configurer votre étiquette de rétention, utilisez les instructions pour [Créer des étiquettes de rétention](./create-apply-retention-labels.md#step-1-create-retention-labels).</span><span class="sxs-lookup"><span data-stu-id="3b85b-158">To create and configure your retention label, see the instructions for [Create retention labels](./create-apply-retention-labels.md#step-1-create-retention-labels).</span></span> <span data-ttu-id="3b85b-159">Mais pour ce qui est de la rétention basée sur un événement, sur la **page Définir les paramètres de  rétention** de l'assistant Créer une étiquette de rétention, après **Démarrer la période de rétention basée sur**, sélectionnez un des types d'événements par défaut dans la liste déroulante, ou créez le vôtre en sélectionnant **Créer un nouveau type d'événement**:</span><span class="sxs-lookup"><span data-stu-id="3b85b-159">But specific to event-based retention, on the **Define retention settings** page of the Create retention label wizard, after **Start the retention period based on**, select one of the default event types from the dropdown list, or create your own by selecting **Create new event type**:</span></span>

![Créer un nouveau type d’événement pour une étiquette de rétention](../media/SPRetention6.png)

<span data-ttu-id="3b85b-161">Un type d’événement est simplement une description générale d’un événement auquel vous voulez associer une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-161">An event type is simply a general description of an event that you want to associate with a retention label.</span></span>

<span data-ttu-id="3b85b-162">Les types d’événements par défaut ont **(type d’événement)** après leur nom dans la liste déroulante afin de faciliter l’identification, et vous pouvez également afficher et créer un type d’événement à partir de la **gestion des enregistrements** > **Événements** > **gérer les types d’événements**.</span><span class="sxs-lookup"><span data-stu-id="3b85b-162">The default event types have **(event type)** after their name in the dropdown list for easier identification, and you can also see and create event type from the **Records management** > **Events** tab > **Manage event types**.</span></span>

<span data-ttu-id="3b85b-163">La rétention basée sur un événement nécessite des paramètres de rétention qui :</span><span class="sxs-lookup"><span data-stu-id="3b85b-163">Event-based retention requires retention settings that:</span></span>
  
- <span data-ttu-id="3b85b-164">Conservent le contenu.</span><span class="sxs-lookup"><span data-stu-id="3b85b-164">Retain the content.</span></span>
    
- <span data-ttu-id="3b85b-165">suppriment automatiquement le contenu ou déclenchent une révision de destruction à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-165">Delete the content automatically or trigger a disposition review at the end of the retention period.</span></span>
  
<span data-ttu-id="3b85b-166">La rétention basée sur un événement est généralement utilisée pour les contenus classés sous la forme d’un enregistrement, c’est le moment idéal pour vérifier si vous avez également besoin de sélectionner l’option qui marque du contenu comme [enregistrement](records-management.md#records).</span><span class="sxs-lookup"><span data-stu-id="3b85b-166">Event-based retention is typically used for content that's declared a record, so this is a good time to check whether you also need to select the option that marks content as a [record](records-management.md#records).</span></span>

<span data-ttu-id="3b85b-167">Si vous utilisez un type d’événement existant plutôt que de créer un nouveau type d’événement, passez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="3b85b-167">If you're using an existing event type rather than creating a new event type, skip to step 3.</span></span>

> [!NOTE]
> <span data-ttu-id="3b85b-168">Une fois que vous avez sélectionné un type d’événement et enregistré l’étiquette de rétention, le type d’événement ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="3b85b-168">After you choose an event type and save the retention label, the event type cannot be changed.</span></span>

### <a name="step-2-create-a-new-event-type-for-your-label"></a><span data-ttu-id="3b85b-169">Étape 2 : Créer un nouveau type d’événement pour votre étiquette</span><span class="sxs-lookup"><span data-stu-id="3b85b-169">Step 2: Create a new event type for your label</span></span>

<span data-ttu-id="3b85b-170">Pour les paramètres de rétention, si vous avez sélectionné **Créer un nouveau type d’événement**, entrez un nom et une description pour votre type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-170">For the retention settings, if you selected **Create new event type**, enter a name and description for your event type.</span></span> <span data-ttu-id="3b85b-171">Sélectionnez ensuite **Suivant**, **Envoyer**, puis **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="3b85b-171">Then select **Next**, **Submit**, and **Done**.</span></span>

<span data-ttu-id="3b85b-172">Une fois de retour dans la page **Définir les paramètres de rétention**, pour **Démarrer la période de rétention sur la base de**, utilisez la liste déroulante pour sélectionner le type d’événement que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="3b85b-172">Back on the **Define retention settings** page, for **Start the retention period based on**, use the dropdown list to select the event type that you created.</span></span>

  
### <a name="step-3-publish-or-auto-apply-the-event-based-retention-labels"></a><span data-ttu-id="3b85b-173">Étape 3 : publier ou appliquer automatiquement les étiquettes de rétention basées sur les événements</span><span class="sxs-lookup"><span data-stu-id="3b85b-173">Step 3: Publish or auto-apply the event-based retention labels</span></span>

<span data-ttu-id="3b85b-174">Comme pour n’importe quelle étiquette de rétention, vous devez publier ou appliquer automatiquement une étiquette basée sur un événement, de sorte qu’elle soit appliquée au contenu de façon manuelle ou automatique :</span><span class="sxs-lookup"><span data-stu-id="3b85b-174">Just like any retention label, you need to publish or auto-apply an event-based label, for it to be manually or automatically applied to content:</span></span>
- [<span data-ttu-id="3b85b-175">Créer des étiquettes de rétention et les appliquer dans les applications</span><span class="sxs-lookup"><span data-stu-id="3b85b-175">Create retention labels and apply them in apps</span></span>](create-apply-retention-labels.md)
- [<span data-ttu-id="3b85b-176">Appliquer automatiquement une étiquette de rétention au contenu</span><span class="sxs-lookup"><span data-stu-id="3b85b-176">Apply a retention label to content automatically</span></span>](apply-retention-labels-automatically.md)

### <a name="step-4-enter-an-asset-id"></a><span data-ttu-id="3b85b-177">Étape 4 : saisissez un ID d’élément</span><span class="sxs-lookup"><span data-stu-id="3b85b-177">Step 4: Enter an asset ID</span></span>

<span data-ttu-id="3b85b-178">Une fois qu’une étiquette basée sur un événement a été appliquée au contenu, vous pouvez entrer un ID d’élément pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="3b85b-178">After an event-based label is applied to content, you can enter an asset ID for each item.</span></span> <span data-ttu-id="3b85b-179">Par exemple, votre organisation peut utiliser :</span><span class="sxs-lookup"><span data-stu-id="3b85b-179">For example, your organization might use:</span></span>
  
- <span data-ttu-id="3b85b-180">Des codes de produit que vous pouvez utiliser pour conserver le contenu relatif à un produit spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b85b-180">Product codes that you can use to retain content for only a specific product.</span></span>
    
- <span data-ttu-id="3b85b-181">Des codes de projet que vous pouvez utiliser pour conserver le contenu relatif à un projet spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b85b-181">Project codes that you can use to retain content for only a specific project.</span></span>
    
- <span data-ttu-id="3b85b-182">ID d’employé à utiliser pour conserver uniquement le contenu d’une personne spécifique.</span><span class="sxs-lookup"><span data-stu-id="3b85b-182">Employee IDs that you can use to retain content for only a specific person.</span></span>
    
<span data-ttu-id="3b85b-183">L’ID d’élément constitue simplement une autre propriété de document qui est disponible dans SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="3b85b-183">Asset ID is simply another document property that's available in SharePoint and OneDrive.</span></span> <span data-ttu-id="3b85b-184">Votre organisation utilise peut-être déjà d’autres ID et propriétés de document pour classer le contenu.</span><span class="sxs-lookup"><span data-stu-id="3b85b-184">Your organization might already use other document properties and IDs to classify content.</span></span> <span data-ttu-id="3b85b-185">Le cas échéant, vous pouvez également utiliser ces propriétés et valeurs lorsque vous créez un événement (voir l’étape 6, plus bas).</span><span class="sxs-lookup"><span data-stu-id="3b85b-185">If so, you can also use those properties and values when you create an event—see step 6 that follows.</span></span> <span data-ttu-id="3b85b-186">L’essentiel est que vous utilisez une combinaison *propriété:valeur* dans les propriétés du document pour associer cet élément à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-186">The important point is that you must use some *property:value* combination in the document properties to associate that item with an event type.</span></span>
  
![Zone de texte pour saisir un ID d’élément](../media/6d31628e-7162-4370-a8d7-de704aafa350.png)
  
### <a name="step-5-create-an-event"></a><span data-ttu-id="3b85b-188">Étape 5 : créer un événement</span><span class="sxs-lookup"><span data-stu-id="3b85b-188">Step 5: Create an event</span></span>

<span data-ttu-id="3b85b-189">Lorsqu’une instance précise de ce type d’événement se produit (par exemple, un produit arrive en fin de vie), accédez à la page **Gestions des enregistrements** > **Événements** dans le Centre de conformité Microsoft 365, et sélectionnez **+ Créer** pour créer un événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-189">When a particular instance of that event type occurs, such as a product reaches its end of life, go to the **Records management** > **Events** page in the Microsoft 365 compliance center, and select **+ Create** to create an event.</span></span> <span data-ttu-id="3b85b-190">Vous devez déclencher un événement en le créant en cliquant ici..</span><span class="sxs-lookup"><span data-stu-id="3b85b-190">You trigger the event by creating it, here.</span></span>

![Créer un événement pour déclencher le démarrage de la rétention pour les étiquettes de rétention basée sur les événements](../media/create-event-records-management.png)

<span data-ttu-id="3b85b-192">Jusqu’à un million d’événements sont pris en charge par client.</span><span class="sxs-lookup"><span data-stu-id="3b85b-192">Up to one million events are supported per tenant.</span></span>

### <a name="step-6-choose-the-same-event-type-used-by-the-label-in-step-2"></a><span data-ttu-id="3b85b-193">Étape 6 : Choisir le même type d’événement utilisé par l’étiquette à l’étape 2</span><span class="sxs-lookup"><span data-stu-id="3b85b-193">Step 6: Choose the same event type used by the label in step 2</span></span>

<span data-ttu-id="3b85b-194">Lorsque vous créez l’événement, choisissez le même type d'événement que celui spécifié dans les paramètres de l’étiquette de rétention à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="3b85b-194">When you create the event, choose the same event type specified in the retention label settings in step 2.</span></span> <span data-ttu-id="3b85b-195">Par exemple, si vous avez sélectionné **Durée de vie du produit** comme type d'événement pour les paramètres de l’étiquette, sélectionnez **Durée de vie du produit** lorsque vous créez l'événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-195">For example, if you selected **Product Lifetime** as your event type for the label settings, select **Product Lifetime** when you create the event.</span></span> <span data-ttu-id="3b85b-196">La période de rétention sera déclenchée uniquement pour le contenu auquel sont appliquées des étiquettes de rétention de ce type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-196">Only content with retention labels applied to it of that event type will have its retention period triggered.</span></span>

![Option dans les paramètres d’événement permettant de choisir un type d’événement](../media/choose-event-type-records-management.png)

<span data-ttu-id="3b85b-198">Par ailleurs, si vous devez créer un événement pour plusieurs étiquettes de rétention qui ont différents types d'événements, sélectionnez l'option **Choisir les étiquettes existantes**.</span><span class="sxs-lookup"><span data-stu-id="3b85b-198">Alternatively, if you need to create an event for multiple retention labels that have different event types, select the **Choose Existing Labels** option.</span></span> <span data-ttu-id="3b85b-199">Sélectionnez ensuite les étiquettes configurées pour les types d’événements que vous voulez associer à cet événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-199">Then, select the labels that are configured for the event types you want to associate with this event.</span></span>

### <a name="step-7-enter-keywords-or-an-asset-id"></a><span data-ttu-id="3b85b-200">Étape 7 : saisir des mots clés ou un ID d’élément</span><span class="sxs-lookup"><span data-stu-id="3b85b-200">Step 7: Enter keywords or an asset ID</span></span>

<span data-ttu-id="3b85b-201">Vous réduisez à présent l’étendue du contenu en spécifiant des ID d’élément pour le contenu SharePoint et OneDrive ou des mots clés pour le contenu Exchange.</span><span class="sxs-lookup"><span data-stu-id="3b85b-201">Now you narrow the scope of the content by specifying asset IDs for SharePoint and OneDrive content, or keywords for Exchange content.</span></span> <span data-ttu-id="3b85b-202">Pour les ID d’élément, la rétention sera appliquée uniquement au contenu comportant la paire *propriété:valeur* spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3b85b-202">For asset IDs, retention will be enforced only on content with the specified *property:value* pair.</span></span> <span data-ttu-id="3b85b-203">Si vous n’entrez pas d’ID d’élément, tout le contenu portant des étiquettes de ce type d’événement se voit appliquer la même date de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-203">If an asset ID is not entered, all content with labels of that event type get the same retention date applied to them.</span></span>

<span data-ttu-id="3b85b-204">Par exemple : Si vous utilisez la propriété ID d’élément, vous entrez `ComplianceAssetID:<value>` dans la zone réservée aux ID d’élément illustrée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3b85b-204">For example: If you're using the Asset ID property, enter `ComplianceAssetID:<value>` in the box for asset IDs shown below.</span></span>
  
<span data-ttu-id="3b85b-205">Votre organisation a peut-être appliqué d’autres propriétés et ID aux documents associés à ce type d’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-205">Your organization might have applied other properties and IDs to the documents related to this event type.</span></span> <span data-ttu-id="3b85b-206">Par exemple, si vous avez besoin de détecter les enregistrements d’un produit spécifique, l’ID peut être une combinaison de la propriété personnalisée ProductID et de la valeur « XYZ ».</span><span class="sxs-lookup"><span data-stu-id="3b85b-206">For example, if you need to detect a specific product's records, the ID might be a combination of your custom property ProductID and the value "XYZ".</span></span> <span data-ttu-id="3b85b-207">Vous entrerez dans ce cas `ProductID:XYZ` dans la zone réservée aux ID d’élément illustrée dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="3b85b-207">In this case, you'd enter `ProductID:XYZ` in the box for asset IDs shown in the following picture.</span></span>
  
<span data-ttu-id="3b85b-208">Pour les éléments Exchange, utilisez des mots clés.</span><span class="sxs-lookup"><span data-stu-id="3b85b-208">For Exchange items, use keywords.</span></span> <span data-ttu-id="3b85b-209">Vous pouvez utiliser une requête en utilisant des opérateurs de recherche tels que ET, OU et NON.</span><span class="sxs-lookup"><span data-stu-id="3b85b-209">You can use a query by using search operators such as AND, OR, and NOT.</span></span> <span data-ttu-id="3b85b-210">Si vous souhaitez en savoir plus, consultez la page [Requêtes par mots-clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="3b85b-210">For more information, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
<span data-ttu-id="3b85b-211">Enfin, sélectionnez la date à laquelle l’événement s’est produit. cette date est utilisée comme début de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-211">Finally, choose the date when the event occurred; this date is used as the start of the retention period.</span></span> <span data-ttu-id="3b85b-212">Une fois que vous avez créé un événement, la date de l’événement est synchronisée avec tout le contenu avec une étiquette de rétention de ce type d’événement, de l’ID d’actif et des mots clés.</span><span class="sxs-lookup"><span data-stu-id="3b85b-212">After you create an event, that event date is synchronized to all the content with a retention label of that event type, asset ID, and keywords.</span></span> <span data-ttu-id="3b85b-213">Comme pour toute étiquette de rétention, cette synchronisation peut prendre jusqu’à sept jours.</span><span class="sxs-lookup"><span data-stu-id="3b85b-213">As with any retention label, this synchronization can take up to seven days.</span></span>
  
![Page Paramètres des événements](../media/40d3c9db-f624-49a5-b38a-d16bcce20231.png)

<span data-ttu-id="3b85b-215">Une fois que vous avez créé un événement, les paramètres de rétention prennent effet pour le contenu déjà étiqueté et indexé.</span><span class="sxs-lookup"><span data-stu-id="3b85b-215">After creating an event, the retention settings take effect for the content that's already labeled and indexed.</span></span> <span data-ttu-id="3b85b-216">Si l’étiquette de rétention est ajoutée au nouveau contenu une fois l’événement créé, vous devez créer un événement avec les mêmes détails.</span><span class="sxs-lookup"><span data-stu-id="3b85b-216">If the retention label is added to new content after the event is created, you must create a new event with the same details.</span></span>

<span data-ttu-id="3b85b-217">La suppression d’un événement n’annule pas les paramètres de rétention qui sont désormais appliqués pour le contenu qui est déjà étiqueté.</span><span class="sxs-lookup"><span data-stu-id="3b85b-217">Deleting an event doesn't cancel the retention settings that are now in effect for the content that's already labeled.</span></span> <span data-ttu-id="3b85b-218">Pour ce faire, créez un événement avec les mêmes détails, mais laissez la date vide.</span><span class="sxs-lookup"><span data-stu-id="3b85b-218">To do that, create a new event with the same details, but leave the date blank.</span></span> 

## <a name="use-content-search-to-find-all-content-with-a-specific-label-or-asset-id"></a><span data-ttu-id="3b85b-219">Utilisation de la recherche de contenu pour rechercher tout le contenu portant une étiquette ou un ID d’élément spécifique</span><span class="sxs-lookup"><span data-stu-id="3b85b-219">Use Content Search to find all content with a specific label or asset ID</span></span>

<span data-ttu-id="3b85b-220">Une fois que les étiquettes de rétention sont attribuées au contenu, vous pouvez utiliser la recherche de contenu pour rechercher tout le contenu classé avec une étiquette de rétention spécifique ou qui contient un ID d’élément spécifique :</span><span class="sxs-lookup"><span data-stu-id="3b85b-220">After retention labels are assigned to content, you can use content search to find all content that's classified with a specific retention label or that contains a specific asset ID:</span></span>
  
- <span data-ttu-id="3b85b-221">Pour trouver tout le contenu portant une étiquette de rétention spécifique, sélectionnez la condition **Étiquette de rétention**, puis saisissez le nom d’étiquette en partie ou en intégralité et utilisez un caractère générique.</span><span class="sxs-lookup"><span data-stu-id="3b85b-221">To find all content with a specific retention label, choose the **Retention label** condition, and then enter the complete label name or part of the label name and use a wildcard.</span></span> 
    
- <span data-ttu-id="3b85b-222">Pour trouver tout le contenu portant un ID d’élément spécifique, saisissez la propriété **ComplianceAssetID** et une valeur, telle que `ComplianceAssetID:<value>`.</span><span class="sxs-lookup"><span data-stu-id="3b85b-222">To find all content with a specific asset ID, enter the **ComplianceAssetID** property and a value, using the format `ComplianceAssetID:<value>`.</span></span> 
    
<span data-ttu-id="3b85b-223">Si vous souhaitez en savoir plus, consultez la page [Requêtes par mots-clés et conditions de recherche pour la recherche de contenu](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="3b85b-223">For more information, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>

## <a name="automate-events-by-using-powershell"></a><span data-ttu-id="3b85b-224">Automatisation des événements à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b85b-224">Automate events by using PowerShell</span></span>

<span data-ttu-id="3b85b-225">Vous pouvez utiliser un script PowerShell pour automatiser une rétention basée sur un événement à partir de vos applications métier.</span><span class="sxs-lookup"><span data-stu-id="3b85b-225">You can use a PowerShell script to automate event-based retention from your business applications.</span></span> <span data-ttu-id="3b85b-226">Les cmdlets PowerShell disponibles pour les rétentions basées sur des événements :</span><span class="sxs-lookup"><span data-stu-id="3b85b-226">The PowerShell cmdlets available for event-based retention:</span></span>
  
- [<span data-ttu-id="3b85b-227">Get-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="3b85b-227">Get-ComplianceRetentionEventType</span></span>](/powershell/module/exchange/get-complianceretentioneventtype)
    
- [<span data-ttu-id="3b85b-228">New-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="3b85b-228">New-ComplianceRetentionEventType</span></span>](/powershell/module/exchange/new-complianceretentioneventtype)
    
- [<span data-ttu-id="3b85b-229">Remove-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="3b85b-229">Remove-ComplianceRetentionEventType</span></span>](/powershell/module/exchange/remove-complianceretentioneventtype)
    
- [<span data-ttu-id="3b85b-230">Set-ComplianceRetentionEventType</span><span class="sxs-lookup"><span data-stu-id="3b85b-230">Set-ComplianceRetentionEventType</span></span>](/powershell/module/exchange/set-complianceretentioneventtype)
    
- [<span data-ttu-id="3b85b-231">Get-ComplianceRetentionEvent</span><span class="sxs-lookup"><span data-stu-id="3b85b-231">Get-ComplianceRetentionEvent</span></span>](/powershell/module/exchange/get-complianceretentionevent)
    
- [<span data-ttu-id="3b85b-232">New-ComplianceRetentionEvent</span><span class="sxs-lookup"><span data-stu-id="3b85b-232">New-ComplianceRetentionEvent</span></span>](/powershell/module/exchange/new-complianceretentionevent)
    

## <a name="automate-events-by-using-a-rest-api"></a><span data-ttu-id="3b85b-233">Automatisation des événements à l’aide de l’API REST</span><span class="sxs-lookup"><span data-stu-id="3b85b-233">Automate events by using a REST API</span></span>

<span data-ttu-id="3b85b-234">Vous pouvez utiliser une API REST pour créer automatiquement les événements qui déclenchent la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-234">You can use a REST API to automatically create the events that trigger the start of the retention time.</span></span>

<span data-ttu-id="3b85b-235">Une API REST est un point de terminaison de service prenant en charge les ensembles d’opérations HTTP (méthodes) qui fournissent les droits d’accès de création/récupération/mise à jour/suppression aux ressources du service.</span><span class="sxs-lookup"><span data-stu-id="3b85b-235">A REST API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources.</span></span> <span data-ttu-id="3b85b-236">Si vous souhaitez en savoir plus, veuillez consulter la section [Composants d’une demande/réponse d’API REST](/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span><span class="sxs-lookup"><span data-stu-id="3b85b-236">For more information, see [Components of a REST API request/response](/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span></span> <span data-ttu-id="3b85b-237">L’API REST de Microsoft 365 vous permet de créer et d’extraire des événements à l’aide des méthodes POST et GET.</span><span class="sxs-lookup"><span data-stu-id="3b85b-237">By using the Microsoft 365 REST API, events can be created and retrieved using the POST and GET methods.</span></span>

<span data-ttu-id="3b85b-238">Vous pouvez utiliser l’API REST de deux manières :</span><span class="sxs-lookup"><span data-stu-id="3b85b-238">There are two options for using the REST API:</span></span>

- <span data-ttu-id="3b85b-239">Avec **Microsoft Power Automate ou une application similaire** pour déclencher automatiquement l’occurrence d’un événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-239">**Microsoft Power Automate or a similar application** to trigger the occurrence of an event automatically.</span></span> <span data-ttu-id="3b85b-240">Microsoft Power Automate est un orchestrateur permettant de se connecter à d'autres systèmes, vous n'avez donc pas besoin d'écrire une solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3b85b-240">Microsoft Power Automate is an orchestrator for connecting to other systems, so you don't need to write a custom solution.</span></span> <span data-ttu-id="3b85b-241">Si vous souhaitez en savoir plus, veuillez consulter le [site web de Power automate](https://flow.microsoft.com/fr-FR/).</span><span class="sxs-lookup"><span data-stu-id="3b85b-241">For more information, see the [Power Automate website](https://flow.microsoft.com/fr-FR/).</span></span>

- <span data-ttu-id="3b85b-242">Avec **PowerShell ou un client HTTP pour appeler l’API REST** pour créer des événements à l’aide de PowerShell (version 6 ou ultérieure), dans le cadre d’une solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="3b85b-242">**PowerShell or an HTTP client to call the REST API** to create events by using PowerShell (version 6 or later), which is part of a custom solution.</span></span>

<span data-ttu-id="3b85b-243">Avant d’utiliser l’API REST, en tant qu’administrateur général, confirmez l’URL à utiliser pour l’appel d’événement de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-243">Before you use the REST API, as a global administrator, confirm the URL to use for the retention event call.</span></span> <span data-ttu-id="3b85b-244">Pour ce faire, exécutez un appel d’événement de rétention GET à l’aide de l’URL de l’API REST :</span><span class="sxs-lookup"><span data-stu-id="3b85b-244">To do this, run a GET retention event call by using the REST API URL:</span></span>

```http
https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent
```

<span data-ttu-id="3b85b-245">Vérifiez le code de réponse.</span><span class="sxs-lookup"><span data-stu-id="3b85b-245">Check the response code.</span></span> <span data-ttu-id="3b85b-246">S’il est 302, récupérez l’URL redirigée à partir de la propriété Location de l’en-tête de réponse, puis utilisez cette URL au lieu de `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent` dans les instructions qui suivent.</span><span class="sxs-lookup"><span data-stu-id="3b85b-246">If it's 302, get the redirected URL from the Location property of the response header and use that URL instead of `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent` in the instructions that follow.</span></span>

<span data-ttu-id="3b85b-247">Les événements qui sont créés automatiquement peuvent être confirmés en les affichant dans le Centre de conformité Microsoft 365 > **Gestion des enregistrements** >  **Événements**.</span><span class="sxs-lookup"><span data-stu-id="3b85b-247">The events that get automatically created can be confirmed by viewing them in the Microsoft 365 compliance center > **Records management** >  **Events**.</span></span>

### <a name="use-microsoft-power-automate-to-create-the-event"></a><span data-ttu-id="3b85b-248">Utiliser Microsoft Power Automate pour créer l’événement</span><span class="sxs-lookup"><span data-stu-id="3b85b-248">Use Microsoft Power Automate to create the event</span></span>

<span data-ttu-id="3b85b-249">Créez un flux qui crée un événement en utilisant l’API REST Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="3b85b-249">Create a flow that creates an event using the Microsoft 365 REST API:</span></span>

![Utilisation le flux pour créer un événement](../media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](../media/automate-event-driven-retention-flow-2.png)

#### <a name="create-an-event"></a><span data-ttu-id="3b85b-252">Créer un événement</span><span class="sxs-lookup"><span data-stu-id="3b85b-252">Create an event</span></span>

<span data-ttu-id="3b85b-253">Utilisation du code d’exemple pour appeler des API REST :</span><span class="sxs-lookup"><span data-stu-id="3b85b-253">Sample code to call the REST API:</span></span>

- <span data-ttu-id="3b85b-254">**Method** : PUBLIER</span><span class="sxs-lookup"><span data-stu-id="3b85b-254">**Method**: POST</span></span>
- <span data-ttu-id="3b85b-255">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span><span class="sxs-lookup"><span data-stu-id="3b85b-255">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span></span>
- <span data-ttu-id="3b85b-256">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-256">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>
- <span data-ttu-id="3b85b-257">**Body** :</span><span class="sxs-lookup"><span data-stu-id="3b85b-257">**Body**:</span></span>
    
    ```xml
    <?xml version='1.0' encoding='utf-8' standalone='yes'?>
    
    <entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'
    
    xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'
    
    xmlns='http://www.w3.org/2005/Atom'>
    
    <category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' />
    
    <updated>9/9/2017 10:50:00 PM</updated>
    
    <content type='application/xml'>
    
    <m:properties>
    
    <d:Name>Employee Termination </d:Name>
    
    <d:EventType>99e0ae64-a4b8-40bb-82ed-645895610f56</d:EventType>
    
    <d:SharePointAssetIdQuery>1234</d:SharePointAssetIdQuery>
    
    <d:EventDateTime>2018-12-01T00:00:00Z </d:EventDateTime>
    
    </m:properties>
    
    </content>
    
    </entry>
    ```
    
- <span data-ttu-id="3b85b-258">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="3b85b-258">**Authentication**: Basic</span></span>
- <span data-ttu-id="3b85b-259">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="3b85b-259">**Username**: "Complianceuser"</span></span>
- <span data-ttu-id="3b85b-260">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="3b85b-260">**Password**: "Compliancepassword"</span></span>


##### <a name="available-parameters"></a><span data-ttu-id="3b85b-261">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="3b85b-261">Available parameters</span></span>


|<span data-ttu-id="3b85b-262">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b85b-262">Parameters</span></span>|<span data-ttu-id="3b85b-263">Description</span><span class="sxs-lookup"><span data-stu-id="3b85b-263">Description</span></span>|<span data-ttu-id="3b85b-264">Notes</span><span class="sxs-lookup"><span data-stu-id="3b85b-264">Notes</span></span>|
|--- |--- |--- |
|<span data-ttu-id="3b85b-265"><d:Name></d:Name></span><span class="sxs-lookup"><span data-stu-id="3b85b-265"><d:Name></d:Name></span></span>|<span data-ttu-id="3b85b-266">Entrez un nom unique pour la base de données,</span><span class="sxs-lookup"><span data-stu-id="3b85b-266">Provide a unique name for the event,</span></span>|<span data-ttu-id="3b85b-267">Ne peut pas contenir les espaces ou les caractères suivants : % \* \ & < \> \| # ?</span><span class="sxs-lookup"><span data-stu-id="3b85b-267">Cannot contain trailing spaces or the following characters: % \* \ & < \> \| # ?</span></span> <span data-ttu-id="3b85b-268">, : ;</span><span class="sxs-lookup"><span data-stu-id="3b85b-268">, : ;</span></span>|
|<span data-ttu-id="3b85b-269"><d:EventType></d:EventType></span><span class="sxs-lookup"><span data-stu-id="3b85b-269"><d:EventType></d:EventType></span></span>|<span data-ttu-id="3b85b-270">Entrez le nom de l’événement (ou Guid),</span><span class="sxs-lookup"><span data-stu-id="3b85b-270">Enter event type name (or Guid),</span></span>|<span data-ttu-id="3b85b-271">Exemple : « Fin de contrat d’un employé ».</span><span class="sxs-lookup"><span data-stu-id="3b85b-271">Example: "Employee termination".</span></span> <span data-ttu-id="3b85b-272">Le type d’événement doit être associé à une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="3b85b-272">Event type has to be associated with a retention label.</span></span>|
|<span data-ttu-id="3b85b-273"><d:SharePointAssetIdQuery></d:SharePointAssetIdQuery></span><span class="sxs-lookup"><span data-stu-id="3b85b-273"><d:SharePointAssetIdQuery></d:SharePointAssetIdQuery></span></span>|<span data-ttu-id="3b85b-274">Entrez « ComplianceAssetId : » suivi de l’ID de l’employé</span><span class="sxs-lookup"><span data-stu-id="3b85b-274">Enter "ComplianceAssetId:" + employee ID</span></span>|<span data-ttu-id="3b85b-275">Example: "ComplianceAssetId:12345"</span><span class="sxs-lookup"><span data-stu-id="3b85b-275">Example: "ComplianceAssetId:12345"</span></span>|
|<span data-ttu-id="3b85b-276"><d:EventDateTime></d:EventDateTime></span><span class="sxs-lookup"><span data-stu-id="3b85b-276"><d:EventDateTime></d:EventDateTime></span></span>|<span data-ttu-id="3b85b-277">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="3b85b-277">Event Date and Time</span></span>|<span data-ttu-id="3b85b-278">Format : AAAA-MM-jjTHH : mm : ssZ ; exemple : 2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="3b85b-278">Format: yyyy-MM-ddTHH:mm:ssZ, Example: 2018-12-01T00:00:00Z</span></span>
|

###### <a name="response-codes"></a><span data-ttu-id="3b85b-279">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-279">Response codes</span></span>

| <span data-ttu-id="3b85b-280">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-280">Response Code</span></span> | <span data-ttu-id="3b85b-281">Description</span><span class="sxs-lookup"><span data-stu-id="3b85b-281">Description</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="3b85b-282">302</span><span class="sxs-lookup"><span data-stu-id="3b85b-282">302</span></span>               | <span data-ttu-id="3b85b-283">Rediriger</span><span class="sxs-lookup"><span data-stu-id="3b85b-283">Redirect</span></span>              |
| <span data-ttu-id="3b85b-284">201</span><span class="sxs-lookup"><span data-stu-id="3b85b-284">201</span></span>               | <span data-ttu-id="3b85b-285">Créé</span><span class="sxs-lookup"><span data-stu-id="3b85b-285">Created</span></span>               |
| <span data-ttu-id="3b85b-286">403</span><span class="sxs-lookup"><span data-stu-id="3b85b-286">403</span></span>               | <span data-ttu-id="3b85b-287">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="3b85b-287">Authorization Failed</span></span>  |
| <span data-ttu-id="3b85b-288">401</span><span class="sxs-lookup"><span data-stu-id="3b85b-288">401</span></span>               | <span data-ttu-id="3b85b-289">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="3b85b-289">Authentication Failed</span></span> |

##### <a name="get-events-based-on-a-time-range"></a><span data-ttu-id="3b85b-290">Obtenir des événements en fonction de l’intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="3b85b-290">Get events based on a time range</span></span>

- <span data-ttu-id="3b85b-291">**Méthode**: GET</span><span class="sxs-lookup"><span data-stu-id="3b85b-291">**Method**: GET</span></span>

- <span data-ttu-id="3b85b-292">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&EndDateTime=2019-01-16`</span><span class="sxs-lookup"><span data-stu-id="3b85b-292">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&EndDateTime=2019-01-16`</span></span>

- <span data-ttu-id="3b85b-293">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-293">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="3b85b-294">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="3b85b-294">**Authentication**: Basic</span></span>

- <span data-ttu-id="3b85b-295">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="3b85b-295">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="3b85b-296">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="3b85b-296">**Password**: "Compliancepassword"</span></span>


###### <a name="response-codes"></a><span data-ttu-id="3b85b-297">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-297">Response codes</span></span>

| <span data-ttu-id="3b85b-298">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-298">Response Code</span></span> | <span data-ttu-id="3b85b-299">Description</span><span class="sxs-lookup"><span data-stu-id="3b85b-299">Description</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="3b85b-300">200</span><span class="sxs-lookup"><span data-stu-id="3b85b-300">200</span></span>               | <span data-ttu-id="3b85b-301">OK, une liste d’événements dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-301">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="3b85b-302">404</span><span class="sxs-lookup"><span data-stu-id="3b85b-302">404</span></span>               | <span data-ttu-id="3b85b-303">Introuvable</span><span class="sxs-lookup"><span data-stu-id="3b85b-303">Not found</span></span>                         |
| <span data-ttu-id="3b85b-304">302</span><span class="sxs-lookup"><span data-stu-id="3b85b-304">302</span></span>               | <span data-ttu-id="3b85b-305">Rediriger</span><span class="sxs-lookup"><span data-stu-id="3b85b-305">Redirect</span></span>                          |
| <span data-ttu-id="3b85b-306">401</span><span class="sxs-lookup"><span data-stu-id="3b85b-306">401</span></span>               | <span data-ttu-id="3b85b-307">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="3b85b-307">Authorization Failed</span></span>              |
| <span data-ttu-id="3b85b-308">403</span><span class="sxs-lookup"><span data-stu-id="3b85b-308">403</span></span>               | <span data-ttu-id="3b85b-309">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="3b85b-309">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="3b85b-310">Obtenir un événement par ID</span><span class="sxs-lookup"><span data-stu-id="3b85b-310">Get an event by ID</span></span>

- <span data-ttu-id="3b85b-311">**Méthode**: GET</span><span class="sxs-lookup"><span data-stu-id="3b85b-311">**Method**: GET</span></span>

- <span data-ttu-id="3b85b-312">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('174e9a86-74ff-4450-8666-7c11f7730f66')`</span><span class="sxs-lookup"><span data-stu-id="3b85b-312">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('174e9a86-74ff-4450-8666-7c11f7730f66')`</span></span>

- <span data-ttu-id="3b85b-313">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-313">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="3b85b-314">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="3b85b-314">**Authentication**: Basic</span></span>

- <span data-ttu-id="3b85b-315">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="3b85b-315">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="3b85b-316">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="3b85b-316">**Password**: "Compliancepassword"</span></span>

###### <a name="response-codes"></a><span data-ttu-id="3b85b-317">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-317">Response codes</span></span>

| <span data-ttu-id="3b85b-318">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-318">Response Code</span></span> | <span data-ttu-id="3b85b-319">Description</span><span class="sxs-lookup"><span data-stu-id="3b85b-319">Description</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="3b85b-320">200</span><span class="sxs-lookup"><span data-stu-id="3b85b-320">200</span></span>               | <span data-ttu-id="3b85b-321">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-321">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="3b85b-322">404</span><span class="sxs-lookup"><span data-stu-id="3b85b-322">404</span></span>               | <span data-ttu-id="3b85b-323">Introuvable</span><span class="sxs-lookup"><span data-stu-id="3b85b-323">Not found</span></span>                                            |
| <span data-ttu-id="3b85b-324">302</span><span class="sxs-lookup"><span data-stu-id="3b85b-324">302</span></span>               | <span data-ttu-id="3b85b-325">Rediriger</span><span class="sxs-lookup"><span data-stu-id="3b85b-325">Redirect</span></span>                                             |
| <span data-ttu-id="3b85b-326">401</span><span class="sxs-lookup"><span data-stu-id="3b85b-326">401</span></span>               | <span data-ttu-id="3b85b-327">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="3b85b-327">Authorization Failed</span></span>                                 |
| <span data-ttu-id="3b85b-328">403</span><span class="sxs-lookup"><span data-stu-id="3b85b-328">403</span></span>               | <span data-ttu-id="3b85b-329">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="3b85b-329">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="3b85b-330">Obtenir un événement par le nom</span><span class="sxs-lookup"><span data-stu-id="3b85b-330">Get an event by name</span></span>

- <span data-ttu-id="3b85b-331">**Méthode**: GET</span><span class="sxs-lookup"><span data-stu-id="3b85b-331">**Method**: GET</span></span>

- <span data-ttu-id="3b85b-332">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span><span class="sxs-lookup"><span data-stu-id="3b85b-332">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span></span>

- <span data-ttu-id="3b85b-333">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-333">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="3b85b-334">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="3b85b-334">**Authentication**: Basic</span></span>

- <span data-ttu-id="3b85b-335">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="3b85b-335">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="3b85b-336">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="3b85b-336">**Password**: "Compliancepassword"</span></span>


###### <a name="response-codes"></a><span data-ttu-id="3b85b-337">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-337">Response codes</span></span>

| <span data-ttu-id="3b85b-338">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="3b85b-338">Response Code</span></span> | <span data-ttu-id="3b85b-339">Description</span><span class="sxs-lookup"><span data-stu-id="3b85b-339">Description</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="3b85b-340">200</span><span class="sxs-lookup"><span data-stu-id="3b85b-340">200</span></span>               | <span data-ttu-id="3b85b-341">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="3b85b-341">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="3b85b-342">404</span><span class="sxs-lookup"><span data-stu-id="3b85b-342">404</span></span>               | <span data-ttu-id="3b85b-343">Introuvable</span><span class="sxs-lookup"><span data-stu-id="3b85b-343">Not found</span></span>                                            |
| <span data-ttu-id="3b85b-344">302</span><span class="sxs-lookup"><span data-stu-id="3b85b-344">302</span></span>               | <span data-ttu-id="3b85b-345">Rediriger</span><span class="sxs-lookup"><span data-stu-id="3b85b-345">Redirect</span></span>                                             |
| <span data-ttu-id="3b85b-346">401</span><span class="sxs-lookup"><span data-stu-id="3b85b-346">401</span></span>               | <span data-ttu-id="3b85b-347">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="3b85b-347">Authorization Failed</span></span>                                 |
| <span data-ttu-id="3b85b-348">403</span><span class="sxs-lookup"><span data-stu-id="3b85b-348">403</span></span>               | <span data-ttu-id="3b85b-349">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="3b85b-349">Authentication Failed</span></span>                                |

### <a name="use-powershell-or-any-http-client-to-create-the-event"></a><span data-ttu-id="3b85b-350">Utiliser PowerShell ou n’importe quel client HTTP pour créer l’événement</span><span class="sxs-lookup"><span data-stu-id="3b85b-350">Use PowerShell or any HTTP client to create the event</span></span>

<span data-ttu-id="3b85b-351">Vous devez utiliser au moins la version 6 de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b85b-351">PowerShell must be version 6 or later.</span></span>

<span data-ttu-id="3b85b-352">Dans une session PowerShell, exécutez le script suivant :</span><span class="sxs-lookup"><span data-stu-id="3b85b-352">In a PowerShell session, run the following script:</span></span>

```powershell
param([string]$baseUri)

$userName = "UserName"

$password = "Password"

$securePassword = ConvertTo-SecureString $password -AsPlainText -Force

$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)

$EventName="EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))"

Write-Host "Start to create an event with name: $EventName"

$body = "<?xml version='1.0' encoding='utf-8' standalone='yes'?>

<entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'

xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'

xmlns='http://www.w3.org/2005/Atom'>

<category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' />

<updated>7/14/2017 2:03:36 PM</updated>

<content type='application/xml'>

<m:properties>

<d:Name>$EventName</d:Name>

<d:EventType>e823b782-9a07-4e30-8091-034fc01f9347</d:EventType>

<d:SharePointAssetIdQuery>'ComplianceAssetId:123'</d:SharePointAssetIdQuery>

</m:properties>

</content>

</entry>"

$event = $null

try

{

$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri "$baseUri/ComplianceRetentionEvent" -ContentType "application/atom+xml" -Authentication Basic -Credential $credentials -MaximumRedirection 0

}

catch

{

$response = $_.Exception.Response

if($response.StatusCode -eq "Redirect")

{

$url = $response.Headers.Location

Write-Host "redirected to $url"

$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType "application/atom+xml" -Authentication Basic -Credential $credentials -MaximumRedirection 0

}

}

$event | fl *

```
