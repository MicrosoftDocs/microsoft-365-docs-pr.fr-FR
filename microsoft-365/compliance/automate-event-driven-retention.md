---
title: Rétentions basées sur des événements
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
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
ms.openlocfilehash: 692671ca5e7d956cb168ac0de2e409e7023cfd04
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42079074"
---
# <a name="automate-event-based-retention"></a><span data-ttu-id="1c456-103">Rétention basée sur des événements</span><span class="sxs-lookup"><span data-stu-id="1c456-103">Automate event-based retention</span></span>

<span data-ttu-id="1c456-p101">L’explosion de contenu dans les organisations et comment il peut devenir assistées (redondantes, obsolètes, triviale) est une affaire sérieuse. Pour continuer à répondre aux exigences légales, commerciales et défis liés à la conformité des réglementations, les organisation doivent pouvoir conserver et protéger les informations importantes et trouver rapidement ce qui est pertinent. Conservant uniquement ce qui est important, les informations pertinentes sont la clé du succès d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="1c456-p101">The explosion of content in organizations and how it can become ROT (redundant, obsolete, trivial) is serious business. To continue to meet legal, business, and regulatory compliance challenges, organizations must be able to keep and protect important information and quickly find what’s relevant. Retaining only important, pertinent information is key to an organization's success.</span></span>

<span data-ttu-id="1c456-p102">Pour répondre à ce besoin, les organisations peuvent donc tirer parti des solutions de rétention dans le centre de conformité et sécurité Office 365. La rétention peut être déclenchée en utilisant les[étiquettes de rétention](labels.md). Une étiquette de rétention a la possibilité de [baser la période de rétention sur un événement spécifique](event-driven-retention.md). En règle générale, la période de rétention est basée sur une date connue, comme la date ou date de dernière modification pour le contenu création. Toutefois, les organisations ont également des exigences à dispose de contenu en fonction des occurrences d’un événement, par exemple 7 ans après qu’un employé quitte une organisation.</span><span class="sxs-lookup"><span data-stu-id="1c456-p102">To help meet this need, organizations can take advantage of retention solutions in the Office 365 Security & Compliance Center. Retention can be triggered by using [retention labels](labels.md). A retention label has the option to [base the retention period on a specific event](event-driven-retention.md). Typically, the retention period is based on a known date, such as the creation date or last modified date for the content. However, organizations also have requirements to dispose of content based on the occurrence of an event, such as seven years after an employee leaves an organization.</span></span>

<span data-ttu-id="1c456-p103">Pour s’assurer de la conformité de la destruction de contenu, il est impératif de savoir quand un événement a lieu. Le volume du contenu en augmentant rapidement, il devient difficile à conserver et dispose du contenu d’une manière opportune et la conformité.</span><span class="sxs-lookup"><span data-stu-id="1c456-p103">To ensure compliant disposal of content, it's imperative to know when an event takes place. With the volume of content increasing rapidly, it's becoming challenging to retain and dispose content in a timely and compliant manner.</span></span>

<span data-ttu-id="1c456-p104">La rétention basée sur un événement résoud ce problème. Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1c456-p104">Event-based retention solves this problem. This topic explains how to set up your business process flows to automate retention through events by using the Microsoft 365 REST API.</span></span>

## <a name="about-event-based-retention"></a><span data-ttu-id="1c456-116">Rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="1c456-116">About event-based retention</span></span>

<span data-ttu-id="1c456-p105">Une organisation peut être grande petite ou moyenne. Le nombre de documents professionnels, documents juridiques, fichiers employé, contrats et documents produit qui sont créés et gérés sur une base quotidienne augmentent considérablement.</span><span class="sxs-lookup"><span data-stu-id="1c456-p105">An organization can be small, medium, or large. The number of business documents, legal documents, employee files, contracts, and product documents that get created and managed on a day-to-day basis is increasing dramatically.</span></span>

<span data-ttu-id="1c456-p106">Par exemple, chaque jour, dizaines et des centaines d’employés rejoignent et quittent organisations. Le service ressources humaines continue de créer, mettre à jour ou supprimer des documents liés à l’employé en respectant les exigences professionnelles. Ce processus est susceptible d’être les stratégies de rétention différentes décrites pour l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="1c456-p106">For example, each day, tens and hundreds of employees are joining and leaving organizations. The HR department continues to create, update, or delete employee-related documents as per business requirements. This process is subject to the different retention policies outlined for the business:</span></span>

- <span data-ttu-id="1c456-p107">**La période de rétention du contenu peut être une date connue** telles que la date que le contenu a été créé, la dernière modification ou étiqueté. Par exemple, vous pouvez conserver les documents pendant sept ans après que qu’ils aient été créés, puis les supprimer.</span><span class="sxs-lookup"><span data-stu-id="1c456-p107">**The period of retention for content can be a known date** such as the date the content was created, last modified, or labeled. For example, you might retain documents for seven years after they're created and then delete them.</span></span>

- <span data-ttu-id="1c456-p108">**La période de rétention du contenu peut également être une date inconnue**. Par exemple, avec des étiquettes de rétention, vous pouvez également baser une période de rétention sur lorsqu’un type spécifique d’événement se produit, par exemple un employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1c456-p108">**The period of retention of content can also be an unknown date**. For example, with retention labels, you can also base a retention period on when a specific type of event occurs, such as an employee leaving the organization.</span></span>

<span data-ttu-id="1c456-p109">Le début de la période de rétention déclenche l’événement, et tout le contenu portant une étiquette pour ce type d’événement obtenez actions de rétention l’étiquette est appliquées dessus. Il s’agit rétention basée sur l’événement.-Pour plus d’informations, voir [vue d’ensemble de rétention basées sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="1c456-p109">The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them. This is called event-based retention. To learn more, see [Overview of event-driven retention](event-driven-retention.md).</span></span>

## <a name="set-up-event-based-retention"></a><span data-ttu-id="1c456-129">Définir la rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="1c456-129">Set up event-based retention</span></span>

<span data-ttu-id="1c456-130">Cette section décrit les activités devant être effectuées avant la conservation du contenu.</span><span class="sxs-lookup"><span data-stu-id="1c456-130">This section describes what needs to be done before retaining content.</span></span>

### <a name="identify-roles"></a><span data-ttu-id="1c456-131">Identifier les rôles</span><span class="sxs-lookup"><span data-stu-id="1c456-131">Identify roles</span></span>

<span data-ttu-id="1c456-132">Identifier les différents rôles d’une organisation qui effectuent des tâches de gestion d’enregistrement et seraient responsables de la rétention efficace et de documents professionnels.</span><span class="sxs-lookup"><span data-stu-id="1c456-132">Identify the different roles in an organization that perform Record Management tasks and would be responsible for effective and efficient retention of business documents.</span></span>

  | <span data-ttu-id="1c456-133">**Persona**</span><span class="sxs-lookup"><span data-stu-id="1c456-133">**Persona**</span></span>| <span data-ttu-id="1c456-134">**Role**</span><span class="sxs-lookup"><span data-stu-id="1c456-134">**Role**</span></span>|
  | - | - |
  | <span data-ttu-id="1c456-135">Administrateur</span><span class="sxs-lookup"><span data-stu-id="1c456-135">Admin</span></span> | <span data-ttu-id="1c456-136">Crée des types d’Événement de Rétention, Étiquettes de Rétention et Référentiels d’Enregistrement dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c456-136">Creates Retention Event types, Retention labels and Record repositories in SharePoint</span></span> |
  | <span data-ttu-id="1c456-137">Gestionnaire d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="1c456-137">Records Manager</span></span>                                  | <span data-ttu-id="1c456-138">Fournit des détails de recommandations et de conformité stratégies de rétention et des plannings de rétention</span><span class="sxs-lookup"><span data-stu-id="1c456-138">Provides Retention Policies and Retention Schedules guidance and compliance details</span></span>   |
  | <span data-ttu-id="1c456-139">Administrateur système (entreprise)</span><span class="sxs-lookup"><span data-stu-id="1c456-139">System Admin (business)</span></span>                          | <span data-ttu-id="1c456-140">Configure et gère les systèmes externes pour fonctionner avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c456-140">Sets up and manages external systems to work with Microsoft 365</span></span>                       |
  | <span data-ttu-id="1c456-141">Travailleur de l'information</span><span class="sxs-lookup"><span data-stu-id="1c456-141">Information Worker</span></span>                               | <span data-ttu-id="1c456-142">Gère le cycle de vie de leur processus métier (RH, Finance, informatique, etc.)</span><span class="sxs-lookup"><span data-stu-id="1c456-142">Manages the lifecycle of their business process (HR, Finance, IT, and so on)</span></span>                 |

### <a name="set-up-the-security--compliance-center"></a><span data-ttu-id="1c456-143">Accéder au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="1c456-143">Set up the Security & Compliance Center</span></span>
  
1. <span data-ttu-id="1c456-144">L’administrateur de conformité crée un type d’événement &ndash; par exemple, la résiliation employé ou expiration de contrat ou fin de fabrication de produit.</span><span class="sxs-lookup"><span data-stu-id="1c456-144">Compliance admin creates an event type &ndash; for example, Employee Termination or Contract Expiration or End of Product Manufacturing.</span></span> <span data-ttu-id="1c456-145">(Voir le processus détaillé de[Rétentions basées sur des événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="1c456-145">(See the step-by-step process in [Event-driven retention](event-driven-retention.md).</span></span>
    
2. <span data-ttu-id="1c456-146">L’administrateur de conformité crée une étiquette en fonction d’un événement et l’associe à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="1c456-146">Compliance admin creates a retention label based on an event and associates the label with an event type.</span></span>
    
    <span data-ttu-id="1c456-147">Il existe quatre types de déclencheurs pour les étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="1c456-147">There are four types of triggers for retention labels:</span></span>
            
    1. <span data-ttu-id="1c456-148">Date de création</span><span class="sxs-lookup"><span data-stu-id="1c456-148">Create date</span></span>
                
    2. <span data-ttu-id="1c456-149">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="1c456-149">Last modified</span></span>
                
    3. <span data-ttu-id="1c456-150">Date étiquette (lorsque le contenu a été étiqueté)</span><span class="sxs-lookup"><span data-stu-id="1c456-150">Label date (when the content was labeled)</span></span>
                
    4. <span data-ttu-id="1c456-151">Basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="1c456-151">Event-based</span></span>
    
3. <span data-ttu-id="1c456-152">L’administrateur de conformité publie l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="1c456-152">Compliance admin publishes the retention label.</span></span>

### <a name="set-up-sharepoint"></a><span data-ttu-id="1c456-153">Configurer SharePoint</span><span class="sxs-lookup"><span data-stu-id="1c456-153">Set up SharePoint</span></span>
   
<span data-ttu-id="1c456-154">Pour créer un référentiel des enregistrements, l’administrateur de conformité :</span><span class="sxs-lookup"><span data-stu-id="1c456-154">To create a records repository, the compliance admin:</span></span>

1. <span data-ttu-id="1c456-155">Crée un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-155">Creates a SharePoint site.</span></span>

2. <span data-ttu-id="1c456-156">Effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c456-156">Does one of the following:</span></span>
        
    - <span data-ttu-id="1c456-p111">Crée une bibliothèque SharePoint : définir l’étiquette en fonction des événement au niveau de la bibliothèque. Pour plus d’informations, voir [application d’une étiquette de rétention par défaut à tout le contenu dans une bibliothèque SharePoint, un dossier ou un ensemble de documents](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="1c456-p111">Creates a SharePoint library: Set event-based label at the library level. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
          
    - <span data-ttu-id="1c456-159">Configure un ensemble de documents dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-159">Sets up a document set in SharePoint.</span></span> <span data-ttu-id="1c456-160">Pour plus d'informations, voir [Présentation des ensembles de documents](https://support.office.com/article/3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span><span class="sxs-lookup"><span data-stu-id="1c456-160">For more information, see [Introduction to document sets](https://support.office.com/article/3DBCD93E-0BED-46B7-B1BA-B31DE2BCD234).</span></span>
      
3. <span data-ttu-id="1c456-161">Affecte un ID d'élément à chaque ensemble de documents de l'employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-161">Assigns an asset ID to each employee document set.</span></span> <span data-ttu-id="1c456-162">Un ID d’élément est un nom de produit ou un code utilisé par l’organisation, par exemple, le numéro d’employé peut être un ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="1c456-162">An asset ID is a product name or code used by the organization, for example, Employee number can be an asset ID.</span></span> <span data-ttu-id="1c456-163">En attribuant l’ID d’élément au dossier, tous les éléments de ce dossier héritent automatiquement du même ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="1c456-163">By assigning the asset ID to the folder, every item in that folder automatically inherits the same asset ID.</span></span> <span data-ttu-id="1c456-164">Cela signifie que la période de rétention de tous les éléments peut être déclenchée par le même événement.</span><span class="sxs-lookup"><span data-stu-id="1c456-164">This means all the items can have their retention period triggered by the same event.</span></span>

## <a name="ways-to-trigger-event-based-retention"></a><span data-ttu-id="1c456-165">Méthodes pour déclencher la lecture rétention basée sur l’événement</span><span class="sxs-lookup"><span data-stu-id="1c456-165">Ways to trigger event-based retention</span></span>

<span data-ttu-id="1c456-166">Il existe deux façons avec lesquelles la rétention basée sur l’événement peut être déclenchée :</span><span class="sxs-lookup"><span data-stu-id="1c456-166">There are two ways in which event-based retention can be triggered:</span></span>

- <span data-ttu-id="1c456-167">**Utilisation de l’interface utilisateur du centre d’administration** il s’agit d’un processus qui peut être utilisé pour conserver moins de contenu à la fois, ou la fréquence à laquelle le déclenchement de la rétention n’est pas fréquente (par exemple, mensuelle ou annuelle).</span><span class="sxs-lookup"><span data-stu-id="1c456-167">**Using the admin center UI** This is a process that can be used to retain less content at a time or the frequency to trigger retention isn't often, such as monthly or yearly.</span></span> <span data-ttu-id="1c456-168">Pour plus d'informations sur cette méthode, voir[Vue d’ensemble de la rétention basée sur un événement](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="1c456-168">For more information about this method, see [Overview of event-driven retention](event-driven-retention.md).</span></span> <span data-ttu-id="1c456-169">Toutefois, cette méthode de déclenchement de la rétention peut prendre du temps et être sujette à des erreurs, ce qui freine l'évolutivité.</span><span class="sxs-lookup"><span data-stu-id="1c456-169">However, this method of triggering retention can be time consuming and prone to error, thus stunting scalability.</span></span> <span data-ttu-id="1c456-170">Par conséquent, une solution automatisée et transparente de déclenchement de la rétention peut améliorer la sécurité et la conformité des données.</span><span class="sxs-lookup"><span data-stu-id="1c456-170">Therefore, an automated, seamless solution to trigger retention can enhance data security and compliance.</span></span>

- <span data-ttu-id="1c456-p115">**À l’aide d’une API REST M365** Ce processus peut être utilisé lorsque les grandes quantités de contenu sont conservées à un moment et/ou la fréquence de rétention déclencheur est récurrente telle que de manière quotidienne ou hebdomadaire. Le flux détecte quand un événement se produit dans votre système métier de, puis crée automatiquement un événement connexe dans le centre de sécurité et conformité. Vous n’avez pas besoin de créer manuellement un événement dans l’interface utilisateur chaque fois que ce qui se passer.</span><span class="sxs-lookup"><span data-stu-id="1c456-p115">**Using a M365 REST API** This process can be used when large amounts of content are to be retained at a time and/or the frequency to trigger retention is often such as daily or weekly. The flow detects when an event occurs in your line-of-business system, and then automatically creates a related event in the Security & Compliance Center. You don't need to manually create an event in the UI each time one occurs.</span></span>

<span data-ttu-id="1c456-174">Il existe deux options d’utilisation de l’API REST :</span><span class="sxs-lookup"><span data-stu-id="1c456-174">There are two options for using the REST API:</span></span>

- <span data-ttu-id="1c456-175">**Microsoft Flow ou une application similaire** peut être utilisée pour déclencher automatiquement l’occurrence d’un événement.</span><span class="sxs-lookup"><span data-stu-id="1c456-175">**Microsoft Flow or a similar application** can be used to trigger the occurrence of an event automatically.</span></span> <span data-ttu-id="1c456-176">Microsoft Flow est un Orchestrator pour la connexion à d’autres systèmes.</span><span class="sxs-lookup"><span data-stu-id="1c456-176">Microsoft Flow is an orchestrator for connecting to other systems.</span></span> <span data-ttu-id="1c456-177">L’utilisation de Microsoft Flow ne nécessite pas de solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="1c456-177">Using Microsoft Flow doesn't require a custom solution.</span></span>

- <span data-ttu-id="1c456-178">**PowerShell ou un HTTP client pour appeler des API REST** à l’aide de PowerShell (version 6 ou version ultérieure) pour appeler l’API REST Microsoft 365 pour créer des événements.</span><span class="sxs-lookup"><span data-stu-id="1c456-178">**PowerShell or an HTTP client to call REST API** Using PowerShell (version 6 or higher) to call Microsoft 365 REST API to create events.</span></span> 

<span data-ttu-id="1c456-179">Une API REST est un point de terminaison de service qui prend en charge les ensembles d’opérations HTTP (méthodes), qui fournissent l’accès de création, récupération/mise à jour/suppression aux ressources du service.</span><span class="sxs-lookup"><span data-stu-id="1c456-179">A Rest API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources.</span></span> <span data-ttu-id="1c456-180">Pour plus d’informations, voir [composants d’une demande/réponse API REST](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span><span class="sxs-lookup"><span data-stu-id="1c456-180">For more information, see [Components of a REST API request/response](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span></span> <span data-ttu-id="1c456-181">Dans ce cas, l’API REST de Microsoft 365 vous permet de créer et d’extraire des événements à l’aide d’opérations (méthodes) publier et récupérer.</span><span class="sxs-lookup"><span data-stu-id="1c456-181">In this case, by using the Microsoft 365 REST API, events can be created and retrieved using operations (methods) POST and GET.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="1c456-182">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="1c456-182">Example scenarios</span></span>

<span data-ttu-id="1c456-183">Envisagez les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="1c456-183">Let’s consider the following scenarios.</span></span>

### <a name="scenario-1-employees-leaving-the-organization"></a><span data-ttu-id="1c456-184">Scénario 1 : Employés quittant l’organisation</span><span class="sxs-lookup"><span data-stu-id="1c456-184">Scenario 1: Employees leaving the organization</span></span> 

<span data-ttu-id="1c456-185">Une organisation crée et stocke de nombreux documents liés à des employés par employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-185">An organization creates and stores numerous employee-related documents per employee.</span></span> <span data-ttu-id="1c456-186">Ces documents sont gérés et conservés pendant l’embauche de chaque employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-186">These documents are managed and retained during the employment of each employee.</span></span> <span data-ttu-id="1c456-187">Cependant, lorsque l’employé quitte l’organisation ou que l’emploi est résilié, l’organisation est obligée par les exigences légales et commerciales de conserver les documents de cet employé pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1c456-187">However, when the employee leaves the organization or the employment is terminated, the organization is obligated by legal and business requirements to retain the documents of that employee for a stipulated period.</span></span>

<span data-ttu-id="1c456-188">Maintenant si plusieurs employés quittent l’organisation tous les jours, l’organisation doit déclencher la lecture l’horloge de rétention de centaines si ce n’est pas de milliers de documents chaque jour.</span><span class="sxs-lookup"><span data-stu-id="1c456-188">Now if multiple employees leave the organization every day, the organization must trigger the retention clock of hundreds if not thousands of documents each day.</span></span>

<span data-ttu-id="1c456-189">En plus de cela, la période de rétention doit être calculée pour chacun de ces employés comme date d’achèvement employé + nombre de jours, mois ou années en fonction du type de l’employé enregistrer.</span><span class="sxs-lookup"><span data-stu-id="1c456-189">In addition to this, the retention period needs to be calculated for each of these employees as Employee termination date + number of days, months, or years based on the type of the employee record.</span></span> <span data-ttu-id="1c456-190">Par exemple, la rémunération du collaborateur des employés et les déclarations d’avantages du même employé peuvent nécessiter une rétention différente.</span><span class="sxs-lookup"><span data-stu-id="1c456-190">For example, worker’s compensation of the employee vs. benefits filings of the same employee may need different retention.</span></span>

<span data-ttu-id="1c456-191">Le diagramme ci-dessous montre comment plusieurs étiquettes peuvent être associées à un seul événement.</span><span class="sxs-lookup"><span data-stu-id="1c456-191">The diagram below shows how there can be multiple labels that are associated with a single event.</span></span> <span data-ttu-id="1c456-192">Dans cet exemple, tous les fichiers figurant sous l’étiquette indemnités du collaborateur et tous les fichiers sous l’étiquette avantages sociaux des employés sont associés à un seul événement, qui est l’employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1c456-192">Here all the files under Worker’s compensation label and all the files under Employee benefits label are both associated with a single event, which is the employee leaving the organization.</span></span> <span data-ttu-id="1c456-193">Chacun de ces fichiers a des horloges de rétention différentes.</span><span class="sxs-lookup"><span data-stu-id="1c456-193">Each of these different files has different retention clocks.</span></span> <span data-ttu-id="1c456-194">Par conséquent, lorsqu’un employé quitte l’organisation, ces fichiers au sein de chaque étiquette ont une période de rétention différente.</span><span class="sxs-lookup"><span data-stu-id="1c456-194">So, when an employee leaves the organization, these files within each label experience a different retention period.</span></span> <span data-ttu-id="1c456-195">Le déclenchement de toutes ces horloges de rétention pour chaque type de fichier ou étiquette pour chaque employé constitue une tâche complexe.</span><span class="sxs-lookup"><span data-stu-id="1c456-195">Triggering all these different retention clocks for each file type or label for each employee is a very challenging task.</span></span> <span data-ttu-id="1c456-196">Imaginez qu’il s’agit de plusieurs employés.</span><span class="sxs-lookup"><span data-stu-id="1c456-196">Imagine doing this for multiple employees.</span></span>

![Diagramme illustrant le type d’événement, des événements et des étiquettes](../media/automate-event-driven-retention-event-diagram-employee-leaving.png)

<span data-ttu-id="1c456-198">Un processus automatisé associé au déclenchement de ces différentes horloges de rétention pour plusieurs employés sera donc un gagne-temps, exempte d’erreur et très efficace.</span><span class="sxs-lookup"><span data-stu-id="1c456-198">Hence an automated process to trigger these different retention clocks for multiple employees will be time-saving, error-free, and extremely efficient.</span></span>

<span data-ttu-id="1c456-199">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="1c456-199">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des actions pour le scénario d’employé quittant l’organisation](../media/automate-event-driven-retention-employee-termination-diagram.png)

  - <span data-ttu-id="1c456-201">L’administrateur crée des dossiers d’employé lié au Document, telles Cartier Marie, John Smith.</span><span class="sxs-lookup"><span data-stu-id="1c456-201">Admin creates employee folders to the Document set such as Jane Doe, John Smith.</span></span>

  - <span data-ttu-id="1c456-202">L’administrateur ajoute des fichiers employé tels que les avantages, paie, rémunération de travailleur à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-202">Admin adds employee files such as Benefits, Payroll, Worker’s Compensation to each employee folder.</span></span>

  - <span data-ttu-id="1c456-203">L’administrateur affecte des ID d’élément à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-203">Admin assigns Asset ID to each employee folder.</span></span> 

  - <span data-ttu-id="1c456-204">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="1c456-204">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="1c456-205">L’administrateur SCC crée des types d’événements liés à l’employé tels que « Renvoi employé », « Embauche employé » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="1c456-205">SCC Admin creates employee-related events types such as “Employee Termination”, “Employee Hire” events.</span></span>

  - <span data-ttu-id="1c456-206">Administrateur SCC crée une étiquette « Employés ».</span><span class="sxs-lookup"><span data-stu-id="1c456-206">SCC Admin creates “Employee Retention” label.</span></span>

  - <span data-ttu-id="1c456-207">Cette étiquette « Employés » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-207">This “Employee Retention” label is published and applied manually or automatically to the employee files in SharePoint.</span></span>

  - <span data-ttu-id="1c456-208">Le Système de Gestion des Ressources Humaines comme Workday peut fonctionner avec Microsoft Flow pour exécuter cette page régulièrement pour gérer les fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-208">HR Management System like Workday can work with Microsoft Flow to run periodically to manage employee files.</span></span>

  - <span data-ttu-id="1c456-209">Si un employé a quitté l’organisation, le flux déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-209">If an employee has left the organization, the Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific employee’s files.</span></span>

#### <a name="using-microsoft-flow"></a><span data-ttu-id="1c456-210">Utilisation Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="1c456-210">Using Microsoft Flow</span></span>

<span data-ttu-id="1c456-211">Étape 1-créer un flux de créer un événement en utilisant l’API REST Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1c456-211">Step 1- Create a flow to create an event using the Microsoft 365 REST API</span></span>

![Utilisation le flux pour créer un événement](../media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](../media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a><span data-ttu-id="1c456-214">Créer un événement</span><span class="sxs-lookup"><span data-stu-id="1c456-214">Create an event</span></span>

<span data-ttu-id="1c456-215">Utilisation du code d’exemple pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="1c456-215">Sample code to call the REST API</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c456-216">Méthode</span><span class="sxs-lookup"><span data-stu-id="1c456-216">Method</span></span></th>
<th><span data-ttu-id="1c456-217">POST</span><span class="sxs-lookup"><span data-stu-id="1c456-217">POST</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c456-218">URL</span><span class="sxs-lookup"><span data-stu-id="1c456-218">URL</span></span></td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent</td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-219">En-têtes</span><span class="sxs-lookup"><span data-stu-id="1c456-219">Headers</span></span></td>
<td><span data-ttu-id="1c456-220">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1c456-220">Content-Type</span></span></td>
<td><span data-ttu-id="1c456-221">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="1c456-221">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c456-222">Corps</span><span class="sxs-lookup"><span data-stu-id="1c456-222">Body</span></span></td>
<td><p><span data-ttu-id="1c456-223">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-223">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="1c456-224">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="1c456-224">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="1c456-225">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="1c456-225">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="1c456-226">xmlns='https://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-226">xmlns='https://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="1c456-227">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-227">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="1c456-228">&lt;mise à jour&gt;9/9/2017 22:50:00&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-228">&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="1c456-229">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-229">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="1c456-230">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-230">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="1c456-231">&lt;d:Name&gt;Licenciement employé&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-231">&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="1c456-232">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-232">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="1c456-233">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-233">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="1c456-234">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-234">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span></span></p>
<p><span data-ttu-id="1c456-235">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-235">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="1c456-236">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-236">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="1c456-237">&lt;/entrée&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-237">&lt;/entry&gt;</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-238">Authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-238">Authentication</span></span></td>
<td><span data-ttu-id="1c456-239">De base</span><span class="sxs-lookup"><span data-stu-id="1c456-239">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c456-240">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c456-240">Username</span></span></td>
<td><span data-ttu-id="1c456-241">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="1c456-241">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-242">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="1c456-242">Password</span></span></td>
<td><span data-ttu-id="1c456-243">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="1c456-243">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a><span data-ttu-id="1c456-244">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="1c456-244">Available parameters</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c456-245"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="1c456-245"><strong>Parameters</strong></span></span></th>
<th><span data-ttu-id="1c456-246"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="1c456-246"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="1c456-247"><strong>Notes</strong></span><span class="sxs-lookup"><span data-stu-id="1c456-247"><strong>Notes</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c456-248">&lt;d:Name&gt;&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-248">&lt;d:Name&gt;&lt;/d:Name&gt;</span></span></td>
<td><span data-ttu-id="1c456-249">Entrez un nom unique pour la base de données,</span><span class="sxs-lookup"><span data-stu-id="1c456-249">Provide a unique name for the event,</span></span></td>
<td><span data-ttu-id="1c456-p121">Un nom ne peut pas contenir les espaces et les caractères suivants : % \* \ &amp; &lt; &gt; | # ? , : ;</span><span class="sxs-lookup"><span data-stu-id="1c456-p121">Cannot contain trailing spaces, and the following characters: % \* \ &amp; &lt; &gt; | # ? , : ;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-252">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-252">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span></span></td>
<td><span data-ttu-id="1c456-253">Entrez le nom de l’événement (ou Guid),</span><span class="sxs-lookup"><span data-stu-id="1c456-253">Enter event type name (or Guid),</span></span></td>
<td><span data-ttu-id="1c456-p122">Exemple : « employé licenciement anticipé ». Le type d’événement doit être associé à une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="1c456-p122">Example: “Employee termination”. Event type has to be associated with a retention label.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c456-256">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-256">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span></span></td>
<td><span data-ttu-id="1c456-257">Entrez « ComplianceAssetId : « + Id d’employé</span><span class="sxs-lookup"><span data-stu-id="1c456-257">Enter “ComplianceAssetId:” + employee Id</span></span></td>
<td><span data-ttu-id="1c456-258">Exemple :&quot;ComplianceAssetId:12345&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-258">Example:&quot;ComplianceAssetId:12345&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-259">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-259">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span></span></td>
<td><span data-ttu-id="1c456-260">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="1c456-260">Event Date and Time</span></span></td>
<td><p><span data-ttu-id="1c456-261">Format : AAAA-MM-JJThh, exemple :</span><span class="sxs-lookup"><span data-stu-id="1c456-261">Format: yyyy-MM-ddTHH:mm:ssZ, Example:</span></span></p>
<p><span data-ttu-id="1c456-262">2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="1c456-262">2018-12-01T00:00:00Z</span></span></p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="1c456-263">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="1c456-263">Response codes</span></span>

| <span data-ttu-id="1c456-264">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="1c456-264">**Response Code**</span></span> | <span data-ttu-id="1c456-265">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c456-265">**Description**</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="1c456-266">302</span><span class="sxs-lookup"><span data-stu-id="1c456-266">302</span></span>               | <span data-ttu-id="1c456-267">Rediriger</span><span class="sxs-lookup"><span data-stu-id="1c456-267">Redirect</span></span>              |
| <span data-ttu-id="1c456-268">201</span><span class="sxs-lookup"><span data-stu-id="1c456-268">201</span></span>               | <span data-ttu-id="1c456-269">Créé</span><span class="sxs-lookup"><span data-stu-id="1c456-269">Created</span></span>               |
| <span data-ttu-id="1c456-270">403</span><span class="sxs-lookup"><span data-stu-id="1c456-270">403</span></span>               | <span data-ttu-id="1c456-271">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="1c456-271">Authorization Failed</span></span>  |
| <span data-ttu-id="1c456-272">401</span><span class="sxs-lookup"><span data-stu-id="1c456-272">401</span></span>               | <span data-ttu-id="1c456-273">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-273">Authentication Failed</span></span> |

##### <a name="get-events-based-on-time-range"></a><span data-ttu-id="1c456-274">Obtenir des événements en fonction de l’intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="1c456-274">Get Events based on time range</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1c456-275">Méthode</span><span class="sxs-lookup"><span data-stu-id="1c456-275">Method</span></span></th>
<th><span data-ttu-id="1c456-276">GET</span><span class="sxs-lookup"><span data-stu-id="1c456-276">GET</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c456-277">URL</span><span class="sxs-lookup"><span data-stu-id="1c456-277">URL</span></span></td>
<td><ol start="4" type="1">
<li><p><span data-ttu-id="1c456-278">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span><span class="sxs-lookup"><span data-stu-id="1c456-278">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span></span></p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-279">En-têtes</span><span class="sxs-lookup"><span data-stu-id="1c456-279">Headers</span></span></td>
<td><span data-ttu-id="1c456-280">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1c456-280">Content-Type</span></span></td>
<td><span data-ttu-id="1c456-281">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="1c456-281">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-282">Authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-282">Authentication</span></span></td>
<td><span data-ttu-id="1c456-283">De base</span><span class="sxs-lookup"><span data-stu-id="1c456-283">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c456-284">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c456-284">Username</span></span></td>
<td><span data-ttu-id="1c456-285">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="1c456-285">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c456-286">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="1c456-286">Password</span></span></td>
<td><span data-ttu-id="1c456-287">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="1c456-287">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="1c456-288">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="1c456-288">Response codes</span></span>

| <span data-ttu-id="1c456-289">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="1c456-289">**Response Code**</span></span> | <span data-ttu-id="1c456-290">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c456-290">**Description**</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="1c456-291">200</span><span class="sxs-lookup"><span data-stu-id="1c456-291">200</span></span>               | <span data-ttu-id="1c456-292">OK, une liste d’événements dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="1c456-292">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="1c456-293">404</span><span class="sxs-lookup"><span data-stu-id="1c456-293">404</span></span>               | <span data-ttu-id="1c456-294">Introuvable</span><span class="sxs-lookup"><span data-stu-id="1c456-294">Not found</span></span>                         |
| <span data-ttu-id="1c456-295">302</span><span class="sxs-lookup"><span data-stu-id="1c456-295">302</span></span>               | <span data-ttu-id="1c456-296">Rediriger</span><span class="sxs-lookup"><span data-stu-id="1c456-296">Redirect</span></span>                          |
| <span data-ttu-id="1c456-297">401</span><span class="sxs-lookup"><span data-stu-id="1c456-297">401</span></span>               | <span data-ttu-id="1c456-298">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="1c456-298">Authorization Failed</span></span>              |
| <span data-ttu-id="1c456-299">403</span><span class="sxs-lookup"><span data-stu-id="1c456-299">403</span></span>               | <span data-ttu-id="1c456-300">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-300">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="1c456-301">Obtenir un événement par ID</span><span class="sxs-lookup"><span data-stu-id="1c456-301">Get an event by ID</span></span>

| <span data-ttu-id="1c456-302">Méthode</span><span class="sxs-lookup"><span data-stu-id="1c456-302">Method</span></span>         | <span data-ttu-id="1c456-303">GET</span><span class="sxs-lookup"><span data-stu-id="1c456-303">GET</span></span>   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| <span data-ttu-id="1c456-304">URL</span><span class="sxs-lookup"><span data-stu-id="1c456-304">URL</span></span>            | <span data-ttu-id="1c456-305">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span><span class="sxs-lookup"><span data-stu-id="1c456-305">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span></span> |                      |
| <span data-ttu-id="1c456-306">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c456-306">Header</span></span>         | <span data-ttu-id="1c456-307">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1c456-307">Content-Type</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="1c456-308">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="1c456-308">application/atom+xml</span></span> |
| <span data-ttu-id="1c456-309">Authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-309">Authentication</span></span> | <span data-ttu-id="1c456-310">De base</span><span class="sxs-lookup"><span data-stu-id="1c456-310">Basic</span></span>                                                                                                                                                                                                                                                              |                      |
| <span data-ttu-id="1c456-311">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c456-311">Username</span></span>       | <span data-ttu-id="1c456-312">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="1c456-312">“Complianceuser”</span></span>                                                                                                                                                                                                                                                   |                      |
| <span data-ttu-id="1c456-313">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="1c456-313">Password</span></span>       | <span data-ttu-id="1c456-314">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="1c456-314">“Compliancepassword”</span></span>                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a><span data-ttu-id="1c456-315">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="1c456-315">Response codes</span></span>

| <span data-ttu-id="1c456-316">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="1c456-316">**Response Code**</span></span> | <span data-ttu-id="1c456-317">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c456-317">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="1c456-318">200</span><span class="sxs-lookup"><span data-stu-id="1c456-318">200</span></span>               | <span data-ttu-id="1c456-319">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="1c456-319">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="1c456-320">404</span><span class="sxs-lookup"><span data-stu-id="1c456-320">404</span></span>               | <span data-ttu-id="1c456-321">Introuvable</span><span class="sxs-lookup"><span data-stu-id="1c456-321">Not found</span></span>                                            |
| <span data-ttu-id="1c456-322">302</span><span class="sxs-lookup"><span data-stu-id="1c456-322">302</span></span>               | <span data-ttu-id="1c456-323">Rediriger</span><span class="sxs-lookup"><span data-stu-id="1c456-323">Redirect</span></span>                                             |
| <span data-ttu-id="1c456-324">401</span><span class="sxs-lookup"><span data-stu-id="1c456-324">401</span></span>               | <span data-ttu-id="1c456-325">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="1c456-325">Authorization Failed</span></span>                                 |
| <span data-ttu-id="1c456-326">403</span><span class="sxs-lookup"><span data-stu-id="1c456-326">403</span></span>               | <span data-ttu-id="1c456-327">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-327">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="1c456-328">Obtenir un événement par le nom</span><span class="sxs-lookup"><span data-stu-id="1c456-328">Get an event by name</span></span>

| <span data-ttu-id="1c456-329">Méthode</span><span class="sxs-lookup"><span data-stu-id="1c456-329">Method</span></span>         | <span data-ttu-id="1c456-330">GET</span><span class="sxs-lookup"><span data-stu-id="1c456-330">GET</span></span>       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| <span data-ttu-id="1c456-331">URL</span><span class="sxs-lookup"><span data-stu-id="1c456-331">URL</span></span>            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| <span data-ttu-id="1c456-332">En-têtes</span><span class="sxs-lookup"><span data-stu-id="1c456-332">Headers</span></span>        | <span data-ttu-id="1c456-333">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1c456-333">Content-Type</span></span>                                                                                                                                 | <span data-ttu-id="1c456-334">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="1c456-334">application/atom+xml</span></span> |
| <span data-ttu-id="1c456-335">Authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-335">Authentication</span></span> | <span data-ttu-id="1c456-336">De base</span><span class="sxs-lookup"><span data-stu-id="1c456-336">Basic</span></span>                                                                                                                                        |                      |
| <span data-ttu-id="1c456-337">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="1c456-337">Username</span></span>       | <span data-ttu-id="1c456-338">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="1c456-338">“Complianceuser”</span></span>                                                                                                                             |                      |
| <span data-ttu-id="1c456-339">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="1c456-339">Password</span></span>       | <span data-ttu-id="1c456-340">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="1c456-340">“Compliancepassword”</span></span>                                                                                                                         |                      |

##### <a name="response-codes"></a><span data-ttu-id="1c456-341">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="1c456-341">Response codes</span></span>

| <span data-ttu-id="1c456-342">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="1c456-342">**Response Code**</span></span> | <span data-ttu-id="1c456-343">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c456-343">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="1c456-344">200</span><span class="sxs-lookup"><span data-stu-id="1c456-344">200</span></span>               | <span data-ttu-id="1c456-345">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="1c456-345">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="1c456-346">404</span><span class="sxs-lookup"><span data-stu-id="1c456-346">404</span></span>               | <span data-ttu-id="1c456-347">Introuvable</span><span class="sxs-lookup"><span data-stu-id="1c456-347">Not found</span></span>                                            |
| <span data-ttu-id="1c456-348">302</span><span class="sxs-lookup"><span data-stu-id="1c456-348">302</span></span>               | <span data-ttu-id="1c456-349">Rediriger</span><span class="sxs-lookup"><span data-stu-id="1c456-349">Redirect</span></span>                                             |
| <span data-ttu-id="1c456-350">401</span><span class="sxs-lookup"><span data-stu-id="1c456-350">401</span></span>               | <span data-ttu-id="1c456-351">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="1c456-351">Authorization Failed</span></span>                                 |
| <span data-ttu-id="1c456-352">403</span><span class="sxs-lookup"><span data-stu-id="1c456-352">403</span></span>               | <span data-ttu-id="1c456-353">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="1c456-353">Authentication Failed</span></span>                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a><span data-ttu-id="1c456-354">L’aide de PowerShell (ver.6 ou une version ultérieure) ou n’importe quel client HTTP</span><span class="sxs-lookup"><span data-stu-id="1c456-354">Using PowerShell (ver.6 or higher) or any HTTP client</span></span>

<span data-ttu-id="1c456-355">Étape 1: Connectez-vous à PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1c456-355">Step 1: Connect to PowerShell.</span></span>

<span data-ttu-id="1c456-356">Étape 2: Exécutez le script suivant.</span><span class="sxs-lookup"><span data-stu-id="1c456-356">Step 2: Run the following script.</span></span>

<table>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c456-357">param([string]$baseUri)</span><span class="sxs-lookup"><span data-stu-id="1c456-357">param([string]$baseUri)</span></span></p>
<p><span data-ttu-id="1c456-358">$userName = &quot;Nomd’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-358">$userName = &quot;UserName&quot;</span></span></p>
<p><span data-ttu-id="1c456-359">$password = &quot;Motdepasse&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-359">$password = &quot;Password&quot;</span></span></p>
<p><span data-ttu-id="1c456-360">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span><span class="sxs-lookup"><span data-stu-id="1c456-360">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span></span></p>
<p><span data-ttu-id="1c456-361">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span><span class="sxs-lookup"><span data-stu-id="1c456-361">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span></span></p>
<p><span data-ttu-id="1c456-362">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-362">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span></span></p>
<p><span data-ttu-id="1c456-363">Écriture hôte &quot;Commencez à créer un événement avec nom : $EventName&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-363">Write-Host &quot;Start to create an event with name: $EventName&quot;</span></span></p>
<p><span data-ttu-id="1c456-364">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-364">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="1c456-365">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="1c456-365">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="1c456-366">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="1c456-366">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="1c456-367">xmlns='https://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-367">xmlns='https://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="1c456-368">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-368">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="1c456-369">&lt;mise à jour&gt;14/7/2017 14:03:36&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-369">&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="1c456-370">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-370">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="1c456-371">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-371">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="1c456-372">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-372">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="1c456-373">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-373">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="1c456-374">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-374">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="1c456-375">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-375">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="1c456-376">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="1c456-376">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="1c456-377">&lt;/entrée&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-377">&lt;/entry&gt;&quot;</span></span></p>
<p><span data-ttu-id="1c456-378">$event = $null</span><span class="sxs-lookup"><span data-stu-id="1c456-378">$event = $null</span></span></p>
<p><span data-ttu-id="1c456-379">Essayez</span><span class="sxs-lookup"><span data-stu-id="1c456-379">try</span></span></p>
<p><span data-ttu-id="1c456-380">{</span><span class="sxs-lookup"><span data-stu-id="1c456-380">{</span></span></p>
<p><span data-ttu-id="1c456-381">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Uri &quot;$baseUri/ComplianceRetentionEvent&quot;- ContentType &quot;application/atom + xml&quot;-l’authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="1c456-381">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="1c456-382">}</span><span class="sxs-lookup"><span data-stu-id="1c456-382">}</span></span></p>
<p><span data-ttu-id="1c456-383">catch</span><span class="sxs-lookup"><span data-stu-id="1c456-383">catch</span></span></p>
<p><span data-ttu-id="1c456-384">{</span><span class="sxs-lookup"><span data-stu-id="1c456-384">{</span></span></p>
<p><span data-ttu-id="1c456-385">$response = $_.Exception.Response</span><span class="sxs-lookup"><span data-stu-id="1c456-385">$response = $_.Exception.Response</span></span></p>
<p><span data-ttu-id="1c456-386">if($response.StatusCode -eq &quot;Redirect&quot;)</span><span class="sxs-lookup"><span data-stu-id="1c456-386">if($response.StatusCode -eq &quot;Redirect&quot;)</span></span></p>
<p><span data-ttu-id="1c456-387">{</span><span class="sxs-lookup"><span data-stu-id="1c456-387">{</span></span></p>
<p><span data-ttu-id="1c456-388">$url = $response.Headers.Location</span><span class="sxs-lookup"><span data-stu-id="1c456-388">$url = $response.Headers.Location</span></span></p>
<p><span data-ttu-id="1c456-389">Écriture hôte &quot;redirigés vers $url&quot;</span><span class="sxs-lookup"><span data-stu-id="1c456-389">Write-Host &quot;redirected to $url&quot;</span></span></p>
<p><span data-ttu-id="1c456-390">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Url -ContentType &quot;application/atom + xml&quot; -l’Authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="1c456-390">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="1c456-391">}</span><span class="sxs-lookup"><span data-stu-id="1c456-391">}</span></span></p>
<p><span data-ttu-id="1c456-392">}</span><span class="sxs-lookup"><span data-stu-id="1c456-392">}</span></span></p>
<p><span data-ttu-id="1c456-393">$event | fl \*</span><span class="sxs-lookup"><span data-stu-id="1c456-393">$event | fl \*</span></span></p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a><span data-ttu-id="1c456-394">Vérifier le résultat dans les deux options</span><span class="sxs-lookup"><span data-stu-id="1c456-394">Verify the outcome in both options</span></span>

<span data-ttu-id="1c456-395">Étape 1 : Accéder au centre de conformité et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1c456-395">Step 1: Go to the Security & Compliance Center.</span></span>

<span data-ttu-id="1c456-396">Étape 2 : Sélectionner **Évènements** sous **Gouvernance des informations**.</span><span class="sxs-lookup"><span data-stu-id="1c456-396">Step 2: Select **Events** under **Information governance**.</span></span>

<span data-ttu-id="1c456-397">Étape 3 : Vérifier l’Événement a été créé.</span><span class="sxs-lookup"><span data-stu-id="1c456-397">Step 3: Verify Event has been created.</span></span>

<span data-ttu-id="1c456-398">De même, les options ci-dessus pour automatiser la rétention basée sur des événements peuvent être également utilisées pour les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="1c456-398">Similarly, the above options to automate event-based retention can be used for the following scenarios as well.</span></span>

### <a name="scenario-2-contracts-expiring"></a><span data-ttu-id="1c456-399">Scénario 2 : Contrats expiration</span><span class="sxs-lookup"><span data-stu-id="1c456-399">Scenario 2: Contracts Expiring</span></span>

<span data-ttu-id="1c456-400">Une organisation peut avoir plusieurs enregistrements pour un seul contrat avec des clients, des fournisseurs et des partenaires.</span><span class="sxs-lookup"><span data-stu-id="1c456-400">An organization can have multiple records for a single contract with customers, vendors, and partners.</span></span> <span data-ttu-id="1c456-401">Ces documents peuvent résider dans une bibliothèque de documents telle que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-401">These documents can reside in a document library like SharePoint.</span></span> <span data-ttu-id="1c456-402">La fin d’un contrat détermine le début de la période de rétention des documents associés au contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-402">The end of a contract determines the start of the retention period of the documents associated with the contract.</span></span> <span data-ttu-id="1c456-403">Par exemple, tous les documents relatifs aux contrats doivent être conservés pendant cinq ans après l'expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-403">For example, all records related to contracts need to be retained for five years from the time the contract expires.</span></span> <span data-ttu-id="1c456-404">L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-404">The event that triggers the five-year retention period is the expiration of the contract.</span></span>

<span data-ttu-id="1c456-405">Un système de gestion de relation client (CRM) pouvez travailler avec Microsoft 365 et la rétention de déclencheur de documents de contrat</span><span class="sxs-lookup"><span data-stu-id="1c456-405">A Customer Relationship Management (CRM) system can work with Microsoft 365 and trigger retention of Contract documents</span></span>

<span data-ttu-id="1c456-406">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="1c456-406">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario d’expiration contrat](../media/automate-event-driven-retention-contract-expiration.png)

  - <span data-ttu-id="1c456-408">L’administrateur crée une bibliothèque SharePoint avec les différents dossiers pour chaque type de contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-408">Admin creates a SharePoint library with various folders for each contract type.</span></span>

  - <span data-ttu-id="1c456-409">L’administrateur ajoute des fichiers de contrat tels que des contrats de licence, les contrats de développement pour chaque dossier contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-409">Admin adds contract files such as License Contracts, Development Contracts to each contract folder.</span></span>

  - <span data-ttu-id="1c456-410">L’administrateur affecte des ID délément à chaque dossier de contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-410">Admin assigns Asset ID to each contract folder.</span></span>

  - <span data-ttu-id="1c456-411">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="1c456-411">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="1c456-412">L’administrateur SCC crée un contrat lié aux types événements tels que « Création de contrat, » , « Expiration de contrat » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="1c456-412">SCC Admin creates contract-related events types such as “Contract Creation”, “Contract Expiration” events.</span></span>

  - <span data-ttu-id="1c456-413">Administrateur SCC crée une étiquette « Expiration de contrat ».</span><span class="sxs-lookup"><span data-stu-id="1c456-413">SCC Admin creates “Contract Expiration” label.</span></span>

  - <span data-ttu-id="1c456-414">Cette étiquette « Expiration du Contrat » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-414">This “ Contract Expiration” label is published and applied manually or automatically to the contract files in SharePoint.</span></span>

  - <span data-ttu-id="1c456-415">Le Système de Gestion de Contrat peut fonctionner avec Microsoft Flow ou une application similaire pour exécuter cette page régulièrement pour gérer les fichiers de contrat.</span><span class="sxs-lookup"><span data-stu-id="1c456-415">Contract Management System can work with Microsoft Flow or a similar application to run periodically to manage contract files.</span></span>

  - <span data-ttu-id="1c456-416">Si un employé a quitté l’organisation, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="1c456-416">If a contract expires, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific contract’s files.</span></span>

### <a name="scenario-3-end-of-product-manufacturing"></a><span data-ttu-id="1c456-417">Scénario 3 : Fin de la fabrication de produit</span><span class="sxs-lookup"><span data-stu-id="1c456-417">Scenario 3: End of Product Manufacturing</span></span>

<span data-ttu-id="1c456-p124">Une entreprise de fabrication produisant différentes lignes de produits crée plusieurs caractéristiques de fabrication et les prix de documents. Lorsque le produit n’est plus fabriqué, toutes les spécifications et documents liée à ce besoin produit sont conservés pendant une période spécifique suivant la fin de la durée de vie du produit.</span><span class="sxs-lookup"><span data-stu-id="1c456-p124">A manufacturing company that produces different lines of products creates many manufacturing specifications and pricing documents. When the product is no longer manufactured, all specifications and documents linked to this product need to be retained for a specific period after the end of the lifetime of the product.</span></span>

<span data-ttu-id="1c456-420">Un système de planification (ERP) peut fonctionner avec Microsoft 365 et Microsoft Flow pour la rétention de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="1c456-420">An Enterprise Resource Planning (ERP) system can work with Microsoft 365 and Microsoft Flow to trigger retention.</span></span>

<span data-ttu-id="1c456-421">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="1c456-421">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario de cycle de vie de produit](../media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - <span data-ttu-id="1c456-423">L’administrateur crée des dossiers du produit dans l’ensemble de Documents tel que produit 1, produit 2, etc.</span><span class="sxs-lookup"><span data-stu-id="1c456-423">Admin creates product folders in the Document set such as Product 1, Product 2, and so on.</span></span>

  - <span data-ttu-id="1c456-424">L’administrateur ajoute des fichiers produit tels que les spécifications de fabrication, produit sur les tarifs, les licences produit pour chaque dossier du produit.</span><span class="sxs-lookup"><span data-stu-id="1c456-424">Admin adds product files such as Manufacturing Specifications, Product Pricing, Product licensing to each product folder.</span></span>

  - <span data-ttu-id="1c456-425">L’administrateur affecte des ID d’élément à chaque dossier produit.</span><span class="sxs-lookup"><span data-stu-id="1c456-425">Admin assigns Asset ID to each product folder.</span></span>

  - <span data-ttu-id="1c456-426">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="1c456-426">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="1c456-427">L’administrateur SCC crée des types d’événement liés à l’employé tels que « Commencer la fabrication de produit », « Fin de fabrication de produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="1c456-427">SCC Admin creates employee-related events types such as “Start of Product Manufacturing”, “End of Product Manufacturing” events.</span></span>

  - <span data-ttu-id="1c456-428">L’administrateur SCC crée l’étiquette « Fin de la Fabrication du Produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="1c456-428">SCC Admin creates “End of Product Manufacturing” label.</span></span>

  - <span data-ttu-id="1c456-429">Cette étiquette «Fin de la Fabrication du Produit» est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1c456-429">This “ End of Product Manufacturing” label is published and applied manually or automatically to the product files in SharePoint.</span></span>

  - <span data-ttu-id="1c456-430">Le Système de Gestion de Contrat ERP peut fonctionner avec Microsoft Flow ou des applications similaires pour s’exécuter régulièrement pour gérer les fichiers de produit.</span><span class="sxs-lookup"><span data-stu-id="1c456-430">ERP Systems can work with Microsoft Flow or similar applications to run periodically to manage product files.</span></span>

  - <span data-ttu-id="1c456-431">Si la fabrication d’un produit se termine, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de produit spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1c456-431">If the manufacturing of a product ends, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific product’s files.</span></span>

## <a name="appendix"></a><span data-ttu-id="1c456-432">Annexe</span><span class="sxs-lookup"><span data-stu-id="1c456-432">Appendix</span></span>

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a><span data-ttu-id="1c456-433">Utiliser les résultats de réponses 302 de redirection pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="1c456-433">Using Redirect 302 response results to call the REST API</span></span>

1. <span data-ttu-id="1c456-434">Appeler un appel d’événement de rétention POST à l’aide de l’URL API REST <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (les autorisations d’administrateur général sont obligatoires)</span><span class="sxs-lookup"><span data-stu-id="1c456-434">Invoke a POST retention event call using the REST API URL <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (Global Admin permissions are required)</span></span>

2. <span data-ttu-id="1c456-p125">Vérifiez le code de réponse. S’il s’agit 302, puis obtenez l’URL redirigé de propriété de l’emplacement de l’en-tête de réponse</span><span class="sxs-lookup"><span data-stu-id="1c456-p125">Check the response code. If it’s 302, then get the redirected URL from Location property of the response header</span></span>

3. <span data-ttu-id="1c456-437">Appeler l’appel d’événement rétention POST à l’aide d’URL redirigé.</span><span class="sxs-lookup"><span data-stu-id="1c456-437">Invoke the POST retention event call again using the redirected URL.</span></span>

## <a name="credits"></a><span data-ttu-id="1c456-438">Crédits</span><span class="sxs-lookup"><span data-stu-id="1c456-438">Credits</span></span>

<span data-ttu-id="1c456-439">Cette rubrique a été révisée par :</span><span class="sxs-lookup"><span data-stu-id="1c456-439">This topic was reviewed by:</span></span>

<span data-ttu-id="1c456-440">Antonio Maio</span><span class="sxs-lookup"><span data-stu-id="1c456-440">Antonio Maio</span></span><br/><span data-ttu-id="1c456-441">MVP Services et applications Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="1c456-441">Microsoft Office Apps and Services MVP</span></span><br/> <span data-ttu-id="1c456-442">Antonio.Maio@Protiviti.com</span><span class="sxs-lookup"><span data-stu-id="1c456-442">Antonio.Maio@Protiviti.com</span></span>
