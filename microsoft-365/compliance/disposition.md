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
ms.openlocfilehash: 47cb8f023f378796f206e436aa33e74b2993ac97
ms.sourcegitcommit: 9d8816ddc3a97676ff947db80265e47b734f5462
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "43952617"
---
# <a name="disposition-of-content"></a><span data-ttu-id="12d39-103">Disposition de contenu</span><span class="sxs-lookup"><span data-stu-id="12d39-103">Disposition of content</span></span>

><span data-ttu-id="12d39-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="12d39-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="12d39-105">Utilisez l’onglet **disposition** de la **gestion des enregistrements** dans le centre de conformité Microsoft 365 pour gérer les révisions de disposition et afficher les [enregistrements](records.md) qui ont été supprimés automatiquement à la fin de leur période de rétention.</span><span class="sxs-lookup"><span data-stu-id="12d39-105">Use the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center to manage disposition reviews and view [records](records.md) that have been automatically deleted at the end of their retention period.</span></span> 

## <a name="prerequisites-for-viewing-content-dispositions"></a><span data-ttu-id="12d39-106">Conditions préalables à l’affichage des suppressions de contenu</span><span class="sxs-lookup"><span data-stu-id="12d39-106">Prerequisites for viewing content dispositions</span></span>

<span data-ttu-id="12d39-107">Pour gérer les révisions de disposition et vérifier que les enregistrements ont été supprimés, vous devez disposer d’autorisations suffisantes et l’audit doit être activé.</span><span class="sxs-lookup"><span data-stu-id="12d39-107">To manage disposition reviews and confirm that records have been deleted, you must have sufficient permissions and auditing must be enabled.</span></span>

### <a name="permissions-for-disposition"></a><span data-ttu-id="12d39-108">Autorisations pour la disposition</span><span class="sxs-lookup"><span data-stu-id="12d39-108">Permissions for disposition</span></span>

<span data-ttu-id="12d39-109">Pour accéder à l’onglet **disposition** dans le centre de conformité Microsoft 365, vous devez être membre du rôle **gestion** de la disposition et du rôle **journaux d’audit en affichage seul** .</span><span class="sxs-lookup"><span data-stu-id="12d39-109">To successfully access the **Disposition** tab in the Microsoft 365 compliance center, you must be members of the **Disposition Management** role and the **View-Only Audit Logs** role.</span></span> <span data-ttu-id="12d39-110">Nous vous recommandons de créer un nouveau groupe de rôles appelé **Relecteurs de disposition**et d’ajouter ces deux rôles à ce groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="12d39-110">We recommend creating a new role group called **Disposition Reviewers**, and add these two roles to that role group.</span></span> 

<span data-ttu-id="12d39-111">Spécifique au rôle **journaux d’audit en affichage seul** :</span><span class="sxs-lookup"><span data-stu-id="12d39-111">Specific to the **View-Only Audit Logs** role:</span></span>

- <span data-ttu-id="12d39-112">Étant donné que la cmdlet sous-jacente utilisée pour effectuer des recherches dans le journal d’audit est une applet de commande Exchange Online, vous devez attribuer ce rôle à des utilisateurs à l’aide du [Centre d’administration Exchange dans Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center), plutôt qu’en utilisant la page des **autorisations** dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="12d39-112">Because the underlying cmdlet used to search the audit log is an Exchange Online cmdlet, you must assign users this role by using the [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center), rather than by using the **Permissions** page in the Security & Compliance Center.</span></span> <span data-ttu-id="12d39-113">Pour obtenir des instructions, consultez la rubrique [gérer des groupes de rôles dans Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span><span class="sxs-lookup"><span data-stu-id="12d39-113">For instructions, see [Manage role groups in Exchange Online](https://docs.microsoft.com/Exchange/permissions-exo/role-groups).</span></span>

- <span data-ttu-id="12d39-114">Les groupes Microsoft 365 ([anciennement groupes Office 365](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) ne sont pas pris en charge pour ce rôle.</span><span class="sxs-lookup"><span data-stu-id="12d39-114">Microsoft 365 Groups ([formerly Office 365 Groups](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) aren't supported for this role.</span></span> <span data-ttu-id="12d39-115">Attribuez plutôt des boîtes aux lettres utilisateur, des utilisateurs de messagerie ou des groupes de sécurité à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="12d39-115">Instead, assign user mailboxes, mail users, or mail-enabled security groups.</span></span>

<span data-ttu-id="12d39-116">Pour obtenir des instructions permettant d’accorder aux utilisateurs le rôle de **gestion de disposition** et de créer votre rôle de **réviseur de disposition** , consultez la rubrique accorder aux utilisateurs l' [accès au centre de sécurité &amp; conformité Office 365](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="12d39-116">For instructions to grant users the **Disposition Management** role and create your new **Disposition Reviewers** role, see [Give users access to the Office 365 Security &amp; Compliance Center](../security/office-365-security/grant-access-to-the-security-and-compliance-center.md).</span></span>

### <a name="enable-auditing"></a><span data-ttu-id="12d39-117">Activer l’audit</span><span class="sxs-lookup"><span data-stu-id="12d39-117">Enable auditing</span></span>

<span data-ttu-id="12d39-118">Assurez-vous que l’audit est activé au moins un jour avant la première action de disposition.</span><span class="sxs-lookup"><span data-stu-id="12d39-118">Make sure that auditing is enabled at least one day before the first disposition action.</span></span> <span data-ttu-id="12d39-119">Pour plus d’informations, consultez la rubrique relative [à la recherche dans le &amp; journal d’audit dans le centre de sécurité conformité Office 365](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="12d39-119">For more information, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span> 

## <a name="disposition-reviews"></a><span data-ttu-id="12d39-120">Révisions avant destruction</span><span class="sxs-lookup"><span data-stu-id="12d39-120">Disposition reviews</span></span>

<span data-ttu-id="12d39-121">Lorsque le contenu atteint la fin de sa période de rétention, il existe plusieurs raisons pour lesquelles vous pouvez souhaiter examiner ce contenu pour décider s’il peut être supprimé en toute sécurité (« supprimé »).</span><span class="sxs-lookup"><span data-stu-id="12d39-121">When content reaches the end of its retention period, there are several reasons why you might want to review that content to decide whether it can be safely deleted ("disposed").</span></span> <span data-ttu-id="12d39-122">Par exemple, vous devrez peut-être :</span><span class="sxs-lookup"><span data-stu-id="12d39-122">For example, you might need to:</span></span>
  
- <span data-ttu-id="12d39-123">Suspendre la suppression du contenu pertinent en cas de litige ou d’audit.</span><span class="sxs-lookup"><span data-stu-id="12d39-123">Suspend the deletion of relevant content in the event of litigation or an audit.</span></span>
    
- <span data-ttu-id="12d39-124">Supprimer le contenu de la liste de disposition pour le stocker dans une archive, si ce contenu a une recherche ou une valeur historique.</span><span class="sxs-lookup"><span data-stu-id="12d39-124">Remove content from the disposition list to store in an archive, if that content has research or historical value.</span></span>
    
- <span data-ttu-id="12d39-125">Affecter une période de rétention différente au contenu, peut-être parce que les paramètres de rétention d’origine étaient une solution temporaire ou provisoire.</span><span class="sxs-lookup"><span data-stu-id="12d39-125">Assign a different retention period to the content, perhaps because the original retention settings were a temporary or provisional solution.</span></span>
    
- <span data-ttu-id="12d39-126">Renvoyer le contenu aux clients ou le transférer vers une autre organisation.</span><span class="sxs-lookup"><span data-stu-id="12d39-126">Return the content to clients or transfer it to another organization.</span></span>

<span data-ttu-id="12d39-127">Lorsqu’une révision de disposition est déclenchée à la fin de la période de rétention :</span><span class="sxs-lookup"><span data-stu-id="12d39-127">When a disposition review is triggered at the end of the retention period:</span></span>
  
- <span data-ttu-id="12d39-128">Les personnes que vous choisissez reçoivent une notification par courrier électronique dont le contenu doit être révisé.</span><span class="sxs-lookup"><span data-stu-id="12d39-128">The people you choose receive an email notification that they have content to review.</span></span> <span data-ttu-id="12d39-129">Ces relecteurs peuvent être des utilisateurs individuels, des groupes de distribution ou des groupes de sécurité ou des groupes Office 365.</span><span class="sxs-lookup"><span data-stu-id="12d39-129">These reviewers can be individual users, distribution or security groups, or Office 365 groups.</span></span> <span data-ttu-id="12d39-130">Notez que les notifications sont envoyées chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="12d39-130">Note that notifications are sent on a weekly basis.</span></span>
    
- <span data-ttu-id="12d39-131">Les réviseurs accèdent à l’onglet **disposition** dans le centre de conformité Microsoft 365 pour examiner le contenu et décider s’il faut le supprimer définitivement, prolonger sa période de rétention ou appliquer une étiquette de rétention différente.</span><span class="sxs-lookup"><span data-stu-id="12d39-131">The reviewers go to the **Disposition** tab in the Microsoft 365 compliance center to review the content and decide whether to permanently delete it, extend its retention period, or apply a different retention label.</span></span>

<span data-ttu-id="12d39-132">Une révision de disposition peut inclure du contenu dans des boîtes aux lettres Exchange, des sites SharePoint, des comptes OneDrive et des groupes Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="12d39-132">A disposition review can include content in Exchange mailboxes, SharePoint sites, OneDrive accounts, and Microsoft 365 groups.</span></span> <span data-ttu-id="12d39-133">Le contenu en attente d’une révision de disposition dans ces emplacements est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="12d39-133">Content awaiting a disposition review in those locations is deleted only after a reviewer chooses to permanently delete the content.</span></span>

<span data-ttu-id="12d39-134">Vous pouvez obtenir une vue d’ensemble de toutes les destructions en attente dans l’onglet **vue d’ensemble** . Par exemple :</span><span class="sxs-lookup"><span data-stu-id="12d39-134">You can see an overview of all pending dispositions in the **Overview** tab. For example:</span></span>

![Vue d’ensemble des dépôts en attente dans la gestion des enregistrements](../media/dispositions-overview.png)

<span data-ttu-id="12d39-136">Lorsque vous sélectionnez l’option **afficher toutes les mises en attente**, vous êtes redirigé vers la page de **disposition** .</span><span class="sxs-lookup"><span data-stu-id="12d39-136">When you select the **View all pending dispositions**, you're taken to the **Disposition** page.</span></span> <span data-ttu-id="12d39-137">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="12d39-137">For example:</span></span>

![Page des dispositions dans le centre de conformité Microsoft 365](../media/disposition-tab.png)


### <a name="workflow-for-a-disposition-review"></a><span data-ttu-id="12d39-139">Flux de travail pour une révision de disposition</span><span class="sxs-lookup"><span data-stu-id="12d39-139">Workflow for a disposition review</span></span>

<span data-ttu-id="12d39-140">Il s’agit du flux de travail de base pour une révision de la disposition lorsqu’une étiquette de rétention est publiée, puis appliquée manuellement par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12d39-140">This is the basic workflow for a disposition review when a retention label is published and then manually applied by a user.</span></span> <span data-ttu-id="12d39-141">Par ailleurs, une étiquette de rétention configurée pour une révision de disposition peut être appliquée automatiquement au contenu.</span><span class="sxs-lookup"><span data-stu-id="12d39-141">Alternatively, a retention label configured for a disposition review can be auto-applied to content.</span></span>
  
![Graphique illustrant le flux de fonctionnement de la disposition](../media/5fb3f33a-cb53-468c-becc-6dda0ec52778.png)
  
<span data-ttu-id="12d39-143">Le déclenchement d’une révision de disposition à la fin de la période de rétention est une option de configuration qui n’est disponible qu’avec une [étiquette de rétention](labels.md).</span><span class="sxs-lookup"><span data-stu-id="12d39-143">Triggering a disposition review at the end of the retention period is a configuration option that's available only with a [retention label](labels.md).</span></span> <span data-ttu-id="12d39-144">Cette option n’est pas disponible dans une stratégie de rétention.</span><span class="sxs-lookup"><span data-stu-id="12d39-144">This option is not available in a retention policy.</span></span>
  
![Paramètres de rétention d’une étiquette](../media/a16dd202-8862-40ac-80ff-6fee974de5da.png)
 
> [!NOTE]
> <span data-ttu-id="12d39-146">Lorsque vous sélectionnez l’option **informer ces personnes lorsque des éléments sont prêts à être examinés**, spécifiez un groupe de sécurité utilisateur ou à extension messagerie.</span><span class="sxs-lookup"><span data-stu-id="12d39-146">When you select the option **Notify these people when there are items ready to review**, specify a user or mail-enabled security group.</span></span> <span data-ttu-id="12d39-147">Les groupes Microsoft 365 ([anciennement groupes Office 365](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) ne sont pas pris en charge pour cette option.</span><span class="sxs-lookup"><span data-stu-id="12d39-147">Microsoft 365 groups ([formerly Office 365 groups](https://techcommunity.microsoft.com/t5/microsoft-365-blog/office-365-groups-will-become-microsoft-365-groups/ba-p/1303601)) are not supported for this option.</span></span>

### <a name="viewing-and-disposing-of-content"></a><span data-ttu-id="12d39-148">Affichage et suppression de contenu</span><span class="sxs-lookup"><span data-stu-id="12d39-148">Viewing and disposing of content</span></span>

<span data-ttu-id="12d39-149">Lorsqu’un réviseur est averti par courrier électronique que le contenu est prêt à être révisé, il passe à l’onglet **disposition** de la **gestion des enregistrements** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="12d39-149">When a reviewer is notified by email that content is ready to review, they go to the **Disposition** tab from **Records Management** in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="12d39-150">Les relecteurs peuvent voir le nombre d’éléments pour chaque étiquette de rétention en attente de destruction, puis sélectionner une étiquette de rétention pour afficher l’ensemble du contenu portant cette étiquette.</span><span class="sxs-lookup"><span data-stu-id="12d39-150">The reviewers can see how many items for each retention label are awaiting disposition, and then select a retention label to see all content with that label.</span></span>

<span data-ttu-id="12d39-151">Une fois que vous avez sélectionné une étiquette de rétention, vous voyez toutes les impositions en attente de cette étiquette à partir de l’onglet **destruction en attente** . Sélectionnez un ou plusieurs éléments où vous pouvez choisir une action et entrez un commentaire de justification :</span><span class="sxs-lookup"><span data-stu-id="12d39-151">After you select a retention label, you then see all pending dispositions for that label from the **Pending disposition** tab. Select one or more items where you can then choose an action and enter a justification comment:</span></span>

![Options de disposition](../media/retention-disposition-options.png)

<span data-ttu-id="12d39-153">Comme vous pouvez le voir à partir de l’image, les actions prises en charge sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="12d39-153">As you can see from the picture, the actions supported are:</span></span> 
  
- <span data-ttu-id="12d39-154">Supprimer définitivement l’élément</span><span class="sxs-lookup"><span data-stu-id="12d39-154">Permanently delete the item</span></span>
- <span data-ttu-id="12d39-155">Prolonger la période de rétention</span><span class="sxs-lookup"><span data-stu-id="12d39-155">Extend the retention period</span></span>
- <span data-ttu-id="12d39-156">Appliquer une étiquette de rétention différente</span><span class="sxs-lookup"><span data-stu-id="12d39-156">Apply a different retention label</span></span>

<span data-ttu-id="12d39-157">En vous fournissant des autorisations sur l’emplacement et le contenu, vous pouvez utiliser le lien dans la colonne **emplacement** pour afficher les documents à leur emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="12d39-157">Providing you have permissions to the location and the content, you can use the link in the **Location** column to view documents in their original location.</span></span> <span data-ttu-id="12d39-158">Lors d’une révision de destruction, le contenu ne se déplace jamais à partir de son emplacement d’origine et n’est jamais supprimé tant que le relecteur n’a pas choisi de le faire.</span><span class="sxs-lookup"><span data-stu-id="12d39-158">During a disposition review, the content never moves from its original location, and it's never deleted until the reviewer chooses to do so.</span></span>
  
<span data-ttu-id="12d39-159">Les notifications par courrier électronique sont envoyées automatiquement aux relecteurs chaque semaine.</span><span class="sxs-lookup"><span data-stu-id="12d39-159">The email notifications are sent automatically to reviewers on a weekly basis.</span></span> <span data-ttu-id="12d39-160">Ce processus planifié signifie que lorsque le contenu atteint la fin de sa période de rétention, il peut falloir jusqu’à sept jours pour que les relecteurs reçoivent la notification par courrier électronique que le contenu attend.</span><span class="sxs-lookup"><span data-stu-id="12d39-160">This scheduled process means that when content reaches the end of its retention period, it might take up to seven days for reviewers to receive the email notification that content is awaiting disposition.</span></span>
  
<span data-ttu-id="12d39-161">Toutes les actions de disposition peuvent être auditées.</span><span class="sxs-lookup"><span data-stu-id="12d39-161">All disposition actions can be audited.</span></span>
  
### <a name="how-long-until-disposed-content-is-permanently-deleted"></a><span data-ttu-id="12d39-162">Durée jusqu’à la suppression définitive du contenu supprimé</span><span class="sxs-lookup"><span data-stu-id="12d39-162">How long until disposed content is permanently deleted</span></span>

<span data-ttu-id="12d39-163">Le contenu en attente d’une révision de disposition est supprimé uniquement lorsqu’un relecteur choisit de supprimer définitivement le contenu.</span><span class="sxs-lookup"><span data-stu-id="12d39-163">Content awaiting a disposition review is deleted only after a reviewer chooses to permanently delete the content.</span></span> <span data-ttu-id="12d39-164">Lorsque le réviseur choisit cette option, le contenu du site SharePoint ou du compte OneDrive devient éligible pour le processus de nettoyage standard décrit dans la [manière dont une stratégie de rétention fonctionne avec le contenu en place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span><span class="sxs-lookup"><span data-stu-id="12d39-164">When the reviewer chooses this option, the content in the SharePoint site or OneDrive account becomes eligible for the standard cleanup process described in [How a retention policy works with content in place](retention-policies.md#how-a-retention-policy-works-with-content-in-place).</span></span>

## <a name="disposition-of-records"></a><span data-ttu-id="12d39-165">Destruction des enregistrements</span><span class="sxs-lookup"><span data-stu-id="12d39-165">Disposition of records</span></span>

> [!NOTE]
> <span data-ttu-id="12d39-166">La possibilité d’afficher des enregistrements qui ont été supprimés automatiquement sans révision de disposition est progressivement déployée sur les clients en avril et le 2020 mai, de sorte que vous ne verrez peut-être pas cette expérience immédiatement.</span><span class="sxs-lookup"><span data-stu-id="12d39-166">The ability to see records that were automatically deleted without a disposition review is gradually rolling out to tenants during April and May 2020, so you might not see this experience immediately.</span></span>

<span data-ttu-id="12d39-167">Utilisez l’onglet **disposition** de la page **gestion des enregistrements** pour identifier les enregistrements supprimés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="12d39-167">Use the **Disposition** tab from the **Records Management** page to identify records that are automatically deleted.</span></span> <span data-ttu-id="12d39-168">Ces éléments affichent les **enregistrements supprimés** dans la colonne **type** .</span><span class="sxs-lookup"><span data-stu-id="12d39-168">These items display **Records Disposed** in the **Type** column.</span></span> <span data-ttu-id="12d39-169">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="12d39-169">For example:</span></span>

![Éléments qui ont été supprimés sans révision de disposition](../media/records-disposed2.png)

<span data-ttu-id="12d39-171">Les éléments affichés dans l’onglet **éléments supprimés** pour les étiquettes d’enregistrement sont conservés pendant une période maximale de 7 ans après la suppression de l’élément, avec une limite de 1 million éléments par enregistrement pour cette période.</span><span class="sxs-lookup"><span data-stu-id="12d39-171">Items that are shown in the **Disposed Items** tab for record labels are kept for up to 7 years after the item was disposed, with a limit of one million items per record for that period.</span></span> <span data-ttu-id="12d39-172">Si vous voyez le nombre **total** proche de cette limite de 1 million et que vous avez besoin de preuves d’imposition pour vos enregistrements, contactez le [support Microsoft](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span><span class="sxs-lookup"><span data-stu-id="12d39-172">If you see the **Count** number nearing this limit of one million, and you need proof of disposition for your records, contact [Microsoft Support](https://docs.microsoft.com/office365/admin/contact-support-for-business-products).</span></span>

> [!NOTE]
> <span data-ttu-id="12d39-173">Cette fonctionnalité est basée sur les informations du [Journal d’audit unifié](search-the-audit-log-in-security-and-compliance.md) et nécessite donc un audit pour être [activé et](turn-audit-log-search-on-or-off.md) utilisable dans une requête afin que les événements correspondants soient capturés.</span><span class="sxs-lookup"><span data-stu-id="12d39-173">This functionality is based on information from the [unified audit log](search-the-audit-log-in-security-and-compliance.md) and therefore requires auditing to be [enabled and searchable](turn-audit-log-search-on-or-off.md) so the corresponding events are captured.</span></span>
    
## <a name="filter-and-export-the-views"></a><span data-ttu-id="12d39-174">Filtrer et exporter les vues</span><span class="sxs-lookup"><span data-stu-id="12d39-174">Filter and export the views</span></span>

<span data-ttu-id="12d39-175">Lorsque vous sélectionnez une étiquette de rétention à partir de la page de **disposition** , l’onglet **destruction en attente** (le cas échéant) et l’onglet **éléments supprimés** vous permettent de filtrer les affichages pour faciliter la recherche des éléments.</span><span class="sxs-lookup"><span data-stu-id="12d39-175">When you select a retention label from the **Disposition** page, the **Pending disposition** tab (if applicable) and the **Disposed items** tab let you filter the views to help you more easily find items.</span></span> 

<span data-ttu-id="12d39-176">Pour les impositions en attente, la plage horaire est basée sur la date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="12d39-176">For pending dispositions, the time range is based on the expiration date.</span></span> <span data-ttu-id="12d39-177">Pour les éléments supprimés, la plage horaire est basée sur la date de suppression.</span><span class="sxs-lookup"><span data-stu-id="12d39-177">For disposed items, the time range is based on the deletion date.</span></span>
  
<span data-ttu-id="12d39-178">Vous pouvez exporter des informations sur les éléments de l’affichage en tant que fichier. csv que vous pouvez ensuite trier et gérer à l’aide d’Excel :</span><span class="sxs-lookup"><span data-stu-id="12d39-178">You can export information about the items in either view as a .csv file that you can then sort and manage using Excel:</span></span>

![Exportation de l’option de destruction](../media/retention-export-option.png)
  
![Données de disposition exportées dans Excel](../media/08e3bc09-b132-47b4-a051-a590b697e725.png)


