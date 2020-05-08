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
ms.openlocfilehash: b94a607b679c6a03624a5af7a1b61f7d7a29dbee
ms.sourcegitcommit: 46644f9778bc70ab6d62783e0a1e60ba2eccc27f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2020
ms.locfileid: "44166125"
---
# <a name="automate-event-based-retention"></a><span data-ttu-id="88165-103">Rétention basée sur des événements</span><span class="sxs-lookup"><span data-stu-id="88165-103">Automate event-based retention</span></span>

><span data-ttu-id="88165-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="88165-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="88165-p101">L’explosion de contenu dans les organisations et comment il peut devenir assistées (redondantes, obsolètes, triviale) est une affaire sérieuse. Pour continuer à répondre aux exigences légales, commerciales et défis liés à la conformité des réglementations, les organisation doivent pouvoir conserver et protéger les informations importantes et trouver rapidement ce qui est pertinent. Conservant uniquement ce qui est important, les informations pertinentes sont la clé du succès d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="88165-p101">The explosion of content in organizations and how it can become ROT (redundant, obsolete, trivial) is serious business. To continue to meet legal, business, and regulatory compliance challenges, organizations must be able to keep and protect important information and quickly find what’s relevant. Retaining only important, pertinent information is key to an organization's success.</span></span>

<span data-ttu-id="88165-p102">Pour répondre à ce besoin, les organisations peuvent donc tirer parti des solutions de rétention dans le centre de conformité et sécurité Office 365. La rétention peut être déclenchée en utilisant les[étiquettes de rétention](labels.md). Une étiquette de rétention a la possibilité de [baser la période de rétention sur un événement spécifique](event-driven-retention.md). En règle générale, la période de rétention est basée sur une date connue, comme la date ou date de dernière modification pour le contenu création. Toutefois, les organisations ont également des exigences à dispose de contenu en fonction des occurrences d’un événement, par exemple 7 ans après qu’un employé quitte une organisation.</span><span class="sxs-lookup"><span data-stu-id="88165-p102">To help meet this need, organizations can take advantage of retention solutions in the Office 365 Security & Compliance Center. Retention can be triggered by using [retention labels](labels.md). A retention label has the option to [base the retention period on a specific event](event-driven-retention.md). Typically, the retention period is based on a known date, such as the creation date or last modified date for the content. However, organizations also have requirements to dispose of content based on the occurrence of an event, such as seven years after an employee leaves an organization.</span></span>

<span data-ttu-id="88165-p103">Pour s’assurer de la conformité de la destruction de contenu, il est impératif de savoir quand un événement a lieu. Le volume du contenu en augmentant rapidement, il devient difficile à conserver et dispose du contenu d’une manière opportune et la conformité.</span><span class="sxs-lookup"><span data-stu-id="88165-p103">To ensure compliant disposal of content, it's imperative to know when an event takes place. With the volume of content increasing rapidly, it's becoming challenging to retain and dispose content in a timely and compliant manner.</span></span>

<span data-ttu-id="88165-p104">La rétention basée sur un événement résoud ce problème. Cette rubrique explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88165-p104">Event-based retention solves this problem. This topic explains how to set up your business process flows to automate retention through events by using the Microsoft 365 REST API.</span></span>

## <a name="about-event-based-retention"></a><span data-ttu-id="88165-117">Rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="88165-117">About event-based retention</span></span>

<span data-ttu-id="88165-p105">Une organisation peut être grande petite ou moyenne. Le nombre de documents professionnels, documents juridiques, fichiers employé, contrats et documents produit qui sont créés et gérés sur une base quotidienne augmentent considérablement.</span><span class="sxs-lookup"><span data-stu-id="88165-p105">An organization can be small, medium, or large. The number of business documents, legal documents, employee files, contracts, and product documents that get created and managed on a day-to-day basis is increasing dramatically.</span></span>

<span data-ttu-id="88165-p106">Par exemple, chaque jour, dizaines et des centaines d’employés rejoignent et quittent organisations. Le service ressources humaines continue de créer, mettre à jour ou supprimer des documents liés à l’employé en respectant les exigences professionnelles. Ce processus est susceptible d’être les stratégies de rétention différentes décrites pour l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="88165-p106">For example, each day, tens and hundreds of employees are joining and leaving organizations. The HR department continues to create, update, or delete employee-related documents as per business requirements. This process is subject to the different retention policies outlined for the business:</span></span>

- <span data-ttu-id="88165-p107">**La période de rétention du contenu peut être une date connue** telles que la date que le contenu a été créé, la dernière modification ou étiqueté. Par exemple, vous pouvez conserver les documents pendant sept ans après que qu’ils aient été créés, puis les supprimer.</span><span class="sxs-lookup"><span data-stu-id="88165-p107">**The period of retention for content can be a known date** such as the date the content was created, last modified, or labeled. For example, you might retain documents for seven years after they're created and then delete them.</span></span>

- <span data-ttu-id="88165-p108">**La période de rétention du contenu peut également être une date inconnue**. Par exemple, avec des étiquettes de rétention, vous pouvez également baser une période de rétention sur lorsqu’un type spécifique d’événement se produit, par exemple un employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="88165-p108">**The period of retention of content can also be an unknown date**. For example, with retention labels, you can also base a retention period on when a specific type of event occurs, such as an employee leaving the organization.</span></span>

<span data-ttu-id="88165-p109">Le début de la période de rétention déclenche l’événement, et tout le contenu portant une étiquette pour ce type d’événement obtenez actions de rétention l’étiquette est appliquées dessus. Il s’agit rétention basée sur l’événement.-Pour plus d’informations, voir [vue d’ensemble de rétention basées sur les événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="88165-p109">The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them. This is called event-based retention. To learn more, see [Overview of event-driven retention](event-driven-retention.md).</span></span>

## <a name="set-up-event-based-retention"></a><span data-ttu-id="88165-130">Définir la rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="88165-130">Set up event-based retention</span></span>

<span data-ttu-id="88165-131">Cette section décrit les activités devant être effectuées avant la conservation du contenu.</span><span class="sxs-lookup"><span data-stu-id="88165-131">This section describes what needs to be done before retaining content.</span></span>

### <a name="identify-roles"></a><span data-ttu-id="88165-132">Identifier les rôles</span><span class="sxs-lookup"><span data-stu-id="88165-132">Identify roles</span></span>

<span data-ttu-id="88165-133">Identifier les différents rôles d’une organisation qui effectuent des tâches de gestion d’enregistrement et seraient responsables de la rétention efficace et de documents professionnels.</span><span class="sxs-lookup"><span data-stu-id="88165-133">Identify the different roles in an organization that perform Record Management tasks and would be responsible for effective and efficient retention of business documents.</span></span>

  | <span data-ttu-id="88165-134">**Persona**</span><span class="sxs-lookup"><span data-stu-id="88165-134">**Persona**</span></span>| <span data-ttu-id="88165-135">**Role**</span><span class="sxs-lookup"><span data-stu-id="88165-135">**Role**</span></span>|
  | - | - |
  | <span data-ttu-id="88165-136">Administrateur</span><span class="sxs-lookup"><span data-stu-id="88165-136">Admin</span></span> | <span data-ttu-id="88165-137">Crée des types d’Événement de Rétention, Étiquettes de Rétention et Référentiels d’Enregistrement dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="88165-137">Creates Retention Event types, Retention labels and Record repositories in SharePoint</span></span> |
  | <span data-ttu-id="88165-138">Gestionnaire d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="88165-138">Records Manager</span></span>                                  | <span data-ttu-id="88165-139">Fournit des détails de recommandations et de conformité stratégies de rétention et des plannings de rétention</span><span class="sxs-lookup"><span data-stu-id="88165-139">Provides Retention Policies and Retention Schedules guidance and compliance details</span></span>   |
  | <span data-ttu-id="88165-140">Administrateur système (entreprise)</span><span class="sxs-lookup"><span data-stu-id="88165-140">System Admin (business)</span></span>                          | <span data-ttu-id="88165-141">Configure et gère les systèmes externes pour fonctionner avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="88165-141">Sets up and manages external systems to work with Microsoft 365</span></span>                       |
  | <span data-ttu-id="88165-142">Travailleur de l'information</span><span class="sxs-lookup"><span data-stu-id="88165-142">Information Worker</span></span>                               | <span data-ttu-id="88165-143">Gère le cycle de vie de leur processus métier (RH, Finance, informatique, etc.)</span><span class="sxs-lookup"><span data-stu-id="88165-143">Manages the lifecycle of their business process (HR, Finance, IT, and so on)</span></span>                 |

### <a name="set-up-the-security--compliance-center"></a><span data-ttu-id="88165-144">Accéder au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="88165-144">Set up the Security & Compliance Center</span></span>
  
1. <span data-ttu-id="88165-145">L’administrateur de conformité crée un type d’événement &ndash; par exemple, la résiliation employé ou expiration de contrat ou fin de fabrication de produit.</span><span class="sxs-lookup"><span data-stu-id="88165-145">Compliance admin creates an event type &ndash; for example, Employee Termination or Contract Expiration or End of Product Manufacturing.</span></span> <span data-ttu-id="88165-146">(Voir le processus détaillé de[Rétentions basées sur des événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="88165-146">(See the step-by-step process in [Event-driven retention](event-driven-retention.md).</span></span>
    
2. <span data-ttu-id="88165-147">L’administrateur de conformité crée une étiquette en fonction d’un événement et l’associe à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="88165-147">Compliance admin creates a retention label based on an event and associates the label with an event type.</span></span>
    
    <span data-ttu-id="88165-148">Il existe quatre types de déclencheurs pour les étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="88165-148">There are four types of triggers for retention labels:</span></span>
            
    1. <span data-ttu-id="88165-149">Date de création</span><span class="sxs-lookup"><span data-stu-id="88165-149">Create date</span></span>
                
    2. <span data-ttu-id="88165-150">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="88165-150">Last modified</span></span>
                
    3. <span data-ttu-id="88165-151">Date étiquette (lorsque le contenu a été étiqueté)</span><span class="sxs-lookup"><span data-stu-id="88165-151">Label date (when the content was labeled)</span></span>
                
    4. <span data-ttu-id="88165-152">Basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="88165-152">Event-based</span></span>
    
3. <span data-ttu-id="88165-153">L’administrateur de conformité publie l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="88165-153">Compliance admin publishes the retention label.</span></span>

### <a name="set-up-sharepoint"></a><span data-ttu-id="88165-154">Configurer SharePoint</span><span class="sxs-lookup"><span data-stu-id="88165-154">Set up SharePoint</span></span>
   
<span data-ttu-id="88165-155">Pour créer un référentiel des enregistrements, l’administrateur de conformité :</span><span class="sxs-lookup"><span data-stu-id="88165-155">To create a records repository, the compliance admin:</span></span>

1. <span data-ttu-id="88165-156">Crée un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-156">Creates a SharePoint site.</span></span>

2. <span data-ttu-id="88165-157">Effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="88165-157">Does one of the following:</span></span>
        
    - <span data-ttu-id="88165-p111">Crée une bibliothèque SharePoint : définir l’étiquette en fonction des événement au niveau de la bibliothèque. Pour plus d’informations, voir [application d’une étiquette de rétention par défaut à tout le contenu dans une bibliothèque SharePoint, un dossier ou un ensemble de documents](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="88165-p111">Creates a SharePoint library: Set event-based label at the library level. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
          
    - <span data-ttu-id="88165-160">Configure un ensemble de documents dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-160">Sets up a document set in SharePoint.</span></span> <span data-ttu-id="88165-161">Pour plus d'informations, voir [Présentation des ensembles de documents](https://support.microsoft.com/fr-FR/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234).</span><span class="sxs-lookup"><span data-stu-id="88165-161">For more information, see [Introduction to document sets](https://support.microsoft.com/fr-FR/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234).</span></span>
      
3. <span data-ttu-id="88165-162">Affecte un ID d'élément à chaque ensemble de documents de l'employé.</span><span class="sxs-lookup"><span data-stu-id="88165-162">Assigns an asset ID to each employee document set.</span></span> <span data-ttu-id="88165-163">Un ID d’élément est un nom de produit ou un code utilisé par l’organisation, par exemple, le numéro d’employé peut être un ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="88165-163">An asset ID is a product name or code used by the organization, for example, Employee number can be an asset ID.</span></span> <span data-ttu-id="88165-164">En attribuant l’ID d’élément au dossier, tous les éléments de ce dossier héritent automatiquement du même ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="88165-164">By assigning the asset ID to the folder, every item in that folder automatically inherits the same asset ID.</span></span> <span data-ttu-id="88165-165">Cela signifie que la période de rétention de tous les éléments peut être déclenchée par le même événement.</span><span class="sxs-lookup"><span data-stu-id="88165-165">This means all the items can have their retention period triggered by the same event.</span></span>

## <a name="ways-to-trigger-event-based-retention"></a><span data-ttu-id="88165-166">Méthodes pour déclencher la lecture rétention basée sur l’événement</span><span class="sxs-lookup"><span data-stu-id="88165-166">Ways to trigger event-based retention</span></span>

<span data-ttu-id="88165-167">Il existe deux façons avec lesquelles la rétention basée sur l’événement peut être déclenchée :</span><span class="sxs-lookup"><span data-stu-id="88165-167">There are two ways in which event-based retention can be triggered:</span></span>

- <span data-ttu-id="88165-168">**Utilisation de l’interface utilisateur du centre d’administration** il s’agit d’un processus qui peut être utilisé pour conserver moins de contenu à la fois, ou la fréquence à laquelle le déclenchement de la rétention n’est pas fréquente (par exemple, mensuelle ou annuelle).</span><span class="sxs-lookup"><span data-stu-id="88165-168">**Using the admin center UI** This is a process that can be used to retain less content at a time or the frequency to trigger retention isn't often, such as monthly or yearly.</span></span> <span data-ttu-id="88165-169">Pour plus d'informations sur cette méthode, voir[Vue d’ensemble de la rétention basée sur un événement](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="88165-169">For more information about this method, see [Overview of event-driven retention](event-driven-retention.md).</span></span> <span data-ttu-id="88165-170">Toutefois, cette méthode de déclenchement de la rétention peut prendre du temps et être sujette à des erreurs, ce qui freine l'évolutivité.</span><span class="sxs-lookup"><span data-stu-id="88165-170">However, this method of triggering retention can be time consuming and prone to error, thus stunting scalability.</span></span> <span data-ttu-id="88165-171">Par conséquent, une solution automatisée et transparente de déclenchement de la rétention peut améliorer la sécurité et la conformité des données.</span><span class="sxs-lookup"><span data-stu-id="88165-171">Therefore, an automated, seamless solution to trigger retention can enhance data security and compliance.</span></span>

- <span data-ttu-id="88165-p115">**À l’aide d’une API REST M365** Ce processus peut être utilisé lorsque les grandes quantités de contenu sont conservées à un moment et/ou la fréquence de rétention déclencheur est récurrente telle que de manière quotidienne ou hebdomadaire. Le flux détecte quand un événement se produit dans votre système métier de, puis crée automatiquement un événement connexe dans le centre de sécurité et conformité. Vous n’avez pas besoin de créer manuellement un événement dans l’interface utilisateur chaque fois que ce qui se passer.</span><span class="sxs-lookup"><span data-stu-id="88165-p115">**Using a M365 REST API** This process can be used when large amounts of content are to be retained at a time and/or the frequency to trigger retention is often such as daily or weekly. The flow detects when an event occurs in your line-of-business system, and then automatically creates a related event in the Security & Compliance Center. You don't need to manually create an event in the UI each time one occurs.</span></span>

<span data-ttu-id="88165-175">Il existe deux options d’utilisation de l’API REST :</span><span class="sxs-lookup"><span data-stu-id="88165-175">There are two options for using the REST API:</span></span>

- <span data-ttu-id="88165-176">**Microsoft Flow ou une application similaire** peut être utilisée pour déclencher automatiquement l’occurrence d’un événement.</span><span class="sxs-lookup"><span data-stu-id="88165-176">**Microsoft Flow or a similar application** can be used to trigger the occurrence of an event automatically.</span></span> <span data-ttu-id="88165-177">Microsoft Flow est un Orchestrator pour la connexion à d’autres systèmes.</span><span class="sxs-lookup"><span data-stu-id="88165-177">Microsoft Flow is an orchestrator for connecting to other systems.</span></span> <span data-ttu-id="88165-178">L’utilisation de Microsoft Flow ne nécessite pas de solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="88165-178">Using Microsoft Flow doesn't require a custom solution.</span></span>

- <span data-ttu-id="88165-179">**PowerShell ou un HTTP client pour appeler des API REST** à l’aide de PowerShell (version 6 ou version ultérieure) pour appeler l’API REST Microsoft 365 pour créer des événements.</span><span class="sxs-lookup"><span data-stu-id="88165-179">**PowerShell or an HTTP client to call REST API** Using PowerShell (version 6 or higher) to call Microsoft 365 REST API to create events.</span></span> 

<span data-ttu-id="88165-180">Une API REST est un point de terminaison de service qui prend en charge les ensembles d’opérations HTTP (méthodes), qui fournissent l’accès de création, récupération/mise à jour/suppression aux ressources du service.</span><span class="sxs-lookup"><span data-stu-id="88165-180">A Rest API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources.</span></span> <span data-ttu-id="88165-181">Pour plus d’informations, voir [composants d’une demande/réponse API REST](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span><span class="sxs-lookup"><span data-stu-id="88165-181">For more information, see [Components of a REST API request/response](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span></span> <span data-ttu-id="88165-182">Dans ce cas, l’API REST de Microsoft 365 vous permet de créer et d’extraire des événements à l’aide d’opérations (méthodes) publier et récupérer.</span><span class="sxs-lookup"><span data-stu-id="88165-182">In this case, by using the Microsoft 365 REST API, events can be created and retrieved using operations (methods) POST and GET.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="88165-183">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="88165-183">Example scenarios</span></span>

<span data-ttu-id="88165-184">Envisagez les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="88165-184">Let’s consider the following scenarios.</span></span>

### <a name="scenario-1-employees-leaving-the-organization"></a><span data-ttu-id="88165-185">Scénario 1 : Employés quittant l’organisation</span><span class="sxs-lookup"><span data-stu-id="88165-185">Scenario 1: Employees leaving the organization</span></span> 

<span data-ttu-id="88165-186">Une organisation crée et stocke de nombreux documents liés à des employés par employé.</span><span class="sxs-lookup"><span data-stu-id="88165-186">An organization creates and stores numerous employee-related documents per employee.</span></span> <span data-ttu-id="88165-187">Ces documents sont gérés et conservés pendant l’embauche de chaque employé.</span><span class="sxs-lookup"><span data-stu-id="88165-187">These documents are managed and retained during the employment of each employee.</span></span> <span data-ttu-id="88165-188">Cependant, lorsque l’employé quitte l’organisation ou que l’emploi est résilié, l’organisation est obligée par les exigences légales et commerciales de conserver les documents de cet employé pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="88165-188">However, when the employee leaves the organization or the employment is terminated, the organization is obligated by legal and business requirements to retain the documents of that employee for a stipulated period.</span></span>

<span data-ttu-id="88165-189">Maintenant si plusieurs employés quittent l’organisation tous les jours, l’organisation doit déclencher la lecture l’horloge de rétention de centaines si ce n’est pas de milliers de documents chaque jour.</span><span class="sxs-lookup"><span data-stu-id="88165-189">Now if multiple employees leave the organization every day, the organization must trigger the retention clock of hundreds if not thousands of documents each day.</span></span>

<span data-ttu-id="88165-190">En plus de cela, la période de rétention doit être calculée pour chacun de ces employés comme date d’achèvement employé + nombre de jours, mois ou années en fonction du type de l’employé enregistrer.</span><span class="sxs-lookup"><span data-stu-id="88165-190">In addition to this, the retention period needs to be calculated for each of these employees as Employee termination date + number of days, months, or years based on the type of the employee record.</span></span> <span data-ttu-id="88165-191">Par exemple, la rémunération du collaborateur des employés et les déclarations d’avantages du même employé peuvent nécessiter une rétention différente.</span><span class="sxs-lookup"><span data-stu-id="88165-191">For example, worker’s compensation of the employee vs. benefits filings of the same employee may need different retention.</span></span>

<span data-ttu-id="88165-192">Le diagramme ci-dessous montre comment plusieurs étiquettes peuvent être associées à un seul événement.</span><span class="sxs-lookup"><span data-stu-id="88165-192">The diagram below shows how there can be multiple labels that are associated with a single event.</span></span> <span data-ttu-id="88165-193">Dans cet exemple, tous les fichiers figurant sous l’étiquette indemnités du collaborateur et tous les fichiers sous l’étiquette avantages sociaux des employés sont associés à un seul événement, qui est l’employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="88165-193">Here all the files under Worker’s compensation label and all the files under Employee benefits label are both associated with a single event, which is the employee leaving the organization.</span></span> <span data-ttu-id="88165-194">Chacun de ces fichiers a des horloges de rétention différentes.</span><span class="sxs-lookup"><span data-stu-id="88165-194">Each of these different files has different retention clocks.</span></span> <span data-ttu-id="88165-195">Par conséquent, lorsqu’un employé quitte l’organisation, ces fichiers au sein de chaque étiquette ont une période de rétention différente.</span><span class="sxs-lookup"><span data-stu-id="88165-195">So, when an employee leaves the organization, these files within each label experience a different retention period.</span></span> <span data-ttu-id="88165-196">Le déclenchement de toutes ces horloges de rétention pour chaque type de fichier ou étiquette pour chaque employé constitue une tâche complexe.</span><span class="sxs-lookup"><span data-stu-id="88165-196">Triggering all these different retention clocks for each file type or label for each employee is a very challenging task.</span></span> <span data-ttu-id="88165-197">Imaginez qu’il s’agit de plusieurs employés.</span><span class="sxs-lookup"><span data-stu-id="88165-197">Imagine doing this for multiple employees.</span></span>

![Diagramme illustrant le type d’événement, des événements et des étiquettes](../media/automate-event-driven-retention-event-diagram-employee-leaving.png)

<span data-ttu-id="88165-199">Un processus automatisé associé au déclenchement de ces différentes horloges de rétention pour plusieurs employés sera donc un gagne-temps, exempte d’erreur et très efficace.</span><span class="sxs-lookup"><span data-stu-id="88165-199">Hence an automated process to trigger these different retention clocks for multiple employees will be time-saving, error-free, and extremely efficient.</span></span>

<span data-ttu-id="88165-200">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="88165-200">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des actions pour le scénario d’employé quittant l’organisation](../media/automate-event-driven-retention-employee-termination-diagram.png)

  - <span data-ttu-id="88165-202">L’administrateur crée des dossiers d’employé lié au Document, telles Cartier Marie, John Smith.</span><span class="sxs-lookup"><span data-stu-id="88165-202">Admin creates employee folders to the Document set such as Jane Doe, John Smith.</span></span>

  - <span data-ttu-id="88165-203">L’administrateur ajoute des fichiers employé tels que les avantages, paie, rémunération de travailleur à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="88165-203">Admin adds employee files such as Benefits, Payroll, Worker’s Compensation to each employee folder.</span></span>

  - <span data-ttu-id="88165-204">L’administrateur affecte des ID d’élément à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="88165-204">Admin assigns Asset ID to each employee folder.</span></span> 

  - <span data-ttu-id="88165-205">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="88165-205">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="88165-206">L’administrateur SCC crée des types d’événements liés à l’employé tels que « Renvoi employé », « Embauche employé » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="88165-206">SCC Admin creates employee-related events types such as “Employee Termination”, “Employee Hire” events.</span></span>

  - <span data-ttu-id="88165-207">Administrateur SCC crée une étiquette « Employés ».</span><span class="sxs-lookup"><span data-stu-id="88165-207">SCC Admin creates “Employee Retention” label.</span></span>

  - <span data-ttu-id="88165-208">Cette étiquette « Employés » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-208">This “Employee Retention” label is published and applied manually or automatically to the employee files in SharePoint.</span></span>

  - <span data-ttu-id="88165-209">Le Système de Gestion des Ressources Humaines comme Workday peut fonctionner avec Microsoft Flow pour exécuter cette page régulièrement pour gérer les fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="88165-209">HR Management System like Workday can work with Microsoft Flow to run periodically to manage employee files.</span></span>

  - <span data-ttu-id="88165-210">Si un employé a quitté l’organisation, le flux déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="88165-210">If an employee has left the organization, the Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific employee’s files.</span></span>

#### <a name="using-microsoft-flow"></a><span data-ttu-id="88165-211">Utilisation Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="88165-211">Using Microsoft Flow</span></span>

<span data-ttu-id="88165-212">Étape 1-créer un flux de créer un événement en utilisant l’API REST Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="88165-212">Step 1- Create a flow to create an event using the Microsoft 365 REST API</span></span>

![Utilisation le flux pour créer un événement](../media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](../media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a><span data-ttu-id="88165-215">Créer un événement</span><span class="sxs-lookup"><span data-stu-id="88165-215">Create an event</span></span>

<span data-ttu-id="88165-216">Utilisation du code d’exemple pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="88165-216">Sample code to call the REST API</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88165-217">Méthode</span><span class="sxs-lookup"><span data-stu-id="88165-217">Method</span></span></th>
<th><span data-ttu-id="88165-218">POST</span><span class="sxs-lookup"><span data-stu-id="88165-218">POST</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88165-219">URL</span><span class="sxs-lookup"><span data-stu-id="88165-219">URL</span></span></td>
<td>https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent</td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-220">En-têtes</span><span class="sxs-lookup"><span data-stu-id="88165-220">Headers</span></span></td>
<td><span data-ttu-id="88165-221">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88165-221">Content-Type</span></span></td>
<td><span data-ttu-id="88165-222">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="88165-222">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88165-223">Corps</span><span class="sxs-lookup"><span data-stu-id="88165-223">Body</span></span></td>
<td><p><span data-ttu-id="88165-224">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-224">&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="88165-225">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="88165-225">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="88165-226">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="88165-226">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="88165-227">xmlns='https://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-227">xmlns='https://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="88165-228">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-228">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="88165-229">&lt;mise à jour&gt;9/9/2017 22:50:00&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-229">&lt;updated&gt;9/9/2017 10:50:00 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="88165-230">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-230">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="88165-231">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-231">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="88165-232">&lt;d:Name&gt;Licenciement employé&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-232">&lt;d:Name&gt;Employee Termination &lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="88165-233">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-233">&lt;d:EventType&gt;99e0ae64-a4b8-40bb-82ed-645895610f56&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="88165-234">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-234">&lt;d:SharePointAssetIdQuery&gt;1234&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="88165-235">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-235">&lt;d:EventDateTime&gt;2018-12-01T00:00:00Z &lt;/d:EventDateTime&gt;</span></span></p>
<p><span data-ttu-id="88165-236">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-236">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="88165-237">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-237">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="88165-238">&lt;/entrée&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-238">&lt;/entry&gt;</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-239">Authentification</span><span class="sxs-lookup"><span data-stu-id="88165-239">Authentication</span></span></td>
<td><span data-ttu-id="88165-240">De base</span><span class="sxs-lookup"><span data-stu-id="88165-240">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88165-241">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="88165-241">Username</span></span></td>
<td><span data-ttu-id="88165-242">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="88165-242">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-243">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="88165-243">Password</span></span></td>
<td><span data-ttu-id="88165-244">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="88165-244">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="available-parameters"></a><span data-ttu-id="88165-245">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="88165-245">Available parameters</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88165-246"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="88165-246"><strong>Parameters</strong></span></span></th>
<th><span data-ttu-id="88165-247"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="88165-247"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="88165-248"><strong>Notes</strong></span><span class="sxs-lookup"><span data-stu-id="88165-248"><strong>Notes</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88165-249">&lt;d:Name&gt;&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-249">&lt;d:Name&gt;&lt;/d:Name&gt;</span></span></td>
<td><span data-ttu-id="88165-250">Entrez un nom unique pour la base de données,</span><span class="sxs-lookup"><span data-stu-id="88165-250">Provide a unique name for the event,</span></span></td>
<td><span data-ttu-id="88165-p121">Un nom ne peut pas contenir les espaces et les caractères suivants : % \* \ &amp; &lt; &gt; | # ? , : ;</span><span class="sxs-lookup"><span data-stu-id="88165-p121">Cannot contain trailing spaces, and the following characters: % \* \ &amp; &lt; &gt; | # ? , : ;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-253">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-253">&lt;d:EventType&gt;&lt;/d:EventType&gt;</span></span></td>
<td><span data-ttu-id="88165-254">Entrez le nom de l’événement (ou Guid),</span><span class="sxs-lookup"><span data-stu-id="88165-254">Enter event type name (or Guid),</span></span></td>
<td><span data-ttu-id="88165-p122">Exemple : « employé licenciement anticipé ». Le type d’événement doit être associé à une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="88165-p122">Example: “Employee termination”. Event type has to be associated with a retention label.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88165-257">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-257">&lt;d:SharePointAssetIdQuery&gt;&lt;/d:SharePointAssetIdQuery&gt;</span></span></td>
<td><span data-ttu-id="88165-258">Entrez « ComplianceAssetId : « + Id d’employé</span><span class="sxs-lookup"><span data-stu-id="88165-258">Enter “ComplianceAssetId:” + employee Id</span></span></td>
<td><span data-ttu-id="88165-259">Exemple :&quot;ComplianceAssetId:12345&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-259">Example:&quot;ComplianceAssetId:12345&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-260">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-260">&lt;d:EventDateTime&gt;&lt;/d:EventDateTime&gt;</span></span></td>
<td><span data-ttu-id="88165-261">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="88165-261">Event Date and Time</span></span></td>
<td><p><span data-ttu-id="88165-262">Format : AAAA-MM-JJThh, exemple :</span><span class="sxs-lookup"><span data-stu-id="88165-262">Format: yyyy-MM-ddTHH:mm:ssZ, Example:</span></span></p>
<p><span data-ttu-id="88165-263">2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="88165-263">2018-12-01T00:00:00Z</span></span></p></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="88165-264">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="88165-264">Response codes</span></span>

| <span data-ttu-id="88165-265">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="88165-265">**Response Code**</span></span> | <span data-ttu-id="88165-266">**Description**</span><span class="sxs-lookup"><span data-stu-id="88165-266">**Description**</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="88165-267">302</span><span class="sxs-lookup"><span data-stu-id="88165-267">302</span></span>               | <span data-ttu-id="88165-268">Rediriger</span><span class="sxs-lookup"><span data-stu-id="88165-268">Redirect</span></span>              |
| <span data-ttu-id="88165-269">201</span><span class="sxs-lookup"><span data-stu-id="88165-269">201</span></span>               | <span data-ttu-id="88165-270">Créé</span><span class="sxs-lookup"><span data-stu-id="88165-270">Created</span></span>               |
| <span data-ttu-id="88165-271">403</span><span class="sxs-lookup"><span data-stu-id="88165-271">403</span></span>               | <span data-ttu-id="88165-272">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="88165-272">Authorization Failed</span></span>  |
| <span data-ttu-id="88165-273">401</span><span class="sxs-lookup"><span data-stu-id="88165-273">401</span></span>               | <span data-ttu-id="88165-274">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="88165-274">Authentication Failed</span></span> |

##### <a name="get-events-based-on-time-range"></a><span data-ttu-id="88165-275">Obtenir des événements en fonction de l’intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="88165-275">Get Events based on time range</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88165-276">Méthode</span><span class="sxs-lookup"><span data-stu-id="88165-276">Method</span></span></th>
<th><span data-ttu-id="88165-277">GET</span><span class="sxs-lookup"><span data-stu-id="88165-277">GET</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88165-278">URL</span><span class="sxs-lookup"><span data-stu-id="88165-278">URL</span></span></td>
<td><ol start="4" type="1">
<li><p><span data-ttu-id="88165-279">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span><span class="sxs-lookup"><span data-stu-id="88165-279">https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&amp;EndDateTime=2019-01-16</span></span></p></li>
</ol></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-280">En-têtes</span><span class="sxs-lookup"><span data-stu-id="88165-280">Headers</span></span></td>
<td><span data-ttu-id="88165-281">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88165-281">Content-Type</span></span></td>
<td><span data-ttu-id="88165-282">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="88165-282">application/atom+xml</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-283">Authentification</span><span class="sxs-lookup"><span data-stu-id="88165-283">Authentication</span></span></td>
<td><span data-ttu-id="88165-284">De base</span><span class="sxs-lookup"><span data-stu-id="88165-284">Basic</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88165-285">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="88165-285">Username</span></span></td>
<td><span data-ttu-id="88165-286">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="88165-286">“Complianceuser”</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88165-287">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="88165-287">Password</span></span></td>
<td><span data-ttu-id="88165-288">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="88165-288">“Compliancepassword”</span></span></td>
<td></td>
</tr>
</tbody>
</table>

##### <a name="response-codes"></a><span data-ttu-id="88165-289">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="88165-289">Response codes</span></span>

| <span data-ttu-id="88165-290">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="88165-290">**Response Code**</span></span> | <span data-ttu-id="88165-291">**Description**</span><span class="sxs-lookup"><span data-stu-id="88165-291">**Description**</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="88165-292">200</span><span class="sxs-lookup"><span data-stu-id="88165-292">200</span></span>               | <span data-ttu-id="88165-293">OK, une liste d’événements dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="88165-293">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="88165-294">404</span><span class="sxs-lookup"><span data-stu-id="88165-294">404</span></span>               | <span data-ttu-id="88165-295">Introuvable</span><span class="sxs-lookup"><span data-stu-id="88165-295">Not found</span></span>                         |
| <span data-ttu-id="88165-296">302</span><span class="sxs-lookup"><span data-stu-id="88165-296">302</span></span>               | <span data-ttu-id="88165-297">Rediriger</span><span class="sxs-lookup"><span data-stu-id="88165-297">Redirect</span></span>                          |
| <span data-ttu-id="88165-298">401</span><span class="sxs-lookup"><span data-stu-id="88165-298">401</span></span>               | <span data-ttu-id="88165-299">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="88165-299">Authorization Failed</span></span>              |
| <span data-ttu-id="88165-300">403</span><span class="sxs-lookup"><span data-stu-id="88165-300">403</span></span>               | <span data-ttu-id="88165-301">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="88165-301">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="88165-302">Obtenir un événement par ID</span><span class="sxs-lookup"><span data-stu-id="88165-302">Get an event by ID</span></span>

| <span data-ttu-id="88165-303">Méthode</span><span class="sxs-lookup"><span data-stu-id="88165-303">Method</span></span>         | <span data-ttu-id="88165-304">GET</span><span class="sxs-lookup"><span data-stu-id="88165-304">GET</span></span>   |                      |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------- |
| <span data-ttu-id="88165-305">URL</span><span class="sxs-lookup"><span data-stu-id="88165-305">URL</span></span>            | <span data-ttu-id="88165-306">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span><span class="sxs-lookup"><span data-stu-id="88165-306">[https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent(‘174e9a86-74ff-4450-8666-7c11f7730f66’)](https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent\('174e9a86-74ff-4450-8666-7c11f7730f66'\))</span></span> |                      |
| <span data-ttu-id="88165-307">En-tête</span><span class="sxs-lookup"><span data-stu-id="88165-307">Header</span></span>         | <span data-ttu-id="88165-308">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88165-308">Content-Type</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="88165-309">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="88165-309">application/atom+xml</span></span> |
| <span data-ttu-id="88165-310">Authentification</span><span class="sxs-lookup"><span data-stu-id="88165-310">Authentication</span></span> | <span data-ttu-id="88165-311">De base</span><span class="sxs-lookup"><span data-stu-id="88165-311">Basic</span></span>                                                                                                                                                                                                                                                              |                      |
| <span data-ttu-id="88165-312">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="88165-312">Username</span></span>       | <span data-ttu-id="88165-313">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="88165-313">“Complianceuser”</span></span>                                                                                                                                                                                                                                                   |                      |
| <span data-ttu-id="88165-314">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="88165-314">Password</span></span>       | <span data-ttu-id="88165-315">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="88165-315">“Compliancepassword”</span></span>                                                                                                                                                                                                                                               |                      |

##### <a name="response-codes"></a><span data-ttu-id="88165-316">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="88165-316">Response codes</span></span>

| <span data-ttu-id="88165-317">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="88165-317">**Response Code**</span></span> | <span data-ttu-id="88165-318">**Description**</span><span class="sxs-lookup"><span data-stu-id="88165-318">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="88165-319">200</span><span class="sxs-lookup"><span data-stu-id="88165-319">200</span></span>               | <span data-ttu-id="88165-320">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="88165-320">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="88165-321">404</span><span class="sxs-lookup"><span data-stu-id="88165-321">404</span></span>               | <span data-ttu-id="88165-322">Introuvable</span><span class="sxs-lookup"><span data-stu-id="88165-322">Not found</span></span>                                            |
| <span data-ttu-id="88165-323">302</span><span class="sxs-lookup"><span data-stu-id="88165-323">302</span></span>               | <span data-ttu-id="88165-324">Rediriger</span><span class="sxs-lookup"><span data-stu-id="88165-324">Redirect</span></span>                                             |
| <span data-ttu-id="88165-325">401</span><span class="sxs-lookup"><span data-stu-id="88165-325">401</span></span>               | <span data-ttu-id="88165-326">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="88165-326">Authorization Failed</span></span>                                 |
| <span data-ttu-id="88165-327">403</span><span class="sxs-lookup"><span data-stu-id="88165-327">403</span></span>               | <span data-ttu-id="88165-328">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="88165-328">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="88165-329">Obtenir un événement par le nom</span><span class="sxs-lookup"><span data-stu-id="88165-329">Get an event by name</span></span>

| <span data-ttu-id="88165-330">Méthode</span><span class="sxs-lookup"><span data-stu-id="88165-330">Method</span></span>         | <span data-ttu-id="88165-331">GET</span><span class="sxs-lookup"><span data-stu-id="88165-331">GET</span></span>       |                      |
| -------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| <span data-ttu-id="88165-332">URL</span><span class="sxs-lookup"><span data-stu-id="88165-332">URL</span></span>            | <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('EventByRESTPost-2226bfebcc2841a8968ba71f9516b763')> |                      |
| <span data-ttu-id="88165-333">En-têtes</span><span class="sxs-lookup"><span data-stu-id="88165-333">Headers</span></span>        | <span data-ttu-id="88165-334">Content-Type</span><span class="sxs-lookup"><span data-stu-id="88165-334">Content-Type</span></span>                                                                                                                                 | <span data-ttu-id="88165-335">application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="88165-335">application/atom+xml</span></span> |
| <span data-ttu-id="88165-336">Authentification</span><span class="sxs-lookup"><span data-stu-id="88165-336">Authentication</span></span> | <span data-ttu-id="88165-337">De base</span><span class="sxs-lookup"><span data-stu-id="88165-337">Basic</span></span>                                                                                                                                        |                      |
| <span data-ttu-id="88165-338">Nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="88165-338">Username</span></span>       | <span data-ttu-id="88165-339">« Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="88165-339">“Complianceuser”</span></span>                                                                                                                             |                      |
| <span data-ttu-id="88165-340">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="88165-340">Password</span></span>       | <span data-ttu-id="88165-341">« Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="88165-341">“Compliancepassword”</span></span>                                                                                                                         |                      |

##### <a name="response-codes"></a><span data-ttu-id="88165-342">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="88165-342">Response codes</span></span>

| <span data-ttu-id="88165-343">**Code de réponse**</span><span class="sxs-lookup"><span data-stu-id="88165-343">**Response Code**</span></span> | <span data-ttu-id="88165-344">**Description**</span><span class="sxs-lookup"><span data-stu-id="88165-344">**Description**</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="88165-345">200</span><span class="sxs-lookup"><span data-stu-id="88165-345">200</span></span>               | <span data-ttu-id="88165-346">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="88165-346">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="88165-347">404</span><span class="sxs-lookup"><span data-stu-id="88165-347">404</span></span>               | <span data-ttu-id="88165-348">Introuvable</span><span class="sxs-lookup"><span data-stu-id="88165-348">Not found</span></span>                                            |
| <span data-ttu-id="88165-349">302</span><span class="sxs-lookup"><span data-stu-id="88165-349">302</span></span>               | <span data-ttu-id="88165-350">Rediriger</span><span class="sxs-lookup"><span data-stu-id="88165-350">Redirect</span></span>                                             |
| <span data-ttu-id="88165-351">401</span><span class="sxs-lookup"><span data-stu-id="88165-351">401</span></span>               | <span data-ttu-id="88165-352">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="88165-352">Authorization Failed</span></span>                                 |
| <span data-ttu-id="88165-353">403</span><span class="sxs-lookup"><span data-stu-id="88165-353">403</span></span>               | <span data-ttu-id="88165-354">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="88165-354">Authentication Failed</span></span>                                |

#### <a name="using-powershell-ver6-or-higher-or-any-http-client"></a><span data-ttu-id="88165-355">L’aide de PowerShell (ver.6 ou une version ultérieure) ou n’importe quel client HTTP</span><span class="sxs-lookup"><span data-stu-id="88165-355">Using PowerShell (ver.6 or higher) or any HTTP client</span></span>

<span data-ttu-id="88165-356">Étape 1: Connectez-vous à PowerShell.</span><span class="sxs-lookup"><span data-stu-id="88165-356">Step 1: Connect to PowerShell.</span></span>

<span data-ttu-id="88165-357">Étape 2: Exécutez le script suivant.</span><span class="sxs-lookup"><span data-stu-id="88165-357">Step 2: Run the following script.</span></span>

<table>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88165-358">param([string]$baseUri)</span><span class="sxs-lookup"><span data-stu-id="88165-358">param([string]$baseUri)</span></span></p>
<p><span data-ttu-id="88165-359">$userName = &quot;Nomd’utilisateur&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-359">$userName = &quot;UserName&quot;</span></span></p>
<p><span data-ttu-id="88165-360">$password = &quot;Motdepasse&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-360">$password = &quot;Password&quot;</span></span></p>
<p><span data-ttu-id="88165-361">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span><span class="sxs-lookup"><span data-stu-id="88165-361">$securePassword = ConvertTo-SecureString $password -AsPlainText -Force</span></span></p>
<p><span data-ttu-id="88165-362">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span><span class="sxs-lookup"><span data-stu-id="88165-362">$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)</span></span></p>
<p><span data-ttu-id="88165-363">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-363">$EventName=&quot;EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))&quot;</span></span></p>
<p><span data-ttu-id="88165-364">Écriture hôte &quot;Commencez à créer un événement avec nom : $EventName&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-364">Write-Host &quot;Start to create an event with name: $EventName&quot;</span></span></p>
<p><span data-ttu-id="88165-365">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-365">$body = &quot;&lt;?xml version='1.0' encoding='utf-8' standalone='yes'?&gt;</span></span></p>
<p><span data-ttu-id="88165-366">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span><span class="sxs-lookup"><span data-stu-id="88165-366">&lt;entry xmlns:d='https://schemas.microsoft.com/ado/2007/08/dataservices'</span></span></p>
<p><span data-ttu-id="88165-367">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span><span class="sxs-lookup"><span data-stu-id="88165-367">xmlns:m='https://schemas.microsoft.com/ado/2007/08/dataservices/metadata'</span></span></p>
<p><span data-ttu-id="88165-368">xmlns='https://www.w3.org/2005/Atom'&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-368">xmlns='https://www.w3.org/2005/Atom'&gt;</span></span></p>
<p><span data-ttu-id="88165-369">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-369">&lt;category scheme='https://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' /&gt;</span></span></p>
<p><span data-ttu-id="88165-370">&lt;mise à jour&gt;14/7/2017 14:03:36&lt;/ mis à jour&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-370">&lt;updated&gt;7/14/2017 2:03:36 PM&lt;/updated&gt;</span></span></p>
<p><span data-ttu-id="88165-371">&lt;content type='application/xml'&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-371">&lt;content type='application/xml'&gt;</span></span></p>
<p><span data-ttu-id="88165-372">&lt;m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-372">&lt;m:properties&gt;</span></span></p>
<p><span data-ttu-id="88165-373">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-373">&lt;d:Name&gt;$EventName&lt;/d:Name&gt;</span></span></p>
<p><span data-ttu-id="88165-374">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-374">&lt;d:EventType&gt;e823b782-9a07-4e30-8091-034fc01f9347&lt;/d:EventType&gt;</span></span></p>
<p><span data-ttu-id="88165-375">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-375">&lt;d:SharePointAssetIdQuery&gt;'ComplianceAssetId:123'&lt;/d:SharePointAssetIdQuery&gt;</span></span></p>
<p><span data-ttu-id="88165-376">&lt;/m:properties&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-376">&lt;/m:properties&gt;</span></span></p>
<p><span data-ttu-id="88165-377">&lt;/contenu&gt;</span><span class="sxs-lookup"><span data-stu-id="88165-377">&lt;/content&gt;</span></span></p>
<p><span data-ttu-id="88165-378">&lt;/entrée&gt;&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-378">&lt;/entry&gt;&quot;</span></span></p>
<p><span data-ttu-id="88165-379">$event = $null</span><span class="sxs-lookup"><span data-stu-id="88165-379">$event = $null</span></span></p>
<p><span data-ttu-id="88165-380">Essayez</span><span class="sxs-lookup"><span data-stu-id="88165-380">try</span></span></p>
<p><span data-ttu-id="88165-381">{</span><span class="sxs-lookup"><span data-stu-id="88165-381">{</span></span></p>
<p><span data-ttu-id="88165-382">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Uri &quot;$baseUri/ComplianceRetentionEvent&quot;- ContentType &quot;application/atom + xml&quot;-l’authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="88165-382">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri &quot;$baseUri/ComplianceRetentionEvent&quot; -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="88165-383">}</span><span class="sxs-lookup"><span data-stu-id="88165-383">}</span></span></p>
<p><span data-ttu-id="88165-384">catch</span><span class="sxs-lookup"><span data-stu-id="88165-384">catch</span></span></p>
<p><span data-ttu-id="88165-385">{</span><span class="sxs-lookup"><span data-stu-id="88165-385">{</span></span></p>
<p><span data-ttu-id="88165-386">$response = $_.Exception.Response</span><span class="sxs-lookup"><span data-stu-id="88165-386">$response = $_.Exception.Response</span></span></p>
<p><span data-ttu-id="88165-387">if($response.StatusCode -eq &quot;Redirect&quot;)</span><span class="sxs-lookup"><span data-stu-id="88165-387">if($response.StatusCode -eq &quot;Redirect&quot;)</span></span></p>
<p><span data-ttu-id="88165-388">{</span><span class="sxs-lookup"><span data-stu-id="88165-388">{</span></span></p>
<p><span data-ttu-id="88165-389">$url = $response.Headers.Location</span><span class="sxs-lookup"><span data-stu-id="88165-389">$url = $response.Headers.Location</span></span></p>
<p><span data-ttu-id="88165-390">Écriture hôte &quot;redirigés vers $url&quot;</span><span class="sxs-lookup"><span data-stu-id="88165-390">Write-Host &quot;redirected to $url&quot;</span></span></p>
<p><span data-ttu-id="88165-391">$event = RestMethod Invoke-corps de texte $body-méthode 'POST'-Url -ContentType &quot;application/atom + xml&quot; -l’Authentification de base-Credential $credentials -MaximumRedirection 0</span><span class="sxs-lookup"><span data-stu-id="88165-391">$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType &quot;application/atom+xml&quot; -Authentication Basic -Credential $credentials -MaximumRedirection 0</span></span></p>
<p><span data-ttu-id="88165-392">}</span><span class="sxs-lookup"><span data-stu-id="88165-392">}</span></span></p>
<p><span data-ttu-id="88165-393">}</span><span class="sxs-lookup"><span data-stu-id="88165-393">}</span></span></p>
<p><span data-ttu-id="88165-394">$event | fl \*</span><span class="sxs-lookup"><span data-stu-id="88165-394">$event | fl \*</span></span></p></td>
</tr>
</tbody>
</table>

#### <a name="verify-the-outcome-in-both-options"></a><span data-ttu-id="88165-395">Vérifier le résultat dans les deux options</span><span class="sxs-lookup"><span data-stu-id="88165-395">Verify the outcome in both options</span></span>

<span data-ttu-id="88165-396">Étape 1 : Accéder au centre de conformité et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="88165-396">Step 1: Go to the Security & Compliance Center.</span></span>

<span data-ttu-id="88165-397">Étape 2 : Sélectionner **Évènements** sous **Gouvernance des informations**.</span><span class="sxs-lookup"><span data-stu-id="88165-397">Step 2: Select **Events** under **Information governance**.</span></span>

<span data-ttu-id="88165-398">Étape 3 : Vérifier l’Événement a été créé.</span><span class="sxs-lookup"><span data-stu-id="88165-398">Step 3: Verify Event has been created.</span></span>

<span data-ttu-id="88165-399">De même, les options ci-dessus pour automatiser la rétention basée sur des événements peuvent être également utilisées pour les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="88165-399">Similarly, the above options to automate event-based retention can be used for the following scenarios as well.</span></span>

### <a name="scenario-2-contracts-expiring"></a><span data-ttu-id="88165-400">Scénario 2 : Contrats expiration</span><span class="sxs-lookup"><span data-stu-id="88165-400">Scenario 2: Contracts Expiring</span></span>

<span data-ttu-id="88165-401">Une organisation peut avoir plusieurs enregistrements pour un seul contrat avec des clients, des fournisseurs et des partenaires.</span><span class="sxs-lookup"><span data-stu-id="88165-401">An organization can have multiple records for a single contract with customers, vendors, and partners.</span></span> <span data-ttu-id="88165-402">Ces documents peuvent résider dans une bibliothèque de documents telle que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-402">These documents can reside in a document library like SharePoint.</span></span> <span data-ttu-id="88165-403">La fin d’un contrat détermine le début de la période de rétention des documents associés au contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-403">The end of a contract determines the start of the retention period of the documents associated with the contract.</span></span> <span data-ttu-id="88165-404">Par exemple, tous les documents relatifs aux contrats doivent être conservés pendant cinq ans après l'expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-404">For example, all records related to contracts need to be retained for five years from the time the contract expires.</span></span> <span data-ttu-id="88165-405">L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-405">The event that triggers the five-year retention period is the expiration of the contract.</span></span>

<span data-ttu-id="88165-406">Un système de gestion de relation client (CRM) pouvez travailler avec Microsoft 365 et la rétention de déclencheur de documents de contrat</span><span class="sxs-lookup"><span data-stu-id="88165-406">A Customer Relationship Management (CRM) system can work with Microsoft 365 and trigger retention of Contract documents</span></span>

<span data-ttu-id="88165-407">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="88165-407">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario d’expiration contrat](../media/automate-event-driven-retention-contract-expiration.png)

  - <span data-ttu-id="88165-409">L’administrateur crée une bibliothèque SharePoint avec les différents dossiers pour chaque type de contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-409">Admin creates a SharePoint library with various folders for each contract type.</span></span>

  - <span data-ttu-id="88165-410">L’administrateur ajoute des fichiers de contrat tels que des contrats de licence, les contrats de développement pour chaque dossier contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-410">Admin adds contract files such as License Contracts, Development Contracts to each contract folder.</span></span>

  - <span data-ttu-id="88165-411">L’administrateur affecte des ID délément à chaque dossier de contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-411">Admin assigns Asset ID to each contract folder.</span></span>

  - <span data-ttu-id="88165-412">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="88165-412">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="88165-413">L’administrateur SCC crée un contrat lié aux types événements tels que « Création de contrat, » , « Expiration de contrat » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="88165-413">SCC Admin creates contract-related events types such as “Contract Creation”, “Contract Expiration” events.</span></span>

  - <span data-ttu-id="88165-414">Administrateur SCC crée une étiquette « Expiration de contrat ».</span><span class="sxs-lookup"><span data-stu-id="88165-414">SCC Admin creates “Contract Expiration” label.</span></span>

  - <span data-ttu-id="88165-415">Cette étiquette « Expiration du Contrat » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-415">This “ Contract Expiration” label is published and applied manually or automatically to the contract files in SharePoint.</span></span>

  - <span data-ttu-id="88165-416">Le Système de Gestion de Contrat peut fonctionner avec Microsoft Flow ou une application similaire pour exécuter cette page régulièrement pour gérer les fichiers de contrat.</span><span class="sxs-lookup"><span data-stu-id="88165-416">Contract Management System can work with Microsoft Flow or a similar application to run periodically to manage contract files.</span></span>

  - <span data-ttu-id="88165-417">Si un employé a quitté l’organisation, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="88165-417">If a contract expires, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific contract’s files.</span></span>

### <a name="scenario-3-end-of-product-manufacturing"></a><span data-ttu-id="88165-418">Scénario 3 : Fin de la fabrication de produit</span><span class="sxs-lookup"><span data-stu-id="88165-418">Scenario 3: End of Product Manufacturing</span></span>

<span data-ttu-id="88165-p124">Une entreprise de fabrication produisant différentes lignes de produits crée plusieurs caractéristiques de fabrication et les prix de documents. Lorsque le produit n’est plus fabriqué, toutes les spécifications et documents liée à ce besoin produit sont conservés pendant une période spécifique suivant la fin de la durée de vie du produit.</span><span class="sxs-lookup"><span data-stu-id="88165-p124">A manufacturing company that produces different lines of products creates many manufacturing specifications and pricing documents. When the product is no longer manufactured, all specifications and documents linked to this product need to be retained for a specific period after the end of the lifetime of the product.</span></span>

<span data-ttu-id="88165-421">Un système de planification (ERP) peut fonctionner avec Microsoft 365 et Microsoft Flow pour la rétention de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="88165-421">An Enterprise Resource Planning (ERP) system can work with Microsoft 365 and Microsoft Flow to trigger retention.</span></span>

<span data-ttu-id="88165-422">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="88165-422">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario de cycle de vie de produit](../media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - <span data-ttu-id="88165-424">L’administrateur crée des dossiers du produit dans l’ensemble de Documents tel que produit 1, produit 2, etc.</span><span class="sxs-lookup"><span data-stu-id="88165-424">Admin creates product folders in the Document set such as Product 1, Product 2, and so on.</span></span>

  - <span data-ttu-id="88165-425">L’administrateur ajoute des fichiers produit tels que les spécifications de fabrication, produit sur les tarifs, les licences produit pour chaque dossier du produit.</span><span class="sxs-lookup"><span data-stu-id="88165-425">Admin adds product files such as Manufacturing Specifications, Product Pricing, Product licensing to each product folder.</span></span>

  - <span data-ttu-id="88165-426">L’administrateur affecte des ID d’élément à chaque dossier produit.</span><span class="sxs-lookup"><span data-stu-id="88165-426">Admin assigns Asset ID to each product folder.</span></span>

  - <span data-ttu-id="88165-427">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="88165-427">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="88165-428">L’administrateur SCC crée des types d’événement liés à l’employé tels que « Commencer la fabrication de produit », « Fin de fabrication de produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="88165-428">SCC Admin creates employee-related events types such as “Start of Product Manufacturing”, “End of Product Manufacturing” events.</span></span>

  - <span data-ttu-id="88165-429">L’administrateur SCC crée l’étiquette « Fin de la Fabrication du Produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="88165-429">SCC Admin creates “End of Product Manufacturing” label.</span></span>

  - <span data-ttu-id="88165-430">Cette étiquette «Fin de la Fabrication du Produit» est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="88165-430">This “ End of Product Manufacturing” label is published and applied manually or automatically to the product files in SharePoint.</span></span>

  - <span data-ttu-id="88165-431">Le Système de Gestion de Contrat ERP peut fonctionner avec Microsoft Flow ou des applications similaires pour s’exécuter régulièrement pour gérer les fichiers de produit.</span><span class="sxs-lookup"><span data-stu-id="88165-431">ERP Systems can work with Microsoft Flow or similar applications to run periodically to manage product files.</span></span>

  - <span data-ttu-id="88165-432">Si la fabrication d’un produit se termine, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de produit spécifiques.</span><span class="sxs-lookup"><span data-stu-id="88165-432">If the manufacturing of a product ends, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific product’s files.</span></span>

## <a name="appendix"></a><span data-ttu-id="88165-433">Annexe</span><span class="sxs-lookup"><span data-stu-id="88165-433">Appendix</span></span>

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a><span data-ttu-id="88165-434">Utiliser les résultats de réponses 302 de redirection pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="88165-434">Using Redirect 302 response results to call the REST API</span></span>

1. <span data-ttu-id="88165-435">Appeler un appel d’événement de rétention POST à l’aide de l’URL API REST <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (les autorisations d’administrateur général sont obligatoires)</span><span class="sxs-lookup"><span data-stu-id="88165-435">Invoke a POST retention event call using the REST API URL <https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent> (Global Admin permissions are required)</span></span>

2. <span data-ttu-id="88165-p125">Vérifiez le code de réponse. S’il s’agit 302, puis obtenez l’URL redirigé de propriété de l’emplacement de l’en-tête de réponse</span><span class="sxs-lookup"><span data-stu-id="88165-p125">Check the response code. If it’s 302, then get the redirected URL from Location property of the response header</span></span>

3. <span data-ttu-id="88165-438">Appeler l’appel d’événement rétention POST à l’aide d’URL redirigé.</span><span class="sxs-lookup"><span data-stu-id="88165-438">Invoke the POST retention event call again using the redirected URL.</span></span>

## <a name="credits"></a><span data-ttu-id="88165-439">Crédits</span><span class="sxs-lookup"><span data-stu-id="88165-439">Credits</span></span>

<span data-ttu-id="88165-440">Cette rubrique a été révisée par :</span><span class="sxs-lookup"><span data-stu-id="88165-440">This topic was reviewed by:</span></span>

<span data-ttu-id="88165-441">Antonio Maio</span><span class="sxs-lookup"><span data-stu-id="88165-441">Antonio Maio</span></span><br/><span data-ttu-id="88165-442">MVP Services et applications Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="88165-442">Microsoft Office Apps and Services MVP</span></span><br/> <span data-ttu-id="88165-443">Antonio.Maio@Protiviti.com</span><span class="sxs-lookup"><span data-stu-id="88165-443">Antonio.Maio@Protiviti.com</span></span>
