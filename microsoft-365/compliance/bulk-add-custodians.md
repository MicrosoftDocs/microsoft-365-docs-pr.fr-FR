---
title: Ajouter des dépositaires en bloc à un cas avancé de découverte électronique
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
ROBOTS: NOINDEX, NOFOLLOW
description: Utilisez l’outil Bulk-Add pour ajouter rapidement plusieurs dépositaires et leurs sources de données associées à un cas dans Advanced eDiscovery.
ms.openlocfilehash: ab9626be01814fa95a959141433b431df9bf7724
ms.sourcegitcommit: 51a9f34796535309b8ca8b52da92da0a3621327b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45024664"
---
# <a name="bulk-add-custodians-to-an-advanced-ediscovery-case"></a><span data-ttu-id="9f30f-103">Ajouter des dépositaires en bloc à un cas avancé de découverte électronique</span><span class="sxs-lookup"><span data-stu-id="9f30f-103">Bulk-add custodians to an Advanced eDiscovery case</span></span>

<span data-ttu-id="9f30f-104">Pour les cas avancés de découverte électronique qui impliquent un grand nombre de dépositaires, vous pouvez importer plusieurs dépositaires à la fois par un fichier CSV qui contient toutes les informations nécessaires pour les ajouter à un cas.</span><span class="sxs-lookup"><span data-stu-id="9f30f-104">For Advanced eDiscovery cases that involve a lot of custodians, you can import multiple custodians at once by a CSV file that contains all the information necessary to add them to a case.</span></span>

## <a name="bulk-add-custodians"></a><span data-ttu-id="9f30f-105">Ajouter des dépositaires en bloc</span><span class="sxs-lookup"><span data-stu-id="9f30f-105">Bulk-add custodians</span></span>

1. <span data-ttu-id="9f30f-106">Saisissez case et accédez à l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="9f30f-106">Enter case and navigate to the **Sources** tab.</span></span>

2. <span data-ttu-id="9f30f-107">Cliquez sur **importer des dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="9f30f-107">Click **Import custodians**</span></span>

3. <span data-ttu-id="9f30f-108">Sur la page de menu volant, cliquez sur **Télécharger un modèle vierge** pour télécharger un fichier de modèle de dépositaire CSV.</span><span class="sxs-lookup"><span data-stu-id="9f30f-108">On the flyout page, click **Download a blank template** to download a CSV custodian template file.</span></span>

4. <span data-ttu-id="9f30f-109">Ajoutez les informations privatives de Troie au fichier CSV et enregistrez-le sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="9f30f-109">Add the custodial information to the CSV file and save it on your local computer.</span></span> <span data-ttu-id="9f30f-110">Pour plus d’informations sur les propriétés du fichier CSV, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="9f30f-110">See the next section for information about the properties in the CSV file.</span></span>

5. <span data-ttu-id="9f30f-111">Sous l’onglet **sources** , cliquez de nouveau sur **importer des dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="9f30f-111">On the **Sources** tab, click **Import Custodians** again.</span></span>

6. <span data-ttu-id="9f30f-112">Sur la page de menu volant, cliquez sur **Parcourir** et téléchargez votre fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="9f30f-112">On flyout page, click **Browse** and the upload your CSV file.</span></span>

   <span data-ttu-id="9f30f-113">Une fois le fichier CSV téléchargé, un travail BulkAddCustodian est créé et affiché sous l’onglet **travaux** . Le travail valide les dépositaires et leurs sources de données correspondantes, puis les ajoute à l’onglet **dépositaires** de la page **sources** du cas.</span><span class="sxs-lookup"><span data-stu-id="9f30f-113">After the CSV file is uploaded, a BulkAddCustodian job is created and displayed on the **Jobs** tab. The job validates the custodians and their corresponding data sources and then adds them to the **Custodians** tab on the **Sources** page of the case.</span></span>

## <a name="custodian-csv-file"></a><span data-ttu-id="9f30f-114">Fichier CSV de dépositaire</span><span class="sxs-lookup"><span data-stu-id="9f30f-114">Custodian CSV file</span></span>

<span data-ttu-id="9f30f-115">Après avoir téléchargé le modèle CSV, vous pouvez ajouter des dépositaires et leur source de données dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="9f30f-115">After you download the CSV template, you can add custodians and their data source in each row.</span></span> <span data-ttu-id="9f30f-116">Veillez à ne pas modifier les noms de colonne dans la ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="9f30f-116">Be sure not to change the column names in the header row.</span></span>

| <span data-ttu-id="9f30f-117">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="9f30f-117">Column name</span></span>|<span data-ttu-id="9f30f-118">Description</span><span class="sxs-lookup"><span data-stu-id="9f30f-118">Description</span></span>|
|:------- |:------------------------------------------------------------|
|<span data-ttu-id="9f30f-119">**Adresse dépositaire**</span><span class="sxs-lookup"><span data-stu-id="9f30f-119">**Custodian ContactEmail**</span></span>     | <span data-ttu-id="9f30f-120">Adresse de messagerie UPN du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9f30f-120">UPN email of custodian.</span></span> <span data-ttu-id="9f30f-121">Exemple : sarad@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f30f-121">Example: sarad@onmicrosoft.contoso.com</span></span>           |
|<span data-ttu-id="9f30f-122">**Exchange activé**</span><span class="sxs-lookup"><span data-stu-id="9f30f-122">**Exchange Enabled**</span></span> | <span data-ttu-id="9f30f-123">Valeur TRUE/FALSe indiquant si la boîte aux lettres du dépositaire doit être ajoutée ou non.</span><span class="sxs-lookup"><span data-stu-id="9f30f-123">TRUE/FALSE value on whether to add custodian's mailbox.</span></span>      |
|<span data-ttu-id="9f30f-124">**OneDrive activé**</span><span class="sxs-lookup"><span data-stu-id="9f30f-124">**OneDrive Enabled**</span></span> | <span data-ttu-id="9f30f-125">Valeur TRUE/FALSe indique s’il faut ajouter le compte OneDrive entreprise du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9f30f-125">TRUE/FALSE value on whether to add custodian's OneDrive for Business account.</span></span> |
|<span data-ttu-id="9f30f-126">**Est OnHold**</span><span class="sxs-lookup"><span data-stu-id="9f30f-126">**Is OnHold**</span></span>        | <span data-ttu-id="9f30f-127">Valeur TRUE/FALSe indiquant si le dépositaire doit être placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="9f30f-127">TRUE/FALSE value on whether to place custodian on hold.</span></span>       |
|<span data-ttu-id="9f30f-128">**Type Workload1**</span><span class="sxs-lookup"><span data-stu-id="9f30f-128">**Workload1 Type**</span></span>         | <span data-ttu-id="9f30f-129">Valeur de chaîne indiquant le type de source de données à associer au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9f30f-129">String value indicating the type of data source to associate with the custodian.</span></span> <br /><span data-ttu-id="9f30f-130">Les valeurs admises sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f30f-130">Possible values include:</span></span> <br /><span data-ttu-id="9f30f-131">ExchangeMailbox, SharePointSite, TeamsMailbox, TeamsSite, YammerMailbox, YammerSite</span><span class="sxs-lookup"><span data-stu-id="9f30f-131">ExchangeMailbox, SharePointSite, TeamsMailbox, TeamsSite, YammerMailbox, YammerSite</span></span> |
|<span data-ttu-id="9f30f-132">**Emplacement Workload1**</span><span class="sxs-lookup"><span data-stu-id="9f30f-132">**Workload1 Location**</span></span>     | <span data-ttu-id="9f30f-133">En fonction de votre type de charge de travail, il s’agit de l’emplacement des données de votre charge de travail (par exemple, l’adresse de messagerie d’une boîte aux lettres Exchange ou l’URL d’un site SharePoint).</span><span class="sxs-lookup"><span data-stu-id="9f30f-133">Depending on your workload type, this would be the data location of your workload (for example, the email address of an Exchange mailbox or the URL for a SharePoint site).</span></span> |
|||

<span data-ttu-id="9f30f-134">Voici un exemple de fichier CSV contenant des informations sur les dépositaires :</span><span class="sxs-lookup"><span data-stu-id="9f30f-134">Here's an example of a CSV file with custodian information:</span></span>  

| <span data-ttu-id="9f30f-135">ContactEmail</span><span class="sxs-lookup"><span data-stu-id="9f30f-135">ContactEmail</span></span>      | <span data-ttu-id="9f30f-136">Exchange activé</span><span class="sxs-lookup"><span data-stu-id="9f30f-136">Exchange Enabled</span></span> | <span data-ttu-id="9f30f-137">OneDrive activé</span><span class="sxs-lookup"><span data-stu-id="9f30f-137">OneDrive Enabled</span></span> | <span data-ttu-id="9f30f-138">Est OnHold</span><span class="sxs-lookup"><span data-stu-id="9f30f-138">Is OnHold</span></span> | <span data-ttu-id="9f30f-139">Type Workload1</span><span class="sxs-lookup"><span data-stu-id="9f30f-139">Workload1 Type</span></span> | <span data-ttu-id="9f30f-140">Emplacement Workload1</span><span class="sxs-lookup"><span data-stu-id="9f30f-140">Workload1 Location</span></span>             |
| ----------------- | ---------------- | ---------------- | --------- | -------------- | ------------------------------ |
|<span data-ttu-id="9f30f-141">sarad@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f30f-141">sarad@onmicrosoft.contoso.com</span></span> | <span data-ttu-id="9f30f-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-142">TRUE</span></span>             | <span data-ttu-id="9f30f-143">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-143">TRUE</span></span>             | <span data-ttu-id="9f30f-144">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-144">TRUE</span></span>      | <span data-ttu-id="9f30f-145">SharePointSite</span><span class="sxs-lookup"><span data-stu-id="9f30f-145">SharePointSite</span></span> | https://contoso.sharepoint.com |
|<span data-ttu-id="9f30f-146">pillarp@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="9f30f-146">pillarp@onmicrosoft.contoso.com</span></span> | <span data-ttu-id="9f30f-147">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-147">TRUE</span></span>             | <span data-ttu-id="9f30f-148">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-148">TRUE</span></span>             | <span data-ttu-id="9f30f-149">TRUE</span><span class="sxs-lookup"><span data-stu-id="9f30f-149">TRUE</span></span>      | |  |
||||||

## <a name="custodian-and-data-source-validation"></a><span data-ttu-id="9f30f-150">Validation des dépositaires et des sources de données</span><span class="sxs-lookup"><span data-stu-id="9f30f-150">Custodian and data source validation</span></span>

<span data-ttu-id="9f30f-151">Lorsque vous chargez le fichier CSV de dépositaire, Advanced eDiscovery effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="9f30f-151">When you upload the custodian CSV file, Advanced eDiscovery does the following things:</span></span>

1. <span data-ttu-id="9f30f-152">Valide les dépositaires et leurs sources de données.</span><span class="sxs-lookup"><span data-stu-id="9f30f-152">Validates the custodians and their data sources.</span></span> 

2. <span data-ttu-id="9f30f-153">Indexe toutes les sources de données pour chaque dépositaire et les place en conservation (si la propriété is OnHold est définie sur TRUE).</span><span class="sxs-lookup"><span data-stu-id="9f30f-153">Indexes all data sources for each custodian and places them on hold (if the Is OnHold property is set to TRUE).</span></span>

### <a name="custodian-validation"></a><span data-ttu-id="9f30f-154">Validation des dépositaires</span><span class="sxs-lookup"><span data-stu-id="9f30f-154">Custodian validation</span></span>

<span data-ttu-id="9f30f-155">Actuellement, nous ne prenons en charge que les dépositaires d’importation dans Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="9f30f-155">Currently, we only support importing custodians that are in Azure Active Directory (AAD).</span></span>

<span data-ttu-id="9f30f-156">Nous vérifions et trouvons des dépositaires à l’aide de la valeur UPN dans la colonne **adresse de messagerie du contact** dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="9f30f-156">We validate and find custodians using the UPN value in the **Contact Email** column in the CSV file.</span></span> <span data-ttu-id="9f30f-157">Les dépositaires validés sont automatiquement ajoutés à l’incident et répertoriés sous l’onglet **dépositaire** de la page **sources** du cas.</span><span class="sxs-lookup"><span data-stu-id="9f30f-157">Custodians that are validated are automatically added to the case and listed on the **Custodian** tab on the **Sources** page of the case.</span></span> <span data-ttu-id="9f30f-158">Si un dépositaire ne peut pas être validé, il est répertorié dans le journal des erreurs pour le travail BulkAddCustodian qui est répertorié sous l’onglet **travaux** dans le cas.</span><span class="sxs-lookup"><span data-stu-id="9f30f-158">If a custodian can't be validated, they are listed in the error log for the BulkAddCustodian job that is listed on the **Jobs** tab in the case.</span></span> <span data-ttu-id="9f30f-159">Les dépositaires non validés ne sont pas ajoutés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="9f30f-159">Unvalidated custodians are not added to the case.</span></span>

### <a name="data-source-validation"></a><span data-ttu-id="9f30f-160">Validation de la source de données</span><span class="sxs-lookup"><span data-stu-id="9f30f-160">Data source validation</span></span>

<span data-ttu-id="9f30f-161">Une fois les dépositaires validés et ajoutés au cas, chaque source de données associée à un dépositaire est validée.</span><span class="sxs-lookup"><span data-stu-id="9f30f-161">After custodians are validated and added to the case, each data source that's associated with a custodian is validated.</span></span> <span data-ttu-id="9f30f-162">Si une source de données pour un dépositaire est introuvable, la valeur **non validée** s’affiche dans la colonne **validé** de l’onglet **dépositaire** .</span><span class="sxs-lookup"><span data-stu-id="9f30f-162">If any data source for a custodian can't be found, the value **Not validated** would be displayed in the **Validated** column on the **Custodian** tab for that custodian.</span></span>

### <a name="remediating-unvalidated-data-sources"></a><span data-ttu-id="9f30f-163">Correction de sources de données non validées</span><span class="sxs-lookup"><span data-stu-id="9f30f-163">Remediating unvalidated data sources</span></span>

<span data-ttu-id="9f30f-164">Pour corriger les dépositaires avec des sources de données non validées :</span><span class="sxs-lookup"><span data-stu-id="9f30f-164">To remediate custodians with unvalidated data sources:</span></span> 

1. <span data-ttu-id="9f30f-165">Sous l’onglet **dépositaire** , sélectionnez un dépositaire qui n’est pas validé.</span><span class="sxs-lookup"><span data-stu-id="9f30f-165">On the **Custodian** tab, select a custodian who isn't validated.</span></span>

2. <span data-ttu-id="9f30f-166">Sur la page de menu volant dépositaire, faites défiler jusqu’à la section **sources de données** pour afficher les sources de données associées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9f30f-166">On the custodian flyout page, scroll to the **Data sources** section to view the data sources that are associated with custodian.</span></span> <span data-ttu-id="9f30f-167">Les sources de données validées et non validées sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="9f30f-167">Both validated and unvalidated data sources are listed.</span></span>

3. <span data-ttu-id="9f30f-168">Dans la section **sources de données** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="9f30f-168">In the **Data sources** section, click **Edit**.</span></span>

4. <span data-ttu-id="9f30f-169">Sur la page **choisir les emplacements privatives d’adresses** , supprimez une source de données non validée.</span><span class="sxs-lookup"><span data-stu-id="9f30f-169">On the **Choose custodial locations** page, remove an unvalidated data source.</span></span>

5. <span data-ttu-id="9f30f-170">Sur la page **Sélectionner des emplacements supplémentaires** , cliquez sur **mettre à jour** pour ajouter des sources de données supplémentaires pour un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="9f30f-170">On the **Select additional locations** page, click **Update** to add additional data sources for a custodian.</span></span>
