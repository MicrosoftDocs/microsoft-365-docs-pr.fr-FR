---
title: Destruction de contenu
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
description: Surveiller et gérer la suppression de contenu, que vous utilisiez une révision de destruction ou que le contenu soit automatiquement supprimé selon les paramètres que vous avez configurés.
ms.openlocfilehash: 9900bbc58818a98ad41f4f796184ccf21041bbfe
ms.sourcegitcommit: a9486f9dc51f0908393000ec3c211e3430c26abd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "49409211"
---
# <a name="disposition-of-content"></a><span data-ttu-id="8d724-103">Destruction de contenu</span><span class="sxs-lookup"><span data-stu-id="8d724-103">Disposition of content</span></span>

><span data-ttu-id="8d724-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="8d724-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="8d724-105">Utilisez l’onglet **Destruction** de **Gestion des enregistrements** dans le Centre de conformité Microsoft 365 pour gérer les révisions de destruction et afficher les [enregistrements](records-management.md#records) qui ont été automatiquement supprimés à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="8d724-105">Use the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center to manage disposition reviews and view [records](records-management.md#records) that have been automatically deleted at the end of their retention period.</span></span> 

## <a name="prerequisites-for-viewing-content-dispositions"></a><span data-ttu-id="8d724-106">Conditions préalables pour l’affichage des suppressions de contenu</span><span class="sxs-lookup"><span data-stu-id="8d724-106">Prerequisites for viewing content dispositions</span></span>

<span data-ttu-id="8d724-107">Pour gérer les révisions de destruction et vérifier que les enregistrements ont été supprimés, vous devez disposer d’autorisations suffisantes et l’audit doit être activé.</span><span class="sxs-lookup"><span data-stu-id="8d724-107">To manage disposition reviews and confirm that records have been deleted, you must have sufficient permissions and auditing must be enabled.</span></span>

### <a name="permissions-for-disposition"></a><span data-ttu-id="8d724-108">Autorisations pour la destruction</span><span class="sxs-lookup"><span data-stu-id="8d724-108">Permissions for disposition</span></span>

<span data-ttu-id="8d724-109">Pour accéder à l’onglet **Destruction** dans le Centre de conformité Microsoft 365, les utilisateurs doivent avoir le rôle d’administrateur de **Gestion des suppressions** .</span><span class="sxs-lookup"><span data-stu-id="8d724-109">To successfully access the **Disposition** tab in the Microsoft 365 compliance center, users must have the **Disposition Management** admin role.</span></span> <span data-ttu-id="8d724-110">Ce rôle est inclus dans les groupes de rôles d’administrateur par défaut, **Administrateur de conformité** et **Administrateur de données de conformité**.</span><span class="sxs-lookup"><span data-stu-id="8d724-110">This role is included in the default admin role groups, **Compliance Administrator** and **Compliance Data Administrator**.</span></span>

<span data-ttu-id="8d724-111">Pour attribuer le rôle de gestion de destruction aux utilisateurs, ajoutez-les à l’un de ces groupes de rôles par défaut ou créez un groupe de rôles personnalisé (par exemple, nommez « Réviseurs de destruction ») et accordez à ce groupe le rôle de gestion de la destruction.</span><span class="sxs-lookup"><span data-stu-id="8d724-111">To grant users this required Disposition Management role, either add them to one of these default role groups, or create a custom role group (for example, named "Disposition Reviewers") and grant this group the Disposition Management role.</span></span>  

> [!NOTE]
> <span data-ttu-id="8d724-112">Même un administrateur général doit avoir accès au rôle **Gestion des suppressions** .</span><span class="sxs-lookup"><span data-stu-id="8d724-112">Even a global admin needs to be granted the **Disposition Management** role.</span></span> 

<span data-ttu-id="8d724-113">De plus, pour afficher le contenu des éléments pendant le processus de destruction, ajoutez des utilisateurs aux deux groupes de rôles suivants : **la visionneuse de contenu de l’Explorateur de contenu** et **visionneuse de liste de l’Explorateur de contenu**.</span><span class="sxs-lookup"><span data-stu-id="8d724-113">Additionally, to view the contents of items during the disposition process, add users to the following two role groups: **Content Explorer Content Viewer** and **Content Explorer List Viewer**.</span></span> <span data-ttu-id="8d724-114">Si les utilisateurs n’ont pas les autorisations de ces groupes de rôles, ils peuvent toujours sélectionner une action de révision de destruction pour achever la révision de destruction, mais vous devez le faire sans avoir la possibilité d’afficher le contenu de l’élément à partir du centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="8d724-114">If users don't have the permissions from these role groups, they can still select a disposition review action to complete the disposition review, but must do so without being able to view the item's contents from the compliance center.</span></span>

<span data-ttu-id="8d724-115">Pour obtenir des instructions, reportez-vous à la rubrique [Octroi de l’accès au Centre de sécurité et conformité Office 365 aux utilisateurs](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8d724-115">For instructions, see [Give users access to the Office 365 Security & Compliance Center](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span></span>

### <a name="enable-auditing"></a><span data-ttu-id="8d724-116">Activer l’audit</span><span class="sxs-lookup"><span data-stu-id="8d724-116">Enable auditing</span></span>

<span data-ttu-id="8d724-117">Assurez-vous que l’audit est activé au moins un jour avant la première action de destruction.</span><span class="sxs-lookup"><span data-stu-id="8d724-117">Make sure that auditing is enabled at least one day before the first disposition action.</span></span> <span data-ttu-id="8d724-118">Pour plus d’informations, reportez-vous à l’article [Effectuer des recherches dans le journal d’audit dans le Centre de sécurité &amp; de conformité Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="8d724-118">For more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 

## <a name="disposition-reviews"></a><span data-ttu-id="8d724-119">Révisions avant destruction</span><span class="sxs-lookup"><span data-stu-id="8d724-119">Disposition reviews</span></span>

<span data-ttu-id="8d724-120">Lorsque le contenu atteint la fin de la période de rétention, vous souhaiterez peut-être réviser ce contenu pour décider s’il peut être supprimé de manière sécurisée (« supprimé »).</span><span class="sxs-lookup"><span data-stu-id="8d724-120">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed").</span></span> <span data-ttu-id="8d724-121">Par exemple, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="8d724-121">For example, you might need to:</span></span>
  
- <span data-ttu-id="8d724-122">Suspendre la suppression de contenu pertinent en cas de litige ou d’audit.</span><span class="sxs-lookup"><span data-stu-id="8d724-122">Suspend the deletion of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="8d724-123">Supprimer le contenu de la liste de destruction pour la stocker dans une archive, si ce contenu comporte des recherches ou une valeur d’historique.</span><span class="sxs-lookup"><span data-stu-id="8d724-123">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="8d724-124">Affecter une période de rétention différente au contenu, peut-être parce que les paramètres de rétention d’origine étaient une solution temporaire ou provisoire.</span><span class="sxs-lookup"><span data-stu-id="8d724-124">Assign a different retention period to the content, perhaps because the original retention settings were a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="8d724-125">Renvoyer le contenu aux clients ou le transférer vers une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="8d724-125">Return the content to clients or transfer it to another organization.</span></span>

<span data-ttu-id="8d724-126">Lorsqu’une révision de destruction est déclenchée à la fin de la période de rétention :</span><span class="sxs-lookup"><span data-stu-id="8d724-126">When a disposition review is triggered at the end of the retention period:</span></span>
  
- <span data-ttu-id="8d724-127">Les personnes que vous sélectionnez reçoivent une notification par courrier électronique indiquant que leur contenu doit être examiné.</span><span class="sxs-lookup"><span data-stu-id="8d724-127">The people you choose receive an email notification that they have content to review.</span></span> <span data-ttu-id="8d724-128">Ces réviseurs peuvent être des utilisateurs individuels ou des groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="8d724-128">These reviewers can be individual users or mail-enabled security groups.</span></span> <span data-ttu-id="8d724-129">Notez que les notifications sont envoyées de façon hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="8d724-129">Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="8d724-130">Les réviseurs accèdent à l’onglet **Destruction** dans le Centre de conformité Microsoft 365 pour examiner le contenu et décider si vous voulez le supprimer définitivement, prolonger sa période de rétention ou appliquer une autre étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="8d724-130">The reviewers go to the **Disposition** tab in the Microsoft 365 compliance center to review the content and decide whether to permanently delete it, extend its retention period, or apply a different retention label.</span></span>

<span data-ttu-id="8d724-131">Une révision de destruction peut inclure du contenu dans les boîtes aux lettres Exchange, les sites SharePoint, les comptes OneDrive et les groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8d724-131">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Microsoft 365 groups.</span></span> <span data-ttu-id="8d724-132">Le contenu en attente de révision de destruction dans ces emplacements est supprimé uniquement lorsqu’un réviseur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="8d724-132">Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>

> [!NOTE]
> <span data-ttu-id="8d724-133">Une boîte aux lettres doit avoir au moins 10 Mo de données pour prendre en charge les révisions de suppression.</span><span class="sxs-lookup"><span data-stu-id="8d724-133">A mailbox must have at least 10 MB data to support disposition reviews.</span></span>

<span data-ttu-id="8d724-134">Vous pouvez voir une vue d’ensemble de toutes les suppressions en attente dans l’onglet **Vue d’ensemble**. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8d724-134">You can see an overview of all pending dispositions in the **Overview** tab. For example:</span></span>

![Destructions en attente dans la vue d’ensemble de la Gestion des enregistrements](../media/dispositions-overview.png)

<span data-ttu-id="8d724-136">Lorsque vous sélectionnez l’option **Afficher toutes les destructions en attente**, vous êtes redirigé vers la page **Destruction** .</span><span class="sxs-lookup"><span data-stu-id="8d724-136">When you select the **View all pending dispositions**, you're taken to the **Disposition** page.</span></span> <span data-ttu-id="8d724-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8d724-137">For example:</span></span>

![Page de destruction dans le centre de conformité Microsoft 365](../media/disposition-tab.png)


### <a name="workflow-for-a-disposition-review"></a><span data-ttu-id="8d724-139">Flux de travail pour une révision de destruction</span><span class="sxs-lookup"><span data-stu-id="8d724-139">Workflow for a disposition review</span></span>

<span data-ttu-id="8d724-140">Le diagramme suivant illustre le flux de travail de base d’une révision de destruction lorsqu’une étiquette de rétention est publiée et appliquée manuellement par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8d724-140">The following diagram shows the basic workflow for a disposition review when a retention label is published and then manually applied by a user.</span></span> <span data-ttu-id="8d724-141">Une étiquette de rétention configurée pour une révision de destruction peut également être appliquée automatiquement au contenu.</span><span class="sxs-lookup"><span data-stu-id="8d724-141">Alternatively, a retention label configured for a disposition review can be auto-applied to content.</span></span>
  
![Graphique montrant le fonctionnement de la destruction](../media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="8d724-143">Le déclenchement d’une révision de suppression à la fin de la période de rétention est une option de configuration disponible uniquement avec une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="8d724-143">Triggering a disposition review at the end of the retention period is a configuration option that's available only with a retention label.</span></span> <span data-ttu-id="8d724-144">Cette option n’est pas disponible pour une stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="8d724-144">This option is not available for a retention policy.</span></span> <span data-ttu-id="8d724-145">Pour plus d’informations sur ces deux solutions de rétention, consultez [En savoir plus sur les stratégies de rétention et les étiquettes de rétention](retention.md).</span><span class="sxs-lookup"><span data-stu-id="8d724-145">For more information about these two retention solutions, see [Learn about retention policies and retention labels](retention.md).</span></span>

<span data-ttu-id="8d724-146">Dans la page **Définir les paramètres de rétention** pour une étiquette de rétention :</span><span class="sxs-lookup"><span data-stu-id="8d724-146">From the **Define retention settings** page for a retention label:</span></span>

![Paramètres de conservation pour une étiquette](../media/disposition-review-option.png)
 
<span data-ttu-id="8d724-148">Une fois que vous avez sélectionné cet option **Déclencher une révision avant destruction**, vous spécifiez les relecteurs de destruction sur la page suivante de l’Assistant :</span><span class="sxs-lookup"><span data-stu-id="8d724-148">After you select this **Trigger a disposition review** option, you specify the disposition reviewers on the next page of the wizard:</span></span>

![Spécification des réviseurs avant destruction](../media/disposition-reviewers.png)

<span data-ttu-id="8d724-150">Pour les réviseurs, spécifiez un utilisateur ou un groupe de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="8d724-150">For the reviewers, specify a user or mail-enabled security group.</span></span> <span data-ttu-id="8d724-151">Les groupes Microsoft 365 ([anciennement groupes Office 365](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) ne sont pas pris en charge pour cette option.</span><span class="sxs-lookup"><span data-stu-id="8d724-151">Microsoft 365 groups ([formerly Office 365 groups](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) are not supported for this option.</span></span>

### <a name="viewing-and-disposing-of-content"></a><span data-ttu-id="8d724-152">Affichage et destruction de contenu</span><span class="sxs-lookup"><span data-stu-id="8d724-152">Viewing and disposing of content</span></span>

<span data-ttu-id="8d724-153">Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt à être examiné, il passe à l’onglet **Destruction** de **Gestion des enregistrements** dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="8d724-153">When a reviewer is notified by email that content is ready to review, they go to the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="8d724-154">Les réviseurs peuvent voir le nombre d’éléments pour chaque étiquette de rétention en attente de destruction, puis sélectionner une étiquette de rétention pour afficher tout le contenu contenant cette étiquette.</span><span class="sxs-lookup"><span data-stu-id="8d724-154">The reviewers can see how many items for each retention label are awaiting disposition, and then select a retention label to see all content with that label.</span></span>

<span data-ttu-id="8d724-155">Une fois que vous avez sélectionné une étiquette de rétention, vous voyez toutes les suppressions en attente de cette étiquette dans l’onglet **Destruction en attente** . Sélectionnez un ou plusieurs éléments à partir desquels vous pouvez choisir une action et entrez un commentaire de justification :</span><span class="sxs-lookup"><span data-stu-id="8d724-155">After you select a retention label, you then see all pending dispositions for that label from the **Pending disposition** tab. Select one or more items where you can then choose an action and enter a justification comment:</span></span>

![Options de destruction](../media/retention-disposition-options.png)

<span data-ttu-id="8d724-157">Comme vous pouvez le voir dans l’image, les actions prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d724-157">As you can see from the picture, the actions supported are:</span></span> 
  
- <span data-ttu-id="8d724-158">Supprimer définitivement l’élément</span><span class="sxs-lookup"><span data-stu-id="8d724-158">Permanently delete the item</span></span>
- <span data-ttu-id="8d724-159">Prolonger la période de rétention</span><span class="sxs-lookup"><span data-stu-id="8d724-159">Extend the retention period</span></span>
- <span data-ttu-id="8d724-160">Appliquer une autre étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="8d724-160">Apply a different retention label</span></span>

<span data-ttu-id="8d724-161">En vous fournissant les autorisations d’accès à l’emplacement et au contenu, vous pouvez utiliser le lien situé dans la colonne **Emplacement** pour afficher les documents dans leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="8d724-161">Providing you have permissions to the location and the content, you can use the link in the **Location** column to view documents in their original location.</span></span> <span data-ttu-id="8d724-162">Lors d’une révision de destruction, le contenu ne se déplace jamais à partir de son emplacement d’origine et n’est jamais supprimé tant que le réviseur n’a pas choisi de le faire.</span><span class="sxs-lookup"><span data-stu-id="8d724-162">During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>

<span data-ttu-id="8d724-163">Les notifications par courrier électronique sont envoyées automatiquement aux réviseurs sur une base hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="8d724-163">The email notifications are sent automatically to reviewers on a weekly basis.</span></span> <span data-ttu-id="8d724-164">Ce processus planifié signifie qu’une fois que le contenu atteint la fin de la période de rétention, il peut arriver que les réviseurs reçoivent jusqu’à sept jours la notification par courrier électronique indiquant que le contenu est en attente de destruction.</span><span class="sxs-lookup"><span data-stu-id="8d724-164">This scheduled process means that when content reaches the end of its retention period, it might take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="8d724-165">Toutes les actions de destruction peuvent faire l’objet d’un audit et le texte de la justification entré par le réviseur est enregistré et affiché dans la colonne **Commentaire** sur la page **Éléments supprimés**.</span><span class="sxs-lookup"><span data-stu-id="8d724-165">All disposition actions can be audited and the justification text entered by the reviewer is saved and displayed in the **Comment** column on the **Disposed items** page.</span></span>
  
### <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="8d724-166">Combien de temps faut-il pour supprimer définitivement du contenu supprimé</span><span class="sxs-lookup"><span data-stu-id="8d724-166">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="8d724-167">Le contenu en attente de révision de destruction est supprimé uniquement lorsqu’un réviseur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="8d724-167">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content.</span></span> <span data-ttu-id="8d724-168">Lorsque le réviseur choisit cette option, le contenu du site SharePoint ou du compte OneDrive est éligible pour le processus de nettoyage standard décrit dans [Fonctionnement des paramètres de rétention avec le contenu en place](retention.md#how-retention-settings-work-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="8d724-168">When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in [How retention settings work with content in place](retention.md#how-retention-settings-work-with-content-in-place).</span></span>

## <a name="disposition-of-records"></a><span data-ttu-id="8d724-169">Destruction des enregistrements</span><span class="sxs-lookup"><span data-stu-id="8d724-169">Disposition of records</span></span>

<span data-ttu-id="8d724-170">Utilisez l’onglet **Destruction** à partir de la page **Gestion des enregistrements** pour identifier les enregistrements qui sont désormais supprimés, soit automatiquement, soit après une révision de suppression.</span><span class="sxs-lookup"><span data-stu-id="8d724-170">Use the **Disposition** tab from the **Records Management** page to identify records that are now deleted, either automatically or after a disposition review.</span></span> <span data-ttu-id="8d724-171">Ces éléments affichent **Enregistrements supprimés** dans la colonne **Type**.</span><span class="sxs-lookup"><span data-stu-id="8d724-171">These items display **Records Disposed** in the **Type** column.</span></span> <span data-ttu-id="8d724-172">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8d724-172">For example:</span></span>

![Éléments supprimés sans révision avant destruction](../media/records-disposed2.png)

<span data-ttu-id="8d724-174">Les éléments qui apparaissent dans la **Éléments supprimés** pour les étiquettes d’enregistrement sont conservés pendant sept ans après la suppression de l’élément, avec une limite de 1 million éléments par enregistrement pour cette période.</span><span class="sxs-lookup"><span data-stu-id="8d724-174">Items that are shown in the **Disposed Items** tab for record labels are kept for up to seven years after the item was disposed, with a limit of one million items per record for that period.</span></span> <span data-ttu-id="8d724-175">Si vous voyez le nombre de **Count** approcher cette limite d'un million, et que vous avez besoin d'une preuve de destruction pour vos enregistrements, contactez le [Support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="8d724-175">If you see the **Count** number nearing this limit of one million, and you need proof of disposition for your records, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

> [!NOTE]
> <span data-ttu-id="8d724-176">Cette fonctionnalité est basée sur les informations du [journal d’audit unifié](search-the-audit-log-in-security-and-compliance.md) et nécessite par conséquent que l’audit soit [activé et puisse faire l’objet d’une recherche](turn-audit-log-search-on-or-off.md) de sorte que les événements correspondants soient capturés.</span><span class="sxs-lookup"><span data-stu-id="8d724-176">This functionality is based on information from the [unified audit log](search-the-audit-log-in-security-and-compliance.md) and therefore requires auditing to be [enabled and searchable](turn-audit-log-search-on-or-off.md) so the corresponding events are captured.</span></span>

<span data-ttu-id="8d724-177">Pour l’audit, recherchez **fichier supprimé marqué comme enregistrement** dans la catégorie **activités de fichier et de page** .</span><span class="sxs-lookup"><span data-stu-id="8d724-177">For auditing, search for **Deleted file marked as a record** in the **File and page activities** category.</span></span> <span data-ttu-id="8d724-178">Cet événement d’audit est applicable aux documents et messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="8d724-178">This audit event is applicable to documents and emails.</span></span>

## <a name="filter-and-export-the-views"></a><span data-ttu-id="8d724-179">Filtrer et exporter les affichages</span><span class="sxs-lookup"><span data-stu-id="8d724-179">Filter and export the views</span></span>

<span data-ttu-id="8d724-180">Lorsque vous sélectionnez une étiquette de rétention dans la page **Destruction** , l’onglet **Destruction en attente** (le cas échéant) et **Éléments supprimés** vous permettent de filtrer les affichages pour trouver des éléments plus facilement.</span><span class="sxs-lookup"><span data-stu-id="8d724-180">When you select a retention label from the **Disposition** page, the **Pending disposition** tab (if applicable) and the **Disposed items** tab let you filter the views to help you more easily find items.</span></span> 

<span data-ttu-id="8d724-181">Pour les destructions en attente, la plage horaire est basée sur la date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="8d724-181">For pending dispositions, the time range is based on the expiration date.</span></span> <span data-ttu-id="8d724-182">Pour les éléments supprimés, la plage horaire est basée sur la date de suppression.</span><span class="sxs-lookup"><span data-stu-id="8d724-182">For disposed items, the time range is based on the deletion date.</span></span>
  
<span data-ttu-id="8d724-183">Vous pouvez exporter les informations relatives aux éléments de l’une ou l’autre vue en tant que fichier .csv que vous pouvez ensuite trier et gérer à l’aide d’Excel :</span><span class="sxs-lookup"><span data-stu-id="8d724-183">You can export information about the items in either view as a .csv file that you can then sort and manage using Excel:</span></span>

![Option d’exportation pour destruction](../media/retention-export-option.png)

