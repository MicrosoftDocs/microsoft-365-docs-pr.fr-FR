---
title: Configurer l’audit avancé dans Microsoft 365
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
ms.collection:
- M365-security-compliance
- m365solution-audit
- m365initiative-compliance
- m365solution-scenario
search.appverid:
- MOE150
- MET150
description: Cet article explique comment configurer l’audit avancé afin que vous pouvez effectuer des enquêtes d’investigation lorsque des comptes d’utilisateur sont compromis ou pour enquêter sur d’autres incidents liés à la sécurité.
ms.openlocfilehash: 825dadee5260a263d005eb3a37f280381f9425a2
ms.sourcegitcommit: 0d1b065c94125b495e9886200f7918de3bda40b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "53339225"
---
# <a name="set-up-advanced-audit-in-microsoft-365"></a><span data-ttu-id="421d7-103">Configurer l’audit avancé dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="421d7-103">Set up Advanced Audit in Microsoft 365</span></span>

<span data-ttu-id="421d7-104">Si votre organisation dispose d’un abonnement et d’une licence d’utilisateur final qui prend en charge l’audit avancé, effectuez les étapes suivantes pour configurer et utiliser les fonctionnalités supplémentaires de l’audit avancé.</span><span class="sxs-lookup"><span data-stu-id="421d7-104">If your organization has a subscription and end user licensing that supports Advanced Audit, perform the following steps to set up and use the additional capabilities in Advanced Audit.</span></span>

![Flux de travail pour configurer l’Audit avancé](../media/AdvancedAuditWorkflow.png)

## <a name="step-1-set-up-advanced-audit-for-users"></a><span data-ttu-id="421d7-106">Étape 1 : Configurer l’audit avancé pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="421d7-106">Step 1: Set up Advanced Audit for users</span></span>

<span data-ttu-id="421d7-107">Les fonctionnalités d’audit avancées telles que la possibilité d’enregistrer des événements importants tels que MailItemsAccessed et envoyer nécessitent une licence E5 appropriée attribuée aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="421d7-107">Advanced Audit features such as the ability to log crucial events such as MailItemsAccessed and Send require an appropriate E5 license assigned to users.</span></span> <span data-ttu-id="421d7-108">De plus, l’application/plan de service d’audit avancé doit être activé pour ces utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="421d7-108">Additionally, the Advanced Auditing app/service plan must be enabled for those users.</span></span> <span data-ttu-id="421d7-109">Pour vérifier que l’application d’audit avancée est attribuée aux utilisateurs, procédez comme suit pour chaque utilisateur :</span><span class="sxs-lookup"><span data-stu-id="421d7-109">To verify that the Advanced Auditing app is assigned to users, perform the following steps for each user:</span></span>

1. <span data-ttu-id="421d7-110">Dans le [Centre d’administration Microsoft 365](https://admin.microsoft.com/Adminportal), accédez à **Utilisateurs** > **Utilisateurs actifs**, puis sélectionnez un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="421d7-110">In the [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal), go to **Users** > **Active users**, and select a user.</span></span>

2. <span data-ttu-id="421d7-111">Dans la page déroulante des propriétés de l’utilisateur, cliquez sur **Licences et applications**.</span><span class="sxs-lookup"><span data-stu-id="421d7-111">On the user properties flyout page, click **Licenses and apps**.</span></span>

3. <span data-ttu-id="421d7-112">Dans la section **Licences,** vérifiez qu’une licence E5 est attribuée à l’utilisateur ou qu’une licence de module add-on appropriée lui est attribuée.</span><span class="sxs-lookup"><span data-stu-id="421d7-112">In the **Licenses** section, verify that the user is assigned an E5 license or is assigned an appropriate add-on license.</span></span> <span data-ttu-id="421d7-113">Pour obtenir la liste des licences qui la prise en charge de l’audit avancé, consultez [la liste des licences d’audit avancée requises.](auditing-solutions-overview.md#advanced-audit-1)</span><span class="sxs-lookup"><span data-stu-id="421d7-113">For a list of licenses that support Advanced Audit, see [Advanced Audit licensing requirements](auditing-solutions-overview.md#advanced-audit-1).</span></span>

4. <span data-ttu-id="421d7-114">Développez la section **Applications** et vérifiez que la case à cocher **Audit avancé Microsoft 365** est activée.</span><span class="sxs-lookup"><span data-stu-id="421d7-114">Expand the **Apps** section, and verify that the **Microsoft 365 Advanced Auditing** checkbox is selected.</span></span>

5. <span data-ttu-id="421d7-115">Si la case à cocher n’est pas sélectionnée, sélectionnez-la, puis cliquez sur **Enregistrer les modifications.**</span><span class="sxs-lookup"><span data-stu-id="421d7-115">If the checkbox isn't selected, select it, and then click **Save changes.**</span></span>

   <span data-ttu-id="421d7-116">La journalisation des enregistrements d’audit pour MailItemsAccessed et Send commence dans les 24 heures.</span><span class="sxs-lookup"><span data-stu-id="421d7-116">The logging of audit records for MailItemsAccessed and Send will begin within 24 hours.</span></span> <span data-ttu-id="421d7-117">Vous devez effectuer l’étape 3 pour démarrer la journalisation de deux autres événements importants d’audit avancé : SearchQueryInitiatedExchange et SearchQueryInitiatedSharePoint.</span><span class="sxs-lookup"><span data-stu-id="421d7-117">You have to perform Step 3 to start logging of two other Advanced Audit crucial events: SearchQueryInitiatedExchange and SearchQueryInitiatedSharePoint.</span></span>

<span data-ttu-id="421d7-118">Pour les organisations qui attribuent des licences à des groupes d’utilisateurs à l’aide d’une gestion de licences basée sur les groupes, vous devez désactiver l’attribution des licences pour Microsoft 365 audit avancé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="421d7-118">For organizations that assign licenses to groups of users by using group-based licensing, you have to turn off the licensing assignment for Microsoft 365 Advanced Auditing for the group.</span></span> <span data-ttu-id="421d7-119">Une fois que vous avez enregistré vos modifications, vérifiez que l’audit avancé Microsoft 365 est désactivé pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="421d7-119">After you save your changes, verify that Microsoft 365 Advanced Auditing is turned off for the group.</span></span> <span data-ttu-id="421d7-120">Réactivez ensuite l’attribution des licences pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="421d7-120">Then turn the licensing assignment for the group back on.</span></span> <span data-ttu-id="421d7-121">Pour obtenir des instructions sur la gestion des licences basée sur les groupes, voir [Attribuer des licences aux utilisateurs par appartenance aux groupes dans Azure Active Directory](/azure/active-directory/users-groups-roles/licensing-groups-assign).</span><span class="sxs-lookup"><span data-stu-id="421d7-121">For instructions about group-based licensing, see [Assign licenses to users by group membership in Azure Active Directory](/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>

<span data-ttu-id="421d7-122">En outre, si vous avez personnalisé les actions de boîte aux lettres qui sont enregistrées sur des boîtes aux lettres utilisateur ou des boîtes aux lettres partagées, les nouveaux événements essentiels publiés par Microsoft ne seront pas automatiquement audités sur ces boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="421d7-122">Also, if you have customized the mailbox actions that are logged on user mailboxes or shared mailboxes, any new crucial events released by Microsoft will not be automatically audited on those mailboxes.</span></span> <span data-ttu-id="421d7-123">Pour plus d’informations sur la modification des actions de boîte aux lettres auditées pour chaque type de connexion, consultez la section « Modifier ou restaurer les actions de boîte aux lettres enregistrées par défaut » dans [Gérer l’audit de boîte aux lettres](enable-mailbox-auditing.md#change-or-restore-mailbox-actions-logged-by-default).</span><span class="sxs-lookup"><span data-stu-id="421d7-123">For information about changing the mailbox actions that are audited for each logon type, see the "Change or restore mailbox actions logged by default" section in [Manage mailbox auditing](enable-mailbox-auditing.md#change-or-restore-mailbox-actions-logged-by-default).</span></span>

## <a name="step-2-enable-crucial-events"></a><span data-ttu-id="421d7-124">Étape 2 : Activer les événements essentiels</span><span class="sxs-lookup"><span data-stu-id="421d7-124">Step 2: Enable crucial events</span></span>

<span data-ttu-id="421d7-125">Vous devez activer la journalité de deux événements essentiels (SearchQueryInitiatedExchange et SearchQueryInitiatedSharePoint) lorsque les utilisateurs effectuent des recherches dans Exchange Online et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="421d7-125">You have to enable two crucial events (SearchQueryInitiatedExchange and SearchQueryInitiatedSharePoint) to be logged when users perform searches in Exchange Online and SharePoint Online.</span></span> <span data-ttu-id="421d7-126">Pour permettre à ces deux événements d’être audités pour les utilisateurs, exécutez la commande suivante (pour chaque utilisateur) [dans Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell):</span><span class="sxs-lookup"><span data-stu-id="421d7-126">To enable these two events to be audited for users, run the following command (for each user) in [Exchange Online PowerShell](/powershell/exchange/connect-to-exchange-online-powershell):</span></span>

```powershell
Set-Mailbox <user> -AuditOwner @{Add="SearchQueryInitiated"}
```

<span data-ttu-id="421d7-127">Dans un environnement multigé géographique, vous devez exécuter la commande **Set-Mailbox** précédente dans la forêt où se trouve la boîte aux lettres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="421d7-127">In a multi-geo environment, you must run the previous **Set-Mailbox** command in the forest where the user's mailbox is located.</span></span> <span data-ttu-id="421d7-128">Pour identifier l’emplacement de la boîte aux lettres de l’utilisateur, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="421d7-128">To identify the user's mailbox location, run the following command:</span></span> 

```powershell
Get-Mailbox <user identity> | FL MailboxLocations
```

<span data-ttu-id="421d7-129">Si la commande permettant d’activer l’audit des requêtes de recherche a été précédemment exécuté dans une forêt différente de celle dans laquelle se trouve la boîte aux lettres de l’utilisateur, vous devez supprimer la valeur SearchQueryInitiated de la boîte aux lettres de l’utilisateur en l’exécutant, puis l’ajouter à la boîte aux lettres de l’utilisateur dans la forêt où se trouve la boîte aux lettres de `Set-Mailbox -AuditOwner @{Remove="SearchQueryInitiated"}` l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="421d7-129">If the command to enable the auditing of search queries was previously run in a forest that's different than the one the user's mailbox is located in, then you must remove the SearchQueryInitiated value from the user's mailbox by running `Set-Mailbox -AuditOwner @{Remove="SearchQueryInitiated"}` and then add it to the user's mailbox in the forest where the user's mailbox is located.</span></span>

## <a name="step-3-set-up-audit-retention-policies"></a><span data-ttu-id="421d7-130">Étape 3 : Configurer des stratégies de rétention d’audit</span><span class="sxs-lookup"><span data-stu-id="421d7-130">Step 3: Set up audit retention policies</span></span>

<span data-ttu-id="421d7-131">En plus de la stratégie par défaut qui conserve les enregistrements d’audit Exchange, SharePoint et Azure AD pendant un an, vous pouvez créer des stratégies de rétention supplémentaires pour le journal d’audit afin de répondre aux exigences des équipes de sécurité, informatique et de conformité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="421d7-131">In additional to the default policy that retains Exchange, SharePoint, and Azure AD audit records for one year, you can create additional audit log retention policies to meet the requirements of your organization's security operations, IT, and compliance teams.</span></span> <span data-ttu-id="421d7-132">Pour plus d’informations, voir [gérer les stratégies de rétention du journal d’audit](audit-log-retention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="421d7-132">For more information, see [Manage audit log retention policies](audit-log-retention-policies.md).</span></span>

## <a name="step-4-search-for-crucial-events"></a><span data-ttu-id="421d7-133">Étape 4 : Rechercher des événements essentiels</span><span class="sxs-lookup"><span data-stu-id="421d7-133">Step 4: Search for crucial events</span></span>

<span data-ttu-id="421d7-134">Maintenant que l’audit avancé est installé pour votre organisation, vous pouvez rechercher des événements essentiels et d’autres activités lors de la conduite d’enquêtes légales.</span><span class="sxs-lookup"><span data-stu-id="421d7-134">Now that you have Advanced Audit set up for your organization, you can search for crucial events and other activities when conducting forensic investigations.</span></span> <span data-ttu-id="421d7-135">Après avoir effectué les étapes 1 et 2, vous pouvez rechercher dans le journal d’audit des événements essentiels et d’autres activités pendant les enquêtes d’investigation de comptes compromis et d’autres types d’enquêtes de sécurité ou de conformité.</span><span class="sxs-lookup"><span data-stu-id="421d7-135">After completing Step 1 and Step 2, you can search the audit log for crucial events and other activities during forensic investigations of compromised accounts and other types of security or compliance investigations.</span></span> <span data-ttu-id="421d7-136">Pour plus d’informations sur la conduite d’une investigation d’investigation d’utilisateurs compromis à l’aide de l’événement crucial MailItemsAccessed, voir [Utiliser l’audit](mailitemsaccessed-forensics-investigations.md)avancé pour examiner les comptes compromis.</span><span class="sxs-lookup"><span data-stu-id="421d7-136">For more information about conducting a forensics investigation of compromised user accounts by using the MailItemsAccessed crucial event, see [Use Advanced Audit to investigate compromised accounts](mailitemsaccessed-forensics-investigations.md).</span></span>
