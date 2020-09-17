---
title: Disposition de contenu
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Surveiller et gérer la suppression du contenu, que vous utilisiez une révision de disposition ou que le contenu soit automatiquement supprimé en fonction des paramètres que vous avez configurés.
ms.openlocfilehash: 6789ab1abe54b76f22462a47326b07a213f19b0c
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950388"
---
# <a name="disposition-of-content"></a><span data-ttu-id="028a5-103">Disposition de contenu</span><span class="sxs-lookup"><span data-stu-id="028a5-103">Disposition of content</span></span>

><span data-ttu-id="028a5-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="028a5-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="028a5-105">Utilisez l’onglet **disposition** de la **gestion des enregistrements** dans le centre de conformité Microsoft 365 pour gérer les révisions de disposition et afficher les [enregistrements](records-management.md#records) qui ont été supprimés automatiquement à la fin de leur période de rétention.</span><span class="sxs-lookup"><span data-stu-id="028a5-105">Use the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center to manage disposition reviews and view [records](records-management.md#records) that have been automatically deleted at the end of their retention period.</span></span> 

## <a name="prerequisites-for-viewing-content-dispositions"></a><span data-ttu-id="028a5-106">Conditions préalables à l’affichage des suppressions de contenu</span><span class="sxs-lookup"><span data-stu-id="028a5-106">Prerequisites for viewing content dispositions</span></span>

<span data-ttu-id="028a5-107">Pour gérer les révisions de disposition et vérifier que les enregistrements ont été supprimés, vous devez disposer d’autorisations suffisantes et l’audit doit être activé.</span><span class="sxs-lookup"><span data-stu-id="028a5-107">To manage disposition reviews and confirm that records have been deleted, you must have sufficient permissions and auditing must be enabled.</span></span>

### <a name="permissions-for-disposition"></a><span data-ttu-id="028a5-108">Autorisations pour la disposition</span><span class="sxs-lookup"><span data-stu-id="028a5-108">Permissions for disposition</span></span>

<span data-ttu-id="028a5-109">Pour accéder à l’onglet **disposition** dans le centre de conformité Microsoft 365, les utilisateurs doivent disposer du rôle d’administrateur de **gestion** des dispositions.</span><span class="sxs-lookup"><span data-stu-id="028a5-109">To successfully access the **Disposition** tab in the Microsoft 365 compliance center, users must have the **Disposition Management** admin role.</span></span> <span data-ttu-id="028a5-110">Ce rôle est inclus dans les groupes de rôles d’administrateur par défaut, **administrateur de conformité** et administrateur des **données de conformité**.</span><span class="sxs-lookup"><span data-stu-id="028a5-110">This role is included in the default admin role groups, **Compliance Administrator** and **Compliance Data Administrator**.</span></span>

<span data-ttu-id="028a5-111">Pour accorder aux utilisateurs ce rôle de gestion de disposition obligatoire, ajoutez-les à l’un de ces groupes de rôles par défaut ou créez un groupe de rôles personnalisé (par exemple, « Reviewers de disposition ») et accordez à ce groupe le rôle de gestion de disposition.</span><span class="sxs-lookup"><span data-stu-id="028a5-111">To grant users this required Disposition Management role, either add them to one of these default role groups, or create a custom role group (for example, named "Disposition Reviewers") and grant this group the Disposition Management role.</span></span>  

> [!NOTE]
> <span data-ttu-id="028a5-112">Même un administrateur global doit disposer du rôle de **gestion** de la disposition.</span><span class="sxs-lookup"><span data-stu-id="028a5-112">Even a global admin needs to be granted the **Disposition Management** role.</span></span> 

<span data-ttu-id="028a5-113">Pour obtenir des instructions, reportez-vous à la rubrique [Octroi de l’accès au Centre de sécurité et conformité Office 365 aux utilisateurs](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="028a5-113">For instructions, see [Give users access to the Office 365 Security & Compliance Center](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span></span>

### <a name="enable-auditing"></a><span data-ttu-id="028a5-114">Activer l’audit</span><span class="sxs-lookup"><span data-stu-id="028a5-114">Enable auditing</span></span>

<span data-ttu-id="028a5-115">Assurez-vous que l’audit est activé au moins un jour avant la première action de disposition.</span><span class="sxs-lookup"><span data-stu-id="028a5-115">Make sure that auditing is enabled at least one day before the first disposition action.</span></span> <span data-ttu-id="028a5-116">Pour plus d’informations, consultez la rubrique relative [à la recherche dans le journal d’audit dans le centre de sécurité &amp; conformité Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="028a5-116">For more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 

## <a name="disposition-reviews"></a><span data-ttu-id="028a5-117">Révisions avant destruction</span><span class="sxs-lookup"><span data-stu-id="028a5-117">Disposition reviews</span></span>

<span data-ttu-id="028a5-118">Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pour lesquelles vous pouvez souhaiter examiner ce contenu pour décider s’il peut être supprimé en toute sécurité (« supprimé »).</span><span class="sxs-lookup"><span data-stu-id="028a5-118">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed").</span></span> <span data-ttu-id="028a5-119">Par exemple, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="028a5-119">For example, you might need to:</span></span>
  
- <span data-ttu-id="028a5-120">Suspendre la suppression du contenu pertinent en cas de litige ou d’audit.</span><span class="sxs-lookup"><span data-stu-id="028a5-120">Suspend the deletion of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="028a5-121">Supprimer le contenu de la liste de disposition pour le stocker dans une archive, si ce contenu a une recherche ou une valeur historique.</span><span class="sxs-lookup"><span data-stu-id="028a5-121">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="028a5-122">Affecter une période de rétention différente au contenu, peut-être parce que les paramètres de rétention d’origine étaient une solution temporaire ou provisoire.</span><span class="sxs-lookup"><span data-stu-id="028a5-122">Assign a different retention period to the content, perhaps because the original retention settings were a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="028a5-123">Renvoyer le contenu aux clients ou le transférer vers une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="028a5-123">Return the content to clients or transfer it to another organization.</span></span>

<span data-ttu-id="028a5-124">Lorsqu’une révision de disposition est déclenchée à la fin de la période de rétention :</span><span class="sxs-lookup"><span data-stu-id="028a5-124">When a disposition review is triggered at the end of the retention period:</span></span>
  
- <span data-ttu-id="028a5-125">Les personnes que vous choisissez reçoivent une notification par courrier électronique dont le contenu doit être révisé.</span><span class="sxs-lookup"><span data-stu-id="028a5-125">The people you choose receive an email notification that they have content to review.</span></span> <span data-ttu-id="028a5-126">Ces relecteurs peuvent être des utilisateurs individuels ou des groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="028a5-126">These reviewers can be individual users or mail-enabled security groups.</span></span> <span data-ttu-id="028a5-127">Notez que les notifications sont envoyées chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="028a5-127">Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="028a5-128">Les réviseurs accèdent à l’onglet **disposition** dans le centre de conformité Microsoft 365 pour examiner le contenu et décider s’il faut le supprimer définitivement, prolonger sa période de rétention ou appliquer une étiquette de rétention différente.</span><span class="sxs-lookup"><span data-stu-id="028a5-128">The reviewers go to the **Disposition** tab in the Microsoft 365 compliance center to review the content and decide whether to permanently delete it, extend its retention period, or apply a different retention label.</span></span>

<span data-ttu-id="028a5-129">Une révision de disposition peut inclure du contenu dans des boîtes aux lettres Exchange, des sites SharePoint, des comptes OneDrive et des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="028a5-129">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Microsoft 365 groups.</span></span> <span data-ttu-id="028a5-130">Le contenu en attente d’une révision de disposition dans ces emplacements est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="028a5-130">Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>

> [!NOTE]
> <span data-ttu-id="028a5-131">Une boîte aux lettres doit avoir au moins 10 Mo de données pour prendre en charge les révisions de la disposition.</span><span class="sxs-lookup"><span data-stu-id="028a5-131">A mailbox must have at least 10 MB data to support disposition reviews.</span></span>

<span data-ttu-id="028a5-132">Vous pouvez obtenir une vue d’ensemble de toutes les destructions en attente dans l’onglet **vue d’ensemble** . Par exemple :</span><span class="sxs-lookup"><span data-stu-id="028a5-132">You can see an overview of all pending dispositions in the **Overview** tab. For example:</span></span>

![Vue d’ensemble des dépôts en attente dans la gestion des enregistrements](../media/dispositions-overview.png)

<span data-ttu-id="028a5-134">Lorsque vous sélectionnez l’option **afficher toutes les mises en attente**, vous êtes redirigé vers la page de **disposition** .</span><span class="sxs-lookup"><span data-stu-id="028a5-134">When you select the **View all pending dispositions**, you're taken to the **Disposition** page.</span></span> <span data-ttu-id="028a5-135">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="028a5-135">For example:</span></span>

![Page des dispositions dans le centre de conformité Microsoft 365](../media/disposition-tab.png)


### <a name="workflow-for-a-disposition-review"></a><span data-ttu-id="028a5-137">Flux de travail pour une révision de disposition</span><span class="sxs-lookup"><span data-stu-id="028a5-137">Workflow for a disposition review</span></span>

<span data-ttu-id="028a5-138">Le diagramme suivant illustre le flux de travail de base pour une révision de la disposition lorsqu’une étiquette de rétention est publiée, puis appliquée manuellement par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="028a5-138">The following diagram shows the basic workflow for a disposition review when a retention label is published and then manually applied by a user.</span></span> <span data-ttu-id="028a5-139">Par ailleurs, une étiquette de rétention configurée pour une révision de disposition peut être appliquée automatiquement au contenu.</span><span class="sxs-lookup"><span data-stu-id="028a5-139">Alternatively, a retention label configured for a disposition review can be auto-applied to content.</span></span>
  
![Graphique illustrant le flux de fonctionnement de la disposition](../media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="028a5-141">Le déclenchement d’une révision de disposition à la fin de la période de rétention est une option de configuration qui n’est disponible qu’avec une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="028a5-141">Triggering a disposition review at the end of the retention period is a configuration option that's available only with a retention label.</span></span> <span data-ttu-id="028a5-142">Cette option n’est pas disponible pour une stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="028a5-142">This option is not available for a retention policy.</span></span> <span data-ttu-id="028a5-143">Pour plus d’informations sur ces deux solutions de rétention, voir [en savoir plus sur les stratégies de rétention et les étiquettes de conservation](retention.md).</span><span class="sxs-lookup"><span data-stu-id="028a5-143">For more information about these two retention solutions, see [Learn about retention policies and retention labels](retention.md).</span></span>
  
![Paramètres de rétention d’une étiquette](../media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
 
> [!NOTE]
> <span data-ttu-id="028a5-145">Lorsque vous sélectionnez l’option **informer ces personnes lorsque des éléments sont prêts à être examinés**, spécifiez un groupe de sécurité utilisateur ou à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="028a5-145">When you select the option **Notify these people when there are items ready to review**, specify a user or mail-enabled security group.</span></span> <span data-ttu-id="028a5-146">Les groupes Microsoft 365 ([anciennement groupes Office 365](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) ne sont pas pris en charge pour cette option.</span><span class="sxs-lookup"><span data-stu-id="028a5-146">Microsoft 365 groups ([formerly Office 365 groups](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) are not supported for this option.</span></span>

### <a name="viewing-and-disposing-of-content"></a><span data-ttu-id="028a5-147">Affichage et suppression de contenu</span><span class="sxs-lookup"><span data-stu-id="028a5-147">Viewing and disposing of content</span></span>

<span data-ttu-id="028a5-148">Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt à être révisé, il passe à l’onglet **disposition** de la **gestion des enregistrements** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="028a5-148">When a reviewer is notified by email that content is ready to review, they go to the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="028a5-149">Les relecteurs peuvent voir le nombre d’éléments pour chaque étiquette de rétention en attente de destruction, puis sélectionner une étiquette de rétention pour afficher l’ensemble du contenu portant cette étiquette.</span><span class="sxs-lookup"><span data-stu-id="028a5-149">The reviewers can see how many items for each retention label are awaiting disposition, and then select a retention label to see all content with that label.</span></span>

<span data-ttu-id="028a5-150">Une fois que vous avez sélectionné une étiquette de rétention, vous voyez toutes les impositions en attente de cette étiquette à partir de l’onglet **destruction en attente** . Sélectionnez un ou plusieurs éléments dans lesquels vous pouvez choisir une action et entrez un commentaire de justification :</span><span class="sxs-lookup"><span data-stu-id="028a5-150">After you select a retention label, you then see all pending dispositions for that label from the **Pending disposition** tab. Select one or more items where you can then choose an action and enter a justification comment:</span></span>

![Options de disposition](../media/retention-disposition-options.png)

<span data-ttu-id="028a5-152">Comme vous pouvez le voir à partir de l’image, les actions prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="028a5-152">As you can see from the picture, the actions supported are:</span></span> 
  
- <span data-ttu-id="028a5-153">Supprimer définitivement l’élément</span><span class="sxs-lookup"><span data-stu-id="028a5-153">Permanently delete the item</span></span>
- <span data-ttu-id="028a5-154">Prolonger la période de rétention</span><span class="sxs-lookup"><span data-stu-id="028a5-154">Extend the retention period</span></span>
- <span data-ttu-id="028a5-155">Appliquer une étiquette de rétention différente</span><span class="sxs-lookup"><span data-stu-id="028a5-155">Apply a different retention label</span></span>

<span data-ttu-id="028a5-156">En vous fournissant des autorisations sur l’emplacement et le contenu, vous pouvez utiliser le lien dans la colonne **emplacement** pour afficher les documents à leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="028a5-156">Providing you have permissions to the location and the content, you can use the link in the **Location** column to view documents in their original location.</span></span> <span data-ttu-id="028a5-157">Lors d’une révision de destruction, le contenu ne se déplace jamais à partir de son emplacement d’origine et n’est jamais supprimé tant que le relecteur n’a pas choisi de le faire.</span><span class="sxs-lookup"><span data-stu-id="028a5-157">During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>

<span data-ttu-id="028a5-158">Les notifications par courrier électronique sont envoyées automatiquement aux relecteurs chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="028a5-158">The email notifications are sent automatically to reviewers on a weekly basis.</span></span> <span data-ttu-id="028a5-159">Ce processus planifié signifie que lorsque le contenu atteint la fin de sa période de rétention, il peut falloir jusqu’à sept jours pour que les relecteurs reçoivent la notification par courrier électronique que le contenu attend.</span><span class="sxs-lookup"><span data-stu-id="028a5-159">This scheduled process means that when content reaches the end of its retention period, it might take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="028a5-160">Toutes les actions de disposition peuvent être auditées et le texte de justification entré par le réviseur est enregistré et affiché dans la colonne **Commentaire** de la page **éléments supprimés** .</span><span class="sxs-lookup"><span data-stu-id="028a5-160">All disposition actions can be audited and the justification text entered by the reviewer is saved and displayed in the **Comment** column on the **Disposed items** page.</span></span>
  
### <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="028a5-161">Durée jusqu’à la suppression définitive du contenu supprimé</span><span class="sxs-lookup"><span data-stu-id="028a5-161">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="028a5-162">Le contenu en attente d’une révision de disposition est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="028a5-162">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content.</span></span> <span data-ttu-id="028a5-163">Lorsque le réviseur choisit cette option, le contenu du site SharePoint ou du compte OneDrive est éligible pour le processus de nettoyage standard décrit dans la rubrique [fonctionnement des paramètres de rétention avec du contenu sur place](retention.md#how-retention-settings-work-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="028a5-163">When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in [How retention settings work with content in place](retention.md#how-retention-settings-work-with-content-in-place).</span></span>

## <a name="disposition-of-records"></a><span data-ttu-id="028a5-164">Destruction des enregistrements</span><span class="sxs-lookup"><span data-stu-id="028a5-164">Disposition of records</span></span>

> [!NOTE]
> <span data-ttu-id="028a5-165">Le déploiement de la preuve de la suppression des enregistrements dans SharePoint et OneDrive est terminé.</span><span class="sxs-lookup"><span data-stu-id="028a5-165">The rollout for proof of disposal for records in SharePoint and OneDrive is complete.</span></span>
>
> <span data-ttu-id="028a5-166">Le déploiement de la preuve de la suppression des enregistrements dans Exchange est presque terminé lorsque nous supprimons cette note.</span><span class="sxs-lookup"><span data-stu-id="028a5-166">Rollout for proof of disposal for records in Exchange is almost complete when we will remove this note.</span></span>

<span data-ttu-id="028a5-167">Utilisez l’onglet **disposition** de la page **gestion des enregistrements** pour identifier les enregistrements qui sont désormais supprimés, automatiquement ou après une révision de destruction.</span><span class="sxs-lookup"><span data-stu-id="028a5-167">Use the **Disposition** tab from the **Records Management** page to identify records that are now deleted, either automatically or after a disposition review.</span></span> <span data-ttu-id="028a5-168">Ces éléments affichent les **enregistrements supprimés** dans la colonne **type** .</span><span class="sxs-lookup"><span data-stu-id="028a5-168">These items display **Records Disposed** in the **Type** column.</span></span> <span data-ttu-id="028a5-169">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="028a5-169">For example:</span></span>

![Éléments qui ont été supprimés sans révision de disposition](../media/records-disposed2.png)

<span data-ttu-id="028a5-171">Les éléments affichés sous l’onglet **éléments supprimés** pour les étiquettes d’enregistrement sont conservés pendant une période maximale de sept ans après la suppression de l’élément, avec une limite de 1 million éléments par enregistrement pour cette période.</span><span class="sxs-lookup"><span data-stu-id="028a5-171">Items that are shown in the **Disposed Items** tab for record labels are kept for up to seven years after the item was disposed, with a limit of one million items per record for that period.</span></span> <span data-ttu-id="028a5-172">Si vous voyez le nombre **total** proche de cette limite de 1 million et que vous avez besoin de preuves d’imposition pour vos enregistrements, contactez le [support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="028a5-172">If you see the **Count** number nearing this limit of one million, and you need proof of disposition for your records, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

> [!NOTE]
> <span data-ttu-id="028a5-173">Cette fonctionnalité est basée sur les informations du [Journal d’audit unifié](search-the-audit-log-in-security-and-compliance.md) et nécessite donc un audit pour être [activé et](turn-audit-log-search-on-or-off.md) utilisable dans une requête afin que les événements correspondants soient capturés.</span><span class="sxs-lookup"><span data-stu-id="028a5-173">This functionality is based on information from the [unified audit log](search-the-audit-log-in-security-and-compliance.md) and therefore requires auditing to be [enabled and searchable](turn-audit-log-search-on-or-off.md) so the corresponding events are captured.</span></span>
    
## <a name="filter-and-export-the-views"></a><span data-ttu-id="028a5-174">Filtrer et exporter les vues</span><span class="sxs-lookup"><span data-stu-id="028a5-174">Filter and export the views</span></span>

<span data-ttu-id="028a5-175">Lorsque vous sélectionnez une étiquette de rétention à partir de la page de **disposition** , l’onglet **destruction en attente** (le cas échéant) et l’onglet **éléments supprimés** vous permettent de filtrer les affichages pour faciliter la recherche des éléments.</span><span class="sxs-lookup"><span data-stu-id="028a5-175">When you select a retention label from the **Disposition** page, the **Pending disposition** tab (if applicable) and the **Disposed items** tab let you filter the views to help you more easily find items.</span></span> 

<span data-ttu-id="028a5-176">Pour les impositions en attente, la plage horaire est basée sur la date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="028a5-176">For pending dispositions, the time range is based on the expiration date.</span></span> <span data-ttu-id="028a5-177">Pour les éléments supprimés, la plage horaire est basée sur la date de suppression.</span><span class="sxs-lookup"><span data-stu-id="028a5-177">For disposed items, the time range is based on the deletion date.</span></span>
  
<span data-ttu-id="028a5-178">Vous pouvez exporter des informations sur les éléments de l’affichage en tant que fichier. csv que vous pouvez ensuite trier et gérer à l’aide d’Excel :</span><span class="sxs-lookup"><span data-stu-id="028a5-178">You can export information about the items in either view as a .csv file that you can then sort and manage using Excel:</span></span>

![Exportation de l’option de destruction](../media/retention-export-option.png)
  
![Données de disposition exportées dans Excel](../media/08e3bc09-b132-47b4-a051-a590b697e725.png)


