---
title: Découverte, protection et création de rapports en vertu du RGPD dans l’environnement de développement/test Microsoft 365
description: Découvrez comment configurer et illustrer les informations d’identification personnelle (PII) en vertu du RGPD dans un environnement de développement/test Microsoft 365.
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: c2112ce8-1c4b-424f-b200-59e161db2d21
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 0a8fc24d43899fbac2653bf5ce2f068f1f67972f
ms.sourcegitcommit: 260bbb93bbda62db9e88c021ccccfa75ac39a32e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "46845886"
---
# <a name="gdpr-discovery-protection-and-reporting-in-the-devtest-environment"></a><span data-ttu-id="203ea-103">Découverte, protection et création de rapports en vertu du RGPD dans l’environnement de développement/test</span><span class="sxs-lookup"><span data-stu-id="203ea-103">GDPR discovery, protection, and reporting in the dev/test environment</span></span>

 <span data-ttu-id="203ea-104">**Résumé :** Faire la démonstration des fonctionnalités du RGPD dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="203ea-104">**Summary:** Demonstrate GDPR capabilities in Microsoft 365.</span></span>

<span data-ttu-id="203ea-105">Cet article décrit comment configurer et faire la démonstration de la découverte, de la protection et de la création de rapports des informations d’identification personnelle (PII) en vertu du Règlement général sur la protection des données (RGPD) dans un environnement de développement/test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="203ea-105">This article describes how you configure and demonstrate personally identifiable information (PII) discovery, protection, and reporting for the General Data Protection Regulation (GDPR) in a Microsoft 365 dev/test environment.</span></span>

## <a name="phase-1-create-and-configure-your-trial-microsoft-365-subscription"></a><span data-ttu-id="203ea-106">Étape 1 : Créer et configurer votre abonnement d’évaluation Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="203ea-106">Phase 1: Create and configure your trial Microsoft 365 subscription</span></span>

<span data-ttu-id="203ea-107">Suivez d’abord les étapes de l’article [Phase 2 de l’environnement de développement/test Microsoft 365](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription).</span><span class="sxs-lookup"><span data-stu-id="203ea-107">First, follow the steps in [Phase 2 of the Microsoft 365 dev/test environment](https://docs.microsoft.com/Office365/Enterprise/office-365-dev-test-environment#phase-2-create-an-office-365-trial-subscription) article.</span></span>

<span data-ttu-id="203ea-108">Ensuite, suivez ces étapes pour configurer le Gestionnaire eDiscovery :</span><span class="sxs-lookup"><span data-stu-id="203ea-108">Next, use these steps to configure the eDiscovery manager:</span></span>

1. <span data-ttu-id="203ea-109">Connectez-vous à votre client d’évaluation Microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="203ea-109">Sign in to your Microsoft 365 trial tenant with your global administrator account.</span></span>
2. <span data-ttu-id="203ea-110">Sur la page d’accueil Microsoft 365, cliquez sur **Sécurité et conformité**.</span><span class="sxs-lookup"><span data-stu-id="203ea-110">From the Microsoft 365 home page, click **Security & Compliance**.</span></span>
3. <span data-ttu-id="203ea-111">Dans le nouvel onglet Sécurité et conformité, cliquez sur **Autorisations** > **Gestionnaire eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="203ea-111">From the new Security & Compliance tab, click **Permissions** > **eDiscovery Manager**.</span></span>
4. <span data-ttu-id="203ea-112">Cliquez sur **Modifier** pour le Gestionnaire eDiscovery, puis cliquez sur **Choisir le Gestionnaire eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="203ea-112">Click **Edit** for eDiscovery Manager, and then click **Choose eDiscovery Manager**.</span></span>
5. <span data-ttu-id="203ea-113">Cliquez sur **+ Ajouter**, recherchez le nom de votre compte d’administrateur général et ajoutez votre compte d’administrateur général comme Gestionnaire eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="203ea-113">Click **+ Add**, search for your global administrator account name and add your global administrator account as an eDiscovery Manager.</span></span>
6. <span data-ttu-id="203ea-114">Cliquez sur **Terminé** > **Enregistrer** > **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="203ea-114">Click **Done** > **Save** > **Close**.</span></span>

## <a name="phase-2-add-personally-identifiable-information-to-your-tenant"></a><span data-ttu-id="203ea-115">Phase 2 : Ajouter des informations d’identification personnelle à votre client</span><span class="sxs-lookup"><span data-stu-id="203ea-115">Phase 2: Add personally identifiable information to your tenant</span></span>

<span data-ttu-id="203ea-116">Dans cette phase, vous créez un document avec des données personnelles pour un ensemble d’exemples de numéro de compte bancaire international (IBAN) et le stockez sur un site SharePoint Online dans votre environnement de développement/test Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="203ea-116">In this phase, you create a document with PII for a set of example International Banking Account Numbers (IBANs) and store it on a SharePoint Online site in your Microsoft 365 dev/test environment.</span></span>

1. <span data-ttu-id="203ea-117">Sur votre ordinateur local, ouvrez Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="203ea-117">On your local computer, open Microsoft Word.</span></span>
2. <span data-ttu-id="203ea-118">Collez le tableau suivant dans le fichier Word et enregistrez-le sous « IBAN.docx » sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="203ea-118">Paste the following table in the Word file and save it as 'IBANs.docx' on your local computer.</span></span>

   |<span data-ttu-id="203ea-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="203ea-119">Number</span></span>|<span data-ttu-id="203ea-120">Pays</span><span class="sxs-lookup"><span data-stu-id="203ea-120">Country</span></span>|<span data-ttu-id="203ea-121">Code</span><span class="sxs-lookup"><span data-stu-id="203ea-121">Code</span></span>|<span data-ttu-id="203ea-122">IBAN</span><span class="sxs-lookup"><span data-stu-id="203ea-122">IBAN</span></span>|
   |---|---|---|---|
   |<span data-ttu-id="203ea-123">1</span><span class="sxs-lookup"><span data-stu-id="203ea-123">1</span></span>|<span data-ttu-id="203ea-124">Autriche SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-124">Austria SEPA</span></span>|<span data-ttu-id="203ea-125">AT</span><span class="sxs-lookup"><span data-stu-id="203ea-125">AT</span></span>|<span data-ttu-id="203ea-126">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="203ea-126">AT611904300234573201</span></span>|
   |<span data-ttu-id="203ea-127">2</span><span class="sxs-lookup"><span data-stu-id="203ea-127">2</span></span>|<span data-ttu-id="203ea-128">Bulgarie SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-128">Bulgaria SEPA</span></span>|<span data-ttu-id="203ea-129">BG</span><span class="sxs-lookup"><span data-stu-id="203ea-129">BG</span></span>|<span data-ttu-id="203ea-130">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="203ea-130">BG80BNBG96611020345678</span></span>|
   |<span data-ttu-id="203ea-131">3</span><span class="sxs-lookup"><span data-stu-id="203ea-131">3</span></span>|<span data-ttu-id="203ea-132">Danemark SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-132">Denmark SEPA</span></span>|<span data-ttu-id="203ea-133">DK</span><span class="sxs-lookup"><span data-stu-id="203ea-133">DK</span></span>|<span data-ttu-id="203ea-134">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="203ea-134">DK5000400440116243</span></span>|
   |<span data-ttu-id="203ea-135">4</span><span class="sxs-lookup"><span data-stu-id="203ea-135">4</span></span>|<span data-ttu-id="203ea-136">Finlande SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-136">Finland SEPA</span></span>|<span data-ttu-id="203ea-137">FI</span><span class="sxs-lookup"><span data-stu-id="203ea-137">FI</span></span>|<span data-ttu-id="203ea-138">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="203ea-138">FI2112345600000785</span></span>|
   |<span data-ttu-id="203ea-139">5</span><span class="sxs-lookup"><span data-stu-id="203ea-139">5</span></span>|<span data-ttu-id="203ea-140">France SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-140">France SEPA</span></span>|<span data-ttu-id="203ea-141">FR</span><span class="sxs-lookup"><span data-stu-id="203ea-141">FR</span></span>|<span data-ttu-id="203ea-142">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="203ea-142">FR1420041010050500013M02606</span></span>|
   |<span data-ttu-id="203ea-143">6</span><span class="sxs-lookup"><span data-stu-id="203ea-143">6</span></span>|<span data-ttu-id="203ea-144">Allemagne SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-144">Germany SEPA</span></span>|<span data-ttu-id="203ea-145">DE</span><span class="sxs-lookup"><span data-stu-id="203ea-145">DE</span></span>|<span data-ttu-id="203ea-146">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="203ea-146">DE89370400440532013000</span></span>|
   |<span data-ttu-id="203ea-147">7</span><span class="sxs-lookup"><span data-stu-id="203ea-147">7</span></span>|<span data-ttu-id="203ea-148">Grèce SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-148">Greece SEPA</span></span>|<span data-ttu-id="203ea-149">GR</span><span class="sxs-lookup"><span data-stu-id="203ea-149">GR</span></span>|<span data-ttu-id="203ea-150">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="203ea-150">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="203ea-151">8</span><span class="sxs-lookup"><span data-stu-id="203ea-151">8</span></span>|<span data-ttu-id="203ea-152">Italie SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-152">Italy SEPA</span></span>|<span data-ttu-id="203ea-153">IT</span><span class="sxs-lookup"><span data-stu-id="203ea-153">IT</span></span>|<span data-ttu-id="203ea-154">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="203ea-154">GR1601101250000000012300695</span></span>|
   |<span data-ttu-id="203ea-155">9</span><span class="sxs-lookup"><span data-stu-id="203ea-155">9</span></span>|<span data-ttu-id="203ea-156">Pays-Bas SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-156">Netherlands SEPA</span></span>|<span data-ttu-id="203ea-157">NL</span><span class="sxs-lookup"><span data-stu-id="203ea-157">NL</span></span>|<span data-ttu-id="203ea-158">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="203ea-158">NL91ABNA0417164300</span></span>|
   |<span data-ttu-id="203ea-159">10</span><span class="sxs-lookup"><span data-stu-id="203ea-159">10</span></span>|<span data-ttu-id="203ea-160">Pologne SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-160">Poland SEPA</span></span>|<span data-ttu-id="203ea-161">PL</span><span class="sxs-lookup"><span data-stu-id="203ea-161">PL</span></span>|<span data-ttu-id="203ea-162">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="203ea-162">PL27114020040000300201355387</span></span>|

   <span data-ttu-id="203ea-163">Remarque : cet ensemble de données d’exemple est dérivé d’informations disponibles publiquement et destinées uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="203ea-163">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

3. <span data-ttu-id="203ea-164">Dans un nouvel onglet de votre navigateur, saisissez : **https://**\<YourTenantName\>**.sharepoint.com**</span><span class="sxs-lookup"><span data-stu-id="203ea-164">In a new tab of your browser, type:  **https://**\<YourTenantName\>**.sharepoint.com**</span></span>
4. <span data-ttu-id="203ea-p101">Cliquez sur **Documents** pour ouvrir la bibliothèque de documents de ce site. Si vous êtes invité à suivre une visite guidée relative à une nouvelle expérience de liste, cliquez sur **Suivant** jusqu’à ce qu’elle se termine.</span><span class="sxs-lookup"><span data-stu-id="203ea-p101">Click **Documents** to open the document library for this site. If you're prompted for a new list experience tour, click **Next** until it's finished.</span></span>
5. <span data-ttu-id="203ea-167">Cliquez sur **Charger** > **Fichiers** puis sélectionnez le document IBAN.docx créé à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="203ea-167">Click **Upload** > **Files** and select the IBANs.docx you created in step 2.</span></span>

## <a name="phase-3-demonstrate-data-discovery"></a><span data-ttu-id="203ea-168">Phase 3 : Faire la démonstration de la découverte des données</span><span class="sxs-lookup"><span data-stu-id="203ea-168">Phase 3: Demonstrate data discovery</span></span>

<span data-ttu-id="203ea-169">Dans cette phase, vous allez faire la démonstration de la recherche afin de trouver le document créé et stocké à la Phase 2, en fonction de son contenu contenant des IBAN.</span><span class="sxs-lookup"><span data-stu-id="203ea-169">In this phase, you demonstrate search to find the document created and stored in Phase 2, based on its content containing IBANs.</span></span>

1. <span data-ttu-id="203ea-170">Dans l’onglet Sécurité et conformité, cliquez sur **Accueil**, puis sur **Recherches et examens** > **Recherche de contenu**.</span><span class="sxs-lookup"><span data-stu-id="203ea-170">From the Security & Compliance tab, click **Home**, and then click **Search & investigation** > **Content search**.</span></span>
2. <span data-ttu-id="203ea-171">Créez un nouvel élément de recherche en cliquant sur **+**.</span><span class="sxs-lookup"><span data-stu-id="203ea-171">Create a new search item by clicking on **+**.</span></span>
3. <span data-ttu-id="203ea-172">Dans une nouvelle fenêtre, fournissez les informations suivantes : a.</span><span class="sxs-lookup"><span data-stu-id="203ea-172">In a new window, provide the following information: a.</span></span> <span data-ttu-id="203ea-173">Nom : recherche IBAN b.</span><span class="sxs-lookup"><span data-stu-id="203ea-173">Name: IBAN Search b.</span></span> <span data-ttu-id="203ea-174">Où voulez-vous effectuer la recherche? : **Sélectionnez des sites spécifiques pour effectuer une recherche** (cliquez sur **+**), puis saisissez l’URL du site : **https://**\<YourTenantName\>**.sharepoint.com/** c.</span><span class="sxs-lookup"><span data-stu-id="203ea-174">Where do you want us to look?: **Choose specific sites to search** (click **+**), and then enter the site's URL: **https://**\<YourTenantName\>**.sharepoint.com/** c.</span></span> <span data-ttu-id="203ea-175">Cliquez sur **Ajouter**, puis sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="203ea-175">Click **Add**, and then click **OK**.</span></span> <span data-ttu-id="203ea-176">Si un avertissement s’affiche, cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="203ea-176">If you see a Warning, click **OK**.</span></span>
    <span data-ttu-id="203ea-177">d.</span><span class="sxs-lookup"><span data-stu-id="203ea-177">d.</span></span> <span data-ttu-id="203ea-178">Cliquez sur **Suivant** dans la fenêtre **Nouvelle recherche**.</span><span class="sxs-lookup"><span data-stu-id="203ea-178">Click **Next** on a **New search** window.</span></span>
    <span data-ttu-id="203ea-179">e.</span><span class="sxs-lookup"><span data-stu-id="203ea-179">e.</span></span> <span data-ttu-id="203ea-180">Pour **Que voulez-vous rechercher ?**  : **saisissez en faisant attention à la casse : « Numéro de compte bancaire international (IBAN) »**, puis cliquez sur **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="203ea-180">For **What do you want us to look for?**: **SensitiveType:"International Banking Account Number (IBAN)"**, and then click **Search**.</span></span>

4. <span data-ttu-id="203ea-181">Vérifiez que vous voyez au moins un élément répertorié dans les résultats **Recherche IBAN**.</span><span class="sxs-lookup"><span data-stu-id="203ea-181">Make sure you see at least one item listed in the **IBAN Search** results.</span></span>

## <a name="phase-4-create-a-custom-sensitive-information-type-via-powershell"></a><span data-ttu-id="203ea-182">Étape 4 : Créer un type d’informations sensibles personnalisé via PowerShell</span><span class="sxs-lookup"><span data-stu-id="203ea-182">Phase 4: Create a custom sensitive information type via PowerShell</span></span>

<span data-ttu-id="203ea-p103">Dans cette phase, vous créez un type d’informations sensibles personnalisé pour la société Contoso fictive à l’aide de Microsoft PowerShell. Contoso utilise un nombre de clients Contoso (CCN) pour identifier chaque client dans sa base de données client. Le CCN se compose de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="203ea-p103">In this phase, you create a custom sensitive information type for the fictional Contoso Corporation using Microsoft PowerShell.  Contoso uses a Contoso Customer Number (CCN) to identify each customer in their customer database. A CCN consists of the following structure:</span></span>

- <span data-ttu-id="203ea-186">Deux chiffres pour représenter l’année de la création de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="203ea-186">Two digits to represent the year that the record was created.</span></span>
  - <span data-ttu-id="203ea-187">Contoso a été fondée en 2002 ; par conséquent, la première valeur possible serait 02.</span><span class="sxs-lookup"><span data-stu-id="203ea-187">Contoso was founded in 2002; therefore, the earliest possible value would be 02.</span></span>
- <span data-ttu-id="203ea-188">Trois décimales pour représenter l’agence partenaire qui a créé l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="203ea-188">Three digits to represent the partner agency that created the record.</span></span>
  - <span data-ttu-id="203ea-189">Les valeurs possibles de l’agence sont comprises entre 000 et 999.</span><span class="sxs-lookup"><span data-stu-id="203ea-189">Possible agency values range from 000 to 999.</span></span>
- <span data-ttu-id="203ea-190">Un caractère alphabétique pour représenter le secteur d’activité.</span><span class="sxs-lookup"><span data-stu-id="203ea-190">An alphabetic character to represent the line of business.</span></span>
  - <span data-ttu-id="203ea-191">Les valeurs possibles sont comprises entre a et z et sont sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="203ea-191">Possible values are a-z and should be case insensitive.</span></span>
- <span data-ttu-id="203ea-192">Un numéro de série à quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="203ea-192">A four-digit serial number.</span></span>
  - <span data-ttu-id="203ea-193">Les valeurs possibles du numéro de série sont comprises entre 0000 et 9999.</span><span class="sxs-lookup"><span data-stu-id="203ea-193">Possible serial number values range from 0000 to 9999.</span></span>

<span data-ttu-id="203ea-p104">Contoso fait toujours référence aux clients en utilisant un CCN dans la correspondance interne, la correspondance externe, les documents, et tout autre formulaire. Contoso a besoin d’un type d’élément sensible personnalisé pour détecter l’utilisation de CCN dans le contenu Microsoft 365 afin d’appliquer la protection à l’utilisation de ce formulaire d’informations d’identification personnelle.</span><span class="sxs-lookup"><span data-stu-id="203ea-p104">Contoso always refers to customers by using a CCN in internal correspondence, external correspondence, documents, and other forms. Contoso needs a custom sensitive item type to detect the use of CCNs in Microsoft 365 content so that they may apply protection to the use of this form of personal identifiable information.</span></span>

1. <span data-ttu-id="203ea-196">Suivez les instructions de connexion avec authentification multifactorielle de la section [Connexion au PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) et connectez-vous au Centre de sécurité et conformité avec l’UPN de votre compte administrateur général.</span><span class="sxs-lookup"><span data-stu-id="203ea-196">Use the multi-factor authentication (MFA) connection instructions in [Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell) and connect to the Security & Compliance Center with UPN of your global administrator account.</span></span>

2. <span data-ttu-id="203ea-197">Exécutez les commandes PowerShell suivantes :</span><span class="sxs-lookup"><span data-stu-id="203ea-197">Run the following PowerShell commands.</span></span>

   ```powershell
   #Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName#Create & start search for sample data
   $searchName = "Sample Customer Information Search"
   $searchQuery = "15080P9562 OR 14040O1119 OR 15020J8317 OR 14050E2330 OR 16050E2166 OR 17040O1118"
   New-ComplianceSearch -Name $searchName -SharePointLocation All -ExchangeLocation All -ContentMatchQuery $searchQuery
   Start-ComplianceSearch -Identity $searchName
   ```

3. <span data-ttu-id="203ea-198">Exécutez les commandes PowerShell suivantes et copiez les GUID générés pour une instance ouverte du bloc-notes sur votre ordinateur dans l’ordre dans lequel ils sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="203ea-198">Run the following PowerShell commands and copy the generated GUIDs to an open instance of Notepad on your computer in the order in which they are listed.</span></span>

   ```powershell
   #Generate three unique GUIDs
   Write-Host "GUID1 = "([guid]::NewGuid().Guid)
   Write-Host "GUID2 = "([guid]::NewGuid().Guid)
   Write-Host "GUID3 = "([guid]::NewGuid().Guid)
   ```

4. <span data-ttu-id="203ea-199">Sur votre ordinateur local, ouvrez une autre instance du bloc-notes et collez-la dans le contenu suivant :</span><span class="sxs-lookup"><span data-stu-id="203ea-199">On your local computer, open another instance of Notepad and paste in the following content:</span></span>

   ```text
   <?xml version="1.0" encoding="utf-8"?>
   <RulePackage xmlns="https://schemas.microsoft.com/office/2011/mce">
   <RulePack id="GUID1">
   <Version major="1" minor="0" build="0" revision="0" />
   <Publisher id="GUID2" />
   <Details defaultLangCode="en">
   <LocalizedDetails langcode="en">
   <PublisherName>Contoso Ltd.</PublisherName>
   <Name>Contoso Rule Package</Name>
   <Description>Defines Contoso's custom set of classification rules</Description>
   </LocalizedDetails>
   </Details>
   </RulePack>
   <Rules>
   <!-- Contoso Customer Number (CCN) -->
   <Entity id="GUID3" patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
   <IdMatch idRef="Regex_contoso_ccn" />
   <Match idRef="Keyword_contoso_ccn" />
   <Match idRef="Regex_eu_date" />
   </Pattern>
   </Entity>
   <Regex id="Regex_contoso_ccn">[0-1][0-9][0-9]{3}[A-Za-z][0-9]{4}</Regex>
   <Keyword id="Keyword_contoso_ccn">
   <Group matchStyle="word">
   <Term caseSensitive="false">customer number</Term>
   <Term caseSensitive="false">customer no</Term>
   <Term caseSensitive="false">customer #</Term>
   <Term caseSensitive="false">customer#</Term>
   <Term caseSensitive="false">Contoso customer</Term>
   </Group>
   </Keyword>
   <Regex id="Regex_eu_date"> (0?[1-9]|[12][0-9]|3[0-1])[\/-](0?[1-9]|1[0-2]|j\x00e4n(uar)?|jan(uary|uari|uar|eiro|vier|v)?|ene(ro)?|genn(aio)? |feb(ruary|ruari|rero|braio|ruar|br)?|f\x00e9vr(ier)?|fev(ereiro)?|mar(zo|o|ch|s)?|m\x00e4rz|maart|apr(ile|il)?|abr(il)?|avril |may(o)?|magg(io)?|mai|mei|mai(o)?|jun(io|i|e|ho)?|giugno|juin|jul(y|io|i|ho)?|lu(glio)?|juil(let)?|ag(o|osto)?|aug(ustus|ust)?|ao\x00fbt|sep|sept(ember|iembre|embre)?|sett(embre)?|set(embro)?|oct(ober|ubre|obre)?|ott(obre)?|okt(ober)?|out(ubro)? |nov(ember|iembre|embre|embro)?|dec(ember)?|dic(iembre|embre)?|dez(ember|embro)?|d\x00e9c(embre)?)[ \/-](19|20)?[0-9]{2}</Regex>
   <LocalizedStrings>
   <Resource idRef="GUID3">
   <Name default="true" langcode="en-us">Contoso Customer Number (CCN)</Name>
   <Description default="true" langcode="en-us">Contoso Customer Number (CCN) that looks for additional keywords and EU formatted date</Description>
   </Resource>
   </LocalizedStrings>
   </Rules>
   </RulePackage>
   ```

5. <span data-ttu-id="203ea-200">Remplacez les valeurs GUID1, GUID2 et GUID3 dans le texte XML de l’étape 4 par leurs valeurs à l’étape 3, puis enregistrez le contenu sur votre ordinateur local avec le nom ContosoCCN.xml.</span><span class="sxs-lookup"><span data-stu-id="203ea-200">Replace the values of GUID1, GUID2, and GUID3 in the XML text of step 4 with their values from step 3, and then save the contents on your local computer with the name ContosoCCN.xml.</span></span>

6. <span data-ttu-id="203ea-201">Saisissez le chemin d’accès à votre fichier ContosoCCN.xml et exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="203ea-201">Fill in the path to your ContosoCCN.xml file and run the following commands.</span></span>

   ```powershell
   #Create new Sensitive Information Type
   $path="<path to the ContosoCCN.xml file, such as C:\Scripts\ContosoCCN.xml>"
   New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path $path -Encoding Byte -ReadCount 0)
   ```

7. <span data-ttu-id="203ea-p105">Dans l’onglet Sécurité et conformité, cliquez sur **Classifications** > **Types d’informations sensibles**. Vous devriez voir le nombre de clients Contoso (CCN) dans la liste.</span><span class="sxs-lookup"><span data-stu-id="203ea-p105">From the Security & Compliance tab, click **Classifications** > **Sensitive information types**. You should see the Contoso Customer Number (CCN) in the list.</span></span>

## <a name="phase-5-demonstrate-data-protection"></a><span data-ttu-id="203ea-204">Phase 5 : Faire la démonstration de la protection des données</span><span class="sxs-lookup"><span data-stu-id="203ea-204">Phase 5: Demonstrate data protection</span></span>

<span data-ttu-id="203ea-205">La protection des informations personnelles dans Microsoft 365 inclut l’utilisation des fonctionnalités de protection contre la perte de données (DLP).</span><span class="sxs-lookup"><span data-stu-id="203ea-205">Protection of personal information in Microsoft 365 includes using data loss prevention (DLP) capabilities.</span></span>  <span data-ttu-id="203ea-206">Grâce aux stratégies DLP, vous pouvez protéger automatiquement les informations sensibles dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="203ea-206">With DLP policies, you can automatically protect sensitive information across Microsoft 365.</span></span>

<span data-ttu-id="203ea-p107">Il existe plusieurs façons d’appliquer la protection. Éduquer et sensibiliser sur l’emplacement de stockage des données des citoyens européens dans votre environnement et sur la façon dont vos employés sont autorisés à les gérer représente un seul niveau de protection des informations à l’aide des stratégies DLP Office 365.</span><span class="sxs-lookup"><span data-stu-id="203ea-p107">There are multiple ways you can apply the protection. Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Office 365 DLP.</span></span>

<span data-ttu-id="203ea-209">Dans cette phase, vous créez une nouvelle stratégie DLP et faites la démonstration de son application sur le fichier IBAN.docx stocké dans SharePoint Online en Phase 2, et lorsque vous tentez d’envoyer un e-mail contenant des IBAN.</span><span class="sxs-lookup"><span data-stu-id="203ea-209">In this phase, you create a new DLP policy and demonstrate how it gets applied to the IBANs.docx file you stored in SharePoint Online in Phase 2 and when you attempt to send an email containing IBANs.</span></span>

1. <span data-ttu-id="203ea-210">Dans l’onglet Sécurité et conformité de votre navigateur, cliquez sur **Accueil**.</span><span class="sxs-lookup"><span data-stu-id="203ea-210">From the Security & Compliance tab of your browser, click **Home**.</span></span>
2. <span data-ttu-id="203ea-211">Cliquez sur **Protection contre la perte de données** > **Stratégie**.</span><span class="sxs-lookup"><span data-stu-id="203ea-211">Click **Data loss prevention** > **Policy**.</span></span>
3. <span data-ttu-id="203ea-212">Cliquez sur **+ Créer une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="203ea-212">Click **+ Create a policy**.</span></span>
4. <span data-ttu-id="203ea-213">Dans **Démarrer avec un modèle ou créer une stratégie personnalisée**, cliquez sur **Personnalisé** > **Stratégie personnalisée** > **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="203ea-213">In **Start with a template or create a custom policy**, click **Custom** > **Custom policy** > **Next**.</span></span>
5. <span data-ttu-id="203ea-p108">Dans **Nommer votre stratégie**, fournissez les informations suivantes, puis cliquez sur **Suivant** : a. Nom : **Stratégie de données personnelles pour les citoyens de l’UE** b. Description : **Protéger les informations d’identification personnelle des citoyens européens**</span><span class="sxs-lookup"><span data-stu-id="203ea-p108">In **Name your policy**, provide the following details and then click **Next**:  a. Name: **EU Citizen PII Policy** b. Description: **Protect the personally identifiable information of European citizens**</span></span>
6. <span data-ttu-id="203ea-p109">Dans **Choisir des emplacements**, sélectionnez **Tous les emplacements dans Microsoft 365**. Cela inclut le contenu des documents Messagerie Exchange, OneDrive et SharePoint. Puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="203ea-p109">In **Choose locations**, select **All locations in Microsoft 365**. This will include content in Exchange email and OneDrive and SharePoint documents. And then click **Next**.</span></span>
7. <span data-ttu-id="203ea-220">Dans **Personnaliser le type de contenu à protéger**, cliquez sur **Rechercher le contenu qui contient :** puis cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="203ea-220">In **Customize the type of content you want to protect**, click **Find content that contains:** and then click **Edit**.</span></span>
8. <span data-ttu-id="203ea-221">Dans **Choisir les types de contenu à protéger**, cliquez sur **Ajouter** > **Types d’informations sensibles**.</span><span class="sxs-lookup"><span data-stu-id="203ea-221">In **Choose the types of content to protect**, click **Add** > **Sensitive info types**.</span></span>
9. <span data-ttu-id="203ea-222">Dans **Types d’informations sensibles**, cliquez sur **+ Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="203ea-222">In **Sensitive info types**, click **+ Add**.</span></span>
10. <span data-ttu-id="203ea-223">Dans **Types d’informations sensibles**, recherchez **IBAN**, cochez la case **Numéro de compte bancaire international (IBAN)**, puis cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="203ea-223">In **Sensitive info types**, search for **IBAN**, select the check box for **International Banking Account Number (IBAN)**, and then click **Add**.</span></span>
11. <span data-ttu-id="203ea-224">Vérifiez que le type d’informations sensibles **Numéro de compte bancaire international (IBAN)** a été ajouté, puis cliquez **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="203ea-224">Confirm that the **International Banking Account Number (IBAN)** sensitive information type was added, and then click **Done**.</span></span>
12. <span data-ttu-id="203ea-225">Dans **Le contenu contient**, vérifiez que les types d’informations sensibles ont été ajoutés, puis sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="203ea-225">In **Content contains**, confirm that the sensitive information types were added and then click **Save**.</span></span>
13. <span data-ttu-id="203ea-226">Dans **Personnaliser le type de contenu à protéger**, confirmez que **Rechercher le contenu qui contient :** contient le **Numéro de compte bancaire international (IBAN)**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="203ea-226">In **Customize the type of content you want to protect**, confirm  **Find content that contains:** contains the **International Banking Account Number (IBAN)**, and then click **Next**.</span></span>
14. <span data-ttu-id="203ea-227">Dans **Détecter le contenu partagé qui contient :**, changez la valeur de **10** à **1**, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="203ea-227">In **Detect when content that's being shared contains:**, change the value from **10** to **1**, and then click **Next**.</span></span>
15. <span data-ttu-id="203ea-228">Dans **Voulez-vous activer la stratégie ou faire d’abord un test ?**, choisissez les paramètres suivants, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="203ea-228">In **Do you want to turn on the policy or test things out first?**, choose the following settings, and then click **Next**.</span></span>
    <span data-ttu-id="203ea-229">a.</span><span class="sxs-lookup"><span data-stu-id="203ea-229">a.</span></span> <span data-ttu-id="203ea-230">Sélectionnez l’option pour **Je souhaite commencer par effectuer des tests** b.</span><span class="sxs-lookup"><span data-stu-id="203ea-230">Select the option for **I'd like to test it out first** b.</span></span> <span data-ttu-id="203ea-231">Cochez la case **Afficher les conseils de stratégie en mode test**</span><span class="sxs-lookup"><span data-stu-id="203ea-231">Select the check box for **Show policy tips while in test mode**</span></span>
16. <span data-ttu-id="203ea-p111">Dans **Vérifier vos paramètres**, cliquez sur **Créer** après avoir consulté les paramètres. REMARQUE : après avoir créé une nouvelle stratégie DLP, vous devrez patienter un certain temps avant qu’elle prenne effet.</span><span class="sxs-lookup"><span data-stu-id="203ea-p111">In **Review your settings**, click **Create** after reviewing the settings. NOTE: After you create a new DLP policy, it will take a while for it to take effect.</span></span>
17. <span data-ttu-id="203ea-234">Sur votre ordinateur local, ouvrez une instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="203ea-234">On your local computer, open a private instance of your browser.</span></span>
18. <span data-ttu-id="203ea-235">Dans la barre d’adresses, saisissez **https://**\<YourTenantName\>**.sharepoint.com** et connectez-vous à l’aide de votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="203ea-235">In the address bar, type **https://**\<YourTenantName\>**.sharepoint.com** and sign in using your global administrator account.</span></span>
19. <span data-ttu-id="203ea-236">Cliquez sur **Documents**.</span><span class="sxs-lookup"><span data-stu-id="203ea-236">Click **Documents**.</span></span>
20. <span data-ttu-id="203ea-p112">Cliquez sur le fichier nommé « IBAN.docx ». Vous devriez voir « Conseil de stratégie pour IBAN.docx ». Le fichier IBAN.docx a été partagé avec des destinataires externes, ce qui constitue une violation de la stratégie DLP.</span><span class="sxs-lookup"><span data-stu-id="203ea-p112">Click the file named 'IBANs.docx'. You should see 'Policy tip for IBANs.docx'.  The IBANs.docx file was shared with external recipients, which violates the DLP policy.</span></span>
21. <span data-ttu-id="203ea-240">Dans la barre d’adresses, saisissez : `https://outlook.office365.com`</span><span class="sxs-lookup"><span data-stu-id="203ea-240">In the address bar, type: `https://outlook.office365.com`</span></span>
22. <span data-ttu-id="203ea-241">Cliquez sur **Nouveau** - **Message électronique** et fournissez les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="203ea-241">Click **New** - **Email message** and provide the following:</span></span>

    - <span data-ttu-id="203ea-242">**À :** \<a personal email address\></span><span class="sxs-lookup"><span data-stu-id="203ea-242">**To:** \<a personal email address\></span></span>
    - <span data-ttu-id="203ea-243">**Objet :** Test RGPD</span><span class="sxs-lookup"><span data-stu-id="203ea-243">**Subject:** GDPR Test</span></span>
    - <span data-ttu-id="203ea-244">**Corps :** copiez le tableau des valeurs indiquées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="203ea-244">**Body:** Copy in the table of values shown below.</span></span>

      |<span data-ttu-id="203ea-245">Nombre</span><span class="sxs-lookup"><span data-stu-id="203ea-245">Number</span></span>|<span data-ttu-id="203ea-246">Pays</span><span class="sxs-lookup"><span data-stu-id="203ea-246">Country</span></span>|<span data-ttu-id="203ea-247">Code</span><span class="sxs-lookup"><span data-stu-id="203ea-247">Code</span></span>|<span data-ttu-id="203ea-248">IBAN</span><span class="sxs-lookup"><span data-stu-id="203ea-248">IBAN</span></span>|
      |---|---|---|---|
      |<span data-ttu-id="203ea-249">1</span><span class="sxs-lookup"><span data-stu-id="203ea-249">1</span></span>|<span data-ttu-id="203ea-250">Autriche SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-250">Austria SEPA</span></span>|<span data-ttu-id="203ea-251">AT</span><span class="sxs-lookup"><span data-stu-id="203ea-251">AT</span></span>|<span data-ttu-id="203ea-252">AT611904300234573201</span><span class="sxs-lookup"><span data-stu-id="203ea-252">AT611904300234573201</span></span>|
      |<span data-ttu-id="203ea-253">2</span><span class="sxs-lookup"><span data-stu-id="203ea-253">2</span></span>|<span data-ttu-id="203ea-254">Bulgarie SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-254">Bulgaria SEPA</span></span>|<span data-ttu-id="203ea-255">BG</span><span class="sxs-lookup"><span data-stu-id="203ea-255">BG</span></span>|<span data-ttu-id="203ea-256">BG80BNBG96611020345678</span><span class="sxs-lookup"><span data-stu-id="203ea-256">BG80BNBG96611020345678</span></span>|
      |<span data-ttu-id="203ea-257">3</span><span class="sxs-lookup"><span data-stu-id="203ea-257">3</span></span>|<span data-ttu-id="203ea-258">Danemark SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-258">Denmark SEPA</span></span>|<span data-ttu-id="203ea-259">DK</span><span class="sxs-lookup"><span data-stu-id="203ea-259">DK</span></span>|<span data-ttu-id="203ea-260">DK5000400440116243</span><span class="sxs-lookup"><span data-stu-id="203ea-260">DK5000400440116243</span></span>|
      |<span data-ttu-id="203ea-261">4</span><span class="sxs-lookup"><span data-stu-id="203ea-261">4</span></span>|<span data-ttu-id="203ea-262">Finlande SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-262">Finland SEPA</span></span>|<span data-ttu-id="203ea-263">FI</span><span class="sxs-lookup"><span data-stu-id="203ea-263">FI</span></span>|<span data-ttu-id="203ea-264">FI2112345600000785</span><span class="sxs-lookup"><span data-stu-id="203ea-264">FI2112345600000785</span></span>|
      |<span data-ttu-id="203ea-265">5</span><span class="sxs-lookup"><span data-stu-id="203ea-265">5</span></span>|<span data-ttu-id="203ea-266">France SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-266">France SEPA</span></span>|<span data-ttu-id="203ea-267">FR</span><span class="sxs-lookup"><span data-stu-id="203ea-267">FR</span></span>|<span data-ttu-id="203ea-268">FR1420041010050500013M02606</span><span class="sxs-lookup"><span data-stu-id="203ea-268">FR1420041010050500013M02606</span></span>|
      |<span data-ttu-id="203ea-269">6</span><span class="sxs-lookup"><span data-stu-id="203ea-269">6</span></span>|<span data-ttu-id="203ea-270">Allemagne SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-270">Germany SEPA</span></span>|<span data-ttu-id="203ea-271">DE</span><span class="sxs-lookup"><span data-stu-id="203ea-271">DE</span></span>|<span data-ttu-id="203ea-272">DE89370400440532013000</span><span class="sxs-lookup"><span data-stu-id="203ea-272">DE89370400440532013000</span></span>|
      |<span data-ttu-id="203ea-273">7</span><span class="sxs-lookup"><span data-stu-id="203ea-273">7</span></span>|<span data-ttu-id="203ea-274">Grèce SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-274">Greece SEPA</span></span>|<span data-ttu-id="203ea-275">GR</span><span class="sxs-lookup"><span data-stu-id="203ea-275">GR</span></span>|<span data-ttu-id="203ea-276">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="203ea-276">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="203ea-277">8</span><span class="sxs-lookup"><span data-stu-id="203ea-277">8</span></span>|<span data-ttu-id="203ea-278">Italie SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-278">Italy SEPA</span></span>|<span data-ttu-id="203ea-279">IT</span><span class="sxs-lookup"><span data-stu-id="203ea-279">IT</span></span>|<span data-ttu-id="203ea-280">GR1601101250000000012300695</span><span class="sxs-lookup"><span data-stu-id="203ea-280">GR1601101250000000012300695</span></span>|
      |<span data-ttu-id="203ea-281">9</span><span class="sxs-lookup"><span data-stu-id="203ea-281">9</span></span>|<span data-ttu-id="203ea-282">Pays-Bas SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-282">Netherlands SEPA</span></span>|<span data-ttu-id="203ea-283">NL</span><span class="sxs-lookup"><span data-stu-id="203ea-283">NL</span></span>|<span data-ttu-id="203ea-284">NL91ABNA0417164300</span><span class="sxs-lookup"><span data-stu-id="203ea-284">NL91ABNA0417164300</span></span>|
      |<span data-ttu-id="203ea-285">10</span><span class="sxs-lookup"><span data-stu-id="203ea-285">10</span></span>|<span data-ttu-id="203ea-286">Pologne SEPA</span><span class="sxs-lookup"><span data-stu-id="203ea-286">Poland SEPA</span></span>|<span data-ttu-id="203ea-287">PL</span><span class="sxs-lookup"><span data-stu-id="203ea-287">PL</span></span>|<span data-ttu-id="203ea-288">PL27114020040000300201355387</span><span class="sxs-lookup"><span data-stu-id="203ea-288">PL27114020040000300201355387</span></span>|
      |

    <span data-ttu-id="203ea-289">Remarque : cet ensemble de données d’exemple est dérivé d’informations disponibles publiquement et destinées uniquement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="203ea-289">Note:- This sample data set is derived from publicly available information and is intended to be used for test purposes only.</span></span>

23. <span data-ttu-id="203ea-290">Vous verrez que la stratégie DLP a reconnu que le corps de l’e-mail contient des IBAN et vous fournit le conseil de stratégie dans la partie supérieure de la fenêtre du message.</span><span class="sxs-lookup"><span data-stu-id="203ea-290">You will see that the DLP policy recognized that body of the email contains IBANs and provides you with the policy tip at the top of the message window.</span></span>
24. <span data-ttu-id="203ea-291">Fermez l’instance privée de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="203ea-291">Close the private instance of your browser.</span></span>

## <a name="phase-6-demonstrate-reporting"></a><span data-ttu-id="203ea-292">Phase 6 : Faire la démonstration de la création de rapports</span><span class="sxs-lookup"><span data-stu-id="203ea-292">Phase 6: Demonstrate reporting</span></span>

<span data-ttu-id="203ea-293">Dans cette phase, vous allez faire la démonstration de la création de rapports Microsoft 365 basée sur la stratégie DLP configurée en Phase 5.</span><span class="sxs-lookup"><span data-stu-id="203ea-293">In this phase, you demonstrate Microsoft 365 reporting based on the DLP policy configured in Phase 5.</span></span>

   1. <span data-ttu-id="203ea-294">Dans l’onglet Sécurité et conformité de votre navigateur, cliquez sur **Accueil**.</span><span class="sxs-lookup"><span data-stu-id="203ea-294">From the Security & Compliance tab of your browser, click **Home**.</span></span>
   2. <span data-ttu-id="203ea-295">Cliquez sur **Rapports** > **Tableau de bord** > **Correspondances de stratégies DLP**.</span><span class="sxs-lookup"><span data-stu-id="203ea-295">Click **Reports** > **Dashboard** > **DLP policy matches**.</span></span>
   3. <span data-ttu-id="203ea-p113">Votre stratégie DLP vous aide à identifier et à protéger les informations sensibles de l’organisation. Par exemple, dans le rapport vous verrez que la stratégie a identifié le document contenant les IBAN stocké dans SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="203ea-p113">Your DLP policy helps identify and protect organization's sensitive information. For example, in the report you will see that the policy identified the document that contains IBANs stored in SharePoint Online.</span></span>

## <a name="see-also"></a><span data-ttu-id="203ea-298">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="203ea-298">See Also</span></span>

[<span data-ttu-id="203ea-299">Protection des informations Office 365 pour RGPD</span><span class="sxs-lookup"><span data-stu-id="203ea-299">Office 365 Information Protection for GDPR</span></span>](office-365-information-protection-for-gdpr.md)

[<span data-ttu-id="203ea-300">RGPD pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="203ea-300">GDPR for Microsoft 365</span></span>](https://docs.microsoft.com/microsoft-365/compliance/gdpr?toc=/microsoft-365/enterprise/toc.json)
