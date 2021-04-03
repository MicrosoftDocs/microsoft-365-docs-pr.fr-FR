---
title: Analyseur de configuration de la conformité Microsoft pour le Gestionnaire de conformité
f1.keywords:
- NOCSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Comprendre comment utiliser l’Analyseur de configuration de conformité Microsoft pour être rapidement opérationnel avec le Gestionnaire de conformité Microsoft.
ms.openlocfilehash: 2b91ac274d7270f5be9530742cf711a3918b287d
ms.sourcegitcommit: 6e5c00f84b5201422aed094f2697016407df8fc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51570373"
---
# <a name="microsoft-compliance-configuration-analyzer-for-compliance-manager-preview"></a><span data-ttu-id="3e199-103">Analyseur de configuration de la conformité Microsoft pour le Gestionnaire de conformité (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="3e199-103">Microsoft Compliance Configuration Analyzer for Compliance Manager (preview)</span></span>

<span data-ttu-id="3e199-104">**Dans cet article :** Découvrez comment installer et exécuter l’outil Microsoft Compliance Configure Analyzer pour commencer rapidement avec le gestionnaire de conformité Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3e199-104">**In this article:** Learn how to install and run the Microsoft Compliance Configure Analyzer tool to get quickly started with Microsoft Compliance Manger.</span></span>

## <a name="microsoft-compliance-configuration-analyzer-mcca-preview-overview"></a><span data-ttu-id="3e199-105">Présentation de l’Analyseur de configuration de la conformité Microsoft (MCCA) (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="3e199-105">Microsoft Compliance Configuration Analyzer (MCCA) (preview) overview</span></span>

<span data-ttu-id="3e199-106">L’Analyseur de configuration de la conformité Microsoft (MCCA) est un outil de prévisualisation qui peut vous aider à démarrer avec le Gestionnaire de [conformité Microsoft.](compliance-manager.md)</span><span class="sxs-lookup"><span data-stu-id="3e199-106">The Microsoft Compliance Configuration Analyzer (MCCA) is a preview tool that can help you get started with [Microsoft Compliance Manager](compliance-manager.md).</span></span> <span data-ttu-id="3e199-107">MCCA est un utilitaire basé sur PowerShell qui récupère les configurations actuelles de votre organisation et les valide par rapport aux meilleures pratiques recommandées de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3e199-107">MCCA is a PowerShell-based utility that will fetch your organization’s current configurations and validate them against Microsoft 365 recommended best practices.</span></span> <span data-ttu-id="3e199-108">Ces meilleures pratiques sont basées sur un ensemble de contrôles qui incluent des réglementations clés et des normes pour la protection des données et la gouvernance des données.</span><span class="sxs-lookup"><span data-stu-id="3e199-108">These best practices are based on a set of controls that include key regulations and standards for data protection and data governance.</span></span>

<span data-ttu-id="3e199-109">MCCA peut vous aider à voir rapidement quelles actions d’amélioration du Gestionnaire de conformité s’appliquent à votre environnement Microsoft 365 actuel.</span><span class="sxs-lookup"><span data-stu-id="3e199-109">MCCA can help you quickly see which improvement actions in Compliance Manger apply to your current Microsoft 365 environment.</span></span> <span data-ttu-id="3e199-110">Chaque action identifiée par MCCA vous donne des recommandations pour l’implémentation, avec des liens directs vers le Gestionnaire de conformité et la solution applicable pour commencer à prendre des mesures correctives.</span><span class="sxs-lookup"><span data-stu-id="3e199-110">Each action identified by MCCA will give you recommendations for implementation, with direct links to Compliance Manager and the applicable solution to start taking corrective action.</span></span>

<span data-ttu-id="3e199-111">Une ressource supplémentaire pour comprendre MCCA consiste à consulter les [instructions README sur GitHub.](https://github.com/OfficeDev/MCCA#overview)</span><span class="sxs-lookup"><span data-stu-id="3e199-111">An additional resource for understanding MCCA is by visiting the [README instructions on GitHub](https://github.com/OfficeDev/MCCA#overview).</span></span> <span data-ttu-id="3e199-112">Cette page fournit des informations détaillées sur les conditions préalables et fournit des instructions d’installation complètes.</span><span class="sxs-lookup"><span data-stu-id="3e199-112">This page provides detailed information about prerequisites and gives full installation instructions.</span></span> <span data-ttu-id="3e199-113">Vous n’avez pas besoin d’un compte GitHub pour accéder à cette page.</span><span class="sxs-lookup"><span data-stu-id="3e199-113">You don’t need a GitHub account to access this page.</span></span>

<span data-ttu-id="3e199-114">Disponibilité : MCCA est disponible pour toutes les organisations titulaires de licences Office 365 et Microsoft 365, ainsi que pour les clients modérés, GCC High et Department of Defense (DoD) de la Communauté du gouvernement américain (GCC).</span><span class="sxs-lookup"><span data-stu-id="3e199-114">**Availability**: MCCA is available to all organizations with Office 365 and Microsoft 365 licenses and US Government Community (GCC) Moderate, GCC High, and Department of Defense (DoD) customers.</span></span>

## <a name="install-mcca-and-run-a-report"></a><span data-ttu-id="3e199-115">Installer MCCA et exécuter un rapport</span><span class="sxs-lookup"><span data-stu-id="3e199-115">Install MCCA and run a report</span></span>

<span data-ttu-id="3e199-116">Vous pouvez installer l’outil MCCA à l’aide Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e199-116">You can install the MCCA tool using Windows PowerShell.</span></span> <span data-ttu-id="3e199-117">Une fois que vous avez téléchargé et installé l’outil, vous n’avez pas besoin de répéter ces étapes pour exécuter des rapports.</span><span class="sxs-lookup"><span data-stu-id="3e199-117">Once you download and install the tool, you don’t need to repeat those steps in order to run reports.</span></span> <span data-ttu-id="3e199-118">Chaque fois que vous ouvrez MCCA, il vous demande vos informations d’identification de connexion et génère un nouveau rapport mis à jour.</span><span class="sxs-lookup"><span data-stu-id="3e199-118">Each time you open MCCA, it will ask you for your login credentials, and it will generate a new, updated report.</span></span>

#### <a name="step-1-install-windows-powershell"></a><span data-ttu-id="3e199-119">Étape 1 : Installer Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e199-119">Step 1: Install Windows PowerShell</span></span>
<span data-ttu-id="3e199-120">Pour commencer, vous aurez besoin du module Exchange Online PowerShell (version 2.0.3 ou supérieure) disponible dans la galerie PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e199-120">To begin, you'll need the Exchange Online PowerShell module (v2.0.3 or higher) that's available in the PowerShell gallery.</span></span> <span data-ttu-id="3e199-121">[Obtenir des instructions d’installation.](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/2.0.3)</span><span class="sxs-lookup"><span data-stu-id="3e199-121">[Get installation instructions](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/2.0.3).</span></span>

#### <a name="step-2-install-mcca"></a><span data-ttu-id="3e199-122">Étape 2 : Installer MCCA</span><span class="sxs-lookup"><span data-stu-id="3e199-122">Step 2: Install MCCA</span></span>

<span data-ttu-id="3e199-123">Pour installer MCCA, commencez par utiliser PowerShell en mode administrateur.</span><span class="sxs-lookup"><span data-stu-id="3e199-123">To install MCCA, start by using PowerShell in administrator mode.</span></span> <span data-ttu-id="3e199-124">Suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="3e199-124">Follow the steps below:</span></span>

1. <span data-ttu-id="3e199-125">Sélectionnez le bouton **Démarrer** de Windows.</span><span class="sxs-lookup"><span data-stu-id="3e199-125">Select the Windows **Start** button.</span></span>
2. <span data-ttu-id="3e199-126">Tapez **PowerShell,** cliquez avec le bouton **droit sur Windows PowerShell,** puis **sélectionnez Exécuter en tant qu’administrateur.**</span><span class="sxs-lookup"><span data-stu-id="3e199-126">Type **PowerShell**, right-click on **Windows PowerShell**, then select **Run as administrator**.</span></span>
1. <span data-ttu-id="3e199-127">Depuis l’invite de commandes, tapez :</span><span class="sxs-lookup"><span data-stu-id="3e199-127">At the command prompt, type:</span></span>

    ```powershell
    Install-Module -Name MCCAPreview
    ```

#### <a name="step-3-run-a-report"></a><span data-ttu-id="3e199-128">Étape 3 : Exécuter un rapport</span><span class="sxs-lookup"><span data-stu-id="3e199-128">Step 3: Run a report</span></span>

<span data-ttu-id="3e199-129">Après avoir installé MCCA, vous pouvez exécuter MCCA et générer un rapport.</span><span class="sxs-lookup"><span data-stu-id="3e199-129">After you install MCCA, you can run MCCA and generate a report.</span></span> <span data-ttu-id="3e199-130">Pour exécuter un rapport :</span><span class="sxs-lookup"><span data-stu-id="3e199-130">To run a report:</span></span>

1. <span data-ttu-id="3e199-131">Ouvrir PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e199-131">Open PowerShell</span></span>
2. <span data-ttu-id="3e199-132">Exécutez l’cmdlet :</span><span class="sxs-lookup"><span data-stu-id="3e199-132">Run the cmdlet:</span></span>

    ```powershell
    Get-MCCAReport
    ```

   <span data-ttu-id="3e199-133">Si vous êtes un client GCC High, vous devez fournir un paramètre d’entrée supplémentaire pour exécuter le rapport :</span><span class="sxs-lookup"><span data-stu-id="3e199-133">If you're a GCC High customer, you'll need to provide an additional input parameter to run the report:</span></span>

    ```powershell
    Get-MCCAReport -ExchangeEnvironmentName O365USGovGCCHigh
    ```

3. <span data-ttu-id="3e199-134">Une fois que MCCA s’exécute, il vérifie la version initiale et demande des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="3e199-134">Once MCCA runs, it does an initial version check and ask for credentials.</span></span> <span data-ttu-id="3e199-135">À l’invite d’entrée du nom d’utilisateur, connectez-vous avec votre adresse de messagerie de compte Microsoft 365 (affichez les rôles éligibles[pour créer des rapports).](#role-based-reporting)</span><span class="sxs-lookup"><span data-stu-id="3e199-135">At the Input the user name prompt, sign in with your Microsoft 365 account email address ([view the roles eligible to create reports](#role-based-reporting)).</span></span> <span data-ttu-id="3e199-136">Entrez ensuite votre mot de passe à l’invite de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3e199-136">Then enter your password at the password prompt.</span></span>

<span data-ttu-id="3e199-137">Votre rapport prendra ensuite environ 2 à 5 minutes pour être généré.</span><span class="sxs-lookup"><span data-stu-id="3e199-137">Your report will then take approximately 2-5 minutes to generate.</span></span> <span data-ttu-id="3e199-138">Une fois l’application effectuée, une fenêtre de navigateur s’ouvre et affiche votre rapport HTML.</span><span class="sxs-lookup"><span data-stu-id="3e199-138">When it’s done, a browser window opens and displays your HTML report.</span></span> <span data-ttu-id="3e199-139">Chaque fois que vous exécutez l’outil, il vous demande vos informations d’identification et génère un nouveau rapport.</span><span class="sxs-lookup"><span data-stu-id="3e199-139">Every time you run the tool, it will ask for your credentials and generate a new report.</span></span> <span data-ttu-id="3e199-140">Ce rapport est stocké localement dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="3e199-140">This report is stored locally in the following directory:</span></span>

<span data-ttu-id="3e199-141">C:\Users \<username> \AppData\Local\Microsoft\MCCA.</span><span class="sxs-lookup"><span data-stu-id="3e199-141">C:\Users\<username>\AppData\Local\Microsoft\MCCA.</span></span> 

<span data-ttu-id="3e199-142">Vous pouvez accéder aux rapports générés précédemment à partir de ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="3e199-142">You can access previously generated reports from this directory.</span></span>

## <a name="understanding-your-report"></a><span data-ttu-id="3e199-143">Comprendre votre rapport</span><span class="sxs-lookup"><span data-stu-id="3e199-143">Understanding your report</span></span>

<span data-ttu-id="3e199-144">Votre rapport reflète les données en fonction de la date et de l’heure à laquelle il a été généré.</span><span class="sxs-lookup"><span data-stu-id="3e199-144">Your report reflects data based on the date and time at which it was generated.</span></span> <span data-ttu-id="3e199-145">La section supérieure fournit des détails sur la moment où elle a été générée, le nom de votre organisation et l’ID de client.</span><span class="sxs-lookup"><span data-stu-id="3e199-145">The top section provides details on when it was generated, your organization name, and tenant ID.</span></span>

#### <a name="geolocation-based-reporting"></a><span data-ttu-id="3e199-146">Rapports basés sur la géolocalisation</span><span class="sxs-lookup"><span data-stu-id="3e199-146">Geolocation-based reporting</span></span>

<span data-ttu-id="3e199-147">La  section Remarque indique que votre rapport est personnalisé en fonction de l’emplacement géographique de votre client.</span><span class="sxs-lookup"><span data-stu-id="3e199-147">The **Note** section shows that your report is customized based on the geographic location of your tenant.</span></span> <span data-ttu-id="3e199-148">Les recommandations répertoriées dans l’outil seront spécifiques à votre pays ou région.</span><span class="sxs-lookup"><span data-stu-id="3e199-148">Recommendations listed in the tool will be specific to your country or region.</span></span>

<span data-ttu-id="3e199-149">Votre sélection de géolocalisation permet d’évaluer les types d’informations sensibles (SIT) qui sont pertinents pour cette géolocalisation et de générer un rapport qui s’aligne sur votre pays ou région.</span><span class="sxs-lookup"><span data-stu-id="3e199-149">Your geolocation selection is used to assess sensitive information types (SITs) which are relevant to that geolocation and generate a report that aligns to your country or region.</span></span> <span data-ttu-id="3e199-150">Choisissez des géolocalisations en fonction des données que vous avez dans votre client.</span><span class="sxs-lookup"><span data-stu-id="3e199-150">Choose geolocations based on data you have in your tenant.</span></span>

<span data-ttu-id="3e199-151">Pour modifier les informations d’emplacement de votre rapport, vous devez fournir un paramètre d’entrée de géolocalisation (-Geo).</span><span class="sxs-lookup"><span data-stu-id="3e199-151">To change your report's location information, you need provide a geolocation (-Geo) input parameter.</span></span> <span data-ttu-id="3e199-152">Vous pouvez choisir une ou plusieurs géolocalisations applicables à votre client.</span><span class="sxs-lookup"><span data-stu-id="3e199-152">You can choose either one or multiple geolocations applicable for your tenant.</span></span>

<span data-ttu-id="3e199-153">Suivez ces instructions pour exécuter un rapport basé sur un emplacement spécifique :</span><span class="sxs-lookup"><span data-stu-id="3e199-153">Follow these instructions to run a report based on a specific location:</span></span>

1. <span data-ttu-id="3e199-154">Ouvrir PowerShell</span><span class="sxs-lookup"><span data-stu-id="3e199-154">Open PowerShell</span></span>
2. <span data-ttu-id="3e199-155">Pour spécifier une région, vous devez exécuter une cmdlet à l’aide des numéros du tableau ci-dessous qui correspondent au pays ou à la région.</span><span class="sxs-lookup"><span data-stu-id="3e199-155">To specify a certain region, you’ll run a cmdlet using the numbers from the table below that correspond to the country or region.</span></span> <span data-ttu-id="3e199-156">Entrez plusieurs nombres en les séparant par une virgule.</span><span class="sxs-lookup"><span data-stu-id="3e199-156">Enter multiple numbers by separating them with a comma.</span></span> <span data-ttu-id="3e199-157">Par exemple, la cmdlet ci-dessous exécute un rapport personnalisé pour Asia-Pacific et le Japon :</span><span class="sxs-lookup"><span data-stu-id="3e199-157">For example, the cmdlet below will run a customized report for Asia-Pacific and Japan:</span></span>

    ```powershell
    Get-MCCAReport -Geo @(1,7)
    ```
  | <span data-ttu-id="3e199-158">Input</span><span class="sxs-lookup"><span data-stu-id="3e199-158">Input</span></span> |  <span data-ttu-id="3e199-159">Pays ou région</span><span class="sxs-lookup"><span data-stu-id="3e199-159">Country or Region</span></span> | 
  | :------------- | :------------: |
  | <span data-ttu-id="3e199-160">1</span><span class="sxs-lookup"><span data-stu-id="3e199-160">1</span></span> | <span data-ttu-id="3e199-161">Asie-Pacifique</span><span class="sxs-lookup"><span data-stu-id="3e199-161">Asia-Pacific</span></span> |
  | <span data-ttu-id="3e199-162">2</span><span class="sxs-lookup"><span data-stu-id="3e199-162">2</span></span> | <span data-ttu-id="3e199-163">Australie</span><span class="sxs-lookup"><span data-stu-id="3e199-163">Australia</span></span> |
  | <span data-ttu-id="3e199-164">3</span><span class="sxs-lookup"><span data-stu-id="3e199-164">3</span></span> | <span data-ttu-id="3e199-165">Canada</span><span class="sxs-lookup"><span data-stu-id="3e199-165">Canada</span></span> |
  | <span data-ttu-id="3e199-166">4 </span><span class="sxs-lookup"><span data-stu-id="3e199-166">4</span></span> | <span data-ttu-id="3e199-167">Europe (à l’exception de la France) / Moyen-Orient / Afrique</span><span class="sxs-lookup"><span data-stu-id="3e199-167">Europe (excluding France) / Middle East / Africa</span></span> |
  | <span data-ttu-id="3e199-168">5 </span><span class="sxs-lookup"><span data-stu-id="3e199-168">5</span></span> | <span data-ttu-id="3e199-169">France</span><span class="sxs-lookup"><span data-stu-id="3e199-169">France</span></span> |
  | <span data-ttu-id="3e199-170">6 </span><span class="sxs-lookup"><span data-stu-id="3e199-170">6</span></span> | <span data-ttu-id="3e199-171">Inde</span><span class="sxs-lookup"><span data-stu-id="3e199-171">India</span></span> |
  | <span data-ttu-id="3e199-172">7 </span><span class="sxs-lookup"><span data-stu-id="3e199-172">7</span></span> | <span data-ttu-id="3e199-173">Japon</span><span class="sxs-lookup"><span data-stu-id="3e199-173">Japan</span></span> |
  | <span data-ttu-id="3e199-174">8 </span><span class="sxs-lookup"><span data-stu-id="3e199-174">8</span></span> | <span data-ttu-id="3e199-175">Corée</span><span class="sxs-lookup"><span data-stu-id="3e199-175">Korea</span></span> |
  | <span data-ttu-id="3e199-176">9 </span><span class="sxs-lookup"><span data-stu-id="3e199-176">9</span></span> | <span data-ttu-id="3e199-177">Amérique du Nord (à l’exception du Canada)</span><span class="sxs-lookup"><span data-stu-id="3e199-177">North America (excluding Canada)</span></span> |
  | <span data-ttu-id="3e199-178">10 </span><span class="sxs-lookup"><span data-stu-id="3e199-178">10</span></span> | <span data-ttu-id="3e199-179">Amérique du Sud</span><span class="sxs-lookup"><span data-stu-id="3e199-179">South America</span></span> |
  | <span data-ttu-id="3e199-180">11</span><span class="sxs-lookup"><span data-stu-id="3e199-180">11</span></span> | <span data-ttu-id="3e199-181">Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="3e199-181">South Africa</span></span> |
  | <span data-ttu-id="3e199-182">12 </span><span class="sxs-lookup"><span data-stu-id="3e199-182">12</span></span> | <span data-ttu-id="3e199-183">Suisse</span><span class="sxs-lookup"><span data-stu-id="3e199-183">Switzerland</span></span> |
  | <span data-ttu-id="3e199-184">13</span><span class="sxs-lookup"><span data-stu-id="3e199-184">13</span></span> | <span data-ttu-id="3e199-185">Émirats arabes unis</span><span class="sxs-lookup"><span data-stu-id="3e199-185">United Arab Emirates</span></span> |
  | <span data-ttu-id="3e199-186">14 </span><span class="sxs-lookup"><span data-stu-id="3e199-186">14</span></span> | <span data-ttu-id="3e199-187">Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="3e199-187">United Kingdom</span></span> |


 > [!NOTE]
> <span data-ttu-id="3e199-188">Le rapport inclut toujours les types d’informations sensibles internationaux pris en charge par MCCA, tels que le code SWIFT, le numéro de carte de crédit, etc.</span><span class="sxs-lookup"><span data-stu-id="3e199-188">The report will always include MCCA supported international sensitive information types such as SWIFT code, credit card number, etc.</span></span>

#### <a name="role-based-reporting"></a><span data-ttu-id="3e199-189">Rapports basés sur les rôles</span><span class="sxs-lookup"><span data-stu-id="3e199-189">Role-based reporting</span></span>

<span data-ttu-id="3e199-190">Votre rapport sera également personnalisé en fonction de votre rôle.</span><span class="sxs-lookup"><span data-stu-id="3e199-190">Your report will also be customized based on your role.</span></span>

<span data-ttu-id="3e199-191">Le tableau ci-dessous indique les rôles qui ont accès aux sections du rapport.</span><span class="sxs-lookup"><span data-stu-id="3e199-191">The table below shows which roles have access to which sections of the report.</span></span> <span data-ttu-id="3e199-192">D’autres rôles au sein de votre organisation (non répertoriés dans le tableau ci-dessous) peuvent ne pas être en mesure d’exécuter l’outil, ou ils peuvent exécuter l’outil et avoir un accès limité aux informations dans le rapport final.</span><span class="sxs-lookup"><span data-stu-id="3e199-192">Other roles within your organization (not listed in the table below) may not be able to run the tool, or they may run the tool and have limited access to information in the final report.</span></span>

<span data-ttu-id="3e199-193">![MCCA : rôles](../media/compliance-manager-mcca-roles.png "Rôles MCCA")</span><span class="sxs-lookup"><span data-stu-id="3e199-193">![MCCA - roles](../media/compliance-manager-mcca-roles.png "MCCA roles")</span></span>

<span data-ttu-id="3e199-194">Exceptions :</span><span class="sxs-lookup"><span data-stu-id="3e199-194">Exceptions:</span></span>
1. <span data-ttu-id="3e199-195">Les utilisateurs ne pourront pas générer de rapport pour l’adresse IP en dehors de la section « Utiliser IRM pour Exchange Online ».</span><span class="sxs-lookup"><span data-stu-id="3e199-195">Users won't be able to generate report for IP apart from “Use IRM for Exchange Online” section.</span></span>
2. <span data-ttu-id="3e199-196">Les utilisateurs pourront générer un rapport pour l’adresse IP à part à partir de la section « Utiliser IRM pour Exchange Online ».</span><span class="sxs-lookup"><span data-stu-id="3e199-196">Users will be able to generate report for IP apart from “Use IRM for Exchange Online” section.</span></span>
3. <span data-ttu-id="3e199-197">Les utilisateurs pourront générer un rapport pour l’adresse IP en dehors de la section « Activer la conformité des communications dans O365 ».</span><span class="sxs-lookup"><span data-stu-id="3e199-197">Users will be able to generate report for IP apart from “Enable Communication Compliance in O365” section.</span></span>
4. <span data-ttu-id="3e199-198">Les utilisateurs ne pourront pas générer de rapport pour l’adresse IP en dehors de la section « Activer l’audit dans Office 365 ».</span><span class="sxs-lookup"><span data-stu-id="3e199-198">Users won't be able to generate report for IP apart from “Enable Auditing in Office 365” section.</span></span>
5. <span data-ttu-id="3e199-199">Les utilisateurs pourront générer un rapport pour l’adresse IP en dehors de la section « Activer l’audit dans Office 365 ».</span><span class="sxs-lookup"><span data-stu-id="3e199-199">Users will be able generate report for IP apart from “Enable Auditing in Office 365” section.</span></span>

#### <a name="solutions-summary-section"></a><span data-ttu-id="3e199-200">Section Résumé des solutions</span><span class="sxs-lookup"><span data-stu-id="3e199-200">Solutions Summary section</span></span>

<span data-ttu-id="3e199-201">La section **Résumé des** solutions du rapport donne une vue d’ensemble des actions d’amélioration que votre organisation peut prendre dans le Gestionnaire de conformité pour vous aider à améliorer votre posture de conformité.</span><span class="sxs-lookup"><span data-stu-id="3e199-201">The **Solutions Summary** section of the report gives an overview of improvement actions that your organization can take in Compliance Manager to help improve your compliance posture.</span></span>

<span data-ttu-id="3e199-202">![MCCA : synthèse des solutions](../media/compliance-manager-mcca-solutions.png "Écran Résumé des solutions MCCA")</span><span class="sxs-lookup"><span data-stu-id="3e199-202">![MCCA - solutions summary](../media/compliance-manager-mcca-solutions.png "MCCA Solutions Summary screen")</span></span>

<span data-ttu-id="3e199-203">MCCA évalue vos configurations actuelles par rapport aux actions d’amélioration recommandées dans le Gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="3e199-203">MCCA evaluates your current configurations against the recommended improvement actions in Compliance Manager.</span></span> <span data-ttu-id="3e199-204">Toute action d’amélioration identifiée par l’outil MCCA comme devant être attentive est répertoriée dans cette section.</span><span class="sxs-lookup"><span data-stu-id="3e199-204">Any improvement action identified by the MCCA tool as needing attention will be listed in this section.</span></span>

<span data-ttu-id="3e199-205">En plus de chaque solution Microsoft, des zones codées en couleur indiquent le nombre d’éléments qui correspondent aux actions d’amélioration dans le Gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="3e199-205">Next to each Microsoft solution are color-coded boxes indicating the number of items that correspond to improvement actions in Compliance Manager.</span></span> <span data-ttu-id="3e199-206">Les actions sont décomposées en trois états d’état :</span><span class="sxs-lookup"><span data-stu-id="3e199-206">The actions are broken down into three status states:</span></span>

- <span data-ttu-id="3e199-207">**OK**: actions qui répondent aux conditions recommandées et qui n’ont pas besoin d’attention pour le moment</span><span class="sxs-lookup"><span data-stu-id="3e199-207">**OK**: the actions that meet recommended conditions and need no attention at this time</span></span>
- <span data-ttu-id="3e199-208">**Amélioration :** actions qui ont besoin d’attention</span><span class="sxs-lookup"><span data-stu-id="3e199-208">**Improvement**: actions that need attention</span></span>
- <span data-ttu-id="3e199-209">**Recommandation**: actions qui n’ont pas besoin d’attention, mais pour lesquelles nous recommandons les meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="3e199-209">**Recommendation**: actions that don’t need attention, but for which we recommend best practices</span></span>
 
<span data-ttu-id="3e199-210">Sélectionnez une zone pour afficher les améliorations et les recommandations.</span><span class="sxs-lookup"><span data-stu-id="3e199-210">Select a box to view improvements and recommendations.</span></span>

<span data-ttu-id="3e199-211">**Éléments avec l’état d’amélioration**</span><span class="sxs-lookup"><span data-stu-id="3e199-211">**Items with the Improvement status**</span></span>

<span data-ttu-id="3e199-212">Sélectionnez la dropdown en face de l’étiquette **d’amélioration** à droite de l’action d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="3e199-212">Select the dropdown next to the **Improvement** label to the right of the improvement action.</span></span> <span data-ttu-id="3e199-213">Vous verrez un résumé rapide et des détails sur vos paramètres actuels et les actions d’amélioration recommandées.</span><span class="sxs-lookup"><span data-stu-id="3e199-213">You’ll see a quick summary and details about your current settings and the recommended improvement actions.</span></span> <span data-ttu-id="3e199-214">Le résumé inclut des liens directs vers le Gestionnaire de conformité, la solution applicable dans le Centre de conformité Microsoft 365 et la documentation appropriée.</span><span class="sxs-lookup"><span data-stu-id="3e199-214">The summary includes direct links into Compliance Manager, the applicable solution in the Microsoft 365 compliance center, and relevant documentation.</span></span>

<span data-ttu-id="3e199-215">Le fait de cliquer sur le lien Gestionnaire de conformité vous permet d’afficher une vue filtrée de toutes les actions d’amélioration au sein de cette solution que vous n’avez pas encore implémentées.</span><span class="sxs-lookup"><span data-stu-id="3e199-215">Clicking on the Compliance Manager link takes you to a filtered view of all the improvement actions within that solution that you have not yet implemented.</span></span> <span data-ttu-id="3e199-216">À partir de là, vous pouvez voir le nombre de points que vous pouvez atteindre pour augmenter votre [score](compliance-score-calculation.md)de conformité, les évaluations qu’ils s’appliquent, ainsi que les réglementations et certifications applicables.</span><span class="sxs-lookup"><span data-stu-id="3e199-216">From there, you can see the number of points you can achieve to increase your [compliance score](compliance-score-calculation.md), and the assessments they apply to, and the applicable regulations and certifications.</span></span>

<span data-ttu-id="3e199-217">Pour la DLP, il existe un bouton **Script** de correction qui vous donne un script PowerShell pré-généré en fonction de ce qui est recommandé.</span><span class="sxs-lookup"><span data-stu-id="3e199-217">For DLP, there’s a **Remediation Script** button that gives you a pre-generated PowerShell script based on what’s recommended.</span></span> <span data-ttu-id="3e199-218">Vous pouvez le copier et le coller directement dans votre console PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e199-218">You can copy and paste it directly in your PowerShell console.</span></span> <span data-ttu-id="3e199-219">Il crée une stratégie DLP en mode test</span><span class="sxs-lookup"><span data-stu-id="3e199-219">It will create a DLP policy in test mode</span></span>

<span data-ttu-id="3e199-220">**Éléments avec l’état Recommandation**</span><span class="sxs-lookup"><span data-stu-id="3e199-220">**Items with Recommendation status**</span></span>

<span data-ttu-id="3e199-221">Sélectionnez la dropdown en face de **l’étiquette Recommandation** à droite de l’action d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="3e199-221">Select the dropdown next to the **Recommendation** label to the right of the improvement action.</span></span> <span data-ttu-id="3e199-222">Vous verrez un résumé de l’environnement Microsoft 365 actuel de votre organisation lié à l’action d’amélioration, ainsi que les meilleures pratiques recommandées.</span><span class="sxs-lookup"><span data-stu-id="3e199-222">You’ll see a summary of your organization’s current Microsoft 365 environment related to the improvement action, along with recommended best practices.</span></span>

## <a name="resources"></a><span data-ttu-id="3e199-223">Ressources</span><span class="sxs-lookup"><span data-stu-id="3e199-223">Resources</span></span>

<span data-ttu-id="3e199-224">Pour plus d’informations sur l’installation, la configuration et l’utilisation de MCCA, voir les [instructions README](https://github.com/OfficeDev/MCCA#overview) sur GitHub (aucun compte GitHub requis).</span><span class="sxs-lookup"><span data-stu-id="3e199-224">For more detailed information on installing, setting up, and using MCCA, see the [README instructions on GitHub](https://github.com/OfficeDev/MCCA#overview) (no GitHub account required).</span></span>

<span data-ttu-id="3e199-225">Pour plus d’informations Windows PowerShell, commencez par [utiliser la documentation PowerShell.](/powershell/scripting/how-to-use-docs?view=powershell-7)</span><span class="sxs-lookup"><span data-stu-id="3e199-225">For more information on Windows PowerShell, start at [How to use the PowerShell documentation](/powershell/scripting/how-to-use-docs?view=powershell-7).</span></span> <span data-ttu-id="3e199-226">Voir aussi [Démarrage Windows PowerShell](/powershell/scripting/windows-powershell/starting-windows-powershell?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="3e199-226">See also [Starting Windows PowerShell](/powershell/scripting/windows-powershell/starting-windows-powershell?view=powershell-7).</span></span>