---
title: Gestion des dépositaires dans un cas avancé eDiscovery
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
description: Découvrez comment afficher les détails, modifier et modifier en bloc la liste des dépositaires dans un cas avancé de découverte électronique.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 95b7a7dbec5656a1ac0692ed465eb5a99d7ca11a
ms.sourcegitcommit: 51a9f34796535309b8ca8b52da92da0a3621327b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45024804"
---
# <a name="manage-custodians-in-an-advanced-ediscovery-case"></a><span data-ttu-id="04e82-103">Gestion des dépositaires dans un cas avancé eDiscovery</span><span class="sxs-lookup"><span data-stu-id="04e82-103">Manage custodians in an Advanced eDiscovery case</span></span>

<span data-ttu-id="04e82-104">La page dépositaires de l’onglet **sources** dans un cas avancé eDiscovery contient la liste de tous les dépositaires qui ont été ajoutés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="04e82-104">The Custodians page on the **Sources** tab in an Advanced eDiscovery case contains a list of all custodians that have been added to the case.</span></span> <span data-ttu-id="04e82-105">Une fois que vous avez ajouté des dépositaires à un cas, les détails de chaque dépositaire sont automatiquement collectés à partir d’Azure Active Directory et peuvent être consultés dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="04e82-105">After you add custodians to a case, details about each custodian are automatically collected from Azure Active Directory and are viewable in Advanced eDiscovery.</span></span>

![Gestion des dépositaires](../media/CustodianDetails.PNG)

## <a name="view-custodian-details"></a><span data-ttu-id="04e82-107">Afficher les détails du dépositaire</span><span class="sxs-lookup"><span data-stu-id="04e82-107">View custodian details</span></span>

<span data-ttu-id="04e82-108">Pour afficher les détails relatifs à un dépositaire, cliquez sur celui-ci dans la liste sous l’onglet **dépositaires** . Une page de menu volant s’affiche et contient les informations suivantes sur le dépositaire :</span><span class="sxs-lookup"><span data-stu-id="04e82-108">To view the details about a custodian, click the custodian from the list on the **Custodians** tab. A flyout page is displayed and contains the following information about the custodian:</span></span>

- <span data-ttu-id="04e82-109">Informations de contact</span><span class="sxs-lookup"><span data-stu-id="04e82-109">Contact information</span></span>

  - <span data-ttu-id="04e82-110">**Nom d’affichage** : nom affiché dans le carnet d’adresses pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-110">**Display Name** - The name displayed in the address book for the custodian.</span></span> <span data-ttu-id="04e82-111">Il s’agit généralement de la combinaison du prénom du dépositaire, de l’initiale du deuxième prénom et du nom de famille.</span><span class="sxs-lookup"><span data-stu-id="04e82-111">This is usually the combination of the custodian's first name, middle initial, and last name.</span></span>
  
   - <span data-ttu-id="04e82-112">**Mail/SMTP** : adresse SMTP principale pour le dépositaire, par exemple, brianj@contoso.onmicrosoft.com.</span><span class="sxs-lookup"><span data-stu-id="04e82-112">**Mail/SMTP** - The primary SMTP address for the custodian, for example, brianj@contoso.onmicrosoft.com.</span></span> <span data-ttu-id="04e82-113">Le nom d’utilisateur principal (UPN) du dépositaire est également mentionné.</span><span class="sxs-lookup"><span data-stu-id="04e82-113">The custodian's user principal name (UPN) is also listed.</span></span>

  - <span data-ttu-id="04e82-114">**Title** -fonction du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-114">**Title** - The custodian's job title.</span></span>

  - <span data-ttu-id="04e82-115">**Department** : nom du service dans lequel le dépositaire travaille.</span><span class="sxs-lookup"><span data-stu-id="04e82-115">**Department** - The name for the department in which the custodian works.</span></span>

  - <span data-ttu-id="04e82-116">**Responsable** : le responsable du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-116">**Manager** - The custodian's manager.</span></span> <span data-ttu-id="04e82-117">Le responsable désigné recevra toutes les communications d’escalade de ce dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-117">The designated manager will receive any escalation communications for this custodian.</span></span>
  
- <span data-ttu-id="04e82-118">Informations d’emplacement</span><span class="sxs-lookup"><span data-stu-id="04e82-118">Location information</span></span>

  - <span data-ttu-id="04e82-119">**Ville** -ville où se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-119">**City** - The city in which the custodian is located.</span></span>

  - <span data-ttu-id="04e82-120">**Département** : État ou province dans l’adresse du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-120">**State** - The state or province in the custodian's address.</span></span>

  - <span data-ttu-id="04e82-121">**Pays/région** : pays/région où se trouve le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-121">**Country/Region** - The country/region where the custodian is located.</span></span>

  - <span data-ttu-id="04e82-122">**Office** : l’emplacement de l’Office dans le lieu d’activité du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-122">**Office** - The office location in the custodian's place of business.</span></span>

- <span data-ttu-id="04e82-123">Informations sur les cas</span><span class="sxs-lookup"><span data-stu-id="04e82-123">Case information</span></span>

  - <span data-ttu-id="04e82-124">**Hold Status** : indique si le dépositaire a été mis en attente.</span><span class="sxs-lookup"><span data-stu-id="04e82-124">**Hold status** - Indicates if the custodian has been placed on hold.</span></span> 

  - <span data-ttu-id="04e82-125">**Statut**de la communication : indique si un avis de mise en attente a été émis pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-125">**Communication status**: Indicates if the custodian has been issued a hold notice.</span></span> <span data-ttu-id="04e82-126">Si le dépositaire a reçu une notification, la valeur de cette propriété est **publiée**.</span><span class="sxs-lookup"><span data-stu-id="04e82-126">If the custodian has been issued a notice, this value of this property is **Published**.</span></span> <span data-ttu-id="04e82-127">Si le dépositaire n’a pas reçu de notification, son statut est non **publié**.</span><span class="sxs-lookup"><span data-stu-id="04e82-127">If the custodian has not been issued a notice, the status is **Un-published**.</span></span> 

  - <span data-ttu-id="04e82-128">**Status** : état du dépositaire dans le cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-128">**Status** - The status of the custodian within the case.</span></span> <span data-ttu-id="04e82-129">L’état **actif** indique que le dépositaire fait partie de l’affaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-129">A status of **Active** indicates that the custodian is part of the case.</span></span> <span data-ttu-id="04e82-130">Si un dépositaire est émis à partir d’un incident, le statut passe à **lancé**.</span><span class="sxs-lookup"><span data-stu-id="04e82-130">If a custodian is released from a case, the status is changed to **Released**.</span></span> 

- <span data-ttu-id="04e82-131">Sources de données et informations d’indexation</span><span class="sxs-lookup"><span data-stu-id="04e82-131">Data sources and indexing information</span></span>

    - <span data-ttu-id="04e82-132">**Sources de données** : affiche le nombre et le type de sources de données (boîtes aux lettres, sites et équipes) qui sont associées au dépositaire et font partie de la demande.</span><span class="sxs-lookup"><span data-stu-id="04e82-132">**Data sources** - Shows the count and type of data sources (mailboxes, sites, and Teams) that are associated with the custodian and are part of the case.</span></span>

    - <span data-ttu-id="04e82-133">Date et heure de **mise à jour** de l’index : indique l’heure et la date de la dernière déclenchement du travail d’indexation avancé.</span><span class="sxs-lookup"><span data-stu-id="04e82-133">**Index updated time** - Indicates the time and date for when the advanced indexing job was last triggered.</span></span> <span data-ttu-id="04e82-134">Cette propriété indique également quand le processus d’indexation avancé est en cours.</span><span class="sxs-lookup"><span data-stu-id="04e82-134">This property will also indicate when the advanced indexing process is currently in progress.</span></span>


## <a name="edit-a-custodian"></a><span data-ttu-id="04e82-135">Modifier un dépositaire</span><span class="sxs-lookup"><span data-stu-id="04e82-135">Edit a custodian</span></span>

<span data-ttu-id="04e82-136">Lors de l’évolution de votre cas, vous pouvez découvrir qu’il peut y avoir des sources de données supplémentaires pertinentes pour un dépositaire spécifique & votre cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-136">As your case progresses, you may discover that there may be additional data sources relevant to a specific custodian & your case.</span></span> <span data-ttu-id="04e82-137">Dans d’autres scénarios, vous souhaiterez peut-être supprimer certaines sources de données qui ont été vérifiées et considérées comme non pertinentes.</span><span class="sxs-lookup"><span data-stu-id="04e82-137">In other scenarios, you may want to remove certain data sources that have been reviewed and deemed as not relevant.</span></span>

<span data-ttu-id="04e82-138">Pour mettre à jour les sources de données associées à un dépositaire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="04e82-138">To update the data sources that are associated with a custodian:</span></span>

1. <span data-ttu-id="04e82-139">Accédez à **ediscovery > Advanced eDiscovery** et ouvrez le cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-139">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>
  
2. <span data-ttu-id="04e82-140">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="04e82-140">Click the **Sources** tab.</span></span>
  
3. <span data-ttu-id="04e82-141">Sur la page **dépositaires** , sélectionnez un dépositaire dans la liste, puis cliquez sur **modifier** sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="04e82-141">On the **Custodians** page, select a custodian from the list and click **Edit** on the flyout page.</span></span>

    ![Modifier des sources de données](../media/EditCustodianDataSource.PNG)
  
4. <span data-ttu-id="04e82-143">Cliquez sur l’onglet **choisir les sources de données** pour modifier les paramètres de la boîte aux lettres Exchange du dépositaire et du compte OneDrive, puis cliquez sur choisir les sources de **données**.</span><span class="sxs-lookup"><span data-stu-id="04e82-143">Click **Choose data sources** tab to change the settings for the custodian's Exchange mailbox and OneDrive account, click **Choose data sources**.</span></span>
  
5. <span data-ttu-id="04e82-144">Cliquez sur l’onglet **Sélectionner des sources de données supplémentaires** pour ajouter ou supprimer des équipes, des groupes SharePoint ou des boîtes aux lettres Exchange associées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-144">Click the **Select additional data sources** tab to add or remove Teams, SharePoint, or Exchange mailboxes associated with the custodian.</span></span> 

    <span data-ttu-id="04e82-145">Pour plus d’informations sur les sources de données associées à un dépositaire, voir « étape 3 : associer des sources de données supplémentaires à un dépositaire » dans [Ajouter des dépositaires à un cas](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian).</span><span class="sxs-lookup"><span data-stu-id="04e82-145">For more information about data sources associated with a custodian, see "Step 3: Associate additional data sources to a custodian" in [Add custodians to a case](add-custodians-to-case.md#step-3-associate-additional-data-sources-to-a-custodian).</span></span> 
  
6. <span data-ttu-id="04e82-146">Cliquez sur **placer des conservations privatives** pour activer ou désactiver la conservation pour le dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-146">Click **Place custodial holds** to enable or disable the hold for the custodian.</span></span>

## <a name="re-index-custodian-data"></a><span data-ttu-id="04e82-147">Réindexer les données du dépositaire</span><span class="sxs-lookup"><span data-stu-id="04e82-147">Re-index custodian data</span></span>

<span data-ttu-id="04e82-148">Dans la plupart des flux de travail eDiscovery pour les enquêtes juridiques, un sous-ensemble des données d’un dépositaire est recherché une fois que le dépositaire est ajouté à un cas juridique.</span><span class="sxs-lookup"><span data-stu-id="04e82-148">In most eDiscovery workflows for legal investigations, a subset of a custodian's data is searched after the custodian is added to a legal case.</span></span> <span data-ttu-id="04e82-149">En raison de la taille des fichiers très volumineux ou d’une éventuelle altération des données, certains éléments des sources de données associées à un dépositaire peuvent être partiellement indexés.</span><span class="sxs-lookup"><span data-stu-id="04e82-149">Because of very large file sizes or possible data corruption, some items in the data sources associated with a custodian may be partially indexed.</span></span> <span data-ttu-id="04e82-150">À l’aide de la fonctionnalité d' [indexation avancée](indexing-custodian-data.md) dans la découverte électronique avancée, la plupart des éléments indexés partiellement peuvent être automatiquement corrigés en réindexant ces éléments à la demande.</span><span class="sxs-lookup"><span data-stu-id="04e82-150">Using the [advanced indexing](indexing-custodian-data.md) capability in the Advanced eDiscovery, most partially indexed items can be automatically remediated by re-indexing these items on demand.</span></span>

<span data-ttu-id="04e82-151">Lorsqu’un dépositaire est ajouté à un cas, les données situées dans les sources de données associées au dépositaire sont automatiquement réindexées (par le processus d’indexation avancé).</span><span class="sxs-lookup"><span data-stu-id="04e82-151">When a custodian is added to a case, the data located in the data sources associated with the custodian is automatically re-indexed (by the advanced indexing process).</span></span> <span data-ttu-id="04e82-152">Cela signifie que vous pouvez laisser les données sur place au lieu de devoir les télécharger et les corriger, puis les Rechercher hors connexion).</span><span class="sxs-lookup"><span data-stu-id="04e82-152">This means you can leave the data in-place instead of having to download and remediate it and then search it offline).</span></span> <span data-ttu-id="04e82-153">Toutefois, pendant le cycle de vie d’un cas juridique, de nouvelles sources de données peuvent être associées à un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-153">However, during the lifecycle of a legal case new data sources might be associated with a custodian.</span></span> <span data-ttu-id="04e82-154">Dans ce cas, vous pouvez réindexer les données du dépositaire en réexécutant le processus d’indexation avancé afin de corriger les éléments partiellement indexés et de mettre à jour l’index des données du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-154">In this case, you can re-index the custodian's data by re-running the advanced indexing process to remediate any partially indexed items and update the index for the custodian's data.</span></span>

<span data-ttu-id="04e82-155">Pour déclencher le processus de réindexation afin d’adresser des éléments partiellement indexés :</span><span class="sxs-lookup"><span data-stu-id="04e82-155">To trigger the re-indexing process to address partially indexed items:</span></span>

1. <span data-ttu-id="04e82-156">Accédez à **ediscovery > Advanced eDiscovery** et ouvrez le cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-156">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2. <span data-ttu-id="04e82-157">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="04e82-157">Click the **Sources** tab.</span></span>

3. <span data-ttu-id="04e82-158">Sur la page **dépositaires** , sélectionnez un dépositaire dont les données doivent être réindexées.</span><span class="sxs-lookup"><span data-stu-id="04e82-158">On the **Custodians** page, select a custodian whose data must be reindexed.</span></span>

4. <span data-ttu-id="04e82-159">Sur la page de la fenêtre volante, cliquez sur **mettre à jour l’index**.</span><span class="sxs-lookup"><span data-stu-id="04e82-159">On the flyout page, click **Update index**.</span></span>

   <span data-ttu-id="04e82-160">Une boîte de dialogue s’affiche, indiquant que le travail d’index a été créé.</span><span class="sxs-lookup"><span data-stu-id="04e82-160">A dialog is displayed saying the index job has been created.</span></span>

<span data-ttu-id="04e82-161">La réindexation des données du dépositaire est un processus long ; le travail correspondant créé est nommé **réindexation des données des dépositaires**.</span><span class="sxs-lookup"><span data-stu-id="04e82-161">Re-indexing custodian data is a long-running process; the corresponding job that's created is named **Re-indexing custodian data**.</span></span> <span data-ttu-id="04e82-162">Vous pouvez suivre l’avancement sous l’onglet **travaux** ou sous l’onglet **dépositaires** en surveillant le statut dans la colonne **État du travail d’indexation** .</span><span class="sxs-lookup"><span data-stu-id="04e82-162">You can track the progress on the **Jobs** tab or on the **Custodians** tab by monitoring the status in the **Indexing job status** column.</span></span>

<span data-ttu-id="04e82-163">Pour plus d’informations, voir :</span><span class="sxs-lookup"><span data-stu-id="04e82-163">For more information, see:</span></span>

- [<span data-ttu-id="04e82-164">Utiliser les erreurs de traitement</span><span class="sxs-lookup"><span data-stu-id="04e82-164">Work with processing errors</span></span>](processing-data-for-case.md)

- [<span data-ttu-id="04e82-165">Gérer les tâches</span><span class="sxs-lookup"><span data-stu-id="04e82-165">Manage jobs</span></span>](managing-jobs-ediscovery20.md)

## <a name="release-a-custodian-from-a-case"></a><span data-ttu-id="04e82-166">Publication d’un dépositaire à partir d’un cas</span><span class="sxs-lookup"><span data-stu-id="04e82-166">Release a custodian from a case</span></span>

<span data-ttu-id="04e82-167">Un dépositaire est publié dans les situations où un cas est fermé, le dépositaire n’est plus tenu de conserver le contenu d’un cas ou lorsque le dépositaire est considéré comme n’étant plus pertinent pour le cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-167">A custodian is released in situations where a case is closed, the custodian is no longer under obligation to preserve content for a case, or when the custodian is deemed to no longer be relevant to the case.</span></span> 

<span data-ttu-id="04e82-168">Si vous libérez un dépositaire après la publication d’une notification de mise en attente, un avis de publication est envoyé au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-168">If you release a custodian after a hold notice was published, a release notice will be sent to the custodian.</span></span> <span data-ttu-id="04e82-169">De plus, toutes les suspensions placées sur les sources de données qui ont été associées au dépositaire sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="04e82-169">Additionally, any holds placed on data sources that were associated with the custodian are removed.</span></span> <span data-ttu-id="04e82-170">Si le dépositaire a été placé sur un *blocage silencieux*, où il n’a pas reçu de notifications de mise en attente légale, un avis de publication ne sera pas envoyé, mais les blocages placés sur les sources de données associées à ce dépositaire sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="04e82-170">If the custodian was placed on a *silent hold*, where they weren't issued any legal hold notifications, a release notice will not be sent but any holds placed on data sources that were associated with that custodian are removed.</span></span>

<span data-ttu-id="04e82-171">Pour libérer un dépositaire :</span><span class="sxs-lookup"><span data-stu-id="04e82-171">To release a custodian:</span></span> 

1. <span data-ttu-id="04e82-172">Accédez à **ediscovery > Advanced eDiscovery** et ouvrez le cas.</span><span class="sxs-lookup"><span data-stu-id="04e82-172">Go to  **eDiscovery > Advanced eDiscovery** and open the case.</span></span>

2. <span data-ttu-id="04e82-173">Cliquez sur l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="04e82-173">Click the **Sources** tab.</span></span>

3. <span data-ttu-id="04e82-174">Sur la page **dépositaires** , puis sélectionnez le dépositaire qui est lancé à partir de l’incident.</span><span class="sxs-lookup"><span data-stu-id="04e82-174">On the **Custodians** page, and then select the custodian who is being released from the case.</span></span>

4. <span data-ttu-id="04e82-175">Sur la page flyout, cliquez sur **libérer le dépositaire**.</span><span class="sxs-lookup"><span data-stu-id="04e82-175">On the flyout page, click **Release custodian**.</span></span>

   <span data-ttu-id="04e82-176">Une page d’avertissement s’affiche pour expliquer que si une conservation est placée sur une source de données associée au dépositaire, la conservation sera supprimée et les autres conservations associées à un autre cas de découverte électronique avancée continueront à s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="04e82-176">A warning page is displayed explaining that if a hold is placed on a data source associated with the custodian, the hold will be removed, and that any other hold associated with a different Advanced eDiscovery case will still apply.</span></span> <span data-ttu-id="04e82-177">Cela inclut d’autres types de fonctionnalités de conservation et de rétention (par exemple, une stratégie de rétention Microsoft 365).</span><span class="sxs-lookup"><span data-stu-id="04e82-177">That includes other types of preservation and retention features (such as a Microsoft 365 retention policy).</span></span>

5. <span data-ttu-id="04e82-178">Cliquez sur **Oui** pour confirmer le lancement du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="04e82-178">Click **Yes** to confirm that you want to release the custodian.</span></span> 

    <span data-ttu-id="04e82-179">L’état de cet utilisateur sous l’onglet **dépositaires** est défini sur **relâché** et le **statut de blocage** sur la page flyout est modifié sur **false**.</span><span class="sxs-lookup"><span data-stu-id="04e82-179">The status for this user on the **Custodians** tab is set to **Released** and the **Hold status** on the flyout page is changed to **False**.</span></span> 

> [!NOTE]
> <span data-ttu-id="04e82-180">Un dépositaire peut être impliqué simultanément dans plusieurs cas juridiques.</span><span class="sxs-lookup"><span data-stu-id="04e82-180">A custodian might be simultaneously involved in several legal cases.</span></span> <span data-ttu-id="04e82-181">Lorsqu’un dépositaire est émis à partir d’un cas, les conservations et notifications dans les autres matières ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="04e82-181">When a custodian is released from a case, the holds and notifications across other matters won't be impacted.</span></span>

## <a name="bulk-edit-custodians"></a><span data-ttu-id="04e82-182">Modifier en bloc des dépositaires</span><span class="sxs-lookup"><span data-stu-id="04e82-182">Bulk-edit custodians</span></span>

<span data-ttu-id="04e82-183">Vous pouvez utiliser l’éditeur en bloc pour modifier plusieurs dépositaires en même temps.</span><span class="sxs-lookup"><span data-stu-id="04e82-183">You can use the bulk editor to edit multiple custodians as the same time.</span></span> <span data-ttu-id="04e82-184">Pour ce faire, sélectionnez au moins deux dépositaires dans l’onglet **dépositaires** pour afficher l’éditeur en bloc, puis cliquez sur l’une des tâches.</span><span class="sxs-lookup"><span data-stu-id="04e82-184">To do this, just select two or more custodians on the **Custodians** tab to display the bulk editor and then click one of tasks.</span></span>

![Page volante permettant de modifier les paramètres de plusieurs dépositaires](../media/AeDBulkEditCustodians.png)
