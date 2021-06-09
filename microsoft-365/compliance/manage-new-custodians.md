---
title: Gérer les dépositaires dans un Advanced eDiscovery de gestion
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
description: Découvrez comment afficher les détails, modifier et modifier en bloc la liste des dépositaires dans Advanced eDiscovery cas.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: a1e9e9d481073c8bb2827d5d65537dbf2b63ef1f
ms.sourcegitcommit: 555b200b618085706dabf8648d27fb6d6427cfce
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/30/2020
ms.locfileid: "49739867"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a><span data-ttu-id="6ccaa-103">Gérer les dépositaires dans un Advanced eDiscovery de gestion</span><span class="sxs-lookup"><span data-stu-id="6ccaa-103">Manage custodians in an Advanced eDiscovery case</span></span>

<span data-ttu-id="6ccaa-104">La page Des dépositaires sous l’onglet **Sources** dans un cas Advanced eDiscovery contient la liste de tous les dépositaires qui ont été ajoutés au cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-104">The Custodians page on the **Sources** tab in an Advanced eDiscovery case contains a list of all custodians that have been added to the case.</span></span> <span data-ttu-id="6ccaa-105">Une fois que vous avez ajouté des dépositaires à un cas, les détails sur chaque dépositaire sont collectés automatiquement à partir de Azure Active Directory et sont consultables dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-105">After you add custodians to a case, details about each custodian are automatically collected from Azure Active Directory and are viewable in Advanced eDiscovery.</span></span>

![Gérer les dépositaires](../media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a><span data-ttu-id="6ccaa-107">Afficher les détails du dépositaire</span><span class="sxs-lookup"><span data-stu-id="6ccaa-107">View custodian details</span></span>

<span data-ttu-id="6ccaa-108">Pour afficher les détails sur un dépositaire, cliquez sur le dépositaire dans la liste sous **l’onglet Dépositaires.** Une page de présentation s’affiche et contient les informations suivantes sur le dépositaire :</span><span class="sxs-lookup"><span data-stu-id="6ccaa-108">To view the details about a custodian, click the custodian from the list on the **Custodians** tab. A flyout page is displayed and contains the following information about the custodian:</span></span>

- <span data-ttu-id="6ccaa-109">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="6ccaa-109">Contact information</span></span>

  - <span data-ttu-id="6ccaa-110">**Nom complet** : nom affiché dans le carnet d’adresses du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-110">**Display Name** - The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="6ccaa-111">Il s’agit généralement de la combinaison du prénom, de l’initiale du deuxième prénom et du nom du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-111">This is usually the combination of the custodian's first name, middle initial, and last name.</span></span>
  
   - <span data-ttu-id="6ccaa-112">**Courrier/SMTP :** adresse SMTP principale du dépositaire, par exemple, brianj@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-112">**Mail/SMTP** - The primary SMTP address for the custodian, for example, brianj@contoso.onmicrosoft.com.</span></span> <span data-ttu-id="6ccaa-113">Le nom d’utilisateur principal (UPN) du dépositaire est également répertorié.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-113">The custodian's user principal name (UPN) is also listed.</span></span>

  - <span data-ttu-id="6ccaa-114">**Titre** : fonction du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-114">**Title** - The custodian's job title.</span></span>

  - <span data-ttu-id="6ccaa-115">**Service** : nom du service dans lequel travaille le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-115">**Department** - The name for the department in which the custodian works.</span></span>

  - <span data-ttu-id="6ccaa-116">**Responsable** : responsable du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-116">**Manager** - The custodian's manager.</span></span> <span data-ttu-id="6ccaa-117">Le responsable désigné recevra toutes les communications d’escalade pour ce dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-117">The designated manager will receive any escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="6ccaa-118">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="6ccaa-118">Location information</span></span>

  - <span data-ttu-id="6ccaa-119">**Ville** - ville dans laquelle se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-119">**City** - The city in which the custodian is located.</span></span>

  - <span data-ttu-id="6ccaa-120">**État** : état ou province dans l’adresse du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-120">**State** - The state or province in the custodian's address.</span></span>

  - <span data-ttu-id="6ccaa-121">**Pays/région** : pays/région où se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-121">**Country/Region** - The country/region where the custodian is located.</span></span>

  - <span data-ttu-id="6ccaa-122">**Office** : emplacement du bureau du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-122">**Office** - The office location in the custodian's place of business.</span></span>

- <span data-ttu-id="6ccaa-123">Informations de cas</span><span class="sxs-lookup"><span data-stu-id="6ccaa-123">Case information</span></span>

  - <span data-ttu-id="6ccaa-124">**Statut de conservation** : indique si le dépositaire a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-124">**Hold status** - Indicates if the custodian has been placed on hold.</span></span> 

  - <span data-ttu-id="6ccaa-125">**État de** la communication : indique si le dépositaire a reçu un avis de conservation.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-125">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="6ccaa-126">Si le dépositaire a reçu un avis, cette valeur de cette propriété est **Publiée**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-126">If the custodian has been issued a notice, this value of this property is **Published**.</span></span> <span data-ttu-id="6ccaa-127">Si le dépositaire n’a pas reçu d’avis, l’état **est Non publié**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-127">If the custodian has not been issued a notice, the status is **Un-published**.</span></span> 

  - <span data-ttu-id="6ccaa-128">**État** : état du dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-128">**Status** - The status of the custodian within the case.</span></span> <span data-ttu-id="6ccaa-129">L’état **Actif** indique que le dépositaire fait partie du cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-129">A status of **Active** indicates that the custodian is part of the case.</span></span> <span data-ttu-id="6ccaa-130">Si un dépositaire est libéré d’un cas, l’état est modifié en **Released**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-130">If a custodian is released from a case, the status is changed to **Released**.</span></span> 

- <span data-ttu-id="6ccaa-131">Sources de données et informations d’indexation</span><span class="sxs-lookup"><span data-stu-id="6ccaa-131">Data sources and indexing information</span></span>

    - <span data-ttu-id="6ccaa-132">**Sources de** données : indique le nombre et le type de sources de données (boîtes aux lettres, sites et Teams) qui sont associées au dépositaire et qui font partie du cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-132">**Data sources** - Shows the count and type of data sources (mailboxes, sites, and Teams) that are associated with the custodian and are part of the case.</span></span>

    - <span data-ttu-id="6ccaa-133">**Heure de mise à jour** de l’index : indique l’heure et la date du dernier déclenchement de la tâche d’indexation avancée.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-133">**Index updated time** - Indicates the time and date for when the advanced indexing job was last triggered.</span></span> <span data-ttu-id="6ccaa-134">Cette propriété indique également quand le processus d’indexation avancé est en cours.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-134">This property will also indicate when the advanced indexing process is currently in progress.</span></span>


## <a name="edit-a-custodian"></a><span data-ttu-id="6ccaa-135">Modifier un dépositaire</span><span class="sxs-lookup"><span data-stu-id="6ccaa-135">Edit a custodian</span></span>

<span data-ttu-id="6ccaa-136">Au fur et à mesure de la progression de votre cas, vous pouvez découvrir qu’il peut y avoir d’autres sources de données pertinentes pour un dépositaire spécifique & votre cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-136">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="6ccaa-137">Dans d’autres scénarios, vous pouvez supprimer certaines sources de données qui ont été examinées et considérées comme non pertinentes.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-137">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="6ccaa-138">Pour mettre à jour les sources de données associées à un dépositaire :</span><span class="sxs-lookup"><span data-stu-id="6ccaa-138">To update the data sources that are associated with a custodian:</span></span>

1. <span data-ttu-id="6ccaa-139">Go to **eDiscovery > Advanced eDiscovery** and open the case.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-139">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>
  
2. <span data-ttu-id="6ccaa-140">Cliquez sur **l’onglet Sources.**</span><span class="sxs-lookup"><span data-stu-id="6ccaa-140">Click the **Sources** tab.</span></span>
  
3. <span data-ttu-id="6ccaa-141">Dans la page **Des dépositaires,** sélectionnez un dépositaire dans la liste, puis cliquez sur **Modifier** dans la page de flyout.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-141">On the **Custodians** page, select a custodian from the list and click **Edit** on the flyout page.</span></span>

    ![Modifier les sources de données](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="6ccaa-143">Cliquez **sur l’onglet** Choisir les sources de données pour modifier les paramètres de la boîte aux lettres du Exchange et du compte OneDrive, cliquez sur Choisir les **sources de données.**</span><span class="sxs-lookup"><span data-stu-id="6ccaa-143">Click **Choose data sources** tab to change the settings for the custodian's Exchange mailbox and OneDrive account, click **Choose data sources**.</span></span>
  
5. <span data-ttu-id="6ccaa-144">Cliquez sur **l’onglet** Sélectionner des sources de données supplémentaires pour ajouter ou supprimer Teams, SharePoint ou Exchange boîtes aux lettres associées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-144">Click the **Select additional data sources** tab to add or remove Teams, SharePoint, or Exchange mailboxes associated with the custodian.</span></span> 

    <span data-ttu-id="6ccaa-145">Pour plus d’informations sur les sources de données associées à un dépositaire, voir [Ajouter des dépositaires à un cas.](add-custodians-to-case.md)</span><span class="sxs-lookup"><span data-stu-id="6ccaa-145">For more information about data sources associated with a custodian, see [Add custodians to a case](add-custodians-to-case.md).</span></span> 
  
6. <span data-ttu-id="6ccaa-146">Cliquez **sur Placer les conservations** en conservation pour activer ou désactiver la conservation pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-146">Click **Place custodial holds** to enable or disable the hold for the custodian.</span></span>

## <a name="re-index-custodian-data"></a><span data-ttu-id="6ccaa-147">Ré-indexer les données des dépositaires</span><span class="sxs-lookup"><span data-stu-id="6ccaa-147">Re-index custodian data</span></span>

<span data-ttu-id="6ccaa-148">Dans la plupart des flux de travail eDiscovery pour les enquêtes juridiques, un sous-ensemble des données d’un dépositaire est recherché une fois que le dépositaire est ajouté à un dossier juridique.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-148">In most eDiscovery workflows for legal investigations, a subset of a custodian's data is searched after the custodian is added to a legal case.</span></span> <span data-ttu-id="6ccaa-149">En raison de très grandes tailles de fichiers ou d’une altération possible des données, certains éléments des sources de données associées à un dépositaire peuvent être partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-149">Because of very large file sizes or possible data corruption, some items in the data sources associated with a custodian may be partially indexed.</span></span> <span data-ttu-id="6ccaa-150">À l’aide de la fonctionnalité [d’indexation](indexing-custodian-data.md) avancée dans le Advanced eDiscovery, la plupart des éléments partiellement indexés peuvent être automatiquement corrigés en réindexant ces éléments à la demande.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-150">Using the [advanced indexing](indexing-custodian-data.md) capability in the Advanced eDiscovery, most partially indexed items can be automatically remediated by re-indexing these items on demand.</span></span>

<span data-ttu-id="6ccaa-151">Lorsqu’un dépositaire est ajouté à un cas, les données situées dans les sources de données associées au dépositaire sont automatiquement ré-indexées (par le processus d’indexation avancé).</span><span class="sxs-lookup"><span data-stu-id="6ccaa-151">When a custodian is added to a case, the data located in the data sources associated with the custodian is automatically re-indexed (by the advanced indexing process).</span></span> <span data-ttu-id="6ccaa-152">Cela signifie que vous pouvez laisser les données en place au lieu de les télécharger et de les corriger, puis de les rechercher hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-152">This means you can leave the data in-place instead of having to download and remediate it and then search it offline).</span></span> <span data-ttu-id="6ccaa-153">Toutefois, pendant le cycle de vie d’un dossier juridique, de nouvelles sources de données peuvent être associées à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-153">However, during the lifecycle of a legal case new data sources might be associated with a custodian.</span></span> <span data-ttu-id="6ccaa-154">Dans ce cas, vous pouvez ré-indexer les données du dépositaire en ré-exécutant le processus d’indexation avancé pour corriger les éléments partiellement indexés et mettre à jour l’index des données du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-154">In this case, you can re-index the custodian's data by re-running the advanced indexing process to remediate any partially indexed items and update the index for the custodian's data.</span></span>

<span data-ttu-id="6ccaa-155">Pour déclencher le processus de ré-indexation afin de traiter les éléments partiellement indexés :</span><span class="sxs-lookup"><span data-stu-id="6ccaa-155">To trigger the re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="6ccaa-156">Go to **eDiscovery > Advanced eDiscovery** and open the case.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-156">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2. <span data-ttu-id="6ccaa-157">Cliquez sur **l’onglet Sources.**</span><span class="sxs-lookup"><span data-stu-id="6ccaa-157">Click the **Sources** tab.</span></span>

3. <span data-ttu-id="6ccaa-158">Dans la page **Des dépositaires,** sélectionnez un dépositaire dont les données doivent être réindexées.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-158">On the **Custodians** page, select a custodian whose data must be reindexed.</span></span>

4. <span data-ttu-id="6ccaa-159">Dans la page volante, cliquez sur **Mettre à jour l’index**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-159">On the flyout page, click **Update index**.</span></span>

   <span data-ttu-id="6ccaa-160">Une boîte de dialogue s’affiche pour dire que le travail d’index a été créé.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-160">A dialog is displayed saying the index job has been created.</span></span>

<span data-ttu-id="6ccaa-161">La ré-indexation des données des dépositaires est un processus de longue durée . la tâche correspondante créée est nommée **Re-indexation des données du dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-161">Re-indexing custodian data is a long-running process; the corresponding job that's created is named **Re-indexing custodian data**.</span></span> <span data-ttu-id="6ccaa-162">Vous pouvez suivre l’avancement sous l’onglet **Travaux** ou sous l’onglet **Dépositaires** en surveillant l’état dans la colonne État du travail **d’indexation.**</span><span class="sxs-lookup"><span data-stu-id="6ccaa-162">You can track the progress on the **Jobs** tab or on the **Custodians** tab by monitoring the status in the **Indexing job status** column.</span></span>

<span data-ttu-id="6ccaa-163">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="6ccaa-163">For more information, see:</span></span>

- [<span data-ttu-id="6ccaa-164">Utiliser les erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="6ccaa-164">Work with processing errors</span></span>](processing-data-for-case.md)

- [<span data-ttu-id="6ccaa-165">Gérer les tâches</span><span class="sxs-lookup"><span data-stu-id="6ccaa-165">Manage jobs</span></span>](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a><span data-ttu-id="6ccaa-166">Libérer un dépositaire d’un cas</span><span class="sxs-lookup"><span data-stu-id="6ccaa-166">Release a custodian from a case</span></span>

<span data-ttu-id="6ccaa-167">Un dépositaire est libéré lorsqu’un cas est fermé, qu’il n’est plus tenu de conserver le contenu d’un cas ou lorsque le dépositaire est considéré comme n’étant plus pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-167">A custodian is released in situations where a case is closed, the custodian is no longer under obligation to preserve content for a case, or when the custodian is deemed to no longer be relevant to the case.</span></span> 

<span data-ttu-id="6ccaa-168">Si vous relâchez un dépositaire après la publication d’une notification de conservation, une notification de publication est envoyée au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-168">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="6ccaa-169">En outre, les conservations placées sur les sources de données associées au dépositaire sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-169">Additionally, any holds placed on data sources that were associated with the custodian are removed.</span></span> <span data-ttu-id="6ccaa-170">Si le dépositaire *a* été placé en conservation silencieuse, où il n’a reçu aucune notification de conservation légale, aucune notification de publication n’est envoyée, mais les conservations placées sur les sources de données associées à ce dépositaire sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-170">If the custodian was placed on a *silent hold*, where they weren't issued any legal hold notifications, a release notice will not be sent but any holds placed on data sources that were associated with that custodian are removed.</span></span>

<span data-ttu-id="6ccaa-171">Pour libérer un dépositaire :</span><span class="sxs-lookup"><span data-stu-id="6ccaa-171">To release a custodian:</span></span> 

1. <span data-ttu-id="6ccaa-172">Go to **eDiscovery > Advanced eDiscovery** and open the case.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-172">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2. <span data-ttu-id="6ccaa-173">Cliquez sur **l’onglet Sources.**</span><span class="sxs-lookup"><span data-stu-id="6ccaa-173">Click the **Sources** tab.</span></span>

3. <span data-ttu-id="6ccaa-174">Dans la page **Des dépositaires,** puis sélectionnez le dépositaire qui est libéré du cas.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-174">On the **Custodians** page, and then select the custodian who is being released from the case.</span></span>

4. <span data-ttu-id="6ccaa-175">Dans la page volante, cliquez sur **Libérer le dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-175">On the flyout page, click **Release custodian**.</span></span>

   <span data-ttu-id="6ccaa-176">Une page d’avertissement s’affiche, expliquant que si une conservation est placée sur une source de données associée au dépositaire, la conservation est supprimée et que toute autre conservation associée à un cas Advanced eDiscovery différent s’applique toujours.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-176">A warning page is displayed explaining that if a hold is placed on a data source associated with the custodian, the hold will be removed, and that any other hold associated with a different Advanced eDiscovery case will still apply.</span></span> <span data-ttu-id="6ccaa-177">Cela inclut d’autres types de fonctionnalités de conservation et de rétention (telles qu’Microsoft 365 stratégie de rétention).</span><span class="sxs-lookup"><span data-stu-id="6ccaa-177">That includes other types of preservation and retention features (such as a Microsoft 365 retention policy).</span></span>

5. <span data-ttu-id="6ccaa-178">Cliquez **sur Oui** pour confirmer que vous souhaitez libérer le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-178">Click **Yes** to confirm that you want to release the custodian.</span></span> 

    <span data-ttu-id="6ccaa-179">L’état de cet utilisateur sous l’onglet **Dépositaires** est définie sur Publication et l’état de conservation sur la page volante est modifié sur **False**.  </span><span class="sxs-lookup"><span data-stu-id="6ccaa-179">The status for this user on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **False**.</span></span> 

> [!NOTE]
> <span data-ttu-id="6ccaa-180">Un dépositaire peut être impliqué simultanément dans plusieurs dossiers juridiques.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-180">A custodian might be simultaneously involved in several legal cases.</span></span> <span data-ttu-id="6ccaa-181">Lorsqu’un dépositaire est libéré d’un cas, les conservations et les notifications sur d’autres questions ne sont pas impactées.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-181">When a custodian is released from a case, the holds and notifications across other matters won't be impacted.</span></span>

## <a name="bulk-edit-custodians"></a><span data-ttu-id="6ccaa-182">Modification en bloc des dépositaires</span><span class="sxs-lookup"><span data-stu-id="6ccaa-182">Bulk-edit custodians</span></span>

<span data-ttu-id="6ccaa-183">Vous pouvez utiliser l’éditeur en bloc pour modifier plusieurs dépositaires en même temps.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-183">You can use the bulk editor to edit multiple custodians as the same time.</span></span> <span data-ttu-id="6ccaa-184">Pour ce faire, sélectionnez simplement deux dépositaires ou plus sous l’onglet **Dépositaires** pour afficher l’éditeur en bloc, puis cliquez sur l’une des tâches.</span><span class="sxs-lookup"><span data-stu-id="6ccaa-184">To do this, just select two or more custodians on the **Custodians** tab to display the bulk editor and then click one of tasks.</span></span>

![Page volante pour modifier les paramètres de plusieurs dépositaires](../media/AeDBulkEditCustodians.png)
