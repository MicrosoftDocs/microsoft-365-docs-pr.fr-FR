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
description: ''
ms.openlocfilehash: 9331e45619f549ea31adcfdd9316eea20e43efef
ms.sourcegitcommit: a005395165db8896f4109674443b5e5e9209861d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/31/2020
ms.locfileid: "44432437"
---
# <a name="bulk-add-custodians-to-an-advanced-ediscovery-case-preview"></a><span data-ttu-id="0c66a-102">Ajouter des dépositaires en bloc à un cas avancé eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="0c66a-102">Bulk-add custodians to an Advanced eDiscovery case (preview)</span></span>

<span data-ttu-id="0c66a-103">Pour les cas avancés de découverte électronique qui impliquent un grand nombre de dépositaires, vous pouvez importer plusieurs dépositaires à la fois par un fichier CSV qui contient toutes les informations nécessaires pour les ajouter à un cas.</span><span class="sxs-lookup"><span data-stu-id="0c66a-103">For Advanced eDiscovery cases that involve a lot of custodians, you can import multiple custodians at once by a CSV file that contains all the information necessary to add them to a case.</span></span>

## <a name="bulk-add-custodians"></a><span data-ttu-id="0c66a-104">Ajouter des dépositaires en bloc</span><span class="sxs-lookup"><span data-stu-id="0c66a-104">Bulk-add custodians</span></span>

1. <span data-ttu-id="0c66a-105">Saisissez case et accédez à l’onglet **sources** .</span><span class="sxs-lookup"><span data-stu-id="0c66a-105">Enter case and navigate to the **Sources** tab.</span></span>

2. <span data-ttu-id="0c66a-106">Cliquez sur **importer des dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="0c66a-106">Click **Import custodians**</span></span>

3. <span data-ttu-id="0c66a-107">Sur la page de menu volant, cliquez sur **Télécharger un modèle vierge** pour télécharger un fichier de modèle de dépositaire CSV.</span><span class="sxs-lookup"><span data-stu-id="0c66a-107">On the flyout page, click **Download a blank template** to download a CSV custodian template file.</span></span>

4. <span data-ttu-id="0c66a-108">Ajoutez les informations privatives de Troie au fichier CSV et enregistrez-le sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0c66a-108">Add the custodial information to the CSV file and save it on your local computer.</span></span> <span data-ttu-id="0c66a-109">Pour plus d’informations sur les propriétés du fichier CSV, consultez la section suivante.</span><span class="sxs-lookup"><span data-stu-id="0c66a-109">See the next section for information about the properties in the CSV file.</span></span>

5. <span data-ttu-id="0c66a-110">Sous l’onglet **sources** , cliquez de nouveau sur **importer des dépositaires** .</span><span class="sxs-lookup"><span data-stu-id="0c66a-110">On the **Sources** tab, click **Import Custodians** again.</span></span> 
6. <span data-ttu-id="0c66a-111">Sur la page de menu volant, cliquez sur **Parcourir** et téléchargez votre fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="0c66a-111">On flyout page, click **Browse** and the upload your CSV file.</span></span>

   <span data-ttu-id="0c66a-112">Une fois le fichier CSV téléchargé, un travail BulkAddCustodian est créé et affiché sous l’onglet **travaux** . Le travail valide les dépositaires et leurs sources de données correspondantes, puis les ajoute à l’onglet **dépositaires** de la page **sources** du cas.</span><span class="sxs-lookup"><span data-stu-id="0c66a-112">After the CSV file is uploaded, a BulkAddCustodian job is created and displayed on the **Jobs** tab. The job validates the custodians and their corresponding data sources and then adds them to the **Custodians** tab on the **Sources** page of the case.</span></span>

## <a name="custodian-csv-file"></a><span data-ttu-id="0c66a-113">Fichier CSV de dépositaire</span><span class="sxs-lookup"><span data-stu-id="0c66a-113">Custodian CSV file</span></span>

<span data-ttu-id="0c66a-114">Après avoir téléchargé le modèle CSV, vous pouvez ajouter des dépositaires et leur source de données dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="0c66a-114">After you download the CSV template, you can add custodians and their data source in each row.</span></span> <span data-ttu-id="0c66a-115">Veillez à ne pas modifier les noms de colonne dans la ligne d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="0c66a-115">Be sure not to change the column names in the the header row.</span></span>

| <span data-ttu-id="0c66a-116">Nom de colonne</span><span class="sxs-lookup"><span data-stu-id="0c66a-116">Column name</span></span>|<span data-ttu-id="0c66a-117">Description</span><span class="sxs-lookup"><span data-stu-id="0c66a-117">Description</span></span>|
|:------- |:------------------------------------------------------------|
|<span data-ttu-id="0c66a-118">**Adresse dépositaire**</span><span class="sxs-lookup"><span data-stu-id="0c66a-118">**Custodian ContactEmail**</span></span>     | <span data-ttu-id="0c66a-119">Adresse de messagerie UPN du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="0c66a-119">UPN email of custodian.</span></span> <span data-ttu-id="0c66a-120">Exemple : sarad@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0c66a-120">Example: sarad@onmicrosoft.contoso.com</span></span>           |
|<span data-ttu-id="0c66a-121">**Exchange activé**</span><span class="sxs-lookup"><span data-stu-id="0c66a-121">**Exchange Enabled**</span></span> | <span data-ttu-id="0c66a-122">Valeur TRUE/FALSe indiquant si la boîte aux lettres du dépositaire doit être ajoutée ou non.</span><span class="sxs-lookup"><span data-stu-id="0c66a-122">TRUE/FALSE value on whether to add custodian's mailbox.</span></span>      |
|<span data-ttu-id="0c66a-123">**OneDrive activé**</span><span class="sxs-lookup"><span data-stu-id="0c66a-123">**OneDrive Enabled**</span></span> | <span data-ttu-id="0c66a-124">Valeur TRUE/FALSe indique s’il faut ajouter le compte OneDrive entreprise du dépositaire.</span><span class="sxs-lookup"><span data-stu-id="0c66a-124">TRUE/FALSE value on whether to add custodian's OneDrive for Business account.</span></span> |
|<span data-ttu-id="0c66a-125">**Est OnHold**</span><span class="sxs-lookup"><span data-stu-id="0c66a-125">**Is OnHold**</span></span>        | <span data-ttu-id="0c66a-126">Valeur TRUE/FALSe indiquant si le dépositaire doit être placé en conservation.</span><span class="sxs-lookup"><span data-stu-id="0c66a-126">TRUE/FALSE value on whether to place custodian on hold.</span></span>       |
|<span data-ttu-id="0c66a-127">**Type Workload1**</span><span class="sxs-lookup"><span data-stu-id="0c66a-127">**Workload1 Type**</span></span>         | <span data-ttu-id="0c66a-128">Valeur de chaîne indiquant le type de source de données à associer au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="0c66a-128">String value indicating the type of data source to associate with the custodian.</span></span> <br /><span data-ttu-id="0c66a-129">Les valeurs admises sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c66a-129">Possible values include:</span></span> <br /><span data-ttu-id="0c66a-130">ExchangeMailbox, SharePointSite, TeamsMailbox, TeamsSite, YammerMailbox, YammerSite</span><span class="sxs-lookup"><span data-stu-id="0c66a-130">ExchangeMailbox, SharePointSite, TeamsMailbox, TeamsSite, YammerMailbox, YammerSite</span></span> |
|<span data-ttu-id="0c66a-131">**Emplacement Workload1**</span><span class="sxs-lookup"><span data-stu-id="0c66a-131">**Workload1 Location**</span></span>     | <span data-ttu-id="0c66a-132">En fonction de votre type de charge de travail, il s’agit de l’emplacement des données de votre charge de travail (par exemple, l’adresse de messagerie d’une boîte aux lettres Exchange ou l’URL d’un site SharePoint).</span><span class="sxs-lookup"><span data-stu-id="0c66a-132">Depending on your workload type, this would be the data location of your workload (for example, the email address of an Exchange mailbox or the URL for a SharePoint site).</span></span> |
|||

<span data-ttu-id="0c66a-133">Voici un exemple de fichier CSV contenant des informations sur les dépositaires :</span><span class="sxs-lookup"><span data-stu-id="0c66a-133">Here's an example of a CSV file with custodian information:</span></span>  

| <span data-ttu-id="0c66a-134">ContactEmail</span><span class="sxs-lookup"><span data-stu-id="0c66a-134">ContactEmail</span></span>      | <span data-ttu-id="0c66a-135">Exchange activé</span><span class="sxs-lookup"><span data-stu-id="0c66a-135">Exchange Enabled</span></span> | <span data-ttu-id="0c66a-136">OneDrive activé</span><span class="sxs-lookup"><span data-stu-id="0c66a-136">OneDrive Enabled</span></span> | <span data-ttu-id="0c66a-137">Est OnHold</span><span class="sxs-lookup"><span data-stu-id="0c66a-137">Is OnHold</span></span> | <span data-ttu-id="0c66a-138">Type Workload1</span><span class="sxs-lookup"><span data-stu-id="0c66a-138">Workload1 Type</span></span> | <span data-ttu-id="0c66a-139">Emplacement Workload1</span><span class="sxs-lookup"><span data-stu-id="0c66a-139">Workload1 Location</span></span>             |
| ----------------- | ---------------- | ---------------- | --------- | -------------- | ------------------------------ |
|<span data-ttu-id="0c66a-140">sarad@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0c66a-140">sarad@onmicrosoft.contoso.com</span></span> | <span data-ttu-id="0c66a-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-141">TRUE</span></span>             | <span data-ttu-id="0c66a-142">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-142">TRUE</span></span>             | <span data-ttu-id="0c66a-143">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-143">TRUE</span></span>      | <span data-ttu-id="0c66a-144">SharePointSite</span><span class="sxs-lookup"><span data-stu-id="0c66a-144">SharePointSite</span></span> | https://contoso.sharepoint.com |
|<span data-ttu-id="0c66a-145">pillarp@onmicrosoft.contoso.com</span><span class="sxs-lookup"><span data-stu-id="0c66a-145">pillarp@onmicrosoft.contoso.com</span></span> | <span data-ttu-id="0c66a-146">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-146">TRUE</span></span>             | <span data-ttu-id="0c66a-147">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-147">TRUE</span></span>             | <span data-ttu-id="0c66a-148">TRUE</span><span class="sxs-lookup"><span data-stu-id="0c66a-148">TRUE</span></span>      | |  |
||||||

## <a name="custodian-and-data-source-validation"></a><span data-ttu-id="0c66a-149">Validation des dépositaires et des sources de données</span><span class="sxs-lookup"><span data-stu-id="0c66a-149">Custodian and data source validation</span></span>

<span data-ttu-id="0c66a-150">Lorsque vous chargez le fichier CSV de dépositaire, Advanced eDiscovery effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c66a-150">When you upload the custodian CSV file, Advanced eDiscovery does the following things:</span></span>

1. <span data-ttu-id="0c66a-151">Valide les dépositaires et leurs sources de données.</span><span class="sxs-lookup"><span data-stu-id="0c66a-151">Validates the custodians and their data sources.</span></span> 

2. <span data-ttu-id="0c66a-152">Indexe toutes les sources de données pour chaque dépositaire et les place en conservation (si la propriété is OnHold est définie sur TRUE).</span><span class="sxs-lookup"><span data-stu-id="0c66a-152">Indexes all data sources for each custodian and places them on hold (if the Is OnHold property is set to TRUE).</span></span>

### <a name="custodian-validation"></a><span data-ttu-id="0c66a-153">Validation des dépositaires</span><span class="sxs-lookup"><span data-stu-id="0c66a-153">Custodian validation</span></span>

<span data-ttu-id="0c66a-154">Actuellement, nous ne prenons en charge que les dépositaires d’importation dans Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="0c66a-154">Currently, we only support importing custodians that are in Azure Active Directory (AAD).</span></span>

<span data-ttu-id="0c66a-155">Nous vérifions et trouvons des dépositaires à l’aide de la valeur UPN dans la colonne **adresse de messagerie du contact** dans le fichier CSV.</span><span class="sxs-lookup"><span data-stu-id="0c66a-155">We validate and find custodians using the UPN value in the **Contact Email** column in the CSV file.</span></span> <span data-ttu-id="0c66a-156">Les dépositaires validés sont automatiquement ajoutés à l’incident et répertoriés sous l’onglet **dépositaire** de la page **sources** du cas.</span><span class="sxs-lookup"><span data-stu-id="0c66a-156">Custodians that are validated are automatically added to the case and listed on the **Custodian** tab on the **Sources** page of the case.</span></span> <span data-ttu-id="0c66a-157">Si un dépositaire ne peut pas être validé, il est répertorié dans le journal des erreurs pour le travail BulkAddCustodian qui est répertorié sous l’onglet **travaux** dans le cas.</span><span class="sxs-lookup"><span data-stu-id="0c66a-157">If a custodian can't be validated, they are listed in the error log for the BulkAddCustodian job that is listed on the **Jobs** tab in the case.</span></span> <span data-ttu-id="0c66a-158">Les dépositaires non validés ne sont pas ajoutés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="0c66a-158">Unvalidated custodians are not added to the case.</span></span>

### <a name="data-source-validation"></a><span data-ttu-id="0c66a-159">Validation de la source de données</span><span class="sxs-lookup"><span data-stu-id="0c66a-159">Data source validation</span></span>

<span data-ttu-id="0c66a-160">Une fois les dépositaires validés et ajoutés au cas, chaque source de données associée à un dépositaire est validée.</span><span class="sxs-lookup"><span data-stu-id="0c66a-160">After custodians are validated and added to the case, each data source that's associated with a custodian is validated.</span></span> <span data-ttu-id="0c66a-161">Si une source de données pour un dépositaire est introuvable, la valeur **non validée** s’affiche dans la colonne **validé** de l’onglet **dépositaire** .</span><span class="sxs-lookup"><span data-stu-id="0c66a-161">If any data source for a custodian can't be found, the value **Not validated** would be displayed in the **Validated** column on the **Custodian** tab for that custodian.</span></span>

### <a name="remediating-unvalidated-data-sources"></a><span data-ttu-id="0c66a-162">Correction de sources de données non validées</span><span class="sxs-lookup"><span data-stu-id="0c66a-162">Remediating unvalidated data sources</span></span>

<span data-ttu-id="0c66a-163">Pour corriger les dépositaires avec des sources de données non validées :</span><span class="sxs-lookup"><span data-stu-id="0c66a-163">To remediate custodians with unvalidated data sources:</span></span> 

1. <span data-ttu-id="0c66a-164">Sous l’onglet **dépositaire** , sélectionnez un dépositaire qui n’est pas validé.</span><span class="sxs-lookup"><span data-stu-id="0c66a-164">On the **Custodian** tab, select a custodian who isn't validated.</span></span>

2. <span data-ttu-id="0c66a-165">Sur la page de menu volant dépositaire, faites défiler jusqu’à la section **sources de données** pour afficher les sources de données associées au dépositaire.</span><span class="sxs-lookup"><span data-stu-id="0c66a-165">On the custodian flyout page, scroll to the **Data sources** section to view the data sources that are associated with custodian.</span></span> <span data-ttu-id="0c66a-166">Les sources de données validées et non validées sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="0c66a-166">Both validated and unvalidated data sources are listed.</span></span>

3. <span data-ttu-id="0c66a-167">Dans la section **sources de données** , cliquez sur **modifier**.</span><span class="sxs-lookup"><span data-stu-id="0c66a-167">In the **Data sources** section, click **Edit**.</span></span>

4. <span data-ttu-id="0c66a-168">Sur la page **choisir les emplacements privatives d’adresses** , supprimez une source de données non validée.</span><span class="sxs-lookup"><span data-stu-id="0c66a-168">On the **Choose custodial locations** page, remove an unvalidated data source.</span></span>

5. <span data-ttu-id="0c66a-169">Sur la page **Sélectionner des emplacements supplémentaires** , cliquez sur **mettre à jour** pour ajouter des sources de données supplémentaires pour un dépositaire.</span><span class="sxs-lookup"><span data-stu-id="0c66a-169">On the **Select additional locations** page, click **Update** to add additional data sources for a custodian.</span></span>
