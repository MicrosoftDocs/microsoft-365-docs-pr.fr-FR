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
ms.openlocfilehash: aeb0b05b2bf9b62dbeff43370edf6902e577a0d7
ms.sourcegitcommit: e8b9a4f18330bc09f665aa941f1286436057eb28
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/14/2020
ms.locfileid: "45126397"
---
# <a name="automate-event-based-retention"></a><span data-ttu-id="02567-103">Rétention basée sur des événements</span><span class="sxs-lookup"><span data-stu-id="02567-103">Automate event-based retention</span></span>

><span data-ttu-id="02567-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="02567-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="02567-p101">L’explosion de contenu dans les organisations et comment il peut devenir assistées (redondantes, obsolètes, triviale) est une affaire sérieuse. Pour continuer à répondre aux exigences légales, commerciales et défis liés à la conformité des réglementations, les organisation doivent pouvoir conserver et protéger les informations importantes et trouver rapidement ce qui est pertinent. Conservant uniquement ce qui est important, les informations pertinentes sont la clé du succès d’une organisation.</span><span class="sxs-lookup"><span data-stu-id="02567-p101">The explosion of content in organizations and how it can become ROT (redundant, obsolete, trivial) is serious business. To continue to meet legal, business, and regulatory compliance challenges, organizations must be able to keep and protect important information and quickly find what’s relevant. Retaining only important, pertinent information is key to an organization's success.</span></span>

<span data-ttu-id="02567-p102">Pour répondre à ce besoin, les organisations peuvent donc tirer parti des solutions de rétention dans le centre de conformité et sécurité Office 365. La rétention peut être déclenchée en utilisant les[étiquettes de rétention](retention.md#retention-labels). Une étiquette de rétention a la possibilité de [baser la période de rétention sur un événement spécifique](event-driven-retention.md). En règle générale, la période de rétention est basée sur une date connue, comme la date ou date de dernière modification pour le contenu création. Toutefois, les organisations ont également des exigences à dispose de contenu en fonction des occurrences d’un événement, par exemple 7 ans après qu’un employé quitte une organisation.</span><span class="sxs-lookup"><span data-stu-id="02567-p102">To help meet this need, organizations can take advantage of retention solutions in the Office 365 Security & Compliance Center. Retention can be triggered by using [retention labels](retention.md#retention-labels). A retention label has the option to [base the retention period on a specific event](event-driven-retention.md). Typically, the retention period is based on a known date, such as the creation date or last modified date for the content. However, organizations also have requirements to dispose of content based on the occurrence of an event, such as seven years after an employee leaves an organization.</span></span>

<span data-ttu-id="02567-p103">Pour s’assurer de la conformité de la destruction de contenu, il est impératif de savoir quand un événement a lieu. Le volume du contenu en augmentant rapidement, il devient difficile à conserver et dispose du contenu d’une manière opportune et la conformité.</span><span class="sxs-lookup"><span data-stu-id="02567-p103">To ensure compliant disposal of content, it's imperative to know when an event takes place. With the volume of content increasing rapidly, it's becoming challenging to retain and dispose content in a timely and compliant manner.</span></span>

<span data-ttu-id="02567-p104">La rétention basée sur un événement résoud ce problème. Cet article explique comment configurer votre flux de processus métier pour automatiser la rétention via des événements à l’aide de l’API REST de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="02567-p104">Event-based retention solves this problem. This article explains how to set up your business process flows to automate retention through events by using the Microsoft 365 REST API.</span></span>

## <a name="about-event-based-retention"></a><span data-ttu-id="02567-117">Rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="02567-117">About event-based retention</span></span>

<span data-ttu-id="02567-p105">Une organisation peut être grande petite ou moyenne. Le nombre de documents professionnels, documents juridiques, fichiers employé, contrats et documents produit qui sont créés et gérés sur une base quotidienne augmentent considérablement.</span><span class="sxs-lookup"><span data-stu-id="02567-p105">An organization can be small, medium, or large. The number of business documents, legal documents, employee files, contracts, and product documents that get created and managed on a day-to-day basis is increasing dramatically.</span></span>

<span data-ttu-id="02567-p106">Par exemple, chaque jour, dizaines et des centaines d’employés rejoignent et quittent organisations. Le service ressources humaines continue de créer, mettre à jour ou supprimer des documents liés à l’employé en respectant les exigences professionnelles. Ce processus est susceptible d’être les stratégies de rétention différentes décrites pour l’entreprise :</span><span class="sxs-lookup"><span data-stu-id="02567-p106">For example, each day, tens and hundreds of employees are joining and leaving organizations. The HR department continues to create, update, or delete employee-related documents as per business requirements. This process is subject to the different retention policies outlined for the business:</span></span>

- <span data-ttu-id="02567-p107">**La période de rétention du contenu peut être une date connue** telles que la date que le contenu a été créé, la dernière modification ou étiqueté. Par exemple, vous pouvez conserver les documents pendant sept ans après que qu’ils aient été créés, puis les supprimer.</span><span class="sxs-lookup"><span data-stu-id="02567-p107">**The period of retention for content can be a known date** such as the date the content was created, last modified, or labeled. For example, you might retain documents for seven years after they're created and then delete them.</span></span>

- <span data-ttu-id="02567-p108">**La période de rétention du contenu peut également être une date inconnue**. Par exemple, avec des étiquettes de rétention, vous pouvez également baser une période de rétention sur lorsqu’un type spécifique d’événement se produit, par exemple un employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="02567-p108">**The period of retention of content can also be an unknown date**. For example, with retention labels, you can also base a retention period on when a specific type of event occurs, such as an employee leaving the organization.</span></span>

<span data-ttu-id="02567-p109">L’événement déclenche le début de la période de rétention, et tout le contenu portant une étiquette pour ce type d’événement se voit appliqué les actions de l’étiquette de rétention. Il s’agit de rétention basée sur l’événement. Pour en savoir plus, consultez [Débuter la rétention lorsqu’un événement se produit](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="02567-p109">The event triggers the start of the retention period, and all content with a label applied for that type of event get the label's retention actions enforced on them. This is called event-based retention. To learn more, see [Start retention when an event occurs](event-driven-retention.md).</span></span>

## <a name="set-up-event-based-retention"></a><span data-ttu-id="02567-130">Définir la rétentions basées sur des événements</span><span class="sxs-lookup"><span data-stu-id="02567-130">Set up event-based retention</span></span>

<span data-ttu-id="02567-131">Cette section décrit les activités devant être effectuées avant la conservation du contenu.</span><span class="sxs-lookup"><span data-stu-id="02567-131">This section describes what needs to be done before retaining content.</span></span>

### <a name="identify-roles"></a><span data-ttu-id="02567-132">Identifier les rôles</span><span class="sxs-lookup"><span data-stu-id="02567-132">Identify roles</span></span>

<span data-ttu-id="02567-133">Identifier les différents rôles d’une organisation qui effectuent des tâches de gestion d’enregistrement et seraient responsables de la rétention efficace et de documents professionnels.</span><span class="sxs-lookup"><span data-stu-id="02567-133">Identify the different roles in an organization that perform Record Management tasks and would be responsible for effective and efficient retention of business documents.</span></span>

  | <span data-ttu-id="02567-134">Persona</span><span class="sxs-lookup"><span data-stu-id="02567-134">Persona</span></span> | <span data-ttu-id="02567-135">Role</span><span class="sxs-lookup"><span data-stu-id="02567-135">Role</span></span> |
  | - | - |
  | <span data-ttu-id="02567-136">Administrateur</span><span class="sxs-lookup"><span data-stu-id="02567-136">Admin</span></span> | <span data-ttu-id="02567-137">Crée des types d’Événement de Rétention, Étiquettes de Rétention et Référentiels d’Enregistrement dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="02567-137">Creates Retention Event types, Retention labels and Record repositories in SharePoint</span></span> |
  | <span data-ttu-id="02567-138">Gestionnaire d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="02567-138">Records Manager</span></span>                                  | <span data-ttu-id="02567-139">Fournit des détails de recommandations et de conformité stratégies de rétention et des plannings de rétention</span><span class="sxs-lookup"><span data-stu-id="02567-139">Provides Retention Policies and Retention Schedules guidance and compliance details</span></span>   |
  | <span data-ttu-id="02567-140">Administrateur système (entreprise)</span><span class="sxs-lookup"><span data-stu-id="02567-140">System Admin (business)</span></span>                          | <span data-ttu-id="02567-141">Configure et gère les systèmes externes pour fonctionner avec Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02567-141">Sets up and manages external systems to work with Microsoft 365</span></span>                       |
  | <span data-ttu-id="02567-142">Travailleur de l'information</span><span class="sxs-lookup"><span data-stu-id="02567-142">Information Worker</span></span>                               | <span data-ttu-id="02567-143">Gère le cycle de vie de leur processus métier (RH, Finance, informatique, etc.)</span><span class="sxs-lookup"><span data-stu-id="02567-143">Manages the lifecycle of their business process (HR, Finance, IT, and so on)</span></span>                 |

### <a name="set-up-the-security--compliance-center"></a><span data-ttu-id="02567-144">Accéder au Centre de Conformité et de Sécurité</span><span class="sxs-lookup"><span data-stu-id="02567-144">Set up the Security & Compliance Center</span></span>
  
1. <span data-ttu-id="02567-145">L’administrateur de conformité crée un type d’événement &ndash; par exemple, la résiliation employé ou expiration de contrat ou fin de fabrication de produit.</span><span class="sxs-lookup"><span data-stu-id="02567-145">Compliance admin creates an event type &ndash; for example, Employee Termination or Contract Expiration or End of Product Manufacturing.</span></span> <span data-ttu-id="02567-146">(Voir le processus détaillé de[Rétentions basées sur des événements](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="02567-146">(See the step-by-step process in [Event-driven retention](event-driven-retention.md).</span></span>
    
2. <span data-ttu-id="02567-147">L’administrateur de conformité crée une étiquette en fonction d’un événement et l’associe à un type d’événement.</span><span class="sxs-lookup"><span data-stu-id="02567-147">Compliance admin creates a retention label based on an event and associates the label with an event type.</span></span>
    
    <span data-ttu-id="02567-148">Il existe quatre types de déclencheurs pour les étiquettes de rétention :</span><span class="sxs-lookup"><span data-stu-id="02567-148">There are four types of triggers for retention labels:</span></span>
            
    1. <span data-ttu-id="02567-149">Date de création</span><span class="sxs-lookup"><span data-stu-id="02567-149">Create date</span></span>
                
    2. <span data-ttu-id="02567-150">Dernière modification</span><span class="sxs-lookup"><span data-stu-id="02567-150">Last modified</span></span>
                
    3. <span data-ttu-id="02567-151">Date étiquette (lorsque le contenu a été étiqueté)</span><span class="sxs-lookup"><span data-stu-id="02567-151">Label date (when the content was labeled)</span></span>
                
    4. <span data-ttu-id="02567-152">Basé sur des événements</span><span class="sxs-lookup"><span data-stu-id="02567-152">Event-based</span></span>
    
3. <span data-ttu-id="02567-153">L’administrateur de conformité publie l’étiquette.</span><span class="sxs-lookup"><span data-stu-id="02567-153">Compliance admin publishes the retention label.</span></span>

### <a name="set-up-sharepoint"></a><span data-ttu-id="02567-154">Configurer SharePoint</span><span class="sxs-lookup"><span data-stu-id="02567-154">Set up SharePoint</span></span>
   
<span data-ttu-id="02567-155">Pour créer un référentiel des enregistrements, l’administrateur de conformité :</span><span class="sxs-lookup"><span data-stu-id="02567-155">To create a records repository, the compliance admin:</span></span>

1. <span data-ttu-id="02567-156">Crée un site SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-156">Creates a SharePoint site.</span></span>

2. <span data-ttu-id="02567-157">Effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="02567-157">Does one of the following:</span></span>
        
    - <span data-ttu-id="02567-p111">Crée une bibliothèque SharePoint : définir l’étiquette en fonction des événement au niveau de la bibliothèque. Pour plus d’informations, voir [application d’une étiquette de rétention par défaut à tout le contenu dans une bibliothèque SharePoint, un dossier ou un ensemble de documents](create-apply-retention-labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="02567-p111">Creates a SharePoint library: Set event-based label at the library level. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](create-apply-retention-labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>

   - <span data-ttu-id="02567-160">Configure un ensemble de documents dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-160">Sets up a document set in SharePoint.</span></span> <span data-ttu-id="02567-161">Pour plus d'informations, voir [Présentation des ensembles de documents](https://support.microsoft.com/fr-FR/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234).</span><span class="sxs-lookup"><span data-stu-id="02567-161">For more information, see [Introduction to document sets](https://support.microsoft.com/fr-FR/office/introduction-to-document-sets-3dbcd93e-0bed-46b7-b1ba-b31de2bcd234).</span></span>
      
3. <span data-ttu-id="02567-162">Affecte un ID d'élément à chaque ensemble de documents de l'employé.</span><span class="sxs-lookup"><span data-stu-id="02567-162">Assigns an asset ID to each employee document set.</span></span> <span data-ttu-id="02567-163">Un ID d’élément est un nom de produit ou un code utilisé par l’organisation, par exemple, le numéro d’employé peut être un ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="02567-163">An asset ID is a product name or code used by the organization, for example, Employee number can be an asset ID.</span></span> <span data-ttu-id="02567-164">En attribuant l’ID d’élément au dossier, tous les éléments de ce dossier héritent automatiquement du même ID d’élément.</span><span class="sxs-lookup"><span data-stu-id="02567-164">By assigning the asset ID to the folder, every item in that folder automatically inherits the same asset ID.</span></span> <span data-ttu-id="02567-165">Cela signifie que la période de rétention de tous les éléments peut être déclenchée par le même événement.</span><span class="sxs-lookup"><span data-stu-id="02567-165">This means all the items can have their retention period triggered by the same event.</span></span>

## <a name="ways-to-trigger-event-based-retention"></a><span data-ttu-id="02567-166">Méthodes pour déclencher la lecture rétention basée sur l’événement</span><span class="sxs-lookup"><span data-stu-id="02567-166">Ways to trigger event-based retention</span></span>

<span data-ttu-id="02567-167">Il existe deux façons avec lesquelles la rétention basée sur l’événement peut être déclenchée :</span><span class="sxs-lookup"><span data-stu-id="02567-167">There are two ways in which event-based retention can be triggered:</span></span>

- <span data-ttu-id="02567-168">**Utilisation de l’interface utilisateur du centre d’administration** il s’agit d’un processus qui peut être utilisé pour conserver moins de contenu à la fois, ou la fréquence à laquelle le déclenchement de la rétention n’est pas fréquente (par exemple, mensuelle ou annuelle).</span><span class="sxs-lookup"><span data-stu-id="02567-168">**Using the admin center UI** This is a process that can be used to retain less content at a time or the frequency to trigger retention isn't often, such as monthly or yearly.</span></span> <span data-ttu-id="02567-169">Pour plus d’informations sur cette méthode, consultez [Débuter la rétention lorsqu’un événement se produit](event-driven-retention.md).</span><span class="sxs-lookup"><span data-stu-id="02567-169">For more information about this method, see [Start retention when an event occurs](event-driven-retention.md).</span></span> <span data-ttu-id="02567-170">Toutefois, cette méthode de déclenchement de la rétention peut prendre du temps et être sujette à des erreurs, ce qui freine l'évolutivité.</span><span class="sxs-lookup"><span data-stu-id="02567-170">However, this method of triggering retention can be time consuming and prone to error, thus stunting scalability.</span></span> <span data-ttu-id="02567-171">Par conséquent, une solution automatisée et transparente de déclenchement de la rétention peut améliorer la sécurité et la conformité des données.</span><span class="sxs-lookup"><span data-stu-id="02567-171">Therefore, an automated, seamless solution to trigger retention can enhance data security and compliance.</span></span>

- <span data-ttu-id="02567-p115">**À l’aide d’une API REST M365** Ce processus peut être utilisé lorsque les grandes quantités de contenu sont conservées à un moment et/ou la fréquence de rétention déclencheur est récurrente telle que de manière quotidienne ou hebdomadaire. Le flux détecte quand un événement se produit dans votre système métier de, puis crée automatiquement un événement connexe dans le centre de sécurité et conformité. Vous n’avez pas besoin de créer manuellement un événement dans l’interface utilisateur chaque fois que ce qui se passer.</span><span class="sxs-lookup"><span data-stu-id="02567-p115">**Using a M365 REST API** This process can be used when large amounts of content are to be retained at a time and/or the frequency to trigger retention is often such as daily or weekly. The flow detects when an event occurs in your line-of-business system, and then automatically creates a related event in the Security & Compliance Center. You don't need to manually create an event in the UI each time one occurs.</span></span>

<span data-ttu-id="02567-175">Il existe deux options d’utilisation de l’API REST :</span><span class="sxs-lookup"><span data-stu-id="02567-175">There are two options for using the REST API:</span></span>

- <span data-ttu-id="02567-176">**Microsoft Flow ou une application similaire** peut être utilisée pour déclencher automatiquement l’occurrence d’un événement.</span><span class="sxs-lookup"><span data-stu-id="02567-176">**Microsoft Flow or a similar application** can be used to trigger the occurrence of an event automatically.</span></span> <span data-ttu-id="02567-177">Microsoft Flow est un Orchestrator pour la connexion à d’autres systèmes.</span><span class="sxs-lookup"><span data-stu-id="02567-177">Microsoft Flow is an orchestrator for connecting to other systems.</span></span> <span data-ttu-id="02567-178">L’utilisation de Microsoft Flow ne nécessite pas de solution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="02567-178">Using Microsoft Flow doesn't require a custom solution.</span></span>

- <span data-ttu-id="02567-179">**PowerShell ou un HTTP client pour appeler des API REST** à l’aide de PowerShell (version 6 ou version ultérieure) pour appeler l’API REST Microsoft 365 pour créer des événements.</span><span class="sxs-lookup"><span data-stu-id="02567-179">**PowerShell or an HTTP client to call REST API** Using PowerShell (version 6 or higher) to call Microsoft 365 REST API to create events.</span></span> 

<span data-ttu-id="02567-180">Une API REST est un point de terminaison de service qui prend en charge les ensembles d’opérations HTTP (méthodes), qui fournissent l’accès de création, récupération/mise à jour/suppression aux ressources du service.</span><span class="sxs-lookup"><span data-stu-id="02567-180">A Rest API is a service endpoint that supports sets of HTTP operations (methods), which provide create/retrieve/update/delete access to the service's resources.</span></span> <span data-ttu-id="02567-181">Pour plus d’informations, voir [composants d’une demande/réponse API REST](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span><span class="sxs-lookup"><span data-stu-id="02567-181">For more information, see [Components of a REST API request/response](https://docs.microsoft.com/rest/api/gettingstarted/#components-of-a-rest-api-requestresponse).</span></span> <span data-ttu-id="02567-182">Dans ce cas, l’API REST de Microsoft 365 vous permet de créer et d’extraire des événements à l’aide d’opérations (méthodes) publier et récupérer.</span><span class="sxs-lookup"><span data-stu-id="02567-182">In this case, by using the Microsoft 365 REST API, events can be created and retrieved using operations (methods) POST and GET.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="02567-183">Exemples de scénarios</span><span class="sxs-lookup"><span data-stu-id="02567-183">Example scenarios</span></span>

<span data-ttu-id="02567-184">Envisagez les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="02567-184">Let’s consider the following scenarios.</span></span>

### <a name="scenario-1-employees-leaving-the-organization"></a><span data-ttu-id="02567-185">Scénario 1 : Employés quittant l’organisation</span><span class="sxs-lookup"><span data-stu-id="02567-185">Scenario 1: Employees leaving the organization</span></span> 

<span data-ttu-id="02567-186">Une organisation crée et stocke de nombreux documents liés à des employés par employé.</span><span class="sxs-lookup"><span data-stu-id="02567-186">An organization creates and stores numerous employee-related documents per employee.</span></span> <span data-ttu-id="02567-187">Ces documents sont gérés et conservés pendant l’embauche de chaque employé.</span><span class="sxs-lookup"><span data-stu-id="02567-187">These documents are managed and retained during the employment of each employee.</span></span> <span data-ttu-id="02567-188">Cependant, lorsque l’employé quitte l’organisation ou que l’emploi est résilié, l’organisation est obligée par les exigences légales et commerciales de conserver les documents de cet employé pendant une période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="02567-188">However, when the employee leaves the organization or the employment is terminated, the organization is obligated by legal and business requirements to retain the documents of that employee for a stipulated period.</span></span>

<span data-ttu-id="02567-189">Maintenant si plusieurs employés quittent l’organisation tous les jours, l’organisation doit déclencher la lecture l’horloge de rétention de centaines si ce n’est pas de milliers de documents chaque jour.</span><span class="sxs-lookup"><span data-stu-id="02567-189">Now if multiple employees leave the organization every day, the organization must trigger the retention clock of hundreds if not thousands of documents each day.</span></span>

<span data-ttu-id="02567-190">En plus de cela, la période de rétention doit être calculée pour chacun de ces employés comme date d’achèvement employé + nombre de jours, mois ou années en fonction du type de l’employé enregistrer.</span><span class="sxs-lookup"><span data-stu-id="02567-190">In addition to this, the retention period needs to be calculated for each of these employees as Employee termination date + number of days, months, or years based on the type of the employee record.</span></span> <span data-ttu-id="02567-191">Par exemple, la rémunération du collaborateur des employés et les déclarations d’avantages du même employé peuvent nécessiter une rétention différente.</span><span class="sxs-lookup"><span data-stu-id="02567-191">For example, worker’s compensation of the employee vs. benefits filings of the same employee may need different retention.</span></span>

<span data-ttu-id="02567-192">Le diagramme ci-dessous montre comment plusieurs étiquettes peuvent être associées à un seul événement.</span><span class="sxs-lookup"><span data-stu-id="02567-192">The diagram below shows how there can be multiple labels that are associated with a single event.</span></span> <span data-ttu-id="02567-193">Dans cet exemple, tous les fichiers figurant sous l’étiquette indemnités du collaborateur et tous les fichiers sous l’étiquette avantages sociaux des employés sont associés à un seul événement, qui est l’employé quittant l’organisation.</span><span class="sxs-lookup"><span data-stu-id="02567-193">Here all the files under Worker’s compensation label and all the files under Employee benefits label are both associated with a single event, which is the employee leaving the organization.</span></span> <span data-ttu-id="02567-194">Chacun de ces fichiers a des horloges de rétention différentes.</span><span class="sxs-lookup"><span data-stu-id="02567-194">Each of these different files has different retention clocks.</span></span> <span data-ttu-id="02567-195">Par conséquent, lorsqu’un employé quitte l’organisation, ces fichiers au sein de chaque étiquette ont une période de rétention différente.</span><span class="sxs-lookup"><span data-stu-id="02567-195">So, when an employee leaves the organization, these files within each label experience a different retention period.</span></span> <span data-ttu-id="02567-196">Le déclenchement de toutes ces horloges de rétention pour chaque type de fichier ou étiquette pour chaque employé constitue une tâche complexe.</span><span class="sxs-lookup"><span data-stu-id="02567-196">Triggering all these different retention clocks for each file type or label for each employee is a very challenging task.</span></span> <span data-ttu-id="02567-197">Imaginez qu’il s’agit de plusieurs employés.</span><span class="sxs-lookup"><span data-stu-id="02567-197">Imagine doing this for multiple employees.</span></span>

![Diagramme illustrant le type d’événement, des événements et des étiquettes](../media/automate-event-driven-retention-event-diagram-employee-leaving.png)

<span data-ttu-id="02567-199">Un processus automatisé associé au déclenchement de ces différentes horloges de rétention pour plusieurs employés sera donc un gagne-temps, exempte d’erreur et très efficace.</span><span class="sxs-lookup"><span data-stu-id="02567-199">Hence an automated process to trigger these different retention clocks for multiple employees will be time-saving, error-free, and extremely efficient.</span></span>

<span data-ttu-id="02567-200">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="02567-200">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des actions pour le scénario d’employé quittant l’organisation](../media/automate-event-driven-retention-employee-termination-diagram.png)

  - <span data-ttu-id="02567-202">L’administrateur crée des dossiers d’employé lié au Document, telles Cartier Marie, John Smith.</span><span class="sxs-lookup"><span data-stu-id="02567-202">Admin creates employee folders to the Document set such as Jane Doe, John Smith.</span></span>

  - <span data-ttu-id="02567-203">L’administrateur ajoute des fichiers employé tels que les avantages, paie, rémunération de travailleur à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="02567-203">Admin adds employee files such as Benefits, Payroll, Worker’s Compensation to each employee folder.</span></span>

  - <span data-ttu-id="02567-204">L’administrateur affecte des ID d’élément à chaque dossier employé.</span><span class="sxs-lookup"><span data-stu-id="02567-204">Admin assigns Asset ID to each employee folder.</span></span> 

  - <span data-ttu-id="02567-205">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="02567-205">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="02567-206">L’administrateur SCC crée des types d’événements liés à l’employé tels que « Renvoi employé », « Embauche employé » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="02567-206">SCC Admin creates employee-related events types such as “Employee Termination”, “Employee Hire” events.</span></span>

  - <span data-ttu-id="02567-207">Administrateur SCC crée une étiquette « Employés ».</span><span class="sxs-lookup"><span data-stu-id="02567-207">SCC Admin creates “Employee Retention” label.</span></span>

  - <span data-ttu-id="02567-208">Cette étiquette « Employés » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-208">This “Employee Retention” label is published and applied manually or automatically to the employee files in SharePoint.</span></span>

  - <span data-ttu-id="02567-209">Le Système de Gestion des Ressources Humaines comme Workday peut fonctionner avec Microsoft Flow pour exécuter cette page régulièrement pour gérer les fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="02567-209">HR Management System like Workday can work with Microsoft Flow to run periodically to manage employee files.</span></span>

  - <span data-ttu-id="02567-210">Si un employé a quitté l’organisation, le flux déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="02567-210">If an employee has left the organization, the Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific employee’s files.</span></span>

#### <a name="using-microsoft-flow"></a><span data-ttu-id="02567-211">Utilisation Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="02567-211">Using Microsoft Flow</span></span>

<span data-ttu-id="02567-212">Étape 1-créer un flux de créer un événement en utilisant l’API REST Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="02567-212">Step 1- Create a flow to create an event using the Microsoft 365 REST API</span></span>

![Utilisation le flux pour créer un événement](../media/automate-event-driven-retention-flow-1.png)

![Utilisation du flux pour appeler des API REST](../media/automate-event-driven-retention-flow-2.png)

##### <a name="create-an-event"></a><span data-ttu-id="02567-215">Créer un événement</span><span class="sxs-lookup"><span data-stu-id="02567-215">Create an event</span></span>

<span data-ttu-id="02567-216">Utilisation du code d’exemple pour appeler des API REST :</span><span class="sxs-lookup"><span data-stu-id="02567-216">Sample code to call the REST API:</span></span>

- <span data-ttu-id="02567-217">**Method** : PUBLIER</span><span class="sxs-lookup"><span data-stu-id="02567-217">**Method**: POST</span></span>
- <span data-ttu-id="02567-218">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span><span class="sxs-lookup"><span data-stu-id="02567-218">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span></span>
- <span data-ttu-id="02567-219">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="02567-219">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>
- <span data-ttu-id="02567-220">**Body** :</span><span class="sxs-lookup"><span data-stu-id="02567-220">**Body**:</span></span>
    
    ```xml
    <?xml version='1.0' encoding='utf-8' standalone='yes'?>
    
    <entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'
    
    xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'
    
    xmlns='http://www.w3.org/2005/Atom'>
    
    <category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' />
    
    <updated>9/9/2017 10:50:00 PM</updated>
    
    <content type='application/xml'>
    
    <m:properties>
    
    <d:Name>Employee Termination </d:Name>
    
    <d:EventType>99e0ae64-a4b8-40bb-82ed-645895610f56</d:EventType>
    
    <d:SharePointAssetIdQuery>1234</d:SharePointAssetIdQuery>
    
    <d:EventDateTime>2018-12-01T00:00:00Z </d:EventDateTime>
    
    </m:properties>
    
    </content>
    
    </entry>
    ```
- <span data-ttu-id="02567-221">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="02567-221">**Authentication**: Basic</span></span>
- <span data-ttu-id="02567-222">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="02567-222">**Username**: "Complianceuser"</span></span>
- <span data-ttu-id="02567-223">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="02567-223">**Password**: "Compliancepassword"</span></span>


##### <a name="available-parameters"></a><span data-ttu-id="02567-224">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="02567-224">Available parameters</span></span>


|<span data-ttu-id="02567-225">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02567-225">Parameters</span></span>|<span data-ttu-id="02567-226">Description</span><span class="sxs-lookup"><span data-stu-id="02567-226">Description</span></span>|<span data-ttu-id="02567-227">Notes</span><span class="sxs-lookup"><span data-stu-id="02567-227">Notes</span></span>|
|--- |--- |--- |
|<span data-ttu-id="02567-228"><d:Name></d:Name></span><span class="sxs-lookup"><span data-stu-id="02567-228"><d:Name></d:Name></span></span>|<span data-ttu-id="02567-229">Entrez un nom unique pour la base de données,</span><span class="sxs-lookup"><span data-stu-id="02567-229">Provide a unique name for the event,</span></span>|<span data-ttu-id="02567-230">Un nom ne peut pas contenir les espaces et les caractères suivants : % \* \ & < \> \| # ?</span><span class="sxs-lookup"><span data-stu-id="02567-230">Cannot contain trailing spaces, and the following characters: % \* \ & < \> \| # ?</span></span> <span data-ttu-id="02567-231">, : ;</span><span class="sxs-lookup"><span data-stu-id="02567-231">, : ;</span></span>|
|<span data-ttu-id="02567-232"><d:EventType></d:EventType></span><span class="sxs-lookup"><span data-stu-id="02567-232"><d:EventType></d:EventType></span></span>|<span data-ttu-id="02567-233">Entrez le nom de l’événement (ou Guid),</span><span class="sxs-lookup"><span data-stu-id="02567-233">Enter event type name (or Guid),</span></span>|<span data-ttu-id="02567-p122">Exemple : « employé licenciement anticipé ». Le type d’événement doit être associé à une étiquette de rétention.</span><span class="sxs-lookup"><span data-stu-id="02567-p122">Example: “Employee termination”. Event type has to be associated with a retention label.</span></span>|
|<span data-ttu-id="02567-236"><d:SharePointAssetIdQuery></d:SharePointAssetIdQuery></span><span class="sxs-lookup"><span data-stu-id="02567-236"><d:SharePointAssetIdQuery></d:SharePointAssetIdQuery></span></span>|<span data-ttu-id="02567-237">Entrez « ComplianceAssetId : « + Id d’employé</span><span class="sxs-lookup"><span data-stu-id="02567-237">Enter “ComplianceAssetId:” + employee Id</span></span>|<span data-ttu-id="02567-238">Example: "ComplianceAssetId:12345"</span><span class="sxs-lookup"><span data-stu-id="02567-238">Example: "ComplianceAssetId:12345"</span></span>|
|<span data-ttu-id="02567-239"><d:EventDateTime></d:EventDateTime></span><span class="sxs-lookup"><span data-stu-id="02567-239"><d:EventDateTime></d:EventDateTime></span></span>|<span data-ttu-id="02567-240">Date et heure de l’événement.</span><span class="sxs-lookup"><span data-stu-id="02567-240">Event Date and Time</span></span>|<span data-ttu-id="02567-241">Format : AAAA-MM-jjTHH : mm : ssZ ; exemple : 2018-12-01T00:00:00Z</span><span class="sxs-lookup"><span data-stu-id="02567-241">Format: yyyy-MM-ddTHH:mm:ssZ, Example: 2018-12-01T00:00:00Z</span></span>
|

##### <a name="response-codes"></a><span data-ttu-id="02567-242">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-242">Response codes</span></span>

| <span data-ttu-id="02567-243">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-243">Response Code</span></span> | <span data-ttu-id="02567-244">Description</span><span class="sxs-lookup"><span data-stu-id="02567-244">Description</span></span>       |
| ----------------- | --------------------- |
| <span data-ttu-id="02567-245">302</span><span class="sxs-lookup"><span data-stu-id="02567-245">302</span></span>               | <span data-ttu-id="02567-246">Rediriger</span><span class="sxs-lookup"><span data-stu-id="02567-246">Redirect</span></span>              |
| <span data-ttu-id="02567-247">201</span><span class="sxs-lookup"><span data-stu-id="02567-247">201</span></span>               | <span data-ttu-id="02567-248">Créé</span><span class="sxs-lookup"><span data-stu-id="02567-248">Created</span></span>               |
| <span data-ttu-id="02567-249">403</span><span class="sxs-lookup"><span data-stu-id="02567-249">403</span></span>               | <span data-ttu-id="02567-250">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="02567-250">Authorization Failed</span></span>  |
| <span data-ttu-id="02567-251">401</span><span class="sxs-lookup"><span data-stu-id="02567-251">401</span></span>               | <span data-ttu-id="02567-252">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="02567-252">Authentication Failed</span></span> |

##### <a name="get-events-based-on-time-range"></a><span data-ttu-id="02567-253">Obtenir des événements en fonction de l’intervalle de temps</span><span class="sxs-lookup"><span data-stu-id="02567-253">Get Events based on time range</span></span>

- <span data-ttu-id="02567-254">**Méthode **: GET</span><span class="sxs-lookup"><span data-stu-id="02567-254">**Method**: GET</span></span>

- <span data-ttu-id="02567-255">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&EndDateTime=2019-01-16`</span><span class="sxs-lookup"><span data-stu-id="02567-255">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent?BeginDateTime=2019-01-11&EndDateTime=2019-01-16`</span></span>

- <span data-ttu-id="02567-256">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="02567-256">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="02567-257">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="02567-257">**Authentication**: Basic</span></span>

- <span data-ttu-id="02567-258">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="02567-258">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="02567-259">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="02567-259">**Password**: "Compliancepassword"</span></span>


##### <a name="response-codes"></a><span data-ttu-id="02567-260">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-260">Response codes</span></span>

| <span data-ttu-id="02567-261">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-261">Response Code</span></span> | <span data-ttu-id="02567-262">Description</span><span class="sxs-lookup"><span data-stu-id="02567-262">Description</span></span>                   |
| ----------------- | --------------------------------- |
| <span data-ttu-id="02567-263">200</span><span class="sxs-lookup"><span data-stu-id="02567-263">200</span></span>               | <span data-ttu-id="02567-264">OK, une liste d’événements dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="02567-264">OK, A list of events in atom+ xml</span></span> |
| <span data-ttu-id="02567-265">404</span><span class="sxs-lookup"><span data-stu-id="02567-265">404</span></span>               | <span data-ttu-id="02567-266">Introuvable</span><span class="sxs-lookup"><span data-stu-id="02567-266">Not found</span></span>                         |
| <span data-ttu-id="02567-267">302</span><span class="sxs-lookup"><span data-stu-id="02567-267">302</span></span>               | <span data-ttu-id="02567-268">Rediriger</span><span class="sxs-lookup"><span data-stu-id="02567-268">Redirect</span></span>                          |
| <span data-ttu-id="02567-269">401</span><span class="sxs-lookup"><span data-stu-id="02567-269">401</span></span>               | <span data-ttu-id="02567-270">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="02567-270">Authorization Failed</span></span>              |
| <span data-ttu-id="02567-271">403</span><span class="sxs-lookup"><span data-stu-id="02567-271">403</span></span>               | <span data-ttu-id="02567-272">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="02567-272">Authentication Failed</span></span>             |

##### <a name="get-an-event-by-id"></a><span data-ttu-id="02567-273">Obtenir un événement par ID</span><span class="sxs-lookup"><span data-stu-id="02567-273">Get an event by ID</span></span>

- <span data-ttu-id="02567-274">**Méthode **: GET</span><span class="sxs-lookup"><span data-stu-id="02567-274">**Method**: GET</span></span>

- <span data-ttu-id="02567-275">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('174e9a86-74ff-4450-8666-7c11f7730f66')`</span><span class="sxs-lookup"><span data-stu-id="02567-275">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent('174e9a86-74ff-4450-8666-7c11f7730f66')`</span></span>

- <span data-ttu-id="02567-276">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="02567-276">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="02567-277">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="02567-277">**Authentication**: Basic</span></span>

- <span data-ttu-id="02567-278">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="02567-278">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="02567-279">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="02567-279">**Password**: "Compliancepassword"</span></span>



##### <a name="response-codes"></a><span data-ttu-id="02567-280">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-280">Response codes</span></span>

| <span data-ttu-id="02567-281">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-281">Response Code</span></span> | <span data-ttu-id="02567-282">Description</span><span class="sxs-lookup"><span data-stu-id="02567-282">Description</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="02567-283">200</span><span class="sxs-lookup"><span data-stu-id="02567-283">200</span></span>               | <span data-ttu-id="02567-284">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="02567-284">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="02567-285">404</span><span class="sxs-lookup"><span data-stu-id="02567-285">404</span></span>               | <span data-ttu-id="02567-286">Introuvable</span><span class="sxs-lookup"><span data-stu-id="02567-286">Not found</span></span>                                            |
| <span data-ttu-id="02567-287">302</span><span class="sxs-lookup"><span data-stu-id="02567-287">302</span></span>               | <span data-ttu-id="02567-288">Rediriger</span><span class="sxs-lookup"><span data-stu-id="02567-288">Redirect</span></span>                                             |
| <span data-ttu-id="02567-289">401</span><span class="sxs-lookup"><span data-stu-id="02567-289">401</span></span>               | <span data-ttu-id="02567-290">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="02567-290">Authorization Failed</span></span>                                 |
| <span data-ttu-id="02567-291">403</span><span class="sxs-lookup"><span data-stu-id="02567-291">403</span></span>               | <span data-ttu-id="02567-292">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="02567-292">Authentication Failed</span></span>                                |

##### <a name="get-an-event-by-name"></a><span data-ttu-id="02567-293">Obtenir un événement par le nom</span><span class="sxs-lookup"><span data-stu-id="02567-293">Get an event by name</span></span>

- <span data-ttu-id="02567-294">**Méthode **: GET</span><span class="sxs-lookup"><span data-stu-id="02567-294">**Method**: GET</span></span>

- <span data-ttu-id="02567-295">**URL** :`https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span><span class="sxs-lookup"><span data-stu-id="02567-295">**URL**: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span></span>

- <span data-ttu-id="02567-296">**Headers** : Clé = Type de contenu, Valeur = application/atom+xml</span><span class="sxs-lookup"><span data-stu-id="02567-296">**Headers**: Key = Content-Type, Value = application/atom+xml</span></span>

- <span data-ttu-id="02567-297">**Authentification** : de base</span><span class="sxs-lookup"><span data-stu-id="02567-297">**Authentication**: Basic</span></span>

- <span data-ttu-id="02567-298">**Nom d’utilisateur** : « Complianceuser »</span><span class="sxs-lookup"><span data-stu-id="02567-298">**Username**: "Complianceuser"</span></span>

- <span data-ttu-id="02567-299">**Password** : « Compliancepassword »</span><span class="sxs-lookup"><span data-stu-id="02567-299">**Password**: "Compliancepassword"</span></span>


##### <a name="response-codes"></a><span data-ttu-id="02567-300">Codes de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-300">Response codes</span></span>

| <span data-ttu-id="02567-301">Code de réponse</span><span class="sxs-lookup"><span data-stu-id="02567-301">Response Code</span></span> | <span data-ttu-id="02567-302">Description</span><span class="sxs-lookup"><span data-stu-id="02567-302">Description</span></span>                                      |
| ----------------- | ---------------------------------------------------- |
| <span data-ttu-id="02567-303">200</span><span class="sxs-lookup"><span data-stu-id="02567-303">200</span></span>               | <span data-ttu-id="02567-304">OK, le corps du message de réponse contient l’événement dans atome + xml</span><span class="sxs-lookup"><span data-stu-id="02567-304">OK, The response body contains the event in atom+xml</span></span> |
| <span data-ttu-id="02567-305">404</span><span class="sxs-lookup"><span data-stu-id="02567-305">404</span></span>               | <span data-ttu-id="02567-306">Introuvable</span><span class="sxs-lookup"><span data-stu-id="02567-306">Not found</span></span>                                            |
| <span data-ttu-id="02567-307">302</span><span class="sxs-lookup"><span data-stu-id="02567-307">302</span></span>               | <span data-ttu-id="02567-308">Rediriger</span><span class="sxs-lookup"><span data-stu-id="02567-308">Redirect</span></span>                                             |
| <span data-ttu-id="02567-309">401</span><span class="sxs-lookup"><span data-stu-id="02567-309">401</span></span>               | <span data-ttu-id="02567-310">Autorisation échouée</span><span class="sxs-lookup"><span data-stu-id="02567-310">Authorization Failed</span></span>                                 |
| <span data-ttu-id="02567-311">403</span><span class="sxs-lookup"><span data-stu-id="02567-311">403</span></span>               | <span data-ttu-id="02567-312">Message d’échec d’authentification</span><span class="sxs-lookup"><span data-stu-id="02567-312">Authentication Failed</span></span>                                |

#### <a name="using-powershell-version-6-or-later-or-any-http-client"></a><span data-ttu-id="02567-313">Utilisation de PowerShell (version 6 ou une version ultérieure) ou n’importe quel client HTTP</span><span class="sxs-lookup"><span data-stu-id="02567-313">Using PowerShell (version 6 or later) or any HTTP client</span></span>

<span data-ttu-id="02567-314">Étape 1: Connectez-vous à PowerShell.</span><span class="sxs-lookup"><span data-stu-id="02567-314">Step 1: Connect to PowerShell.</span></span>

<span data-ttu-id="02567-315">Étape 2: Exécutez le script suivant.</span><span class="sxs-lookup"><span data-stu-id="02567-315">Step 2: Run the following script.</span></span>

```powershell
param([string]$baseUri)

$userName = "UserName"

$password = "Password"

$securePassword = ConvertTo-SecureString $password -AsPlainText -Force

$credentials = New-Object System.Management.Automation.PSCredential($userName, $securePassword)

$EventName="EventByRESTPost-$(([Guid]::NewGuid()).ToString('N'))"

Write-Host "Start to create an event with name: $EventName"

$body = "<?xml version='1.0' encoding='utf-8' standalone='yes'?>

<entry xmlns:d='http://schemas.microsoft.com/ado/2007/08/dataservices'

xmlns:m='http://schemas.microsoft.com/ado/2007/08/dataservices/metadata'

xmlns='http://www.w3.org/2005/Atom'>

<category scheme='http://schemas.microsoft.com/ado/2007/08/dataservices/scheme' term='Exchange.ComplianceRetentionEvent' />

<updated>7/14/2017 2:03:36 PM</updated>

<content type='application/xml'>

<m:properties>

<d:Name>$EventName</d:Name>

<d:EventType>e823b782-9a07-4e30-8091-034fc01f9347</d:EventType>

<d:SharePointAssetIdQuery>'ComplianceAssetId:123'</d:SharePointAssetIdQuery>

</m:properties>

</content>

</entry>"

$event = $null

try

{

$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri "$baseUri/ComplianceRetentionEvent" -ContentType "application/atom+xml" -Authentication Basic -Credential $credentials -MaximumRedirection 0

}

catch

{

$response = $_.Exception.Response

if($response.StatusCode -eq "Redirect")

{

$url = $response.Headers.Location

Write-Host "redirected to $url"

$event = Invoke-RestMethod -Body $body -Method 'POST' -Uri $url -ContentType "application/atom+xml" -Authentication Basic -Credential $credentials -MaximumRedirection 0

}

}

$event | fl *

```


#### <a name="verify-the-outcome-in-both-options"></a><span data-ttu-id="02567-316">Vérifier le résultat dans les deux options</span><span class="sxs-lookup"><span data-stu-id="02567-316">Verify the outcome in both options</span></span>

<span data-ttu-id="02567-317">Étape 1 : Accéder au centre de conformité et de sécurité.</span><span class="sxs-lookup"><span data-stu-id="02567-317">Step 1: Go to the Security & Compliance Center.</span></span>

<span data-ttu-id="02567-318">Étape 2 : Sélectionner **Évènements** sous **Gouvernance des informations**.</span><span class="sxs-lookup"><span data-stu-id="02567-318">Step 2: Select **Events** under **Information governance**.</span></span>

<span data-ttu-id="02567-319">Étape 3 : Vérifier l’Événement a été créé.</span><span class="sxs-lookup"><span data-stu-id="02567-319">Step 3: Verify Event has been created.</span></span>

<span data-ttu-id="02567-320">De même, les options ci-dessus pour automatiser la rétention basée sur des événements peuvent être également utilisées pour les scénarios suivants.</span><span class="sxs-lookup"><span data-stu-id="02567-320">Similarly, the above options to automate event-based retention can be used for the following scenarios as well.</span></span>

### <a name="scenario-2-contracts-expiring"></a><span data-ttu-id="02567-321">Scénario 2 : Contrats expiration</span><span class="sxs-lookup"><span data-stu-id="02567-321">Scenario 2: Contracts Expiring</span></span>

<span data-ttu-id="02567-322">Une organisation peut avoir plusieurs enregistrements pour un seul contrat avec des clients, des fournisseurs et des partenaires.</span><span class="sxs-lookup"><span data-stu-id="02567-322">An organization can have multiple records for a single contract with customers, vendors, and partners.</span></span> <span data-ttu-id="02567-323">Ces documents peuvent résider dans une bibliothèque de documents telle que SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-323">These documents can reside in a document library like SharePoint.</span></span> <span data-ttu-id="02567-324">La fin d’un contrat détermine le début de la période de rétention des documents associés au contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-324">The end of a contract determines the start of the retention period of the documents associated with the contract.</span></span> <span data-ttu-id="02567-325">Par exemple, tous les documents relatifs aux contrats doivent être conservés pendant cinq ans après l'expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-325">For example, all records related to contracts need to be retained for five years from the time the contract expires.</span></span> <span data-ttu-id="02567-326">L’événement qui déclenche la période de rétention de cinq ans est l’expiration du contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-326">The event that triggers the five-year retention period is the expiration of the contract.</span></span>

<span data-ttu-id="02567-327">Un système de gestion de relation client (CRM) pouvez travailler avec Microsoft 365 et la rétention de déclencheur de documents de contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-327">A Customer Relationship Management (CRM) system can work with Microsoft 365 and trigger retention of Contract documents.</span></span>

<span data-ttu-id="02567-328">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="02567-328">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario d’expiration contrat](../media/automate-event-driven-retention-contract-expiration.png)

  - <span data-ttu-id="02567-330">L’administrateur crée une bibliothèque SharePoint avec les différents dossiers pour chaque type de contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-330">Admin creates a SharePoint library with various folders for each contract type.</span></span>

  - <span data-ttu-id="02567-331">L’administrateur ajoute des fichiers de contrat tels que des contrats de licence, les contrats de développement pour chaque dossier contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-331">Admin adds contract files such as License Contracts, Development Contracts to each contract folder.</span></span>

  - <span data-ttu-id="02567-332">L’administrateur affecte des ID délément à chaque dossier de contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-332">Admin assigns Asset ID to each contract folder.</span></span>

  - <span data-ttu-id="02567-333">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="02567-333">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="02567-334">L’administrateur SCC crée un contrat lié aux types événements tels que « Création de contrat, » , « Expiration de contrat » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="02567-334">SCC Admin creates contract-related events types such as “Contract Creation”, “Contract Expiration” events.</span></span>

  - <span data-ttu-id="02567-335">Administrateur SCC crée une étiquette « Expiration de contrat ».</span><span class="sxs-lookup"><span data-stu-id="02567-335">SCC Admin creates “Contract Expiration” label.</span></span>

  - <span data-ttu-id="02567-336">Cette étiquette « Expiration du Contrat » est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-336">This “ Contract Expiration” label is published and applied manually or automatically to the contract files in SharePoint.</span></span>

  - <span data-ttu-id="02567-337">Le Système de Gestion de Contrat peut fonctionner avec Microsoft Flow ou une application similaire pour exécuter cette page régulièrement pour gérer les fichiers de contrat.</span><span class="sxs-lookup"><span data-stu-id="02567-337">Contract Management System can work with Microsoft Flow or a similar application to run periodically to manage contract files.</span></span>

  - <span data-ttu-id="02567-338">Si un employé a quitté l’organisation, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de l’employé.</span><span class="sxs-lookup"><span data-stu-id="02567-338">If a contract expires, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific contract’s files.</span></span>

### <a name="scenario-3-end-of-product-manufacturing"></a><span data-ttu-id="02567-339">Scénario 3 : Fin de la fabrication de produit</span><span class="sxs-lookup"><span data-stu-id="02567-339">Scenario 3: End of Product Manufacturing</span></span>

<span data-ttu-id="02567-p124">Une entreprise de fabrication produisant différentes lignes de produits crée plusieurs caractéristiques de fabrication et les prix de documents. Lorsque le produit n’est plus fabriqué, toutes les spécifications et documents liée à ce besoin produit sont conservés pendant une période spécifique suivant la fin de la durée de vie du produit.</span><span class="sxs-lookup"><span data-stu-id="02567-p124">A manufacturing company that produces different lines of products creates many manufacturing specifications and pricing documents. When the product is no longer manufactured, all specifications and documents linked to this product need to be retained for a specific period after the end of the lifetime of the product.</span></span>

<span data-ttu-id="02567-342">Un système de planification (ERP) peut fonctionner avec Microsoft 365 et Microsoft Flow pour la rétention de déclencheur.</span><span class="sxs-lookup"><span data-stu-id="02567-342">An Enterprise Resource Planning (ERP) system can work with Microsoft 365 and Microsoft Flow to trigger retention.</span></span>

<span data-ttu-id="02567-343">**Configuration Automatisée de Rétention Basée sur des événements pour ce scénario:**</span><span class="sxs-lookup"><span data-stu-id="02567-343">**Configuring Automated Event Based Retention for this scenario:**</span></span>

![Diagramme des rôles et des tâches pour le scénario de cycle de vie de produit](../media/automate-event-driven-retention-product-lifecycle-expiration.png)

  - <span data-ttu-id="02567-345">L’administrateur crée des dossiers du produit dans l’ensemble de Documents tel que produit 1, produit 2, etc.</span><span class="sxs-lookup"><span data-stu-id="02567-345">Admin creates product folders in the Document set such as Product 1, Product 2, and so on.</span></span>

  - <span data-ttu-id="02567-346">L’administrateur ajoute des fichiers produit tels que les spécifications de fabrication, produit sur les tarifs, les licences produit pour chaque dossier du produit.</span><span class="sxs-lookup"><span data-stu-id="02567-346">Admin adds product files such as Manufacturing Specifications, Product Pricing, Product licensing to each product folder.</span></span>

  - <span data-ttu-id="02567-347">L’administrateur affecte des ID d’élément à chaque dossier produit.</span><span class="sxs-lookup"><span data-stu-id="02567-347">Admin assigns Asset ID to each product folder.</span></span>

  - <span data-ttu-id="02567-348">L’administrateur SCG se connecte au Centre de Conformité et de Sécurité.</span><span class="sxs-lookup"><span data-stu-id="02567-348">SCC Admin logs into the Security & Compliance Center.</span></span>

  - <span data-ttu-id="02567-349">L’administrateur SCC crée des types d’événement liés à l’employé tels que « Commencer la fabrication de produit », « Fin de fabrication de produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="02567-349">SCC Admin creates employee-related events types such as “Start of Product Manufacturing”, “End of Product Manufacturing” events.</span></span>

  - <span data-ttu-id="02567-350">L’administrateur SCC crée l’étiquette « Fin de la Fabrication du Produit » dans le Centre de Sécurité et Conformité.</span><span class="sxs-lookup"><span data-stu-id="02567-350">SCC Admin creates “End of Product Manufacturing” label.</span></span>

  - <span data-ttu-id="02567-351">Cette étiquette «Fin de la Fabrication du Produit» est publiée et appliquée manuellement ou automatiquement aux fichiers employé dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="02567-351">This “ End of Product Manufacturing” label is published and applied manually or automatically to the product files in SharePoint.</span></span>

  - <span data-ttu-id="02567-352">Le Système de Gestion de Contrat ERP peut fonctionner avec Microsoft Flow ou des applications similaires pour s’exécuter régulièrement pour gérer les fichiers de produit.</span><span class="sxs-lookup"><span data-stu-id="02567-352">ERP Systems can work with Microsoft Flow or similar applications to run periodically to manage product files.</span></span>

  - <span data-ttu-id="02567-353">Si la fabrication d’un produit se termine, Microsoft Flow déclenche l’événement M365 en fonction de la rétention l’API REST qui va commencer l’horloge de rétention sur des fichiers de produit spécifiques.</span><span class="sxs-lookup"><span data-stu-id="02567-353">If the manufacturing of a product ends, Microsoft Flow will trigger the M365 Event Based Retention REST API that will begin the retention clock on the specific product’s files.</span></span>

## <a name="appendix"></a><span data-ttu-id="02567-354">Annexe</span><span class="sxs-lookup"><span data-stu-id="02567-354">Appendix</span></span>

### <a name="using-redirect-302-response-results-to-call-the-rest-api"></a><span data-ttu-id="02567-355">Utiliser les résultats de réponses 302 de redirection pour appeler des API REST</span><span class="sxs-lookup"><span data-stu-id="02567-355">Using Redirect 302 response results to call the REST API</span></span>

1. <span data-ttu-id="02567-356">Appeler un appel d’événement de rétention POST à l’aide de l’URL API REST : `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span><span class="sxs-lookup"><span data-stu-id="02567-356">Invoke a POST retention event call by using the REST API URL: `https://ps.compliance.protection.outlook.com/psws/service.svc/ComplianceRetentionEvent`</span></span>
    
    <span data-ttu-id="02567-357">Les autorisations d'administrateur global sont requises.</span><span class="sxs-lookup"><span data-stu-id="02567-357">Global administrator permissions are required.</span></span>

2. <span data-ttu-id="02567-358">Vérifiez le code de réponse.</span><span class="sxs-lookup"><span data-stu-id="02567-358">Check the response code.</span></span> <span data-ttu-id="02567-359">S’il s’agit 302, puis obtenez l’URL redirigé de propriété de l’emplacement de l’en-tête de réponse.</span><span class="sxs-lookup"><span data-stu-id="02567-359">If it's 302, then get the redirected URL from Location property of the response header.</span></span>

3. <span data-ttu-id="02567-360">Appeler l’appel d’événement rétention POST à l’aide d’URL redirigé.</span><span class="sxs-lookup"><span data-stu-id="02567-360">Invoke the POST retention event call again using the redirected URL.</span></span>

## <a name="credits"></a><span data-ttu-id="02567-361">Crédits</span><span class="sxs-lookup"><span data-stu-id="02567-361">Credits</span></span>

<span data-ttu-id="02567-362">Cette rubrique a été révisée par :</span><span class="sxs-lookup"><span data-stu-id="02567-362">This topic was reviewed by:</span></span>

<span data-ttu-id="02567-363">Antonio Maio</span><span class="sxs-lookup"><span data-stu-id="02567-363">Antonio Maio</span></span><br/><span data-ttu-id="02567-364">MVP Services et applications Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="02567-364">Microsoft Office Apps and Services MVP</span></span><br/> <span data-ttu-id="02567-365">Antonio.Maio@Protiviti.com</span><span class="sxs-lookup"><span data-stu-id="02567-365">Antonio.Maio@Protiviti.com</span></span>
