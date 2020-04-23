---
title: Application d’une protection aux données personnelles
f1.keywords:
- NOCSH
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 02/07/2018
audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
- M365-security-compliance
- SPO_Content
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez comment utiliser les stratégies de protection contre la perte de données (DLP) pour protéger les données personnelles dans Microsoft 365.
ms.openlocfilehash: 54bfdd27f5c18d6c145b1e9f13c5e92c1b322048
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43634272"
---
# <a name="apply-protection-to-personal-data"></a><span data-ttu-id="372fa-103">Application d’une protection aux données personnelles</span><span class="sxs-lookup"><span data-stu-id="372fa-103">Apply protection to personal data</span></span>

<span data-ttu-id="372fa-104">La protection des informations personnelles dans Microsoft 365 inclut l’utilisation des fonctionnalités de protection contre la perte de données.</span><span class="sxs-lookup"><span data-stu-id="372fa-104">Protection of personal information in Microsoft 365 includes using data loss prevention capabilities.</span></span> <span data-ttu-id="372fa-105">Les stratégies de protection contre la perte de données (DLP) disponibles dans le Centre de sécurité et conformité vous permettent d’identifier, de surveiller et de protéger automatiquement des informations sensibles dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="372fa-105">With data loss prevention (DLP) policies in the compliance center, you can identify, monitor, and automatically protect sensitive information across Microsoft 365.</span></span>

<span data-ttu-id="372fa-p102">Cette rubrique décrit comment utiliser la protection contre la perte de données pour protéger les données personnelles. Elle répertorie également les autres fonctionnalités de protection qui peuvent être utilisées pour se conformer au règlement général sur la protection des données (RGPD), notamment en définissant des autorisations dans les bibliothèques SharePoint et en utilisant des stratégies d’accès aux appareils.</span><span class="sxs-lookup"><span data-stu-id="372fa-p102">This topic describes how to use DLP to protect personal data. This topic also lists other protection capabilities that can be used to achieve GDPR compliance, including setting permissions in SharePoint libraries and using device access policies.</span></span>

## <a name="apply-protection-using-data-loss-prevention-in-microsoft-365"></a><span data-ttu-id="372fa-108">Application d’une protection à l’aide de la protection contre la perte de données dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="372fa-108">Apply protection using data loss prevention in Microsoft 365</span></span>

<span data-ttu-id="372fa-109">Avec la protection contre la perte de données, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="372fa-109">With DLP, you can:</span></span>

-   <span data-ttu-id="372fa-110">identifier les informations sensibles dans de nombreux emplacements ;</span><span class="sxs-lookup"><span data-stu-id="372fa-110">Identify sensitive information across many locations.</span></span>

-   <span data-ttu-id="372fa-111">empêcher le partage accidentel d’informations sensibles ;</span><span class="sxs-lookup"><span data-stu-id="372fa-111">Prevent accidental sharing of sensitive information.</span></span>

-   <span data-ttu-id="372fa-112">aider les utilisateurs à respecter les règles de conformité sans interrompre leur flux de travail ; et</span><span class="sxs-lookup"><span data-stu-id="372fa-112">Help users learn how to stay compliant without interrupting their workflow.</span></span>

-   <span data-ttu-id="372fa-113">Consulter les rapports DLP présentant le contenu qui correspond aux stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="372fa-113">View DLP reports showing content that matches your organization's DLP policies.</span></span>

<span data-ttu-id="372fa-114">Pour plus d’informations, reportez-vous à [Vue d’ensemble des stratégies de protection contre la perte de données](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e).</span><span class="sxs-lookup"><span data-stu-id="372fa-114">For more information, see [Overview of data loss prevention policies](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e).</span></span>

![Options de création d’une stratégie de protection contre la perte de données](../media/Apply-protection-to-personal-data-in-Office-365-image1.png)

<span data-ttu-id="372fa-116">Cette illustration montre les options permettant de créer une stratégie DLP :</span><span class="sxs-lookup"><span data-stu-id="372fa-116">This illustration shows the options for creating a DLP policy:</span></span>

-   <span data-ttu-id="372fa-p103">Sélectionnez la protection à appliquer. La protection peut inclure :</span><span class="sxs-lookup"><span data-stu-id="372fa-p103">Choose the protection to apply. Protection can include:</span></span>

    -   <span data-ttu-id="372fa-119">Des conseils de stratégie pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="372fa-119">Policy tips for users</span></span>

    -   <span data-ttu-id="372fa-120">Un rapport par e-mail pour les administrateurs</span><span class="sxs-lookup"><span data-stu-id="372fa-120">Email report for admins</span></span>

    -   <span data-ttu-id="372fa-121">Des processus empêchant le partage en externe, en interne ou les deux</span><span class="sxs-lookup"><span data-stu-id="372fa-121">Prevent sharing externally, internally, or both</span></span>

-   <span data-ttu-id="372fa-p104">Sélectionnez les critères pour l’application de la protection. « Appliquer la protection... ...aux documents ayant le type de contenu... » : vous pouvez configurer la stratégie pour qu’elle utilise des types d’informations sensibles et/ou des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="372fa-p104">Choose the criteria for applying the protection. Apply the protection to documents with this type of content: you can configure the policy to use sensitive information types and/or labels.</span></span>

### <a name="using-dlp-for-gdpr-compliance"></a><span data-ttu-id="372fa-124">Utilisation de la protection contre la perte de données pour le respect du RGPD</span><span class="sxs-lookup"><span data-stu-id="372fa-124">Using DLP for GDPR compliance</span></span>

<span data-ttu-id="372fa-p105">L’une des utilisations principales de la protection contre la perte de données Microsoft 365 consiste à identifier les données personnelles liées à des résidents de l’UE dans votre environnement Microsoft 365. La protection contre la perte de données Microsoft 365 peut indiquer à vos équipes de conformité l’endroit où sont stockées les informations personnelles dans SharePoint Online et OneDrive Entreprise, ou leur signaler quand des utilisateurs envoient des courriers électroniques contenant des informations personnelles. La protection contre la perte de données peut également fournir des conseils de stratégie à vos salariés lorsqu’ils manipulent des informations personnelles liées à des personnes résidant dans l’UE.</span><span class="sxs-lookup"><span data-stu-id="372fa-p105">One of the primary uses of Microsoft 365 DLP is to identify personal data related to EU data subjects in your Microsoft 365 environment. Microsoft 365 DLP can notify your compliance teams of where personal information is stored in SharePoint Online and OneDrive for Business, or when users send email containing personal information. DLP can also provide policy tips to your employees when working with personal information related to EU residents.</span></span>

<span data-ttu-id="372fa-p106">En indiquant ainsi où les données des résidents de l’UE sont stockées dans votre environnement, en faisant de la sensibilisation à ce sujet et en comprenant comment vos salariés sont autorisés à les manipuler, vous appliquez un premier niveau de protection des informations selon la protection contre la perte de données de Microsoft 365. Souvent, les salariés qui ont déjà accès à ce type d’informations ont besoin de cet accès pour effectuer leur travail quotidien. L’application de stratégies DLP pour respecter le RGPD ne requiert pas nécessairement une restriction d’accès.</span><span class="sxs-lookup"><span data-stu-id="372fa-p106">Educating and raising awareness to where EU resident data is stored in your environment and how your employees are permitted to handle it represents one level of information protection using Microsoft 365 DLP. Often, employees who already have access to this type of information require this access to do their day to day work. Enforcing DLP policies to help comply with GDPR may not require restricting access.</span></span>

<span data-ttu-id="372fa-p107">Toutefois, le respect du RGPD implique généralement une évaluation des risques de l’organisation d’un point de vue juridique et de la sécurité des informations, l’identification du type des informations personnelles et de l’endroit où elles sont stockées, ainsi que de la justification juridique pour le stockage et le traitement de ces informations. En fonction de cette évaluation, la mise en œuvre de stratégies pour protéger l’organisation et respecter le RGPD peut nécessiter la suppression de l’accès des employés aux documents contenant des informations personnelles sur des résidents de l’UE. Si une protection supplémentaire est requise, une protection DLP supplémentaire peut être configurée.</span><span class="sxs-lookup"><span data-stu-id="372fa-p107">However, complying with GDPR typically involves a risk-based assessment of the organization from both a legal and information security perspective, identification of what type and where personal information is stored, as well as if there's a legal justification to store and process that information. Based on this assessment, implementing policies to protect the organization and comply with GDPR might require removing access for employees to documents that contain personal information for EU data subjects. In cases where further protection is required, additional DLP protection can be configured.</span></span>

<span data-ttu-id="372fa-p108">Le tableau suivant répertorie trois configurations de protection à l’aide de la DLP. La première configuration, Sensibilisation, peut être utilisée comme niveau minimal et point de départ de la protection pour le RGPD.</span><span class="sxs-lookup"><span data-stu-id="372fa-p108">The following table lists three configurations of increasing protection using DLP. The first configuration, awareness, can be used as a starting point and minimum level of protection for GDPR.</span></span>

### <a name="example-protection-levels-that-can-be-configured-with-dlp-policies-and-used-for-gdpr-compliance"></a><span data-ttu-id="372fa-136">Exemple de niveaux de protection pouvant être configurés avec des stratégies DLP et utilisés pour le respect du RGPD</span><span class="sxs-lookup"><span data-stu-id="372fa-136">Example protection levels that can be configured with DLP policies and used for GDPR compliance</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-137"><strong>Niveau de protection</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-137"><strong>Protection level</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-138"><strong>Configuration DLP pour les documents contenant des informations personnelles liées aux données de résidents de l’UE</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-138"><strong>DLP configuration for documents with personal information related to EU data subjects</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-139"><strong>Avantages et risques</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-139"><strong>Benefits and risks</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-140">Sensibilisation</span><span class="sxs-lookup"><span data-stu-id="372fa-140">Awareness</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-141">Envoi de notifications par courrier électronique aux équipes de conformité lorsque ces données sont détectées dans des documents figurant dans SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="372fa-141">Send email notifications to compliance teams when this data is found in documents in SharePoint Online and OneDrive for Business.</span></span></p>
<p><span data-ttu-id="372fa-142">Personnalisation et affichage de conseils de stratégie destinés aux employés dans SharePoint et OneDrive Entreprise lors de l’accès à des documents contenant ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-142">Customize and display Policy Tips to employees in SharePoint and OneDrive for Business when accessing documents containing this data.</span></span></p>
<p><span data-ttu-id="372fa-143">Détection et signalement du partage de ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-143">Detect and report when this data is being shared.</span></span></p></td>
<td align="left"><p><span data-ttu-id="372fa-144">Les équipes de conformité et les salariés sont sensibilisés et savent où sont stockées ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-144">Raise awareness with compliance teams and employees about where this data is stored.</span></span></p>
<p><span data-ttu-id="372fa-145">Les salariés connaissent la stratégie d’entreprise concernant la gestion des documents contenant ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-145">Educate employees on corporate policy for handling documents containing this data.</span></span></p>
<p><span data-ttu-id="372fa-146">Les salariés peuvent quand même partager ces données en interne ou en externe.</span><span class="sxs-lookup"><span data-stu-id="372fa-146">Does not prevent employees from sharing this data internally or externally.</span></span></p>
<p><span data-ttu-id="372fa-147">Vous pouvez consulter les rapports DLP pour les données partagées et décider si vous devez augmenter la protection.</span><span class="sxs-lookup"><span data-stu-id="372fa-147">You can review DLP reports for shared data and decide if you need to increase the protection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-148">Empêcher le partage externe</span><span class="sxs-lookup"><span data-stu-id="372fa-148">Prevent external sharing</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-149">Restriction d’accès aux documents contenant ces données dans SharePoint Online et OneDrive Entreprise lorsque ce contenu est partagé avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="372fa-149">Restrict access to documents that contain this data in SharePoint Online and OneDrive for Business when that content is shared with external users.</span></span></p>
<p><span data-ttu-id="372fa-150">Blocage de l’envoi de messages électroniques comportant des documents contenant ces données à des destinataires externes.</span><span class="sxs-lookup"><span data-stu-id="372fa-150">Prevent sending emails with documents that contain this data to external recipients.</span></span></p>
<p><span data-ttu-id="372fa-151">Détection et signalement du partage de ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-151">Detect and report when this data is being shared.</span></span></p></td>
<td align="left"><p><span data-ttu-id="372fa-152">Le partage externe de ces données est bloqué mais les employés peuvent utiliser ces données en interne.</span><span class="sxs-lookup"><span data-stu-id="372fa-152">Prevents external sharing of this data while allowing for employees to work with this data internally.</span></span></p>
<p><span data-ttu-id="372fa-153">Vous pouvez consulter les rapports DLP des données partagées en interne et décider si vous devez augmenter cette protection.</span><span class="sxs-lookup"><span data-stu-id="372fa-153">You can review DLP reports for internally shared data and decide if you need to increase this protection.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-154">Empêcher le partage interne et externe</span><span class="sxs-lookup"><span data-stu-id="372fa-154">Prevent internal and external sharing</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-155">Restriction de l’accès aux documents contenant ces données dans SharePoint Online et OneDrive Entreprise lorsque ce contenu est partagé en interne ou en externe.</span><span class="sxs-lookup"><span data-stu-id="372fa-155">Restrict access to documents that contain this data in SharePoint Online and OneDrive for Business when that content is shared internally or externally.</span></span></p>
<p><span data-ttu-id="372fa-156">Blocage de l’envoi de messages électroniques contenant ces données à des destinataires externes et internes.</span><span class="sxs-lookup"><span data-stu-id="372fa-156">Prevent sending emails that contain this data to both internal and external recipients.</span></span></p></td>
<td align="left"><p><span data-ttu-id="372fa-157">Le partage interne et externe de ces données est bloqué.</span><span class="sxs-lookup"><span data-stu-id="372fa-157">Prevents internal and external sharing of this data.</span></span></p>
<p><span data-ttu-id="372fa-158">Les employés peuvent ne pas pouvoir effectuer des tâches nécessitant l’utilisation de ces données.</span><span class="sxs-lookup"><span data-stu-id="372fa-158">Employees might not be able to complete tasks that require working with this data.</span></span></p>
<p><span data-ttu-id="372fa-159">Vous pouvez consulter les rapports DLP pour les données partagées en interne ou en externe et décider si les utilisateurs finaux doivent être formés.</span><span class="sxs-lookup"><span data-stu-id="372fa-159">You can review DLP reports for internally or externally shared data and decide if end-user training is needed.</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-p109">Remarque : plus le niveau de protection est élevé, plus la possibilité pour les utilisateurs d’accéder aux informations est restreinte, et cela peut éventuellement avoir un impact sur leur productivité ou la possibilité pour eux d’effectuer leurs tâches quotidiennes. L’augmentation des niveaux de protection par l’implémentation de stratégies qui ont un impact sur les salariés est généralement accompagnée d’une formation des utilisateurs finaux, de l’explication des nouvelles stratégies et procédures de sécurité aux utilisateurs pour les aider à continuer à être productifs dans un environnement plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="372fa-p109">Note: As the levels of protection increase, the ability of users to access information will decrease in some cases, and could potentially impact their productivity or ability to complete day to day tasks. Increasing protection levels by implementing policies that impact employees is typically accompanied by end-user training, educating users on new security policies and procedures to help them continue to be productive in a more secure environment.</span></span>

### <a name="example-dlp-policy-for-gdpr--awareness"></a><span data-ttu-id="372fa-162">Exemple de stratégie DLP pour le RGPD — Sensibilisation</span><span class="sxs-lookup"><span data-stu-id="372fa-162">Example DLP policy for GDPR — Awareness</span></span> 

<span data-ttu-id="372fa-163">Nom : Sensibilisation pour les données personnelles soumises au RGPD.</span><span class="sxs-lookup"><span data-stu-id="372fa-163">Name: Awareness for personal data that is subject to GDPR.</span></span>

<span data-ttu-id="372fa-164">Description : Afficher des conseils de stratégie aux employés, avertir les équipes de conformité lorsque ces données se trouvent dans des documents dans SharePoint Online et OneDrive Entreprise, détecter le partage de ces données en dehors de votre organisation et le signaler.</span><span class="sxs-lookup"><span data-stu-id="372fa-164">Description: Display policy tips to employees, notify compliance teams when this data is found in documents in SharePoint Online and OneDrive for Business, detect and report when this data is being shared outside your organization.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-165"><strong>Commande</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-165"><strong>Control</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-166"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-166"><strong>Settings</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-167">Choisir les informations à protéger</span><span class="sxs-lookup"><span data-stu-id="372fa-167">Choose information to protect</span></span></td>
<td align="left"><span data-ttu-id="372fa-168">Sélectionnez un modèle de stratégie personnalisé.</span><span class="sxs-lookup"><span data-stu-id="372fa-168">Select a Custom policy template.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-169">Emplacements</span><span class="sxs-lookup"><span data-stu-id="372fa-169">Locations</span></span></td>
<td align="left"><span data-ttu-id="372fa-170">Tous les emplacements dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="372fa-170">All locations in Microsoft 365</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-171">Chercher du contenu qui contient</span><span class="sxs-lookup"><span data-stu-id="372fa-171">Find content that contains</span></span></td>
<td align="left"><span data-ttu-id="372fa-172">Cliquez sur « Modifier » et ajoutez tous les types d’informations sensibles traités dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="372fa-172">Click 'Edit' and add all the sensitive information types you curated for your environment.</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-173">Détecter quand ce contenu est partagé</span><span class="sxs-lookup"><span data-stu-id="372fa-173">Detect when this content is shared</span></span></td>
<td align="left"><span data-ttu-id="372fa-174">Cochez cette case, puis sélectionnez « avec des personnes se trouvant en dehors de mon organisation ».</span><span class="sxs-lookup"><span data-stu-id="372fa-174">Check this box and select 'with people outside my organization.'</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-175">Avertir les utilisateurs lorsque le contenu correspond aux paramètres de la stratégie</span><span class="sxs-lookup"><span data-stu-id="372fa-175">Notify users when content matches the policy settings</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-176">Cochez cette case (« Afficher des conseils de stratégie aux utilisateurs et leur envoyer une notification par courrier électronique ».)</span><span class="sxs-lookup"><span data-stu-id="372fa-176">Check this box ("Show policy tips to users and send them an email notification.")</span></span></p>
<p><span data-ttu-id="372fa-p110">Cliquez sur « Personnaliser le conseil et le courrier électronique » et mettez à jour les champs pour votre environnement. Consultez les notifications par défaut dans cet article : <a href="https://support.office.com/article/Send-email-notifications-and-show-policy-tips-for-DLP-policies-87496bc5-9601-4473-8021-cb05c71369c1?ui=en-US&amp;rs=en-US&amp;ad=US">Envoyer des notifications par courrier électronique et afficher des conseils de stratégie pour les stratégies DLP</a>.</span><span class="sxs-lookup"><span data-stu-id="372fa-p110">Click 'Customize the tip and email' and update these for your environment. See the default notifications in this article: <a href="https://support.office.com/article/Send-email-notifications-and-show-policy-tips-for-DLP-policies-87496bc5-9601-4473-8021-cb05c71369c1?ui=en-US&amp;rs=en-US&amp;ad=US">Send email notifications and show policy tips for DLP policies</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-179">Détecter quand une quantité spécifique d’informations sensibles est partagée à un moment donné</span><span class="sxs-lookup"><span data-stu-id="372fa-179">Detect when a specific amount of sensitive info is being shared at one time</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-180">« Détecter quand du contenu partagé contient : Au moins ____ instances du même type d’informations sensibles » : définissez ce paramètre sur 1.</span><span class="sxs-lookup"><span data-stu-id="372fa-180">'Detect when content that's being shared contains: At least ____ instances of the same sensitive info type' — Set this to 1.</span></span></p>
<p><span data-ttu-id="372fa-p111">« Envoyer des rapports d’incident par courrier électronique » : cochez cette case. Cliquez sur « Choisir quoi inclure dans le rapport et qui le reçoit ». Veillez à ajouter votre équipe de conformité.</span><span class="sxs-lookup"><span data-stu-id="372fa-p111">'Send incident reports in email' — check this box. Click 'Choose what to include in the report and who receives it.' Be sure to add your compliance team.</span></span></p>
<p><span data-ttu-id="372fa-184">« Déterminer qui peut accéder au contenu et remplacer la stratégie » : désactivez cette case à cocher pour recevoir des notifications concernant les informations sensibles sans empêcher les utilisateurs d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="372fa-184">'Restrict who can access the content and override the policy' — clear this checkbox to receive notifications about sensitive information without preventing users from access that information.</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-185">Tous les emplacements incluent :</span><span class="sxs-lookup"><span data-stu-id="372fa-185">All locations includes:</span></span>

- <span data-ttu-id="372fa-186">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="372fa-186">SharePoint Online</span></span>

- <span data-ttu-id="372fa-187">Les comptes OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="372fa-187">OneDrive for Business accounts</span></span>

- <span data-ttu-id="372fa-188">Les boîtes aux lettres Exchange</span><span class="sxs-lookup"><span data-stu-id="372fa-188">Exchange mailboxes</span></span>

<span data-ttu-id="372fa-189">Étant donné que la recherche de contenu ne vous permet actuellement pas de tester les types d’informations sensibles dans les courriers électroniques, vous pouvez créer des stratégies distinctes pour Exchange avec un sous-ensemble de types d’informations sensibles dans chaque stratégie et surveiller le déploiement de ces stratégies.</span><span class="sxs-lookup"><span data-stu-id="372fa-189">Because Content Search doesn't currently let you test sensitive information types with email, consider creating separate policies for Exchange with a subset of sensitive information types in each policy and monitoring the rollout of these policies.</span></span>

## <a name="additional-protection-you-can-apply-to-protect-personal-data-in-microsoft-365"></a><span data-ttu-id="372fa-190">Protection supplémentaire pouvant être appliquée pour protéger les données personnelles dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="372fa-190">Additional protection you can apply to protect personal data in Microsoft 365</span></span>

<span data-ttu-id="372fa-p112">Les types d’informations sensibles, les libellés et les stratégies de protection contre la perte de données vous aident à identifier les documents contenant des données spécifiques et à appliquer la protection. Toutefois, pour que ces protections s’appliquent, les autorisations appropriées doivent être définies pour l’accès aux données, les utilisateurs doivent posséder des comptes non compromis et des appareils intègres.</span><span class="sxs-lookup"><span data-stu-id="372fa-p112">Sensitive information types, labels, and data loss protection policies help you identify documents containing specific data and apply protection. However, these protections depend on appropriate permissions being set for access to data, users with accounts that aren't compromised, and devices that are healthy.</span></span>

<span data-ttu-id="372fa-193">L’illustration suivante détaille une protection supplémentaire que vous pouvez appliquer pour protéger l’accès aux données personnelles.</span><span class="sxs-lookup"><span data-stu-id="372fa-193">The following illustration details additional protection you can apply to protect access to personal data.</span></span>

![Protection supplémentaire pour protéger l’accès aux données personnelles](../media/Apply-protection-to-personal-data-in-Office-365-image2.png)

<span data-ttu-id="372fa-195">Pour l’accessibilité, le tableau suivant fournit les mêmes informations que l’illustration.</span><span class="sxs-lookup"><span data-stu-id="372fa-195">For accessibility, the following table provides the same information in the illustration.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-196"><strong>Portée de la protection</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-196"><strong>Scope of protection</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-197"><strong>Fonctionnalités</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-197"><strong>Capabilities</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-198">Protection au niveau du document et du courrier électronique (y compris le courrier en transit, mais pas les boîtes aux lettres au repos pour l’instant)</span><span class="sxs-lookup"><span data-stu-id="372fa-198">Document and email-level protection (includes mail in transit, but not currently mailboxes at rest)</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-199">Types d’informations sensibles</span><span class="sxs-lookup"><span data-stu-id="372fa-199">Sensitive information types</span></span></p>
<p><span data-ttu-id="372fa-200">Libellés Office</span><span class="sxs-lookup"><span data-stu-id="372fa-200">Office labels</span></span></p>
<p><span data-ttu-id="372fa-201">Stratégies de protection contre la perte de données</span><span class="sxs-lookup"><span data-stu-id="372fa-201">Data loss prevention policies</span></span></p>
<p><span data-ttu-id="372fa-202">Chiffrement des messages Microsoft 365 pour la messagerie</span><span class="sxs-lookup"><span data-stu-id="372fa-202">Microsoft 365 Message Encryption for email</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-203">Protection au niveau du site et de la bibliothèque (inclut les sites SharePoint Online et OneDrive Entreprise)</span><span class="sxs-lookup"><span data-stu-id="372fa-203">Site and library-level protection (includes SharePoint Online and OneDrive for Business sites)</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-204">Autorisations pour les sites et les bibliothèques SharePoint Online et OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="372fa-204">Permissions for SharePoint Online and OneDrive for Business sites and libraries</span></span></p>
<p><span data-ttu-id="372fa-205">Stratégies de partage externe pour SharePoint Online et OneDrive Entreprise (au niveau du site)</span><span class="sxs-lookup"><span data-stu-id="372fa-205">External sharing policies for SharePoint Online and OneDrive for Business (site-level)</span></span></p>
<p><span data-ttu-id="372fa-206">Stratégies d’accès d’appareil au niveau du site</span><span class="sxs-lookup"><span data-stu-id="372fa-206">Site-level device access policies</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-207">Protection de l’accès aux services (inclut l’accès à tous les services dans Microsoft 365)</span><span class="sxs-lookup"><span data-stu-id="372fa-207">Service access protection (includes access to all services in Microsoft 365)</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-208">Protection de l’accès aux identités et aux appareils dans la suite Enterprise Mobility + Security (EMS)</span><span class="sxs-lookup"><span data-stu-id="372fa-208">Identity and device access protection in Enterprise Mobility + Security (EMS) suite</span></span></p>
<p><span data-ttu-id="372fa-209">Gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="372fa-209">Privileged access management</span></span></p>
<p><span data-ttu-id="372fa-210">Fonctionnalités de sécurité Windows 10</span><span class="sxs-lookup"><span data-stu-id="372fa-210">Windows 10 security capabilities</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-211">Le reste de cet article fournit des informations supplémentaires sur chacune de ces catégories de protection.</span><span class="sxs-lookup"><span data-stu-id="372fa-211">The rest of this article provides more information on each of these categories of protection.</span></span>

### <a name="capabilities-that-are-ok-to-use-with-gdpr"></a><span data-ttu-id="372fa-212">Fonctionnalités pouvant être utilisées avec le RGPD</span><span class="sxs-lookup"><span data-stu-id="372fa-212">Capabilities that are OK to use with GDPR</span></span>

<span data-ttu-id="372fa-p113">Vous pouvez utiliser les fonctionnalités suivantes dans un environnement configuré pour le respect du RGPD. Ces fonctionnalités ne sont pas nécessaires pour le respect du RGPD, mais elles peuvent être utilisées sans nuire à votre capacité à détecter, protéger, surveiller et signaler les données liées au respect du RGPD.</span><span class="sxs-lookup"><span data-stu-id="372fa-p113">You can use the following capabilities in an environment configured for GDPR compliance. These capabilities are not necessary for GDPR compliance, but they can be used without adversely affecting your ability to discover, protect, monitor, and report on data related to GDPR compliance.</span></span>

<span data-ttu-id="372fa-p114">Clé client : permet aux clients de fournir et de garder le contrôle sur les clés de chiffrement utilisées pour chiffrer les données au repos dans Microsoft 365. Recommandé uniquement pour les clients ayant besoin, à titre réglementaire, de gérer leurs propres clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="372fa-p114">Customer Key — Allows customers to provide and retain control over the encryption keys that are used to encrypt data at rest within Microsoft 365. Recommended only for customers with a regulatory need to manage their own encryption keys.</span></span>

<span data-ttu-id="372fa-p115">Customer Lockbox : vous permet de contrôler l’accès des ingénieurs de support Microsoft à vos données, si nécessaire, pour résoudre un problème technique au cas par cas. Vous pouvez décider d’accorder ou non l’accès à vos données à l’ingénieur de support. Un délai d’expiration est fourni avec chaque demande.</span><span class="sxs-lookup"><span data-stu-id="372fa-p115">Customer Lockbox — Customer lockbox allows you to control how a Microsoft support engineer accesses your data, if needed, to fix a technical issue on a case by case basis. You can control whether to give the support engineer access to your data or not. An expiration time is provided with each request.</span></span>

## <a name="site-and-library-level-protection"></a><span data-ttu-id="372fa-220">Protection au niveau du site et de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="372fa-220">Site and library-level protection</span></span>

### <a name="permissions-for-sharepoint-and-onedrive-for-business-libraries"></a><span data-ttu-id="372fa-221">Autorisations pour les bibliothèques SharePoint et OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="372fa-221">Permissions for SharePoint and OneDrive for Business libraries</span></span>

<span data-ttu-id="372fa-p116">Utilisez des autorisations dans SharePoint pour établir ou restreindre l’accès des utilisateurs au site ou à son contenu. Ajoutez des utilisateurs individuels ou des groupes Azure Active Directory aux groupes SharePoint par défaut. Vous pouvez également créer un groupe personnalisé pour un contrôle plus précis.</span><span class="sxs-lookup"><span data-stu-id="372fa-p116">Use permissions in SharePoint to provide or restrict user access to the site or its contents. Add individual users or Azure Active Directory groups to the default SharePoint groups. Or, create a custom group for finer-grain control.</span></span>

![Niveaux d’autorisation de Contrôle total à Afficher uniquement](../media/Apply-protection-to-personal-data-in-Office-365-image3.png)

<span data-ttu-id="372fa-p117">L’illustration représente les niveaux d’autorisation complète de contrôle pour l’affichage seul. Le tableau ci-dessous présente les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="372fa-p117">The illustration plots permission levels from Full control to View Only. The following table includes the same information.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-228"><strong>Contrôle total</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-228"><strong>Full Control</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-229"><strong>Concevoir</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-229"><strong>Design</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-230"><strong>Modifier</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-230"><strong>Edit</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-231"><strong>Contribuer</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-231"><strong>Contribute</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-232"><strong>Lire</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-232"><strong>Read</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-233"><strong>Afficher uniquement</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-233"><strong>View Only</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"></td>
<td align="left"><span data-ttu-id="372fa-234">Contribuer + approuver et personnaliser</span><span class="sxs-lookup"><span data-stu-id="372fa-234">Contribute + approve and customize</span></span></td>
<td align="left"><span data-ttu-id="372fa-235">Contribuer + ajouter, modifier et supprimer des listes (pas seulement des éléments de liste)</span><span class="sxs-lookup"><span data-stu-id="372fa-235">Contribute + add, edit, and delete lists (not just list items)</span></span></td>
<td align="left"><span data-ttu-id="372fa-236">Afficher, ajouter, mettre à jour et supprimer des éléments de liste et des documents</span><span class="sxs-lookup"><span data-stu-id="372fa-236">View, add, update, delete list items and documents</span></span></td>
<td align="left"><span data-ttu-id="372fa-237">Afficher et télécharger</span><span class="sxs-lookup"><span data-stu-id="372fa-237">View and download</span></span></td>
<td align="left"><span data-ttu-id="372fa-238">Afficher, pas de téléchargement</span><span class="sxs-lookup"><span data-stu-id="372fa-238">View, no download</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-239">Plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="372fa-239">More information:</span></span>

-   [<span data-ttu-id="372fa-240">Présentation des niveaux d’autorisation dans SharePoint</span><span class="sxs-lookup"><span data-stu-id="372fa-240">Understanding permission levels in SharePoint</span></span>](https://support.office.com/en-US/article/Understanding-permission-levels-in-SharePoint-87ecbb0e-6550-491a-8826-c075e4859848)

-   [<span data-ttu-id="372fa-241">Présentation des groupes SharePoint</span><span class="sxs-lookup"><span data-stu-id="372fa-241">Understanding SharePoint groups</span></span>](https://support.office.com/en-US/article/Understanding-SharePoint-groups-94d9b261-161e-4ace-829e-eca1c8cd2eb8)

### <a name="external-sharing-policies-for-sharepoint-and-onedrive-for-business-libraries"></a><span data-ttu-id="372fa-242">Stratégies de partage externe pour les bibliothèques SharePoint et OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="372fa-242">External sharing policies for SharePoint and OneDrive for Business libraries</span></span>

<span data-ttu-id="372fa-p118">De nombreuses organisations autorisent le partage externe pour encourager la collaboration. Découvrez comment vos paramètres client sont configurés. Ensuite, passez en revue les paramètres de partage externe pour les sites qui contiennent des données personnelles.</span><span class="sxs-lookup"><span data-stu-id="372fa-p118">Many organizations allow external sharing to support collaboration. Find out how your tenant-wide settings are configured. Then review the external sharing settings for sites that contain personal data.</span></span>

<span data-ttu-id="372fa-246">Un utilisateur externe est une personne extérieure à votre organisation qui est invitée à accéder à vos sites et documents SharePoint Online, mais ne dispose d’aucune licence pour votre abonnement SharePoint Online ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="372fa-246">An external user is someone outside of your organization who is invited to access your SharePoint Online sites and documents but doesn't have a license for your SharePoint Online or Microsoft Microsoft 365 subscription.</span></span>

<span data-ttu-id="372fa-247">Les stratégies de partage externe s’appliquent à SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="372fa-247">External sharing policies apply to both SharePoint Online and OneDrive for Business.</span></span>

-   <span data-ttu-id="372fa-248">Vous devez être administrateur SharePoint Online pour configurer des stratégies de partage.</span><span class="sxs-lookup"><span data-stu-id="372fa-248">You must be a SharePoint Online admin to configure sharing policies.</span></span>

-   <span data-ttu-id="372fa-249">Vous devez être propriétaire de site ou disposer des autorisations Contrôle total pour partager un site ou un document avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="372fa-249">You must be a Site Owner or have full control permissions to share a site or document with external users.</span></span>

<span data-ttu-id="372fa-250">Le tableau suivant récapitule les contrôles que vous pouvez configurer.</span><span class="sxs-lookup"><span data-stu-id="372fa-250">The following table summarizes the controls you can configure.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-251"><strong>Catégorie de contrôle</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-251"><strong>Control category</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-252"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-252"><strong>Options</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-253">Type de partage</span><span class="sxs-lookup"><span data-stu-id="372fa-253">Type of sharing</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-254">Ne pas autoriser le partage en dehors de votre organisation (cette option peut être définie pour des collections de sites individuelles)</span><span class="sxs-lookup"><span data-stu-id="372fa-254">Don't allow sharing outside your organization (can be set for individual site collections)</span></span></p>
<p><span data-ttu-id="372fa-255">Autoriser le partage avec des utilisateurs externes authentifiés uniquement (les options Autoriser nouveaux et Limiter aux existants peuvent être définies pour les collections de sites individuelles)\*</span><span class="sxs-lookup"><span data-stu-id="372fa-255">Allow sharing to authenticated external users only (allow new or limit to existing, can be set for individual site collections)\*</span></span></p>
<p><span data-ttu-id="372fa-256">Autoriser le partage à des utilisateurs externes avec un lien d’accès anonyme (cette option peut être définie pour des collections de sites individuelles)</span><span class="sxs-lookup"><span data-stu-id="372fa-256">Allow sharing to external users with an anonymous access link (can be set for individual site collections)</span></span></p>
<p><span data-ttu-id="372fa-257">Limiter le partage externe à l’aide de domaines (liste de domaines autorisés et de domaines bloqués)</span><span class="sxs-lookup"><span data-stu-id="372fa-257">Limit external sharing using domains (allow and deny list)</span></span></p>
<p><span data-ttu-id="372fa-258">Choisir le type de lien par défaut (anonyme, partageable au sein de la société ou restreint)</span><span class="sxs-lookup"><span data-stu-id="372fa-258">Choose the default link type (anonymous, company shareable, or restricted)</span></span></p>
</td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-259">Ce que les utilisateurs externes peuvent faire</span><span class="sxs-lookup"><span data-stu-id="372fa-259">What external users can do</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-260">Empêcher les utilisateurs externes de partager des fichiers, des dossiers et des sites qu’ils ne possèdent pas</span><span class="sxs-lookup"><span data-stu-id="372fa-260">Prevent external users from sharing files, folders, sites they don't own</span></span></p>
<p><span data-ttu-id="372fa-261">Exiger que les utilisateurs externes acceptent les invitations de partage avec le même compte que celui auquel l’invitation a été envoyée</span><span class="sxs-lookup"><span data-stu-id="372fa-261">Require external users to accept sharing invitations with the same account the invitation was sent to</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-262">Notifications</span><span class="sxs-lookup"><span data-stu-id="372fa-262">Notifications</span></span></td>
<td align="left"><p><span data-ttu-id="372fa-p119">Actuellement disponible uniquement dans OneDrive Entreprise. Avertir les propriétaires dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="372fa-p119">Currently only available in OneDrive for Business. Notify owners when:</span></span></p>
- <p><span data-ttu-id="372fa-265">Des utilisateurs invitent des utilisateurs externes supplémentaires à collaborer sur des fichiers partagés</span><span class="sxs-lookup"><span data-stu-id="372fa-265">Users invite additional external users to shared files</span></span></p>
- <p><span data-ttu-id="372fa-266">Les utilisateurs externes acceptent les invitations à accéder aux fichiers</span><span class="sxs-lookup"><span data-stu-id="372fa-266">External users accept invitations to access files</span></span></p>
- <p><span data-ttu-id="372fa-267">Un lien d’accès anonyme est créé ou modifié</span><span class="sxs-lookup"><span data-stu-id="372fa-267">An anonymous access link is created or changed</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-268">Plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="372fa-268">More information:</span></span>

-   [<span data-ttu-id="372fa-269">Gérer le partage externe pour votre environnement SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="372fa-269">Manage external sharing for your SharePoint Online environment</span></span>](https://support.office.com/article/Manage-external-sharing-for-your-SharePoint-Online-environment-C8A462EB-0723-4B0B-8D0A-70FEAFE4BE85?ui=en-US&rs=en-US&ad=US)

-   [<span data-ttu-id="372fa-270">Partager des sites ou des documents avec des personnes extérieures à votre organisation</span><span class="sxs-lookup"><span data-stu-id="372fa-270">Share sites or documents with people outside your organization</span></span>](https://support.office.com/en-US/article/Share-sites-or-documents-with-people-outside-your-organization-80e49744-e30f-44db-8d51-16661b1d4232)

### <a name="site-level-device-access-policies"></a><span data-ttu-id="372fa-271">Stratégies d’accès aux appareils au niveau du site</span><span class="sxs-lookup"><span data-stu-id="372fa-271">Site-level device access policies</span></span>

<span data-ttu-id="372fa-p120">SharePoint Online et OneDrive Entreprise vous permettent de configurer des stratégies d’accès aux appareils au niveau du site. Cela vous permet de configurer plus de protection pour les sites comportant des données sensibles.</span><span class="sxs-lookup"><span data-stu-id="372fa-p120">SharePoint Online and OneDrive for Business let you configure device access policies at the site level. This lets you configure more protection for sites with sensitive data.</span></span>

<span data-ttu-id="372fa-274">Si vous configurez des stratégies d’accès aux appareils au niveau du site, veillez à les coordonner avec les stratégies au niveau du client et également avec les stratégies d’accès configurées dans Azure Active Directory, Intune et Intune App Management.</span><span class="sxs-lookup"><span data-stu-id="372fa-274">If you configure site-level device access policies, be sure to coordinate these with tenant-level policies and also with access policies that are configured in Azure Active Directory, Intune, and Intune App Management.</span></span>

<span data-ttu-id="372fa-p121">Les stratégies d’accès aux appareils pour SharePoint et OneDrive Entreprise nécessitent des stratégies de prise en charge dans Azure Active Directory et Microsoft Intune en fonction du scénario que vous mettez en place. Le tableau suivant récapitule les objectifs que vous pouvez atteindre avec des stratégies d’accès aux appareils et indique quels produits nécessitent des stratégies de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="372fa-p121">Device access policies for SharePoint and OneDrive for Business require supporting policies in Azure Active Directory and Microsoft Intune depending on the scenario you're implementing. The following table summarizes objectives you can achieve with device access policies and indicates which products require supporting policies.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="372fa-277">Autoriser l’accès uniquement à partir d’emplacements d’adresse IP spécifiques</span><span class="sxs-lookup"><span data-stu-id="372fa-277">Only allow access from specific IP address locations</span></span></th>
<th align="left"><span data-ttu-id="372fa-278">Empêcher les utilisateurs de télécharger des fichiers sur des appareils non associés à un domaine</span><span class="sxs-lookup"><span data-stu-id="372fa-278">Prevent users from downloading files to non-domain joined devices</span></span></th>
<th align="left"><span data-ttu-id="372fa-279">Bloquer l’accès sur les appareils non associés à un domaine</span><span class="sxs-lookup"><span data-stu-id="372fa-279">Block access on non-domain joined devices</span></span></th>
<th align="left"><span data-ttu-id="372fa-280">Empêcher les utilisateurs de télécharger des fichiers sur des appareils non conformes</span><span class="sxs-lookup"><span data-stu-id="372fa-280">Prevent users from downloading files to non-compliant devices</span></span></th>
<th align="left"><span data-ttu-id="372fa-281">Bloquer l’accès sur les appareils non conformes</span><span class="sxs-lookup"><span data-stu-id="372fa-281">Block access on non-compliant devices</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-282">Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="372fa-282">SharePoint admin center</span></span></td>
<td align="left"><span data-ttu-id="372fa-283">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-283">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-284">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-284">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-285">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-285">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-286">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-286">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-287">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-287">Yes</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-288">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="372fa-288">Azure Active Directory</span></span></td>
<td align="left"></td>
<td align="left"><span data-ttu-id="372fa-289">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-289">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-290">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-290">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-291">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-291">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-292">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-292">Yes</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-293">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="372fa-293">Microsoft Intune</span></span></td>
<td align="left"></td>
<td align="left"></td>
<td align="left"></td>
<td align="left"><span data-ttu-id="372fa-294">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-294">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-295">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-295">Yes</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-296">Plus d’informations : [Centre d’administration SharePoint Online : Contrôler l’accès à partir d’appareils non gérés](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="372fa-296">More information: [SharePoint Online admin center: Control access from unmanaged devices](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&rs=en-US&ad=US).</span></span>

## <a name="service-access-protection-for-identities-and-devices"></a><span data-ttu-id="372fa-297">Protection de l’accès au service pour les appareils et les identités</span><span class="sxs-lookup"><span data-stu-id="372fa-297">Service access protection for identities and devices</span></span>

<span data-ttu-id="372fa-p122">Microsoft vous recommande de configurer la protection pour les identités et les appareils qui accèdent au service. Le travail que vous effectuez pour protéger l’accès aux services Microsoft 365 peut également être utilisé pour protéger l’accès à d’autres services SaaS et PaaS, et même à des applications dans d’autres fournisseurs cloud.</span><span class="sxs-lookup"><span data-stu-id="372fa-p122">Microsoft recommends you configure protection for identities and devices that access the service. The work you put into protecting access to Microsoft 365 services can also be used to protect access to other SaaS services, PaaS services, and even apps in other cloud providers.</span></span>

<span data-ttu-id="372fa-300">La protection de l’accès pour les appareils et les identités fournit une référence de base de la protection pour garantir que les identités ne sont pas compromises, que les appareils sont sûrs et que les données des organisations figurant sur les appareils sont isolées et protégées.</span><span class="sxs-lookup"><span data-stu-id="372fa-300">Access protection for identities and devices provides a baseline of protection to ensure that identities aren't compromised, devices are safe, and organization data that is accessed on devices is isolated and protected.</span></span>

<span data-ttu-id="372fa-301">Pour obtenir des recommandations pour commencer et des instructions de configuration, reportez-vous à [Conseils de sécurité Microsoft pour les campagnes électorales, les organisations à but non lucratif et d’autres organisations flexibles](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance).</span><span class="sxs-lookup"><span data-stu-id="372fa-301">For starting point recommendations and configuration guidance, see [Microsoft security guidance for political campaigns, nonprofits, and other agile organizations](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance).</span></span>

<span data-ttu-id="372fa-302">Pour les environnements d’identité hybrides avec AD FS, reportez-vous aux [configurations et aux stratégies de sécurité recommandées](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance).</span><span class="sxs-lookup"><span data-stu-id="372fa-302">For hybrid identity environments with AD FS, see [Recommended security policies and configurations](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance).</span></span>

<span data-ttu-id="372fa-p123">L’illustration suivante décrit les relations entre les services cloud (SaaS, PaaS), les types de comptes (comptes de domaine clients et comptes B2B) et les fonctionnalités de service d’accès. Il est important de noter les fonctionnalités qui peuvent être utilisées avec les comptes B2B.</span><span class="sxs-lookup"><span data-stu-id="372fa-p123">The following illustration describes how cloud services (SaaS, PaaS), account types (tenant domain accounts vs. B2B accounts), and service access capabilities relate. It's important to note which capabilities can be used with B2B accounts.</span></span>

![Services cloud, types de comptes et fonctionnalités d’accès](../media/Apply-protection-to-personal-data-in-Office-365-image4.png)

<span data-ttu-id="372fa-306">Pour l’accessibilité, le reste de cette section décrit cette illustration.</span><span class="sxs-lookup"><span data-stu-id="372fa-306">For accessibility, the rest of this section describes this illustration.</span></span>

### <a name="cloud-services"></a><span data-ttu-id="372fa-307">Services cloud</span><span class="sxs-lookup"><span data-stu-id="372fa-307">Cloud services</span></span>

<span data-ttu-id="372fa-p124">Azure Active Directory fournit un accès basé sur l’identité à n’importe quel service cloud, y compris les fournisseurs non-Microsoft tels qu’Amazon Web Services. L’illustration montre Microsoft 365, une « autres application SaaS » et une « application PaaS ». Les flèches pointent d’Azure Active Directory vers chacun de ces services, et montrent qu’Azure Active Directory peut être utilisé pour l’authentification à tous ces types d’application.</span><span class="sxs-lookup"><span data-stu-id="372fa-p124">Azure Active Directory provides identity access to any cloud service, including non-Microsoft providers such as Amazon Web Services. The illustration shows Microsoft 365, "Other SaaS app," and "PaaS app." Arrows point from Azure Active Directory to each of these services, showing that Azure Active Directory can be used for authentication to all of these app types.</span></span>

### <a name="types-of-accounts"></a><span data-ttu-id="372fa-311">Types de comptes</span><span class="sxs-lookup"><span data-stu-id="372fa-311">Types of accounts</span></span>

<span data-ttu-id="372fa-p125">Les comptes de domaine clients sont des comptes que vous ajoutez à votre client et que vous gérez directement. Les comptes B2B sont des comptes pour les utilisateurs extérieurs à votre organisation que vous invitez pour collaborer avec eux. Il peut s’agir d’autres comptes Microsoft 365, de comptes d’autres organisations ou de comptes clients (par exemple, Gmail). L’illustration montre les deux types de comptes dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="372fa-p125">Tenant domain accounts are account you add to your tenant and manage directly. B2B accounts are accounts for users outside your organization you invite to collaborate with. These can be other Microsoft 365 accounts, other organization accounts, or consumer accounts (such as Gmail). The illustration shows both account types within Azure Active Directory.</span></span>

### <a name="capabilities"></a><span data-ttu-id="372fa-316">Fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="372fa-316">Capabilities</span></span>

<span data-ttu-id="372fa-p126">Les fonctionnalités figurant dans le tableau suivant protègent les identités et les appareils. Le tableau indique les fonctionnalités qui peuvent également être utilisées avec des comptes B2B, comme dans l’illustration.</span><span class="sxs-lookup"><span data-stu-id="372fa-p126">The capabilities in the following table protect identities and devices. The table indicates which capabilities can also be used with B2B accounts, similar to the illustration.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="372fa-319"><strong>Fonctionnalité</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-319"><strong>Capability</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-320"><strong>Fonctionne avec les comptes de domaine clients</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-320"><strong>Works with tenant domain accounts</strong></span></span></th>
<th align="left"><span data-ttu-id="372fa-321"><strong>Fonctionne avec les comptes Azure B2B (sans licence supplémentaire)</strong></span><span class="sxs-lookup"><span data-stu-id="372fa-321"><strong>Works with Azure B2B accounts (without additional licensing)</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-322">Authentification multifacteur et accès conditionnel</span><span class="sxs-lookup"><span data-stu-id="372fa-322">Multi-factor authentication and conditional access</span></span></td>
<td align="left"><span data-ttu-id="372fa-323">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-323">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-324">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-324">Yes</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-325">Azure AD Identity Protection</span><span class="sxs-lookup"><span data-stu-id="372fa-325">Azure AD Identity Protection</span></span></td>
<td align="left"><span data-ttu-id="372fa-326">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-326">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-327">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-327">Yes</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-328">Azure AD Privileged Identity Management</span><span class="sxs-lookup"><span data-stu-id="372fa-328">Azure AD Privileged Identity Management</span></span></td>
<td align="left"><span data-ttu-id="372fa-329">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-329">Yes</span></span></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-330">Gestion des applications mobiles (MAM)</span><span class="sxs-lookup"><span data-stu-id="372fa-330">Mobile Application Management (MAM)</span></span></td>
<td align="left"><span data-ttu-id="372fa-331">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-331">Yes</span></span></td>
<td align="left"></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="372fa-332">Gestion et inscription des appareils</span><span class="sxs-lookup"><span data-stu-id="372fa-332">Device enrollment and management</span></span></td>
<td align="left"><span data-ttu-id="372fa-333">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-333">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-334">Seule une organisation peut gérer un appareil</span><span class="sxs-lookup"><span data-stu-id="372fa-334">Only one organization can manage a device</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="372fa-335">Fonctionnalités de sécurité Windows 10 (l’accès conditionnel basé sur la conformité de l’appareil nécessite une gestion des appareils)</span><span class="sxs-lookup"><span data-stu-id="372fa-335">Windows 10 security capabilities (conditional access based on device compliance requires device management)</span></span></td>
<td align="left"><span data-ttu-id="372fa-336">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-336">Yes</span></span></td>
<td align="left"><span data-ttu-id="372fa-337">Oui</span><span class="sxs-lookup"><span data-stu-id="372fa-337">Yes</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="372fa-338">Vous pouvez ajouter des licences à des comptes B2B pour donner à ces utilisateurs des fonctionnalités supplémentaires, si nécessaire, pour protéger l’accès à des données personnelles dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="372fa-338">You can add licenses to B2B accounts to give these users additional capabilities, if needed, to protect access to personal data in your environment.</span></span>
