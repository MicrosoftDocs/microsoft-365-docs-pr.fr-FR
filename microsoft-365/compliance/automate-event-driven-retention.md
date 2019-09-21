---
title: Rétentions basées sur des événements
ms.author: stephow
author: stephow-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.
ms.openlocfilehash: 3a5dc3efb88eaa4eabe1b01731d17f5ac418f99d
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078874"
---
# <a name="automate-event-based-retention"></a><span data-ttu-id="2ce70-103">Rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="2ce70-103">Automate event-based retention</span></span>

<span data-ttu-id="2ce70-p101">L’explosion de contenu dans les organisations et comment il peut devenir assistées (redondantes, obsolètes, triviale) est une affaire sérieuse. Pour continuer à répondre aux exigences légales, commerciales et défis liés à la conformité des réglementations, les entreprises doivent pouvoir conserver et protéger les informations importantes et trouver rapidement ce qui est pertinent. Conservant uniquement ce qui est important, les informations pertinentes sont la clé du succès d’une entreprise.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p101">The explosion of content in organizations and how it can become ROT (redundant, obsolete, trivial) is serious business. To continue to meet legal, business, and regulatory compliance challenges, businesses must be able to keep and protect important information and quickly find what’s relevant. Retaining only important, pertinent information is key to a business’s success.</span></span>

<span data-ttu-id="2ce70-p102">Les organisations peuvent donc tirer parti des solutions de rétention dans le centre de conformité et sécurité Office 365. La rétention peut être déclenchée en utilisant les[étiquettes de rétention](labels.md). Une étiquette de rétention a la possibilité de [baser la période de rétention sur un événement spécifique](event-driven-retention.md). En règle générale, la période de rétention est basée sur une date connue, comme la date ou date de dernière modification pour le contenu création. Toutefois, les organisations ont également des exigences à dispose de contenu en fonction des occurrences d’un événement, par exemple 7 ans après qu’un employé quitte une organisation.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p102">Hence organizations can take advantage of retention solutions in the Office 365 Security & Compliance Center. Retention can be triggered by using [retention labels](labels.md). A retention label has the option to [base the retention period on a specific event](event-driven-retention.md). Typically, the retention period is based on a known date, such as the creation date or last modified date for the content. However, organizations also have requirements to dispose of content based on the occurrence of an event, such as 7 years after an employee leaves an organization.</span></span>

<span data-ttu-id="2ce70-p103">Pour s’assurer de la conformité de la destruction de contenu, il est impératif de savoir quand un événement a lieu. Le volume du contenu en augmentant rapidement, il devient difficile à conserver et dispose du contenu d’une manière opportune et la conformité.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p103">In order to ensure compliant disposal of content, it is imperative to know when an event takes place. With the volume of content increasing rapidly, it is becoming challenging to retain and dispose content in a timely and compliant manner.</span></span>

<span data-ttu-id="2ce70-p104">La rétention basée sur un événement résoud ce problème. Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p104">Event-based retention solves this problem. This topic explains how to set up your business process flows to automate retention through events by using the Microsoft 365 REST API.</span></span>

## <a name="about-event-based-retention"></a><span data-ttu-id="2ce70-116">Rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="2ce70-116">About event-based retention</span></span>

<span data-ttu-id="2ce70-p105">Une organisation peut être grande petite ou moyenne. Le nombre de documents professionnels, documents juridiques, fichiers employé, contrats et documents produit qui sont créés et gérés sur une base quotidienne augmentent considérablement.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p105">An organization can be small, medium, or large. The number of business documents, legal documents, employee files, contracts, and product documents that get created and managed on a day to day basis is increasing dramatically.</span></span>

<span data-ttu-id="2ce70-p106">Par exemple, chaque jour, dizaines et des centaines d’employés rejoignent et quittent organisations. Le service ressources humaines continue de créer, mettre à jour ou supprimer des documents liés à l’employé en respectant les exigences professionnelles. Ce processus est susceptible d’être les stratégies de rétention différentes décrites pour l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="2ce70-p106">For example, each day, tens and hundreds of employees are joining and leaving organizations. The HR department continues to create, update, or delete employee-related documents as per business requirements. This process is subject to the different retention policies outlined for the business:</span></span>

- <span data-ttu-id="2ce70-p107">**La période de rétention du contenu peut être une date connue** telles que la date que le contenu a été créé, la dernière modification ou étiqueté. Par exemple, vous pouvez conserver les documents pendant sept ans après que qu’ils aient été créés, puis les supprimer.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p107">**The period of retention for content can be a known date** such as the date the content was created, last modified or labeled. For example, you might retain documents for seven years after they're created and then delete them.</span></span>

- <span data-ttu-id="2ce70-p108">**La période de rétention du contenu peut également être une date inconnue**. Par exemple, avec des étiquettes de rétention, vous pouvez également baser une période de rétention sur lorsqu’un type spécifique d’événement se produit, par exemple un employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p108">**The period of retention of content can also be an unknown date**. For example, with retention labels, you can also base a retention period on when a specific type of event occurs, such as an employee leaving the organization.</span></span>

<span data-ttu-id="2ce70-p109">Le début de la période de rétention déclenche l’événement, et tout le contenu portant une étiquette pour ce type d’événement obtenez actions de rétention l’étiquette est appliquées dessus. Il s’agit rétention basée sur l’événement-pour plus d’informations, voir [vue d’ensemble de rétention basées sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="2ce70-p109">The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them. This is called event-based retention - to learn more, see [Overview of event-driven retention](event-driven-retention.md).</span></span>

## <a name="set-up-event-based-retention"></a><span data-ttu-id="2ce70-128">Définir la rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="2ce70-128">Set up event-based retention</span></span>

<span data-ttu-id="2ce70-129">Cette section décrit les activités devant être effectuées avant la conservation du contenu.</span><span class="sxs-lookup"><span data-stu-id="2ce70-129">This section describes what needs to be done prior to retaining content.</span></span>

### <a name="identify-roles"></a><span data-ttu-id="2ce70-130">Identifier les rôles</span><span class="sxs-lookup"><span data-stu-id="2ce70-130">Identify roles</span></span>

<span data-ttu-id="2ce70-131">Identifier les différents rôles d’une organisation qui effectuent des tâches de gestion d’enregistrement qui seraient responsables de la rétention efficace et de documents professionnels.</span><span class="sxs-lookup"><span data-stu-id="2ce70-131">Identify the different roles in an organization that perform Record Management tasks that would be responsible for effective and efficient retention of business documents.</span></span>

  | <span data-ttu-id="2ce70-132">**Persona**</span><span class="sxs-lookup"><span data-stu-id="2ce70-132">**Persona**</span></span>| <span data-ttu-id="2ce70-133">**Role**</span><span class="sxs-lookup"><span data-stu-id="2ce70-133">**Role**</span></span>|
  | - | - |
  | <span data-ttu-id="2ce70-134">Administrateur</span><span class="sxs-lookup"><span data-stu-id="2ce70-134">Admin</span></span> | <span data-ttu-id="2ce70-135">Crée des types d’Événement de Rétention, Étiquettes de Rétention et Référentiels d’Enregistrement dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ce70-135">Creates Retention Event types, Retention labels and Record repositories in SharePoint</span></span> |
  | <span data-ttu-id="2ce70-136">Gestionnaire d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="2ce70-136">Records Manager</span></span>                                  | <span data-ttu-id="2ce70-137">Fournit des détails de recommandations et de conformité stratégies de rétention et des plannings de rétention</span><span class="sxs-lookup"><span data-stu-id="2ce70-137">Provides Retention Policies and Retention Schedules guidance and compliance details</span></span>   |
  | <span data-ttu-id="2ce70-138">Administrateur système (entreprise)</span><span class="sxs-lookup"><span data-stu-id="2ce70-138">System Admin (business)</span></span>                          | <span data-ttu-id="2ce70-139">Configure et gère les systèmes externes pour fonctionner avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2ce70-139">Sets up and manages external systems to work with Microsoft 365</span></span>                       |
  | <span data-ttu-id="2ce70-140">Travailleur de l'information</span><span class="sxs-lookup"><span data-stu-id="2ce70-140">Information Worker</span></span>                               | <span data-ttu-id="2ce70-141">Gère le cycle de vie de leur processus métier (RH, Finance, etc. informatique)</span><span class="sxs-lookup"><span data-stu-id="2ce70-141">Manages the lifecycle of their business process (HR, Finance, IT etc)</span></span>                 |

### <a name="set-up-the-security--compliance-center"></a><span data-ttu-id="2ce70-142">Accéder au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ce70-142">Set up the Security & Compliance Center</span></span>
  
1. <span data-ttu-id="2ce70-143">L’administrateur de conformité crée un type d’événement : par exemple, la résiliation employé ou expiration de contrat ou fin de fabrication de produit (reportez-vous aux processus étape par étape dans l’article[rétention événement](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="2ce70-143">Compliance admin creates an event type – for example, Employee Termination or Contract Expiration or End of Product Manufacturing (Please refer to step by step process in [Event-driven retention](event-driven-retention.md).</span></span>
    
1. <span data-ttu-id="2ce70-144">L’administrateur de conformité crée une étiquette en fonction d’un événement et l’associe à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="2ce70-144">Compliance admin creates a retention label based on an event and associates the label with an event type.</span></span>
    
1. <span data-ttu-id="2ce70-145">Il existe 4 types de déclencheurs pour les étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="2ce70-145">There are 4 types of triggers for retention labels:</span></span>
            
    1. <span data-ttu-id="2ce70-146">Date de création</span><span class="sxs-lookup"><span data-stu-id="2ce70-146">Create date</span></span>
                
    1. <span data-ttu-id="2ce70-147">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="2ce70-147">Last modified</span></span>
                
    1. <span data-ttu-id="2ce70-148">Date étiquette (lorsque le contenu a été étiqueté)</span><span class="sxs-lookup"><span data-stu-id="2ce70-148">Label date (when the content was labeled)</span></span>
                
    1. <span data-ttu-id="2ce70-149">Basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="2ce70-149">Event-based</span></span>
    
1. <span data-ttu-id="2ce70-150">L’administrateur de conformité publie l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="2ce70-150">Compliance admin publishes the retention label.</span></span>

### <a name="set-up-sharepoint"></a><span data-ttu-id="2ce70-151">Configurer SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ce70-151">Set up SharePoint</span></span>
   
<span data-ttu-id="2ce70-152">Pour créer un référentiel des enregistrements, l’administrateur de conformité :</span><span class="sxs-lookup"><span data-stu-id="2ce70-152">To create a records repository, the compliance admin:</span></span>

1. <span data-ttu-id="2ce70-153">Crée un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="2ce70-153">Creates a SharePoint site.</span></span>

1. <span data-ttu-id="2ce70-154">Effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ce70-154">Does one of the following:</span></span>
        
    - <span data-ttu-id="2ce70-p110">Crée une bibliothèque SharePoint : définir l’étiquette en fonction des événement au niveau de la bibliothèque. Pour plus d’informations, voir [application d’une étiquette de rétention par défaut à tout le contenu dans une bibliothèque SharePoint, un dossier ou un ensemble de documents](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="2ce70-p110">Creates a SharePoint library: Set event-based label at the library level. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
          
    - <span data-ttu-id="2ce70-p111">Configure un Document ensemble dans SharePoint. Pour plus d’informations, voir [présentation des ensembles de documents](https://support.office.com/fr-FR/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span><span class="sxs-lookup"><span data-stu-id="2ce70-p111">Sets up a Document set in SharePoint. For more information, see [Introduction to document sets](https://support.office.com/fr-FR/article/Introduction-to-Document-Sets-3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span></span>
      
1. <span data-ttu-id="2ce70-p112">Attribue des Id de l’élément (biens QU'ID est un nom de produit ou un code utilisé par l’organisation, par exemple, la matricule peut être un id de l’élément) à chaque document employé définir (en attribuant des biens QU'ID dans le dossier, tous les éléments dans ce dossier hérite automatiquement le même ID de biens. Cela signifie que tous les éléments peuvent avoir leur période de rétention déclenchée par le même événement.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p112">Assigns Asset Id (asset ID is a product name or code used by the organization, for example, Employee number can be an asset id) to each employee document set (By assigning the asset ID to the folder, every item in that folder automatically inherits the same asset ID. This means all the items can have their retention period triggered by the same event.</span></span>

## <a name="ways-to-trigger-event-based-retention"></a><span data-ttu-id="2ce70-161">Méthodes pour déclencher la lecture rétention basée sur l’événement</span><span class="sxs-lookup"><span data-stu-id="2ce70-161">Ways to trigger event-based retention</span></span>

<span data-ttu-id="2ce70-162">Il existe deux façons avec lesquelles la rétention basée sur l’événement peut être déclenchée :</span><span class="sxs-lookup"><span data-stu-id="2ce70-162">There are two ways in which event-based retention can be triggered:</span></span>

- <span data-ttu-id="2ce70-p113">**Utiliser l’interface utilisateur du centre de conformité** il s’agit d’un processus qui peut être utilisé pour conserver moins de contenu à la fois ou la fréquence de déclenchement de rétention n’est pas souvent, par exemple, mensuelle ou annuelle. Pour plus d’informations sur cette méthode, voir [vue d’ensemble de rétention basée sur les événements](event-driven-retention.md). Toutefois, cette méthode pour déclencher la rétention peut prendre du temps et est sujette aux erreurs, et peut donc ralentir l’évolutivité. Par conséquent, une solution automatisée plus transparente associée au déclenchement de rétention peut améliorer la sécurité et conformité des données.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p113">**Using the admin center UI** This is a process that can be used to retain less content at a time or the frequency to trigger retention is not often, such as monthly or yearly. For more information on this method, see [Overview of event-driven retention](event-driven-retention.md). However, this way to trigger retention can be time-consuming and prone to error, thus stunting scalability. Therefore, an automated, seamless solution to trigger retention can enhance the security and compliance of data.</span></span>

- <span data-ttu-id="2ce70-p114">**À l’aide d’une API REST M365** Ce processus peut être utilisé lorsque les grandes quantités de contenu sont conservées à un moment et/ou la fréquence de rétention déclencheur est récurrente telle que de manière quotidienne ou hebdomadaire. Le flux détecte quand un événement se produit dans votre système métier de, puis crée automatiquement un événement connexe dans le centre de sécurité et conformité. Vous n’avez pas besoin de créer manuellement un événement dans l’interface utilisateur chaque fois que ce qui se passer.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p114">**Using a M365 REST API** This process can be used when large amounts of content are to be retained at a time and/or the frequency to trigger retention is often such as daily or weekly. The flow detects when an event occurs in your line-of-business system, and then automatically creates a related event in the Security & Compliance Center. You don't need to manually create an event in the UI each time one occurs.</span></span>

<span data-ttu-id="2ce70-170">Il existe deux options d’utilisation de l’API REST :</span><span class="sxs-lookup"><span data-stu-id="2ce70-170">There are two options for using the REST API:</span></span>

- <span data-ttu-id="2ce70-p115">**Microsoft Flow ou une application similaire** peut être utilisé(e )pour déclencher automatiquement l’occurrence d’un événement. Microsoft Flow est un orchestrateur pour la connexion à d’autres systèmes. À l’aide de Microsoft Flow ne requiert pas une solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p115">**Microsoft Flow or a similar application** can be used to trigger the occurrence of an event automatically. Microsoft Flow is an orchestrator for connecting to other systems. Using Microsoft Flow does not require a custom solution.</span></span>

- <span data-ttu-id="2ce70-174">**PowerShell ou un HTTP client pour appeler des API REST** à l’aide de PowerShell (version 6 ou version ultérieure) pour appeler l’API REST Microsoft 365 pour créer des événements.</span><span class="sxs-lookup"><span data-stu-id="2ce70-174">**PowerShell or an HTTP client to call REST API** Using PowerShell (version 6 or higher) to call Microsoft 365 REST API to create events.</span></span> 

<span data-ttu-id="2ce70-p116">L’API Rest est un point de terminaison de service qui prend en charge des ensembles d’opérations HTTP (méthodes), qui fournit créer/récupération/mise à jour/supprimer l’accès aux ressources de service- pour plus d’informations, voir [composants d’une demande de l’API REST/réponse](https://docs.microsoft.com/fr-FR/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse) . Dans ce cas, les événements peuvent être créés en utilisant l’API REST de Microsoft 365 et récupérées à l’aide d’opérations (méthodes) POST et GET.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p116">A Rest API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources - for more information, see [Components of a REST API request/response](https://docs.microsoft.com/fr-FR/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse). In this case, by using the Microsoft 365 REST API, events can be created and retrieved using operations (methods) POST and GET.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="2ce70-177">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="2ce70-177">Example scenarios</span></span>

<span data-ttu-id="2ce70-178">Envisagez les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="2ce70-178">Let’s consider the following scenarios.</span></span>

### <a name="scenario-1-employees-leaving-the-organization"></a><span data-ttu-id="2ce70-179">Scénario 1 : Employés quittant l’organisation</span><span class="sxs-lookup"><span data-stu-id="2ce70-179">Scenario 1: Employees leaving the organization</span></span> 

<span data-ttu-id="2ce70-p117">Une organisation crée et stocke plusieurs documents liés à l’employé par employé. Ces documents sont gérés et conservées pendant le recrutement de chaque employé. Toutefois, lorsque l’employé quitte l’organisation ou l’emploi terminé, l’organisation est obligée par les exigences juridiques et professionnelles de conserver les documents de cet employé pendant une période prévue.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p117">An organization creates and stores numerous employee related documents per employee. These documents are managed and retained during the employment of each employee. However, when the employee leaves the organization or the employment is terminated, the organization is obligated by legal and business requirements to retain the documents of that employee for a stipulated period.</span></span>

<span data-ttu-id="2ce70-183">Maintenant si plusieurs employés quittent l’organisation tous les jours, l’organisation doit déclencher la lecture l’horloge de rétention de centaines si ce n’est pas de milliers de documents chaque jour.</span><span class="sxs-lookup"><span data-stu-id="2ce70-183">Now if multiple employees leave the organization every day, the organization must trigger the retention clock of hundreds if not thousands of documents each day.</span></span>

<span data-ttu-id="2ce70-p118">En plus de cela, la période de rétention doit être calculée pour chacun de ces employés comme date d’achèvement employé + nombre de jours, mois ou années en fonction du type de l’employé enregistrer. Par exemple, la rémunération du travailleur de le déclarations employés et les avantages de l’employé doivent avoir différentes rétentions.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p118">In addition to this, the retention period needs to be calculated for each of these employees as Employee termination date + number of days, months or years based on the type of the employee record. For example, worker’s compensation of the employee vs benefits filings of the same employee may need different retention.</span></span>

<span data-ttu-id="2ce70-p119">Le diagramme ci-dessous montre comment vous pouvez avoir plusieurs étiquettes qui sont associées à un événement spécifique. Tous les fichiers sous étiquette de travailleur rémunération et tous les fichiers sous étiquette avantages employé sont associés à un événement unique qui est l’employé quittant l’organisation. Chacun de ces différents fichiers doit avoir une différente horloge de rétention. Par conséquent, lorsqu’un employé quitte l’organisation, ces fichiers dans chaque étiquette rencontrent une différente période de rétention. Pour déclencher la lecture toutes ces différentes horloges de rétention pour chaque type de fichier ou une étiquette pour chaque employé est une tâche très difficile. Imaginez effectuer cette action pour plusieurs employés.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p119">The diagram below shows how there can be multiple labels that are associated with a single event. Here all the files under Worker’s compensation label and all the files under Employee benefits label are both associated with a single event which is the employee leaving the organization. Each of these different files have different retention clocks. So, when an employee leaves the organization, these files within each label experience a different retention period. To trigger all these different retention clocks for each file type or label for each employee is a very challenging task. Imagine doing this for multiple employees.</span></span>

![Diagramme illustrant le type d’événement, des événements et des étiquettes](media/automate-event-driven-retention-event-diagram-employee-leaving.png)

<span data-ttu-id="2ce70-193">Un processus automatisé associé au déclenchement de ces différentes horloges de rétention pour plusieurs employés sera donc un gagne-temps, exempte d’erreur et très efficace.</span><span class="sxs-lookup"><span data-stu-id="2ce70-193">Hence an automated process to trigger these different retention clocks for multiple employees will be time-saving, error-free and extremely efficient .</span></span>

<span data-ttu-id="2ce70-194">**Configuration automatisée de rétention basée sur des événements dans ce scénario :**</span><span class="sxs-lookup"><span data-stu-id="2ce70-194">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des actions pour le scénario d’employé quittant l’organisation](media/automate-event-driven-retention-employee-termination-diagram.png)

  - <span data-ttu-id="2ce70-196">L’administrateur crée des dossiers d’employé lié au Document, telles Cartier Marie, John Smith.</span><span class="sxs-lookup"><span data-stu-id="2ce70-196">Admin c reates employee folders to the Document set such as Jane Doe, John Smith.</span></span>

  - <span data-ttu-id="2ce70-197">L’administrateur ajoute des fichiers employé tels que les avantages, paie, rémunération de travailleur à chaque dossier employé</span><span class="sxs-lookup"><span data-stu-id="2ce70-197">Admin adds employee files such as Benefits, Payroll, Worker’s Compensation to each employee folder</span></span>

  - <span data-ttu-id="2ce70-198">L’administrateur affecte des Id de l’élément à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="2ce70-198">Admin assigns Asset Id to each employee folder.</span></span> 

  - <span data-ttu-id="2ce70-199">L SCC d’administration</span><span class="sxs-lookup"><span data-stu-id="2ce70-199">SCC Admin l</span></span>

  - <span data-ttu-id="2ce70-200">Connexions dans le Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ce70-200">Logs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="2ce70-201">L’administrateur SCC crée des types d’événements liés à l’employé tels que « Renvoi employé », « Embauche employé » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="2ce70-201">SCC Admin creates employee related events types such as “Employee Termination”, “Employee Hire” events.</span></span>

  - <span data-ttu-id="2ce70-202">Administrateur SCC crée une étiquette « Employés ».</span><span class="sxs-lookup"><span data-stu-id="2ce70-202">SCC Admin creates “Employee Retention” label.</span></span>

  - <span data-ttu-id="2ce70-203">Cette étiquette « Employés » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ce70-203">This “Employee Retention” label is published and applied manually or automatically to the employee files in SharePoint</span></span>

  - <span data-ttu-id="2ce70-204">Le Système de Gestion des Ressources Humaines comme Workday peut fonctionner avec Microsoft Flow pour exécuter cette page régulièrement pour gérer les fichiers de l’employé</span><span class="sxs-lookup"><span data-stu-id="2ce70-204">HR Management System like Workday can work with Microsoft Flow to run periodically to manage employee files</span></span>

  - <span data-ttu-id="2ce70-205">Si un employé a quitté l’organisation, le flux déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="2ce70-205">If an employee has left the organization, the Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific employee’s files.</span></span>

#### <a name="using-microsoft-flow"></a><span data-ttu-id="2ce70-206">Utilisation Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="2ce70-206">Using Microsoft Flow</span></span>

<span data-ttu-id="2ce70-207">Étape 1-créer un flux de créer un événement en utilisant l’API REST Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2ce70-207">Step 1- Create a flow to create an event using the Microsoft 365 REST API</span></span>

![Utilisation le flux pour créer un événement](media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a><span data-ttu-id="2ce70-210">Créer un événement</span><span class="sxs-lookup"><span data-stu-id="2ce70-210">Create an event</span></span>

<span data-ttu-id="2ce70-211">Utilisation du code d’exemple pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="2ce70-211">Sample code to call the REST API</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ce70-212">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ce70-212">Method</span></span></th>
<th><span data-ttu-id="2ce70-213">POST</span><span class="sxs-lookup"><span data-stu-id="2ce70-213">POST</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ce70-214">URL</span><span class="sxs-lookup"><span data-stu-id="2ce70-214">URL</span></span></td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent</td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-215">En-têtes</span><span class="sxs-lookup"><span data-stu-id="2ce70-215">Headers</span></span></td>
<td><span data-ttu-id="2ce70-216">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ce70-216">Content-Type</span></span></td>
<td><span data-ttu-id="2ce70-217">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-217">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ce70-218">Corps</span><span class="sxs-lookup"><span data-stu-id="2ce70-218">Body</span></span></td>
<td><p><span data-ttu-id="2ce70-219">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-219">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="2ce70-220">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="2ce70-220">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="2ce70-221">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="2ce70-221">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="2ce70-222">xmlns='http://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-222">xmlns='http://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="2ce70-223">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-223">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="2ce70-224">&lt;mise à jour&gt;9/9/2017 22:50:00&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-224">&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="2ce70-225">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-225">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="2ce70-226">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-226">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="2ce70-227">&lt;d:Name&gt;Licenciement employé&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-227">&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="2ce70-228">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-228">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="2ce70-229">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-229">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="2ce70-230">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-230">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span></span></p>
<p><span data-ttu-id="2ce70-231">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-231">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="2ce70-232">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-232">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="2ce70-233">&lt;/entrée&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-233">&lt;/entry&gt;</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-234">Authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-234">Authentication</span></span></td>
<td><span data-ttu-id="2ce70-235">De base</span><span class="sxs-lookup"><span data-stu-id="2ce70-235">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ce70-236">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ce70-236">Username</span></span></td>
<td><span data-ttu-id="2ce70-237">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="2ce70-237">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-238">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="2ce70-238">Password</span></span></td>
<td><span data-ttu-id="2ce70-239">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="2ce70-239">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a><span data-ttu-id="2ce70-240">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="2ce70-240">Available parameters</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ce70-241"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="2ce70-241"><strong>Parameters</strong></span></span></th>
<th><span data-ttu-id="2ce70-242"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="2ce70-242"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="2ce70-243"><strong>Notes</strong></span><span class="sxs-lookup"><span data-stu-id="2ce70-243"><strong>Notes</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ce70-244">&lt;d:Name&gt;&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-244">&lt;d:Name&gt;&lt;/d:Name&gt;</span></span></td>
<td><span data-ttu-id="2ce70-245">Entrez un nom unique pour la base de données,</span><span class="sxs-lookup"><span data-stu-id="2ce70-245">Provide a unique name for the event,</span></span></td>
<td><span data-ttu-id="2ce70-p120">Un nom ne peut pas contenir les espaces et les caractères suivants : % \* \ &amp; &lt; &gt; | # ? , : ;</span><span class="sxs-lookup"><span data-stu-id="2ce70-p120">Cannot contain trailing spaces, and the following characters: % \* \ &amp; &lt; &gt; | # ? , : ;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-248">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-248">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span></span></td>
<td><span data-ttu-id="2ce70-249">Entrez le nom de l’événement (ou Guid),</span><span class="sxs-lookup"><span data-stu-id="2ce70-249">Enter event type name (or Guid),</span></span></td>
<td><span data-ttu-id="2ce70-p121">Exemple : « employé licenciement anticipé ». Le type d’événement doit être associé à une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p121">Example: “Employee termination”. Event type has to be associated with a retention label.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ce70-252">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-252">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span></span></td>
<td><span data-ttu-id="2ce70-253">Entrez « ComplianceAssetId : « + Id d’employé</span><span class="sxs-lookup"><span data-stu-id="2ce70-253">Enter “ComplianceAssetId:” + employee Id</span></span></td>
<td><span data-ttu-id="2ce70-254">Exemple :&quot;ComplianceAssetId:12345&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-254">Example:&quot;ComplianceAssetId:12345&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-255">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-255">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span></span></td>
<td><span data-ttu-id="2ce70-256">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2ce70-256">Event Date and Time</span></span></td>
<td><p><span data-ttu-id="2ce70-257">Format : AAAA-MM-JJThh, exemple :</span><span class="sxs-lookup"><span data-stu-id="2ce70-257">Format: yyyy-MM-ddTHH:mm:ssZ, Example:</span></span></p>
<p><span data-ttu-id="2ce70-258">2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="2ce70-258">2018-12-01T00:00:00Z</span></span></p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="2ce70-259">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="2ce70-259">Response codes</span></span>

| <span data-ttu-id="2ce70-260">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="2ce70-260">**Response Code**</span></span> | <span data-ttu-id="2ce70-261">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ce70-261">**Description**</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="2ce70-262">302</span><span class="sxs-lookup"><span data-stu-id="2ce70-262">302</span></span>               | <span data-ttu-id="2ce70-263">Rediriger</span><span class="sxs-lookup"><span data-stu-id="2ce70-263">Redirect</span></span>              |
| <span data-ttu-id="2ce70-264">201</span><span class="sxs-lookup"><span data-stu-id="2ce70-264">201</span></span>               | <span data-ttu-id="2ce70-265">Créé</span><span class="sxs-lookup"><span data-stu-id="2ce70-265">Created</span></span>               |
| <span data-ttu-id="2ce70-266">403</span><span class="sxs-lookup"><span data-stu-id="2ce70-266">403</span></span>               | <span data-ttu-id="2ce70-267">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="2ce70-267">Authorization Failed</span></span>  |
| <span data-ttu-id="2ce70-268">401</span><span class="sxs-lookup"><span data-stu-id="2ce70-268">401</span></span>               | <span data-ttu-id="2ce70-269">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-269">Authentication Failed</span></span> |

##### <a name="get-events-based-on-time-range"></a><span data-ttu-id="2ce70-270">Obtenir des événements en fonction de l’intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="2ce70-270">Get Events based on time range</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2ce70-271">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ce70-271">Method</span></span></th>
<th><span data-ttu-id="2ce70-272">GET</span><span class="sxs-lookup"><span data-stu-id="2ce70-272">GET</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2ce70-273">URL</span><span class="sxs-lookup"><span data-stu-id="2ce70-273">URL</span></span></td>
<td><ol start="4" type="1">
<li><p><span data-ttu-id="2ce70-274">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span><span class="sxs-lookup"><span data-stu-id="2ce70-274">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span></span></p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-275">En-têtes</span><span class="sxs-lookup"><span data-stu-id="2ce70-275">Headers</span></span></td>
<td><span data-ttu-id="2ce70-276">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ce70-276">Content-Type</span></span></td>
<td><span data-ttu-id="2ce70-277">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-277">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-278">Authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-278">Authentication</span></span></td>
<td><span data-ttu-id="2ce70-279">De base</span><span class="sxs-lookup"><span data-stu-id="2ce70-279">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2ce70-280">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ce70-280">Username</span></span></td>
<td><span data-ttu-id="2ce70-281">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="2ce70-281">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2ce70-282">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="2ce70-282">Password</span></span></td>
<td><span data-ttu-id="2ce70-283">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="2ce70-283">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="2ce70-284">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="2ce70-284">Response codes</span></span>

| <span data-ttu-id="2ce70-285">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="2ce70-285">**Response Code**</span></span> | <span data-ttu-id="2ce70-286">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ce70-286">**Description**</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="2ce70-287">200</span><span class="sxs-lookup"><span data-stu-id="2ce70-287">200</span></span>               | <span data-ttu-id="2ce70-288">OK, une liste d’événements dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-288">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="2ce70-289">404</span><span class="sxs-lookup"><span data-stu-id="2ce70-289">404</span></span>               | <span data-ttu-id="2ce70-290">Introuvable</span><span class="sxs-lookup"><span data-stu-id="2ce70-290">Not found</span></span>                         |
| <span data-ttu-id="2ce70-291">302</span><span class="sxs-lookup"><span data-stu-id="2ce70-291">302</span></span>               | <span data-ttu-id="2ce70-292">Rediriger</span><span class="sxs-lookup"><span data-stu-id="2ce70-292">Redirect</span></span>                          |
| <span data-ttu-id="2ce70-293">401</span><span class="sxs-lookup"><span data-stu-id="2ce70-293">401</span></span>               | <span data-ttu-id="2ce70-294">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="2ce70-294">Authorization Failed</span></span>              |
| <span data-ttu-id="2ce70-295">403</span><span class="sxs-lookup"><span data-stu-id="2ce70-295">403</span></span>               | <span data-ttu-id="2ce70-296">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-296">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="2ce70-297">Obtenir un événement par ID</span><span class="sxs-lookup"><span data-stu-id="2ce70-297">Get an event by ID</span></span>

| <span data-ttu-id="2ce70-298">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ce70-298">Method</span></span>         | <span data-ttu-id="2ce70-299">GET</span><span class="sxs-lookup"><span data-stu-id="2ce70-299">GET</span></span>   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| <span data-ttu-id="2ce70-300">URL</span><span class="sxs-lookup"><span data-stu-id="2ce70-300">URL</span></span>            | <span data-ttu-id="2ce70-301">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span><span class="sxs-lookup"><span data-stu-id="2ce70-301">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span></span> |                      |
| <span data-ttu-id="2ce70-302">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ce70-302">Header</span></span>         | <span data-ttu-id="2ce70-303">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ce70-303">Content-Type</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="2ce70-304">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-304">application/atom+xml</span></span> |
| <span data-ttu-id="2ce70-305">Authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-305">Authentication</span></span> | <span data-ttu-id="2ce70-306">De base</span><span class="sxs-lookup"><span data-stu-id="2ce70-306">Basic</span></span>                                                                                                                                                                                                                                                              |                      |
| <span data-ttu-id="2ce70-307">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ce70-307">Username</span></span>       | <span data-ttu-id="2ce70-308">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="2ce70-308">“Complianceuser”</span></span>                                                                                                                                                                                                                                                   |                      |
| <span data-ttu-id="2ce70-309">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="2ce70-309">Password</span></span>       | <span data-ttu-id="2ce70-310">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="2ce70-310">“Compliancepassword”</span></span>                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a><span data-ttu-id="2ce70-311">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="2ce70-311">Response codes</span></span>

| <span data-ttu-id="2ce70-312">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="2ce70-312">**Response Code**</span></span> | <span data-ttu-id="2ce70-313">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ce70-313">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="2ce70-314">200</span><span class="sxs-lookup"><span data-stu-id="2ce70-314">200</span></span>               | <span data-ttu-id="2ce70-315">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-315">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="2ce70-316">404</span><span class="sxs-lookup"><span data-stu-id="2ce70-316">404</span></span>               | <span data-ttu-id="2ce70-317">Introuvable</span><span class="sxs-lookup"><span data-stu-id="2ce70-317">Not found</span></span>                                            |
| <span data-ttu-id="2ce70-318">302</span><span class="sxs-lookup"><span data-stu-id="2ce70-318">302</span></span>               | <span data-ttu-id="2ce70-319">Rediriger</span><span class="sxs-lookup"><span data-stu-id="2ce70-319">Redirect</span></span>                                             |
| <span data-ttu-id="2ce70-320">401</span><span class="sxs-lookup"><span data-stu-id="2ce70-320">401</span></span>               | <span data-ttu-id="2ce70-321">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="2ce70-321">Authorization Failed</span></span>                                 |
| <span data-ttu-id="2ce70-322">403</span><span class="sxs-lookup"><span data-stu-id="2ce70-322">403</span></span>               | <span data-ttu-id="2ce70-323">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-323">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="2ce70-324">Obtenir un événement par le nom</span><span class="sxs-lookup"><span data-stu-id="2ce70-324">Get an event by name</span></span>

| <span data-ttu-id="2ce70-325">Méthode</span><span class="sxs-lookup"><span data-stu-id="2ce70-325">Method</span></span>         | <span data-ttu-id="2ce70-326">GET</span><span class="sxs-lookup"><span data-stu-id="2ce70-326">GET</span></span>       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| <span data-ttu-id="2ce70-327">URL</span><span class="sxs-lookup"><span data-stu-id="2ce70-327">URL</span></span>            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| <span data-ttu-id="2ce70-328">En-têtes</span><span class="sxs-lookup"><span data-stu-id="2ce70-328">Headers</span></span>        | <span data-ttu-id="2ce70-329">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ce70-329">Content-Type</span></span>                                                                                                                                 | <span data-ttu-id="2ce70-330">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-330">application/atom+xml</span></span> |
| <span data-ttu-id="2ce70-331">Authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-331">Authentication</span></span> | <span data-ttu-id="2ce70-332">De base</span><span class="sxs-lookup"><span data-stu-id="2ce70-332">Basic</span></span>                                                                                                                                        |                      |
| <span data-ttu-id="2ce70-333">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="2ce70-333">Username</span></span>       | <span data-ttu-id="2ce70-334">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="2ce70-334">“Complianceuser”</span></span>                                                                                                                             |                      |
| <span data-ttu-id="2ce70-335">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="2ce70-335">Password</span></span>       | <span data-ttu-id="2ce70-336">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="2ce70-336">“Compliancepassword”</span></span>                                                                                                                         |                      |

##### <a name="response-codes"></a><span data-ttu-id="2ce70-337">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="2ce70-337">Response codes</span></span>

| <span data-ttu-id="2ce70-338">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="2ce70-338">**Response Code**</span></span> | <span data-ttu-id="2ce70-339">**Description**</span><span class="sxs-lookup"><span data-stu-id="2ce70-339">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="2ce70-340">200</span><span class="sxs-lookup"><span data-stu-id="2ce70-340">200</span></span>               | <span data-ttu-id="2ce70-341">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="2ce70-341">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="2ce70-342">404</span><span class="sxs-lookup"><span data-stu-id="2ce70-342">404</span></span>               | <span data-ttu-id="2ce70-343">Introuvable</span><span class="sxs-lookup"><span data-stu-id="2ce70-343">Not found</span></span>                                            |
| <span data-ttu-id="2ce70-344">302</span><span class="sxs-lookup"><span data-stu-id="2ce70-344">302</span></span>               | <span data-ttu-id="2ce70-345">Rediriger</span><span class="sxs-lookup"><span data-stu-id="2ce70-345">Redirect</span></span>                                             |
| <span data-ttu-id="2ce70-346">401</span><span class="sxs-lookup"><span data-stu-id="2ce70-346">401</span></span>               | <span data-ttu-id="2ce70-347">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="2ce70-347">Authorization Failed</span></span>                                 |
| <span data-ttu-id="2ce70-348">403</span><span class="sxs-lookup"><span data-stu-id="2ce70-348">403</span></span>               | <span data-ttu-id="2ce70-349">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="2ce70-349">Authentication Failed</span></span>                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a><span data-ttu-id="2ce70-350">L’aide de PowerShell (ver.6 ou une version ultérieure) ou n’importe quel client HTTP</span><span class="sxs-lookup"><span data-stu-id="2ce70-350">Using PowerShell (ver.6 or higher) or any HTTP client</span></span>

<span data-ttu-id="2ce70-351">Étape 1: Connectez-vous à PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2ce70-351">Step 1: Connect to PowerShell.</span></span>

<span data-ttu-id="2ce70-352">Étape 2: Exécutez le script suivant.</span><span class="sxs-lookup"><span data-stu-id="2ce70-352">Step 2: Run the following script.</span></span>

<table>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ce70-353">param([string]$baseUri)</span><span class="sxs-lookup"><span data-stu-id="2ce70-353">param([string]$baseUri)</span></span></p>
<p><span data-ttu-id="2ce70-354">$userName = &quot;Nomd’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-354">$userName = &quot;UserName&quot;</span></span></p>
<p><span data-ttu-id="2ce70-355">$password = &quot;Motdepasse&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-355">$password = &quot;Password&quot;</span></span></p>
<p><span data-ttu-id="2ce70-356">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span><span class="sxs-lookup"><span data-stu-id="2ce70-356">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span></span></p>
<p><span data-ttu-id="2ce70-357">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span><span class="sxs-lookup"><span data-stu-id="2ce70-357">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span></span></p>
<p><span data-ttu-id="2ce70-358">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-358">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span></span></p>
<p><span data-ttu-id="2ce70-359">Écriture hôte &quot;Commencez à créer un événement avec nom : $EventName&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-359">Write-Host &quot;Start to create an event with name: $EventName&quot;</span></span></p>
<p><span data-ttu-id="2ce70-360">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-360">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="2ce70-361">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="2ce70-361">&lt;entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="2ce70-362">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="2ce70-362">xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="2ce70-363">xmlns='http://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-363">xmlns='http://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="2ce70-364">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-364">&lt;category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="2ce70-365">&lt;mise à jour&gt;14/7/2017 14:03:36&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-365">&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="2ce70-366">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-366">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="2ce70-367">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-367">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="2ce70-368">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-368">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="2ce70-369">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-369">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="2ce70-370">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-370">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="2ce70-371">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-371">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="2ce70-372">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="2ce70-372">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="2ce70-373">&lt;/entrée&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-373">&lt;/entry&gt;&quot;</span></span></p>
<p><span data-ttu-id="2ce70-374">$event = $null</span><span class="sxs-lookup"><span data-stu-id="2ce70-374">$event = $null</span></span></p>
<p><span data-ttu-id="2ce70-375">Essayez</span><span class="sxs-lookup"><span data-stu-id="2ce70-375">try</span></span></p>
<p><span data-ttu-id="2ce70-376">{</span><span class="sxs-lookup"><span data-stu-id="2ce70-376">{</span></span></p>
<p><span data-ttu-id="2ce70-377">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Uri &quot;$baseUri/ComplianceRetentionEvent&quot;- ContentType &quot;application/atom + xml&quot;-l’authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="2ce70-377">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="2ce70-378">}</span><span class="sxs-lookup"><span data-stu-id="2ce70-378">}</span></span></p>
<p><span data-ttu-id="2ce70-379">catch</span><span class="sxs-lookup"><span data-stu-id="2ce70-379">catch</span></span></p>
<p><span data-ttu-id="2ce70-380">{</span><span class="sxs-lookup"><span data-stu-id="2ce70-380">{</span></span></p>
<p><span data-ttu-id="2ce70-381">$response = $_.Exception.Response</span><span class="sxs-lookup"><span data-stu-id="2ce70-381">$response = $_.Exception.Response</span></span></p>
<p><span data-ttu-id="2ce70-382">if($response.StatusCode -eq &quot;Redirect&quot;)</span><span class="sxs-lookup"><span data-stu-id="2ce70-382">if($response.StatusCode -eq &quot;Redirect&quot;)</span></span></p>
<p><span data-ttu-id="2ce70-383">{</span><span class="sxs-lookup"><span data-stu-id="2ce70-383">{</span></span></p>
<p><span data-ttu-id="2ce70-384">$url = $response.Headers.Location</span><span class="sxs-lookup"><span data-stu-id="2ce70-384">$url = $response.Headers.Location</span></span></p>
<p><span data-ttu-id="2ce70-385">Écriture hôte &quot;redirigés vers $url&quot;</span><span class="sxs-lookup"><span data-stu-id="2ce70-385">Write-Host &quot;redirected to $url&quot;</span></span></p>
<p><span data-ttu-id="2ce70-386">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Url -ContentType &quot;application/atom + xml&quot; -l’Authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="2ce70-386">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="2ce70-387">}</span><span class="sxs-lookup"><span data-stu-id="2ce70-387">}</span></span></p>
<p><span data-ttu-id="2ce70-388">}</span><span class="sxs-lookup"><span data-stu-id="2ce70-388">}</span></span></p>
<p><span data-ttu-id="2ce70-389">$event | fl \*</span><span class="sxs-lookup"><span data-stu-id="2ce70-389">$event | fl \*</span></span></p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a><span data-ttu-id="2ce70-390">Vérifier le résultat dans les deux options</span><span class="sxs-lookup"><span data-stu-id="2ce70-390">Verify the outcome in both options</span></span>

<span data-ttu-id="2ce70-391">Étape 1: Accéder au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ce70-391">Step 1: Go to Security & Compliance Center</span></span>

<span data-ttu-id="2ce70-392">Étape 2 : Cliquez sur les événements sous gouvernance des données</span><span class="sxs-lookup"><span data-stu-id="2ce70-392">Step 2: Click on Events under Data Governance</span></span>

<span data-ttu-id="2ce70-393">Étape 3 : Vérifier l’Événement a été créé.</span><span class="sxs-lookup"><span data-stu-id="2ce70-393">Step 3: Verify Event has been created.</span></span>

<span data-ttu-id="2ce70-394">De même, les options ci-dessus pour automatiser la rétention basée sur des événements peuvent être également utilisées pour les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="2ce70-394">Similarly, the above options to automate event based retention can be used for the following scenarios as well.</span></span>

### <a name="scenario-2-contracts-expiring"></a><span data-ttu-id="2ce70-395">Scénario 2 : Contrats expiration</span><span class="sxs-lookup"><span data-stu-id="2ce70-395">Scenario 2: Contracts Expiring</span></span>

<span data-ttu-id="2ce70-p122">Une organisation peut avoir plusieurs enregistrements pour un contrat unique avec des clients, fournisseurs et partenaires. Ces documents peuvent résider dans une bibliothèque de documents tels que SharePoint. La fin d’un contrat détermine le début de la période de rétention des documents associé au contrat. Par exemple : tous les enregistrements liés au contrats doivent être conservés pour cinq ans de l’heure de l’expiration du contrat. L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p122">An organization can have multiple records for a single contract with customers, vendors and partners. These documents can reside in a document library like SharePoint. The ending of a contract determines the start of the retention period of the documents associated with the contract. For example: all records related to contracts need to be retained for five years from the time the contract expires. The event that triggers the five-year retention period is the expiration of the contract.</span></span>

<span data-ttu-id="2ce70-401">Un système de gestion de relation client (CRM) pouvez travailler avec Microsoft 365 et la rétention de déclencheur de documents de contrat</span><span class="sxs-lookup"><span data-stu-id="2ce70-401">A Customer Relationship Management (CRM) system can work with Microsoft 365 and trigger retention of Contract documents</span></span>

<span data-ttu-id="2ce70-402">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="2ce70-402">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario d’expiration contrat](media/automate-event-driven-retention-contract-expiration.png)

  - <span data-ttu-id="2ce70-404">L’administrateur crée une bibliothèque SharePoint avec les différents dossiers pour chaque type de contrat.</span><span class="sxs-lookup"><span data-stu-id="2ce70-404">Admin creates a SharePoint library with various folders for each contract type.</span></span>

  - <span data-ttu-id="2ce70-405">L’administrateur ajoute des fichiers de contrat tels que des contrats de licence, les contrats de développement pour chaque dossier contrat</span><span class="sxs-lookup"><span data-stu-id="2ce70-405">Admin adds contract files such as License Contracts, Development Contracts to each contract folder</span></span>

  - <span data-ttu-id="2ce70-406">L’administrateur affecte des Id de l’élément à chaque dossier de contrat.</span><span class="sxs-lookup"><span data-stu-id="2ce70-406">Admin assigns Asset Id to each contract folder</span></span>

  - <span data-ttu-id="2ce70-407">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ce70-407">SCC Admin logs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="2ce70-408">L’administrateur SCC crée un contrat lié aux types événements tels que « Création de contrat, » , « Expiration de contrat » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="2ce70-408">SCC Admin creates contract related events types such as “Contract Creation”, “Contract Expiration” events.</span></span>

  - <span data-ttu-id="2ce70-409">Administrateur SCC crée une étiquette « Expiration de contrat ».</span><span class="sxs-lookup"><span data-stu-id="2ce70-409">SCC Admin creates “Contract Expiration” label.</span></span>

  - <span data-ttu-id="2ce70-410">Cette étiquette « Expiration du Contrat » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ce70-410">This “ Contract Expiration” label is published and applied manually or automatically to the contract files in SharePoint</span></span>

  - <span data-ttu-id="2ce70-411">Le Système de Gestion de Contrat peut fonctionner avec Microsoft Flow ou une application similaire pour exécuter cette page régulièrement pour gérer les fichiers de contrat</span><span class="sxs-lookup"><span data-stu-id="2ce70-411">Contract Management System can work with Microsoft Flow or a similar application to run periodically to manage contract files</span></span>

  - <span data-ttu-id="2ce70-412">Si un employé a quitté l’organisation, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="2ce70-412">If a contract expires, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific contract’s files.</span></span>

### <a name="scenario-3-end-of-product-manufacturing"></a><span data-ttu-id="2ce70-413">Scénario 3 : Fin de la fabrication de produit</span><span class="sxs-lookup"><span data-stu-id="2ce70-413">Scenario 3: End of Product Manufacturing</span></span>

<span data-ttu-id="2ce70-p123">Une entreprise de fabrication produisant différentes lignes de produits crée plusieurs caractéristiques de fabrication et les prix de documents. Lorsque le produit n’est plus fabriqué, toutes les spécifications et documents liée à ce besoin produit sont conservés pendant une période spécifique suivant la fin de la durée de vie du produit.</span><span class="sxs-lookup"><span data-stu-id="2ce70-p123">A manufacturing company that produces different lines of products creates many manufacturing specifications and pricing documents. When the product is no longer manufactured, all specifications and documents linked to this product need to be retained for a specific period after the end of the lifetime of the product.</span></span>

<span data-ttu-id="2ce70-416">Un système de planification (ERP) peut fonctionner avec Microsoft 365 et Microsoft Flow pour la rétention de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="2ce70-416">An Enterprise Resource Planning (ERP) system can work with Microsoft 365 and Microsoft Flow to trigger retention.</span></span>

<span data-ttu-id="2ce70-417">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="2ce70-417">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario de cycle de vie de produit](media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - <span data-ttu-id="2ce70-419">L’administrateur crée des dossiers du produit dans l’ensemble de Documents tel que produit 1, produit 2, etc..</span><span class="sxs-lookup"><span data-stu-id="2ce70-419">Admin creates product folders in the Document set such as Product 1, Product 2, etc.</span></span>

  - <span data-ttu-id="2ce70-420">L’administrateur ajoute des fichiers produit tels que les spécifications de fabrication, produit sur les tarifs, les licences produit pour chaque dossier du produit</span><span class="sxs-lookup"><span data-stu-id="2ce70-420">Admin adds product files such as Manufacturing Specifications, Product Pricing, Product licensing to each product folder</span></span>

  - <span data-ttu-id="2ce70-421">L’administrateur affecte des Id de l’élément à chaque dossier produit.</span><span class="sxs-lookup"><span data-stu-id="2ce70-421">Admin assigns Asset Id to each productfolder.</span></span>

  - <span data-ttu-id="2ce70-422">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="2ce70-422">SCC Admin logs into the Security & Compliance Center</span></span>

  - <span data-ttu-id="2ce70-423">L’administrateur SCC crée des types d’événement liés à l’employé tels que « Commencer la fabrication de produit », « Fin de fabrication de produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="2ce70-423">SCC Admin creates employee related events types such as “Start of Product Manufacturing”, “End of Product Manufacturing” events.</span></span>

  - <span data-ttu-id="2ce70-424">L’administrateur SCC crée l’étiquette « Fin de la Fabrication du Produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="2ce70-424">SCC Admin creates “End of Product Manufacturing” label.</span></span>

  - <span data-ttu-id="2ce70-425">Cette étiquette «Fin de la Fabrication du Produit» est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ce70-425">This “ End of Product Manufacturing” label is published and applied manually or automatically to the product files in SharePoint</span></span>

  - <span data-ttu-id="2ce70-426">Le Système de Gestion de Contrat ERP peut fonctionner avec Microsoft Flow ou des applications similaires pour s’exécuter régulièrement pour gérer les fichiers de produit</span><span class="sxs-lookup"><span data-stu-id="2ce70-426">ERP Systems can work with Microsoft Flow or similar applications to run periodically to manage product files</span></span>

  - <span data-ttu-id="2ce70-427">Si la fabrication d’un produit se termine, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de produit spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2ce70-427">If the manufacturing of a product ends, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific product’s files.</span></span>

## <a name="appendix"></a><span data-ttu-id="2ce70-428">Annexe</span><span class="sxs-lookup"><span data-stu-id="2ce70-428">Appendix</span></span>

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a><span data-ttu-id="2ce70-429">Utiliser les résultats de réponses 302 de redirection pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="2ce70-429">Using Redirect 302 response results to call the REST API</span></span>

1.  <span data-ttu-id="2ce70-430">Appeler un appel d’événement de rétention POST à l’aide de l’URL API REST <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (les autorisations d’administrateur général sont obligatoires)</span><span class="sxs-lookup"><span data-stu-id="2ce70-430">Invoke a POST retention event call using the REST API URL <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (Global Admin permissions are required)</span></span>

2.  <span data-ttu-id="2ce70-p124">Vérifiez le code de réponse. S’il s’agit 302, puis obtenez l’URL redirigé de propriété de l’emplacement de l’en-tête de réponse</span><span class="sxs-lookup"><span data-stu-id="2ce70-p124">Check the response code. If it’s 302, then get the redirected URL from Location property of the response header</span></span>

3.  <span data-ttu-id="2ce70-433">Appeler l’appel d’événement rétention POST à l’aide d’URL redirigé.</span><span class="sxs-lookup"><span data-stu-id="2ce70-433">Invoke the POST retention event call again using the redirected URL.</span></span>

## <a name="credits"></a><span data-ttu-id="2ce70-434">Crédits</span><span class="sxs-lookup"><span data-stu-id="2ce70-434">Credits</span></span>

<span data-ttu-id="2ce70-435">Cette rubrique a été révisée par :</span><span class="sxs-lookup"><span data-stu-id="2ce70-435">This topic was reviewed by:</span></span>

<span data-ttu-id="2ce70-436">Antonio Maio</span><span class="sxs-lookup"><span data-stu-id="2ce70-436">Antonio Maio</span></span><br/><span data-ttu-id="2ce70-437">MVP Services et applications Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="2ce70-437">Microsoft Office Apps and Services MVP</span></span><br/> <span data-ttu-id="2ce70-438">Antonio.Maio@Protiviti.com</span><span class="sxs-lookup"><span data-stu-id="2ce70-438">Antonio.Maio@Protiviti.com</span></span>
