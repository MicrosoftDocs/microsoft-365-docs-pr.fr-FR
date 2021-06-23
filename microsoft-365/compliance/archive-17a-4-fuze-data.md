---
title: Configurer un connecteur pour archiver les données de la fusion dans Microsoft 365
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
description: Découvrez comment configurer et utiliser un connecteur 17a-4 Fuze DataParser pour importer et archiver des données de fuze dans Microsoft 365.
ms.openlocfilehash: eb7e66bf3a8d00431ad7e393471110b36efa8e65
ms.sourcegitcommit: 778103d20a2b4c43e524aa436775764d8d8d4c33
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/23/2021
ms.locfileid: "53096429"
---
# <a name="set-up-a-connector-to-archive-fuze-data-preview"></a><span data-ttu-id="b362b-103">Configurer un connecteur pour archiver les données de la fusion (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="b362b-103">Set up a connector to archive Fuze data (preview)</span></span>

<span data-ttu-id="b362b-104">Utilisez [Fuze DataParser](https://www.17a-4.com/fuze-dataparser/) de 17a-4 LLC pour importer et archiver des données de Fuze vers les boîtes aux lettres des utilisateurs de Microsoft 365 organisation.</span><span class="sxs-lookup"><span data-stu-id="b362b-104">Use the [Fuze DataParser](https://www.17a-4.com/fuze-dataparser/) from 17a-4 LLC to import and archive data from Fuze to user mailboxes in your Microsoft 365 organization.</span></span> <span data-ttu-id="b362b-105">DataParser inclut un connecteur Fuze configuré pour capturer des éléments à partir d’une source de données tierce et importer ces éléments dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-105">The DataParser includes a Fuze connector that's configured to capture items from a third-party data source and import those items to Microsoft 365.</span></span> <span data-ttu-id="b362b-106">Le connecteur Fuze DataParser convertit les données Fuze au format de message électronique, puis importe ces éléments dans les boîtes aux lettres des utilisateurs Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-106">The Fuze DataParser connector converts Fuze data to an email message format and then imports those items to user mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="b362b-107">Une fois les données de l’événement stockées dans les boîtes aux lettres des utilisateurs, vous pouvez appliquer des fonctionnalités de conformité Microsoft 365 telles que la conservation pour litige, eDiscovery, les stratégies et étiquettes de rétention, ainsi que la conformité des communications.</span><span class="sxs-lookup"><span data-stu-id="b362b-107">After Fuze data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation Hold, eDiscovery, retention policies and retention labels, and communication compliance.</span></span> <span data-ttu-id="b362b-108">L’utilisation d’un connecteur Fuze pour importer et archiver des données dans Microsoft 365 peut aider votre organisation à rester conforme aux stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="b362b-108">Using a Fuze connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-fuze-data"></a><span data-ttu-id="b362b-109">Vue d’ensemble des données de l’archivage</span><span class="sxs-lookup"><span data-stu-id="b362b-109">Overview of archiving Fuze data</span></span>

<span data-ttu-id="b362b-110">La vue d’ensemble suivante explique le processus d’utilisation d’un connecteur de données pour archiver les données de fusion dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-110">The following overview explains the process of using a data connector to archive Fuze data in Microsoft 365.</span></span>

![Flux de travail d’archivage pour les données De feu à partir de 17a-4](../media/FuzeDataParserConnectorWorkflow.png)

1. <span data-ttu-id="b362b-112">Votre organisation travaille avec 17a-4 pour configurer l’analyseur de données En cours.</span><span class="sxs-lookup"><span data-stu-id="b362b-112">Your organization works with 17a-4 to set up and configure the Fuze DataParser.</span></span>

2. <span data-ttu-id="b362b-113">Régulièrement, les éléments Fuze sont collectés par DataParser.</span><span class="sxs-lookup"><span data-stu-id="b362b-113">On a regular basis, Fuze items are collected by the DataParser.</span></span> <span data-ttu-id="b362b-114">DataParser convertit également le contenu d’un message au format de message électronique.</span><span class="sxs-lookup"><span data-stu-id="b362b-114">The DataParser also converts the content of a message to an email message format.</span></span>

3. <span data-ttu-id="b362b-115">Le connecteur DataParser que vous créez dans le Centre de conformité Microsoft 365 se connecte à DataParser et transfère les messages vers un emplacement stockage Azure sécurisé dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b362b-115">The Fuze DataParser connector that you create in the Microsoft 365 compliance center connects to DataParser and transfers the messages to a secure Azure Storage location in the Microsoft cloud.</span></span>

4. <span data-ttu-id="b362b-116">Un sous-dossier du dossier Boîte de réception nommé **Fuze DataParser** est créé dans les boîtes aux lettres utilisateur et les éléments Fuze sont importés dans ce dossier.</span><span class="sxs-lookup"><span data-stu-id="b362b-116">A subfolder in the Inbox folder named **Fuze DataParser** is created in the user mailboxes, and the Fuze items are imported to that folder.</span></span> <span data-ttu-id="b362b-117">Le connecteur détermine la boîte aux lettres dans laquelle importer des éléments à l’aide de la valeur de la *propriété Email.*</span><span class="sxs-lookup"><span data-stu-id="b362b-117">The connector determines which mailbox to import items to by using the value of the *Email* property.</span></span> <span data-ttu-id="b362b-118">Chaque élément Fuze contient cette propriété, qui est remplie avec l’adresse e-mail de chaque participant.</span><span class="sxs-lookup"><span data-stu-id="b362b-118">Every Fuze item contains this property, which is populated with the email address of every participant.</span></span>

## <a name="before-you-set-up-a-connector"></a><span data-ttu-id="b362b-119">Avant de configurer un connecteur</span><span class="sxs-lookup"><span data-stu-id="b362b-119">Before you set up a connector</span></span>

- <span data-ttu-id="b362b-120">Créez un compte DataParser pour les connecteurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b362b-120">Create a DataParser account for Microsoft connectors.</span></span> <span data-ttu-id="b362b-121">Pour ce faire, contactez [17a-4 LLC.](https://www.17a-4.com/contact/)</span><span class="sxs-lookup"><span data-stu-id="b362b-121">To do this, contact [17a-4 LLC](https://www.17a-4.com/contact/).</span></span> <span data-ttu-id="b362b-122">Vous devez vous inscrire à ce compte lorsque vous créez le connecteur à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b362b-122">You need to sign into this account when you create the connector in Step 1.</span></span>

- <span data-ttu-id="b362b-123">L’utilisateur qui crée le connecteur Fuze DataParser à l’étape 1 (et le termine à l’étape 3) doit être affecté au rôle Importation/Exportation de boîte aux lettres dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b362b-123">The user who creates the Fuze DataParser connector in Step 1 (and completes it in Step 3) must be assigned to the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="b362b-124">Ce rôle est requis pour ajouter des connecteurs sur la page **Connecteurs de données** dans la Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-124">This role is required to add connectors on the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="b362b-125">Par défaut, ce rôle n’est pas attribué à un groupe de rôles dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b362b-125">By default, this role is not assigned to a role group in Exchange Online.</span></span> <span data-ttu-id="b362b-126">Vous pouvez ajouter le rôle Importation/Exportation de boîte aux lettres au groupe de rôles Gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b362b-126">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="b362b-127">Vous pouvez également créer un groupe de rôles, attribuer le rôle Importation/Exportation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="b362b-127">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="b362b-128">Pour plus d’informations, voir les [sections](/Exchange/permissions-exo/role-groups#modify-role-groups) Créer des groupes de rôles ou Modifier des groupes de rôles dans l’article « Gérer les groupes de rôles dans Exchange Online ». [](/Exchange/permissions-exo/role-groups#create-role-groups)</span><span class="sxs-lookup"><span data-stu-id="b362b-128">For more information, see the [Create role groups](/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="step-1-set-up-a-fuze-dataparser-connector"></a><span data-ttu-id="b362b-129">Étape 1 : Configurer un connecteur Fuze DataParser</span><span class="sxs-lookup"><span data-stu-id="b362b-129">Step 1: Set up a Fuze DataParser connector</span></span>

<span data-ttu-id="b362b-130">La première étape consiste à accéder à la page Connecteurs de données dans le Centre de conformité Microsoft 365 et à créer un connecteur 17a-4 pour les données Fuze.</span><span class="sxs-lookup"><span data-stu-id="b362b-130">The first step is to access to the Data connectors page in the Microsoft 365 compliance center and create a 17a-4 connector for Fuze data.</span></span>

1. <span data-ttu-id="b362b-131">Go to <https://compliance.microsoft.com> and then click Data **connectors**  >  **Fuze DataParser**.</span><span class="sxs-lookup"><span data-stu-id="b362b-131">Go to <https://compliance.microsoft.com> and then click **Data connectors** > **Fuze DataParser**.</span></span>

2. <span data-ttu-id="b362b-132">Dans la page de description du produit **Fuze DataParser,** cliquez **sur Ajouter un connecteur.**</span><span class="sxs-lookup"><span data-stu-id="b362b-132">On the **Fuze DataParser** product description page, click **Add connector**.</span></span>

3. <span data-ttu-id="b362b-133">Dans la page **Conditions d’utilisation,** cliquez sur **Accepter.**</span><span class="sxs-lookup"><span data-stu-id="b362b-133">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="b362b-134">Entrez un nom unique qui identifie le connecteur, puis cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="b362b-134">Enter a unique name that identifies the connector and then click **Next**.</span></span>

5. <span data-ttu-id="b362b-135">Connectez-vous à votre compte 17a-4 et complétez les étapes de l’Assistant De connexion Fuze DataParser.</span><span class="sxs-lookup"><span data-stu-id="b362b-135">Sign in to your 17a-4 account and complete the steps in the Fuze DataParser connection wizard.</span></span>

## <a name="step-2-configure-the-fuze-dataparser-connector"></a><span data-ttu-id="b362b-136">Étape 2 : Configurer le connecteur Fuze DataParser</span><span class="sxs-lookup"><span data-stu-id="b362b-136">Step 2: Configure the Fuze DataParser connector</span></span>

<span data-ttu-id="b362b-137">Travaillez avec la prise en charge 17a-4 pour configurer le connecteur Fuze DataParser.</span><span class="sxs-lookup"><span data-stu-id="b362b-137">Work with 17a-4 Support to configure the Fuze DataParser connector.</span></span>

## <a name="step-3-map-users"></a><span data-ttu-id="b362b-138">Étape 3 : Ma cartographier les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="b362b-138">Step 3: Map users</span></span>

<span data-ttu-id="b362b-139">Le connecteur Fuze DataParser maie automatiquement les utilisateurs à leurs adresses Microsoft 365 courrier avant d’importer des données dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-139">The Fuze DataParser connector will automatically map users to their Microsoft 365 email addresses before importing data to Microsoft 365.</span></span>

## <a name="step-4-monitor-the-fuze-dataparser-connector"></a><span data-ttu-id="b362b-140">Étape 4 : Surveiller le connecteur Fuze DataParser</span><span class="sxs-lookup"><span data-stu-id="b362b-140">Step 4: Monitor the Fuze DataParser connector</span></span>

<span data-ttu-id="b362b-141">Après avoir créé un connecteur Fuze DataParser, vous pouvez afficher l’état du connecteur dans le Centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b362b-141">After you create a Fuze DataParser connector, you can view the connector status in the Microsoft 365 compliance center.</span></span>

1. <span data-ttu-id="b362b-142">Go to <https://compliance.microsoft.com> and click **Data connectors** in the left nav.</span><span class="sxs-lookup"><span data-stu-id="b362b-142">Go to <https://compliance.microsoft.com> and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="b362b-143">Cliquez sur **l’onglet Connecteurs,** puis sélectionnez le connecteur Fuze DataParser que vous avez créé pour afficher la page de présentation, qui contient les propriétés et les informations sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="b362b-143">Click the **Connectors** tab and then select the Fuze DataParser connector that you created to display the flyout page, which contains the properties and information about the connector.</span></span>

3. <span data-ttu-id="b362b-144">Sous **État du connecteur avec source,** cliquez sur le lien Télécharger le journal pour ouvrir (ou enregistrer) le journal d’état du connecteur. </span><span class="sxs-lookup"><span data-stu-id="b362b-144">Under **Connector status with source**, click the **Download log** link to open (or save) the status log for the connector.</span></span> <span data-ttu-id="b362b-145">Ce journal contient des données qui ont été importées dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b362b-145">This log contains data that has been imported to the Microsoft cloud.</span></span>

## <a name="known-issues"></a><span data-ttu-id="b362b-146">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="b362b-146">Known issues</span></span>

<span data-ttu-id="b362b-147">Pour l’instant, l’importation de pièces jointes ou d’éléments dont la taille est supérieure à 10 Mo n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b362b-147">At this time, we don't support importing attachments or items that are larger than 10 MB.</span></span> <span data-ttu-id="b362b-148">La prise en charge des éléments plus volumineux sera disponible à une date ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b362b-148">Support for larger items will be available at a later date.</span></span>
