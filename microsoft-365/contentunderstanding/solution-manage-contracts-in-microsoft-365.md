---
title: Gérer des contrats en utilisant la solution Microsoft 365
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.date: ''
ms.prod: microsoft-365-enterprise
ms.collection: m365solution-managecontracts m365solution-overview
search.appverid: ''
localization_priority: None
ROBOTS: ''
description: Découvrez comment gérer les contrats à l’aide Microsoft 365 solution SharePoint syntex, SharePoint listes, Microsoft Teams et Power Automate.
ms.openlocfilehash: 352ebd1b9170aaf7829c414e87f7a79c4f17a1df
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52843769"
---
# <a name="manage-contracts-using-a-microsoft-365-solution"></a><span data-ttu-id="4fea9-103">Gérer des contrats en utilisant la solution Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="4fea9-103">Manage contracts using a Microsoft 365 solution</span></span>

<span data-ttu-id="4fea9-104">Cet article explique comment créer une solution de gestion des contrats pour votre organisation à l’aide SharePoint Syntex et des composants de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4fea9-104">This article describes how to create a contracts management solution for your organization by using SharePoint Syntex and components of Microsoft 365.</span></span> <span data-ttu-id="4fea9-105">Il vous fournit une infrastructure pour vous aider à planifier et à créer une solution qui répond aux besoins uniques de votre entreprise.</span><span class="sxs-lookup"><span data-stu-id="4fea9-105">It provides you with a framework to help you plan and create a solution that fits your unique business needs.</span></span> <span data-ttu-id="4fea9-106">Même si cette solution ne convient pas à l’ensemble de votre entreprise, une partie de celle-ci peut être adoptée dans votre planification de création d’une solution de gestion de contrat personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4fea9-106">Even if this solution doesn't suit your business needs as a whole, parts of it can be adopted in your planning to create a custom contract management solution.</span></span>

<span data-ttu-id="4fea9-107">*Cet ensemble de contenu documente une solution Microsoft 365 développée par Tom Mol design avec l’équipe Stratégie de solution de travail moderne chez Microsoft.*</span><span class="sxs-lookup"><span data-stu-id="4fea9-107">*This content set documents a Microsoft 365 solution developed by Thomas Molbach with the Modern Work Solution Strategy Team at Microsoft.*</span></span>

## <a name="identify-the-business-problem"></a><span data-ttu-id="4fea9-108">Identifier le problème d’entreprise</span><span class="sxs-lookup"><span data-stu-id="4fea9-108">Identify the business problem</span></span>

<span data-ttu-id="4fea9-109">La première étape de la planification de votre système de gestion des contrats consiste à comprendre le problème que vous essayez de résoudre.</span><span class="sxs-lookup"><span data-stu-id="4fea9-109">The first step in planning your contract management system is to understand the problem you're trying to solve.</span></span> <span data-ttu-id="4fea9-110">Pour cette solution, quatre problèmes clés doivent être résolus :</span><span class="sxs-lookup"><span data-stu-id="4fea9-110">For this solution, four key issues need to be addressed:</span></span>

- <span data-ttu-id="4fea9-111">**Identifier les contrats**.</span><span class="sxs-lookup"><span data-stu-id="4fea9-111">**Identify contracts**.</span></span> <span data-ttu-id="4fea9-112">Votre organisation travaille avec de nombreux documents, tels que des factures, des contrats, des déclarations de travail, etc.</span><span class="sxs-lookup"><span data-stu-id="4fea9-112">Your organization works with many documents, such as invoices, contracts, statements of work, and so on.</span></span>  <span data-ttu-id="4fea9-113">Certains sont des biens numériques envoyés par courrier électronique, d’autres des biens papier envoyés par courrier électronique traditionnel.</span><span class="sxs-lookup"><span data-stu-id="4fea9-113">Some are digital assets sent through email, and some are paper assets sent through traditional mail.</span></span> <span data-ttu-id="4fea9-114">Vous avez besoin d’un moyen d’identifier tous les contrats client de tous les autres documents, puis de les classer comme tels.</span><span class="sxs-lookup"><span data-stu-id="4fea9-114">You need a way to identify all customer contracts from all other documents, and then classifying them as such.</span></span>

- <span data-ttu-id="4fea9-115">**Suivi de l’historique des approbations de contrat.**</span><span class="sxs-lookup"><span data-stu-id="4fea9-115">**Track the history of contract approvals**.</span></span> <span data-ttu-id="4fea9-116">Votre organisation a besoin d’un moyen fiable pour déterminer si les contrats ont été approuvés ou rejetés, et si le paiement a été effectué.</span><span class="sxs-lookup"><span data-stu-id="4fea9-116">Your organization needs a reliable way to find whether contracts have been either approved or rejected, and whether payment has been processed.</span></span> 

- <span data-ttu-id="4fea9-117">**Site pour gérer les approbations de contrat.**</span><span class="sxs-lookup"><span data-stu-id="4fea9-117">**Site to manage contract approvals**.</span></span> <span data-ttu-id="4fea9-118">Votre organisation doit configurer un site de collaboration dans lequel toutes les parties prenantes requises peuvent facilement examiner les contrats.</span><span class="sxs-lookup"><span data-stu-id="4fea9-118">Your organization needs to set up a collaborative site in which all required stakeholders can easily review contracts.</span></span> <span data-ttu-id="4fea9-119">Les parties prenantes doivent pouvoir examiner l’intégralité du contrat si nécessaire, mais se soucient principalement de voir plusieurs champs clés de chaque contrat (par exemple, le nom du client, le numéro de bon de service et le coût total).</span><span class="sxs-lookup"><span data-stu-id="4fea9-119">Stakeholders should be able to review the whole contract if needed, but mostly care about seeing several key fields from each contract (for example, customer name, PO number, and total cost).</span></span> <span data-ttu-id="4fea9-120">Les parties prenantes doivent pouvoir facilement approuver ou rejeter les contrats entrants.</span><span class="sxs-lookup"><span data-stu-id="4fea9-120">Stakeholders should be able to easily approve or reject incoming contracts.</span></span>

- <span data-ttu-id="4fea9-121">**Contrats révisés d’itinéraire.**</span><span class="sxs-lookup"><span data-stu-id="4fea9-121">**Route reviewed contracts**.</span></span> <span data-ttu-id="4fea9-122">Les contrats approuvés et rejetés doivent être acheminés via un flux de travail spécifique.</span><span class="sxs-lookup"><span data-stu-id="4fea9-122">Approved and rejected contracts need to be routed through a specific workflow.</span></span> <span data-ttu-id="4fea9-123">Les contrats approuvés doivent être acheminés vers une application tierce pour le traitement des paiements.</span><span class="sxs-lookup"><span data-stu-id="4fea9-123">Approved contracts need to be routed to a third-party application for payment processing.</span></span> <span data-ttu-id="4fea9-124">Les contrats rejetés doivent être acheminés pour une révision supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="4fea9-124">Rejected contracts need to be routed for additional review.</span></span>

## <a name="overview-of-the-solution"></a><span data-ttu-id="4fea9-125">Vue d’ensemble de la solution</span><span class="sxs-lookup"><span data-stu-id="4fea9-125">Overview of the solution</span></span>

  ![Diagramme de la solution utilisant SharePoint Syntex, SharePoint listes, Teams et Power Automate.](../media/content-understanding/syntex-solution-manage-contracts-setup-steps.png)

<span data-ttu-id="4fea9-127">Cette solution de gestion des contrats comprend quatre composants de Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="4fea9-127">This contract management solution guidance includes four components of Microsoft 365:</span></span>

- <span data-ttu-id="4fea9-128">**Microsoft SharePoint Syntex :** créez des modèles pour identifier et classer vos fichiers de contrat, puis extrayez les données appropriées à partir de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="4fea9-128">**Microsoft SharePoint Syntex**: Create models to identify and classify your contract files and then extract the appropriate data from them.</span></span>

- <span data-ttu-id="4fea9-129">**Listes SharePoint Microsoft**: utilisez la mise en forme disponible dans les listes SharePoint modernes pour présenter les contrats dans un format commercial convivial.</span><span class="sxs-lookup"><span data-stu-id="4fea9-129">**Microsoft SharePoint lists**: Use the formatting available in modern SharePoint lists to present contracts in a business-friendly format.</span></span>

- <span data-ttu-id="4fea9-130">**Microsoft Teams**: utilisez les fonctionnalités d’un canal Teams et des onglets associés pour permettre à vos parties prenantes de réviser et de gérer les contrats.</span><span class="sxs-lookup"><span data-stu-id="4fea9-130">**Microsoft Teams**: Use the functionality of a Teams channel and associated tabs to allow your stakeholders to review and manage contracts.</span></span>

- <span data-ttu-id="4fea9-131">**Power Automate**: utilisez des flux pour guider les contrats dans le processus d’approbation, puis vers une application tierce pour le paiement.</span><span class="sxs-lookup"><span data-stu-id="4fea9-131">**Power Automate**: Use flows to guide contracts through the approval process, and then to a third-party application for payment.</span></span>

### <a name="how-it-all-works"></a><span data-ttu-id="4fea9-132">Fonctionnement</span><span class="sxs-lookup"><span data-stu-id="4fea9-132">How it all works</span></span>

  ![Diagramme de la solution montrant le flux de travail pour télécharger des documents, extraire des données, avertir les parties prenantes et approuver ou rejeter le contrat.](../media/content-understanding/syntex-solution-manage-contracts-overview.png)

1. <span data-ttu-id="4fea9-134">Les documents sont téléchargés vers une bibliothèque SharePoint documents.</span><span class="sxs-lookup"><span data-stu-id="4fea9-134">Documents are uploaded to a SharePoint document library.</span></span> <span data-ttu-id="4fea9-135">Un SharePoint de compréhension de document Syntex a été appliqué à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="4fea9-135">A SharePoint Syntex document understanding model has been applied to the document library.</span></span> <span data-ttu-id="4fea9-136">Il vérifie chaque fichier pour voir s’il y a une correspondance avec un type de contenu « contrat » qu’il est entraîné à rechercher.</span><span class="sxs-lookup"><span data-stu-id="4fea9-136">It checks each file to see if any match a "contract" content type it's trained to look for.</span></span> <span data-ttu-id="4fea9-137">S’il trouve une correspondance, il classifie le fichier en tant que « contrat » et met à jour le type de contenu pour le document.</span><span class="sxs-lookup"><span data-stu-id="4fea9-137">If it finds a match, it classifies the file as a "contract" and updates the content type for the document.</span></span>

2. <span data-ttu-id="4fea9-138">Le modèle tire également des données spécifiques de chaque fichier de contrat que les parties prenantes souhaitent voir, telles que le *client,* le coût et le montant *des frais.*</span><span class="sxs-lookup"><span data-stu-id="4fea9-138">The model also pulls out specific data from each contract file that stakeholders are interested in seeing, such as the *Client*, *Contractor*, and *Fee amount*.</span></span>

    <span data-ttu-id="4fea9-139">La page suivante est un exemple de contrat que le modèle est formé pour identifier.</span><span class="sxs-lookup"><span data-stu-id="4fea9-139">The following page is an example of a contract that the model is trained to identify.</span></span>

      ![Exemple de contrat.](../media/content-understanding/contract.png)

3. <span data-ttu-id="4fea9-141">Dans Microsoft Teams, toutes les parties prenantes sont membres d’un canal Teams sécurisé dans lequel tous les contrats de la bibliothèque de documents sont visibles pour approbation ou rejet.</span><span class="sxs-lookup"><span data-stu-id="4fea9-141">In Microsoft Teams, all stakeholders are members of a secure Teams channel in which all contracts in the document library are visible for approval or rejection.</span></span> <span data-ttu-id="4fea9-142">À l’Teams, toutes les parties prenantes sont averties lorsque de nouveaux contrats doivent être révisés.</span><span class="sxs-lookup"><span data-stu-id="4fea9-142">By using Teams functionality, all stakeholders are notified when new contracts need to be reviewed.</span></span>
 
4. <span data-ttu-id="4fea9-143">À l’Power Automate, les contrats sont déplacés via le processus d’approbation dans Teams canal.</span><span class="sxs-lookup"><span data-stu-id="4fea9-143">By using Power Automate, contracts are moved through the approval process in the Teams channel.</span></span> <span data-ttu-id="4fea9-144">Lorsqu’un membre approuve un contrat, l’état du contrat est modifié pour approuver, tous les membres sont avertis par le biais d’un billet Teams et un élément de ligne est créé pour montrer que le contrat est prêt pour le paiement.</span><span class="sxs-lookup"><span data-stu-id="4fea9-144">When a member approves a contract, the contract status is changed to approve, all members are notified through a Teams post, and a line item is created to show that the contract is ready for payout.</span></span> <span data-ttu-id="4fea9-145">Ce processus peut être étendu pour écrire directement dans une application financière tierce pour paiement.</span><span class="sxs-lookup"><span data-stu-id="4fea9-145">This process can be extended to write directly to a third-party financial application for payment.</span></span>

5.  <span data-ttu-id="4fea9-146">Lorsqu’un membre rejette un contrat, l’état est rejeté et tous les membres sont avertis par le biais d’Teams billet.</span><span class="sxs-lookup"><span data-stu-id="4fea9-146">When a member rejects a contract, the status is changed to rejected, and all members are notified through a Teams post.</span></span>

6. <span data-ttu-id="4fea9-147">Le résultat final de cette solution est un processus d’entreprise automatisé pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="4fea9-147">The end result of this solution is an automated business process for your organization.</span></span> <span data-ttu-id="4fea9-148">Les employés peuvent facilement utiliser la vue de vignette personnalisée dans Teams pour lancer et surveiller le flux de travail d’approbation de vos documents.</span><span class="sxs-lookup"><span data-stu-id="4fea9-148">Employees can easily use the custom tile view in Teams to initiate and monitor the approval workflow of your documents.</span></span> 

     ![Onglet Contrats.](../media/content-understanding/tile-view.png)

### <a name="licensing-requirements"></a><span data-ttu-id="4fea9-150">Conditions d'octroi de licence</span><span class="sxs-lookup"><span data-stu-id="4fea9-150">Licensing requirements</span></span>

<span data-ttu-id="4fea9-151">Cette solution s’appuie sur les fonctionnalités suivantes, disponibles dans le cadre d’une licence Microsoft 365 Entreprise (E1, E3, E5, F3) ou Business (De base, Standard ou Premium) :</span><span class="sxs-lookup"><span data-stu-id="4fea9-151">This solution relies on the following functionality, all available as part of a Microsoft 365 Enterprise (E1, E3, E5, F3) or Business (Basic, Standard, or Premium) license:</span></span>

-   <span data-ttu-id="4fea9-152">Microsoft SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="4fea9-152">Microsoft SharePoint Syntex</span></span>
-   <span data-ttu-id="4fea9-153">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="4fea9-153">Microsoft Teams</span></span>
-   <span data-ttu-id="4fea9-154">Power Automate</span><span class="sxs-lookup"><span data-stu-id="4fea9-154">Power Automate</span></span>

## <a name="create-the-solution"></a><span data-ttu-id="4fea9-155">Créer la solution</span><span class="sxs-lookup"><span data-stu-id="4fea9-155">Create the solution</span></span>

<span data-ttu-id="4fea9-156">Les sections suivantes détailleront la configuration de votre solution de gestion des contrats.</span><span class="sxs-lookup"><span data-stu-id="4fea9-156">The next sections will go into detail about how to configure your contracts management solution.</span></span> <span data-ttu-id="4fea9-157">Il est divisé en trois étapes :</span><span class="sxs-lookup"><span data-stu-id="4fea9-157">It's divided into three steps:</span></span>

- [<span data-ttu-id="4fea9-158">Étape 1. Utiliser SharePoint Syntex pour identifier les fichiers de contrat et extraire des données</span><span class="sxs-lookup"><span data-stu-id="4fea9-158">Step 1. Use SharePoint Syntex to identify contract files and extract data</span></span>](solution-manage-contracts-step1.md)
- [<span data-ttu-id="4fea9-159">Étape 2. Utiliser Microsoft Teams pour créer votre canal de gestion de contrat</span><span class="sxs-lookup"><span data-stu-id="4fea9-159">Step 2. Use Microsoft Teams to create your contract management channel</span></span>](solution-manage-contracts-step2.md)
- [<span data-ttu-id="4fea9-160">Étape 3. Utiliser Power Automate pour créer votre flux pour traiter vos contrats</span><span class="sxs-lookup"><span data-stu-id="4fea9-160">Step 3. Use Power Automate to create your flow to process your contracts</span></span>](solution-manage-contracts-step3.md)
