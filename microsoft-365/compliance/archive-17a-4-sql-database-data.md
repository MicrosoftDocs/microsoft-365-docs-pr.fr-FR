---
title: Configurer un connecteur pour archiver des SQL de données dans Microsoft 365
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
description: Découvrez comment configurer et utiliser un connecteur DataParser 17a-4 SQL pour importer et archiver SQL données dans Microsoft 365.
ms.openlocfilehash: 51fd433ad072ba5afe0b314d7b61041728337240
ms.sourcegitcommit: 410f6e1c6cf53c3d9013b89d6e0b40a050ee9cad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "53137666"
---
# <a name="set-up-a-connector-to-archive-sql-data-preview"></a><span data-ttu-id="88d41-103">Configurer un connecteur pour archiver les SQL données (aperçu)</span><span class="sxs-lookup"><span data-stu-id="88d41-103">Set up a connector to archive SQL data (preview)</span></span>

<span data-ttu-id="88d41-104">Utilisez la [SQL DataParser](https://www.17a-4.com/sql-dataparser/) de 17a-4 LLC pour importer et archiver des données à partir d’une base de données SQL vers les boîtes aux lettres des utilisateurs de Microsoft 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="88d41-104">Use the [SQL DataParser](https://www.17a-4.com/sql-dataparser/) from 17a-4 LLC to import and archive data from a SQL database to user mailboxes in your Microsoft 365 organization.</span></span> <span data-ttu-id="88d41-105">DataParser inclut un connecteur SQL configuré pour capturer des éléments à partir d’une source de données tierce et importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-105">The DataParser includes a SQL connector that's configured to capture items from a third-party data source and import those items to Microsoft 365.</span></span> <span data-ttu-id="88d41-106">Le SQL DataParser convertit les données SQL au format de message électronique, puis importe ces éléments dans les boîtes aux lettres des utilisateurs Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-106">The SQL DataParser connector converts SQL data to an email message format and then imports those items to user mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="88d41-107">Une fois SQL données stockées dans les boîtes aux lettres des utilisateurs, vous pouvez appliquer des fonctionnalités de conformité Microsoft 365 telles que la conservation pour litige, eDiscovery, les stratégies et étiquettes de rétention, ainsi que la conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="88d41-107">After SQL data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, retention policies and retention labels, and communication compliance.</span></span> <span data-ttu-id="88d41-108">L’utilisation d SQL pour importer et archiver des données dans Microsoft 365 peut aider votre organisation à rester conforme aux stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="88d41-108">Using a SQL connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-sql-data"></a><span data-ttu-id="88d41-109">Vue d’ensemble de l’archivage SQL données</span><span class="sxs-lookup"><span data-stu-id="88d41-109">Overview of archiving SQL data</span></span>

<span data-ttu-id="88d41-110">La vue d’ensemble suivante explique le processus d’utilisation d’un connecteur de données pour archiver SQL données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-110">The following overview explains the process of using a data connector to archive SQL data in Microsoft 365.</span></span>

![Flux de travail d’archivage pour SQL données 17a-4](../media/SQLDatabaseDataParserConnectorWorkflow.png)

1. <span data-ttu-id="88d41-112">Votre organisation travaille en 17a-4 pour configurer l’analyseur de SQL données.</span><span class="sxs-lookup"><span data-stu-id="88d41-112">Your organization works with 17a-4 to set up and configure the SQL DataParser.</span></span>

2. <span data-ttu-id="88d41-113">Régulièrement, les SQL sont collectés par DataParser.</span><span class="sxs-lookup"><span data-stu-id="88d41-113">On a regular basis, SQL items are collected by the DataParser.</span></span> <span data-ttu-id="88d41-114">DataParser convertit également le contenu d’un message au format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="88d41-114">The DataParser also converts the content of a message to an email message format.</span></span>

3. <span data-ttu-id="88d41-115">Le SQL DataParser que vous créez dans le Centre de conformité Microsoft 365 se connecte à DataParser et transfère les messages vers un emplacement stockage Azure sécurisé dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88d41-115">The SQL DataParser connector that you create in the Microsoft 365 compliance center connects to DataParser and transfers the messages to a secure Azure Storage location in the Microsoft cloud.</span></span>

4. <span data-ttu-id="88d41-116">Un sous-dossier du dossier Boîte de réception nommé **SQL DataParser** est créé dans les boîtes aux lettres utilisateur et les éléments SQL sont importés dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="88d41-116">A subfolder in the Inbox folder named **SQL DataParser** is created in the user mailboxes, and the SQL items are imported to that folder.</span></span> <span data-ttu-id="88d41-117">Le connecteur détermine la boîte aux lettres dans laquelle importer des éléments à l’aide de la valeur de la *propriété Email.*</span><span class="sxs-lookup"><span data-stu-id="88d41-117">The connector determines which mailbox to import items to by using the value of the *Email* property.</span></span> <span data-ttu-id="88d41-118">Chaque SQL contient cette propriété, qui est remplie avec l’adresse e-mail de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="88d41-118">Every SQL item contains this property, which is populated with the email address of every participant.</span></span>

## <a name="before-you-set-up-a-connector"></a><span data-ttu-id="88d41-119">Avant de configurer un connecteur</span><span class="sxs-lookup"><span data-stu-id="88d41-119">Before you set up a connector</span></span>

- <span data-ttu-id="88d41-120">Créez un compte DataParser pour les connecteurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88d41-120">Create a DataParser account for Microsoft connectors.</span></span> <span data-ttu-id="88d41-121">Pour ce faire, contactez [17a-4 LLC.](https://www.17a-4.com/contact/)</span><span class="sxs-lookup"><span data-stu-id="88d41-121">To do this, contact [17a-4 LLC](https://www.17a-4.com/contact/).</span></span> <span data-ttu-id="88d41-122">Vous devez vous inscrire à ce compte lorsque vous créez le connecteur à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="88d41-122">You need to sign into this account when you create the connector in Step 1.</span></span>

- <span data-ttu-id="88d41-123">L’utilisateur qui crée le connecteur DataParser SQL à l’étape 1 (et le termine à l’étape 3) doit être affecté au rôle Importation/Exportation de boîte aux lettres à l’Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="88d41-123">The user who creates the SQL DataParser connector in Step 1 (and completes it in Step 3) must be assigned to the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="88d41-124">Ce rôle est requis pour ajouter des connecteurs sur la page **Connecteurs de données** dans la Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-124">This role is required to add connectors on the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="88d41-125">Par défaut, ce rôle n’est pas attribué à un groupe de rôles dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="88d41-125">By default, this role is not assigned to a role group in Exchange Online.</span></span> <span data-ttu-id="88d41-126">Vous pouvez ajouter le rôle Importation/Exportation de boîte aux lettres au groupe de rôles Gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="88d41-126">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="88d41-127">Vous pouvez également créer un groupe de rôles, attribuer le rôle Importation/Exportation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="88d41-127">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="88d41-128">Pour plus d’informations, voir les [sections](/Exchange/permissions-exo/role-groups#modify-role-groups) Créer des groupes de rôles ou Modifier des groupes de rôles dans l’article « Gérer les groupes de rôles dans Exchange Online ». [](/Exchange/permissions-exo/role-groups#create-role-groups)</span><span class="sxs-lookup"><span data-stu-id="88d41-128">For more information, see the [Create role groups](/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-set-up-a-sql-dataparser-connector"></a><span data-ttu-id="88d41-129">Étape 1 : Configurer un connecteur DataParser SQL’analyseur de données</span><span class="sxs-lookup"><span data-stu-id="88d41-129">Step 1: Set up a SQL DataParser connector</span></span>

<span data-ttu-id="88d41-130">La première étape consiste à accéder à la page Connecteurs de données dans le Centre de conformité Microsoft 365 et à créer un connecteur 17a-4 pour SQL données.</span><span class="sxs-lookup"><span data-stu-id="88d41-130">The first step is to access to the Data connectors page in the Microsoft 365 compliance center and create a 17a-4 connector for SQL data.</span></span>

1. <span data-ttu-id="88d41-131">Go to <https://compliance.microsoft.com> and then click Data **connectors**  >  **SQL DataParser**.</span><span class="sxs-lookup"><span data-stu-id="88d41-131">Go to <https://compliance.microsoft.com> and then click **Data connectors** > **SQL DataParser**.</span></span>

2. <span data-ttu-id="88d41-132">Dans la page SQL description du produit **DataParser,** cliquez **sur Ajouter un connecteur.**</span><span class="sxs-lookup"><span data-stu-id="88d41-132">On the **SQL DataParser** product description page, click **Add connector**.</span></span>

3. <span data-ttu-id="88d41-133">Dans la page **Conditions d’utilisation,** cliquez sur **Accepter.**</span><span class="sxs-lookup"><span data-stu-id="88d41-133">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="88d41-134">Entrez un nom unique qui identifie le connecteur, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="88d41-134">Enter a unique name that identifies the connector and then click **Next**.</span></span>

5. <span data-ttu-id="88d41-135">Connectez-vous à votre compte 17a-4 et complétez les étapes de l SQL de connexion DataParser.</span><span class="sxs-lookup"><span data-stu-id="88d41-135">Sign in to your 17a-4 account and complete the steps in the SQL DataParser connection wizard.</span></span>

## <a name="step-2-configure-the-sql-dataparser-connector"></a><span data-ttu-id="88d41-136">Étape 2 : Configurer le connecteur SQL DataParser</span><span class="sxs-lookup"><span data-stu-id="88d41-136">Step 2: Configure the SQL DataParser connector</span></span>

<span data-ttu-id="88d41-137">Travaillez avec la prise en charge 17a-4 pour configurer SQL connecteur DataParser.</span><span class="sxs-lookup"><span data-stu-id="88d41-137">Work with 17a-4 Support to configure the SQL DataParser connector.</span></span>

## <a name="step-3-map-users"></a><span data-ttu-id="88d41-138">Étape 3 : Ma cartographier les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="88d41-138">Step 3: Map users</span></span>

<span data-ttu-id="88d41-139">Le SQL DataParser masique automatiquement les utilisateurs à leurs adresses Microsoft 365 courrier avant d’importer des données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-139">The SQL DataParser connector will automatically map users to their Microsoft 365 email addresses before importing data to Microsoft 365.</span></span>

## <a name="step-4-monitor-the-sql-dataparser-connector"></a><span data-ttu-id="88d41-140">Étape 4 : Surveiller le connecteur SQL DataParser</span><span class="sxs-lookup"><span data-stu-id="88d41-140">Step 4: Monitor the SQL DataParser connector</span></span>

<span data-ttu-id="88d41-141">Après avoir créé un SQL DataParser, vous pouvez afficher l’état du connecteur dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="88d41-141">After you create a SQL DataParser connector, you can view the connector status in the Microsoft 365 compliance center.</span></span>

1. <span data-ttu-id="88d41-142">Go to <https://compliance.microsoft.com> and click **Data connectors** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="88d41-142">Go to <https://compliance.microsoft.com> and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="88d41-143">Cliquez sur **l’onglet Connecteurs,** puis sélectionnez le connecteur DataParser SQL que vous avez créé pour afficher la page de présentation, qui contient les propriétés et les informations sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="88d41-143">Click the **Connectors** tab and then select the SQL DataParser connector that you created to display the flyout page, which contains the properties and information about the connector.</span></span>

3. <span data-ttu-id="88d41-144">Sous **État du connecteur avec source,** cliquez sur le lien Télécharger le journal pour ouvrir (ou enregistrer) le journal d’état du connecteur. </span><span class="sxs-lookup"><span data-stu-id="88d41-144">Under **Connector status with source**, click the **Download log** link to open (or save) the status log for the connector.</span></span> <span data-ttu-id="88d41-145">Ce journal contient des données qui ont été importées dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88d41-145">This log contains data that has been imported to the Microsoft cloud.</span></span>

## <a name="known-issues"></a><span data-ttu-id="88d41-146">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="88d41-146">Known issues</span></span>

<span data-ttu-id="88d41-147">Pour l’instant, l’importation de pièces jointes ou d’éléments dont la taille est supérieure à 10 Mo n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="88d41-147">At this time, we don't support importing attachments or items that are larger than 10 MB.</span></span> <span data-ttu-id="88d41-148">La prise en charge des éléments plus volumineux sera disponible à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88d41-148">Support for larger items will be available at a later date.</span></span>
