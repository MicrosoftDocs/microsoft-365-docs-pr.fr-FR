---
title: Configuration d’un connecteur pour l’archivage des données de message Bloomberg
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
ms.collection: M365-security-compliance
description: Les administrateurs peuvent configurer un connecteur de données pour importer et archiver des données à partir de l’outil de messagerie de message Bloomberg dans Microsoft 365. Cela vous permet d’archiver des données provenant de sources de données tierces dans Microsoft 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer les données tierces de votre organisation.
ms.openlocfilehash: 700a0619d2299fc7254628059787478cc0e168fa
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937339"
---
# <a name="set-up-a-connector-to-archive-bloomberg-message-data-preview"></a><span data-ttu-id="c5a78-104">Configuration d’un connecteur pour l’archivage des données de message Bloomberg (aperçu)</span><span class="sxs-lookup"><span data-stu-id="c5a78-104">Set up a connector to archive Bloomberg Message data (preview)</span></span>

<span data-ttu-id="c5a78-105">Utilisez un connecteur de données dans le centre de conformité Microsoft 365 pour importer et archiver des données de messagerie électronique des services financiers à partir de l’outil de collaboration [message Bloomberg](https://www.bloomberg.com/professional/product/collaboration/) .</span><span class="sxs-lookup"><span data-stu-id="c5a78-105">Use a data connector in the Microsoft 365 compliance center to import and archive financial services email data from the [Bloomberg Message](https://www.bloomberg.com/professional/product/collaboration/) collaboration tool.</span></span> <span data-ttu-id="c5a78-106">Une fois que vous avez configuré et configuré un connecteur, celui-ci se connecte au site Bloomberg Secure FTP (SFTP) de votre organisation une fois par jour et importe des éléments de courrier électronique vers des boîtes aux lettres dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-106">After you set up and configure a connector, it connects to your organization's Bloomberg secure FTP (SFTP) site once every day, and imports email items to mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="c5a78-107">Une fois que les données de message Bloomberg sont stockées dans les boîtes aux lettres des utilisateurs, vous pouvez appliquer les fonctionnalités de conformité de Microsoft 365 telles que la conservation pour litige, la recherche de contenu, l’archivage inaltérable, l’audit, la conformité de la communication et les stratégies de rétention de Microsoft 365 aux données de message Bloomberg.</span><span class="sxs-lookup"><span data-stu-id="c5a78-107">After Bloomberg Message data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation hold, content search, In-place archiving, auditing, Communication compliance, and Microsoft 365 retention policies to Bloomberg Message data.</span></span> <span data-ttu-id="c5a78-108">Par exemple, vous pouvez rechercher des messages électroniques de message Bloomberg à l’aide de l’outil de recherche de contenu ou associer la boîte aux lettres qui contient les données de message Bloomberg à un dépositaire dans un cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="c5a78-108">For example, you can search Bloomberg Message emails using the content search tool or associate the mailbox that contains the Bloomberg Message data with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="c5a78-109">L’utilisation d’un connecteur de messages Bloomberg pour importer et archiver des données dans Microsoft 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="c5a78-109">Using a Bloomberg Message connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-bloomberg-message-data"></a><span data-ttu-id="c5a78-110">Vue d’ensemble de l’archivage des données de message Bloomberg</span><span class="sxs-lookup"><span data-stu-id="c5a78-110">Overview of archiving Bloomberg Message data</span></span>

<span data-ttu-id="c5a78-111">La vue d’ensemble suivante décrit le processus d’utilisation d’un connecteur pour archiver les données de message Bloomberg dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-111">The following overview explains the process of using a connector to archive Bloomberg Message data in Microsoft 365.</span></span>

![Processus d’importation et d’archivage des messages Bloomberg](../media/BloombergMessageArchiving.png)

1. <span data-ttu-id="c5a78-113">Votre organisation travaille avec Bloomberg pour configurer un site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-113">Your organization works with Bloomberg to set up a Bloomberg SFTP site.</span></span> <span data-ttu-id="c5a78-114">Vous allez également utiliser Bloomberg pour configurer le message Bloomberg afin de copier les messages électroniques vers le site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-114">You'll also work with Bloomberg to configure Bloomberg Message to copy email messages to the Bloomberg SFTP site.</span></span>

2. <span data-ttu-id="c5a78-115">Une fois toutes les 24 heures, les messages électroniques provenant du message Bloomberg sont copiés sur le site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-115">Once every 24 hours, email messages from Bloomberg Message are copied to the Bloomberg SFTP site.</span></span>

3. <span data-ttu-id="c5a78-116">Le connecteur de messages Bloomberg que vous créez dans le centre de conformité Microsoft 365 se connecte au site de Bloomberg SFTP tous les jours et transfère les messages électroniques des 24 heures précédents vers une zone de stockage Azure sécurisée dans le Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c5a78-116">The Bloomberg Message connector that you create in the Microsoft 365 compliance center connects to the Bloomberg SFTP site every day and transfers the email messages from the previous 24 hours to a secure Azure Storage area in the Microsoft Cloud.</span></span>

4. <span data-ttu-id="c5a78-117">Le connecteur importe les éléments de message électronique dans la boîte aux lettres d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="c5a78-117">The connector imports the email message items to the mailbox of a specific user.</span></span> <span data-ttu-id="c5a78-118">Un nouveau dossier nommé BloombergMessage sera créé dans la boîte aux lettres de l’utilisateur spécifique et les éléments y seront importés.</span><span class="sxs-lookup"><span data-stu-id="c5a78-118">A new folder named BloombergMessage will be created in the specific user's mailbox and the items will be imported to it.</span></span> 

   <span data-ttu-id="c5a78-119">Le connecteur effectue cette opération à l’aide de la valeur de la propriété CorporateEmailAddress.</span><span class="sxs-lookup"><span data-stu-id="c5a78-119">The connector does this by using the value of the CorporateEmailAddress property.</span></span> <span data-ttu-id="c5a78-120">Chaque message électronique contient cette propriété, qui est renseignée avec l’adresse de messagerie de chaque participant du message électronique.</span><span class="sxs-lookup"><span data-stu-id="c5a78-120">Every email message contains this property, which is populated with the email address of every participant of the email message.</span></span> <span data-ttu-id="c5a78-121">Outre le mappage utilisateur automatique à l’aide de la valeur de la propriété *CorporateEmailAddress* , vous pouvez également définir un mappage personnalisé en chargeant un fichier de mappage CSV.</span><span class="sxs-lookup"><span data-stu-id="c5a78-121">In addition to automatic user mapping using the value of the *CorporateEmailAddress* property, you can also define a custom mapping by uploading a CSV mapping file.</span></span> <span data-ttu-id="c5a78-122">Ce fichier de mappage contient un UUID Bloomberg et l’adresse de boîte aux lettres Microsoft 365 correspondante pour chaque utilisateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c5a78-122">This mapping file contains a Bloomberg UUID and the corresponding Microsoft 365 mailbox address for each user in your organization.</span></span> <span data-ttu-id="c5a78-123">Si vous activez le mappage utilisateur automatique et que vous fournissez un mappage personnalisé, pour chaque élément de courrier, le connecteur regarde d’abord le fichier de mappage personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c5a78-123">If you enable automatic user mapping and provide a custom mapping, for every email item the connector will first look at the custom-mapping file.</span></span> <span data-ttu-id="c5a78-124">S’il ne trouve pas d’utilisateur Microsoft 365 valide correspondant à l’UUID Bloomberg d’un utilisateur, le connecteur utilise la propriété *CorporateEmailAddress* de l’élément de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c5a78-124">If it doesn't find a valid Microsoft 365 user that corresponds to a user's Bloomberg UUID, the connector uses the *CorporateEmailAddress* property of the email item.</span></span> <span data-ttu-id="c5a78-125">Si le connecteur ne trouve pas d’utilisateur valide de Microsoft 365 dans le fichier de mappage personnalisé ou dans la propriété *CorporateEmailAddress* de l’élément de courrier, l’élément n’est pas importé.</span><span class="sxs-lookup"><span data-stu-id="c5a78-125">If the connector doesn't find a valid Microsoft 365 user in either the custom-mapping file or the *CorporateEmailAddress* property of the email item, the item won't be imported.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c5a78-126">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c5a78-126">Before you begin</span></span>

<span data-ttu-id="c5a78-127">La plupart des étapes d’implémentation requises pour l’archivage des données de message Bloomberg sont externes à Microsoft 365 et doivent être effectuées avant de pouvoir créer le connecteur dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="c5a78-127">Many of the implementation steps required to archive Bloomberg Message data are external to Microsoft 365 and must be completed before you can create the connector in the compliance center.</span></span>

- <span data-ttu-id="c5a78-128">Votre organisation doit consentir à autoriser le service d’importation Office 365 à accéder aux données de boîte aux lettres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c5a78-128">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="c5a78-129">Pour accepter cette demande, accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365, puis acceptez la demande.</span><span class="sxs-lookup"><span data-stu-id="c5a78-129">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span> <span data-ttu-id="c5a78-130">Vous devez effectuer cette étape avant de pouvoir créer le connecteur de messages Bloomberg à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="c5a78-130">You have to complete this step before you can successfully create the Bloomberg Message connector in Step 3.</span></span>

- <span data-ttu-id="c5a78-131">S’abonner à [Bloomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA).</span><span class="sxs-lookup"><span data-stu-id="c5a78-131">Subscribe to [Bloomberg Anywhere](https://www.bloomberg.com/professional/product/remote-access/?bbgsum-page=DG-WS-PROF-PROD-BBA).</span></span> <span data-ttu-id="c5a78-132">Cette opération est nécessaire afin que vous puissiez vous connecter à Bloomberg Anywhere pour accéder au site Bloomberg SFTP que vous devez configurer et configurer.</span><span class="sxs-lookup"><span data-stu-id="c5a78-132">This is required so that you can log in to Bloomberg Anywhere to access the Bloomberg SFTP site that you have to set up and configure.</span></span>

- <span data-ttu-id="c5a78-133">Configurez un site Bloomberg SFTP (Secure File Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="c5a78-133">Set up a Bloomberg SFTP (Secure file transfer protocol) site.</span></span> <span data-ttu-id="c5a78-134">Après avoir travaillé avec Bloomberg pour configurer le site SFTP, les données du message Bloomberg sont téléchargées sur le site SFTP tous les jours.</span><span class="sxs-lookup"><span data-stu-id="c5a78-134">After working with Bloomberg to set up the SFTP site, data from Bloomberg Message is uploaded to the SFTP site every day.</span></span> <span data-ttu-id="c5a78-135">Le connecteur que vous créez à l’étape 2 se connecte à ce site SFTP et transfère les données de messagerie vers des boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-135">The connector you create in Step 2 connects to this SFTP site and transfers the email data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="c5a78-136">SFTP chiffre également les données de message Bloomberg qui sont envoyées aux boîtes aux lettres pendant le processus de transfert.</span><span class="sxs-lookup"><span data-stu-id="c5a78-136">SFTP also encrypts the Bloomberg Message data that is sent to mailboxes during the transfer process.</span></span>

  <span data-ttu-id="c5a78-137">Pour plus d’informations sur Bloomberg SFTP (également appelé *BB-SFTP*) :</span><span class="sxs-lookup"><span data-stu-id="c5a78-137">For information about Bloomberg SFTP (also called *BB-SFTP*):</span></span>

  - <span data-ttu-id="c5a78-138">Consultez le document « standards de connectivité SFTP » sur le [support Bloomberg](https://www.bloomberg.com/professional/support/documentation/).</span><span class="sxs-lookup"><span data-stu-id="c5a78-138">See the "SFTP Connectivity Standards" document at [Bloomberg Support](https://www.bloomberg.com/professional/support/documentation/).</span></span>

  - <span data-ttu-id="c5a78-139">Contacter le [support client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).</span><span class="sxs-lookup"><span data-stu-id="c5a78-139">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc).</span></span>

   > [!NOTE]
   > <span data-ttu-id="c5a78-140">Si votre organisation a déjà déployé un connecteur pour archiver les données Bloomberg instantanées, vous n’avez pas besoin de configurer un autre site SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-140">If your organization already deployed a connector to archive Instant Bloomberg data, you don't need to set up another SFTP site.</span></span> <span data-ttu-id="c5a78-141">Vous pouvez utiliser le même site SFTP pour le connecteur de messages Bloomberg.</span><span class="sxs-lookup"><span data-stu-id="c5a78-141">You can use the same SFTP site for the Bloomberg Message connector.</span></span>

- <span data-ttu-id="c5a78-142">Une fois que vous avez travaillé avec Bloomberg pour configurer un site SFTP, Bloomberg vous fournira des informations après avoir répondu au message d’implémentation Bloomberg.</span><span class="sxs-lookup"><span data-stu-id="c5a78-142">After you work with Bloomberg to set up an SFTP site, Bloomberg will provide some information to you after you respond to the Bloomberg implementation email message.</span></span> <span data-ttu-id="c5a78-143">Enregistrez une copie des informations suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5a78-143">Save a copy of the following information.</span></span> <span data-ttu-id="c5a78-144">Vous l’utilisez pour configurer un connecteur à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="c5a78-144">You use it to set up a connector in Step 3.</span></span>

  - <span data-ttu-id="c5a78-145">Le code de confirmation, qui est un ID pour votre organisation et est utilisé pour se connecter au site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-145">Firm code, which is an ID for your organization and is used to log in to the Bloomberg SFTP site.</span></span>

  - <span data-ttu-id="c5a78-146">Mot de passe pour votre site Bloomberg SFTP</span><span class="sxs-lookup"><span data-stu-id="c5a78-146">Password for your Bloomberg SFTP site</span></span>

  - <span data-ttu-id="c5a78-147">URL du site de Bloomberg SFTP (par exemple, sftp.bloomberg.com).</span><span class="sxs-lookup"><span data-stu-id="c5a78-147">URL for Bloomberg SFTP site (for example, sftp.bloomberg.com).</span></span> <span data-ttu-id="c5a78-148">En outre, Bloomberg peut également fournir une adresse IP correspondante pour le site de Bloomberg SFTP, qui peut également être utilisée pour configurer le connecteur.</span><span class="sxs-lookup"><span data-stu-id="c5a78-148">In addition, Bloomberg may also provide a corresponding IP address for the Bloomberg SFTP site, which also can be used to set up the connector.</span></span>

  - <span data-ttu-id="c5a78-149">Numéro de port pour le site Bloomberg SFTP</span><span class="sxs-lookup"><span data-stu-id="c5a78-149">Port number for Bloomberg SFTP site</span></span>

- <span data-ttu-id="c5a78-150">L’utilisateur qui crée un connecteur de message Bloomberg à l’étape 3 (et qui télécharge les clés publiques et l’adresse IP à l’étape 1) doit se voir attribuer le rôle d’exportation d’importation de boîte aux lettres dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c5a78-150">The user who creates a Bloomberg Message connector in Step 3 (and who downloads the public keys and IP address in Step 1) must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="c5a78-151">Cela est nécessaire pour ajouter des connecteurs dans la page **connecteurs de données** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-151">This is required to add connectors in the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="c5a78-152">Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c5a78-152">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="c5a78-153">Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="c5a78-153">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="c5a78-154">Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="c5a78-154">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="c5a78-155">Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article « gérer des groupes de rôles dans Exchange Online ».</span><span class="sxs-lookup"><span data-stu-id="c5a78-155">For more information, see the [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>


## <a name="step-1-obtain-ssh-and-pgp-public-keys"></a><span data-ttu-id="c5a78-156">Étape 1 : obtenir des clés publiques SSH et PGP</span><span class="sxs-lookup"><span data-stu-id="c5a78-156">Step 1: Obtain SSH and PGP public keys</span></span>

<span data-ttu-id="c5a78-157">La première étape consiste à obtenir une copie des clés publiques pour le protocole SSH (Secure Shell) et PGP (Pretty bonne confidentialité).</span><span class="sxs-lookup"><span data-stu-id="c5a78-157">The first step is to obtain a copy of the public keys for Secure Shell (SSH) and Pretty Good Privacy (PGP).</span></span> <span data-ttu-id="c5a78-158">Utilisez ces clés à l’étape 2 pour configurer le site Bloomberg SFTP de sorte que le connecteur (que vous créez à l’étape 3) se connecte au site SFTP et transfère les données e-mail du message Bloomberg vers les boîtes aux lettres Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-158">You use these keys in Step 2 to configure the Bloomberg SFTP site to allow the connector (that you create in Step 3) to connect to the SFTP site and transfer the Bloomberg Message email data to Microsoft 365 mailboxes.</span></span> <span data-ttu-id="c5a78-159">Vous pouvez également obtenir une adresse IP dans cette étape, que vous utiliserez lors de la configuration du site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-159">You also obtain an IP address in this step, which you use when configuring the Bloomberg SFTP site.</span></span>

1. <span data-ttu-id="c5a78-160">Accédez à [ https://compliance.microsoft.com\ ] ( https://compliance.microsoft.com) et cliquez sur **connecteurs de données** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="c5a78-160">Go to [https://compliance.microsoft.com\](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="c5a78-161">Sur la page **connecteurs de données** , sous **message Bloomberg**, cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="c5a78-161">On the **Data connectors** page under **Bloomberg Message**, click **View**.</span></span>

3. <span data-ttu-id="c5a78-162">Sur la page Description du produit **Bloomberg message** , cliquez sur **Ajouter un connecteur** .</span><span class="sxs-lookup"><span data-stu-id="c5a78-162">On the **Bloomberg Message** product description page, click **Add connector**</span></span>

4. <span data-ttu-id="c5a78-163">Sur la page **conditions de service** , cliquez sur **accepter**.</span><span class="sxs-lookup"><span data-stu-id="c5a78-163">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="c5a78-164">Sur le **site ajouter des informations d’identification pour Bloomberg SFTP** sous étape 1, cliquez sur les liens **Télécharger la clé SSH**, **Télécharger la clé PGP**et **Télécharger l’adresse IP** pour enregistrer une copie de chaque fichier sur votre ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c5a78-164">On the **Add credentials for Bloomberg SFTP site** under step 1, click the **Download SSH key**, **Download PGP key**, and **Download IP address** links to save a copy of each file to your local computer.</span></span> <span data-ttu-id="c5a78-165">Ces fichiers contiennent les éléments suivants qui sont utilisés pour configurer le site de Bloomberg SFTP à l’étape 2 :</span><span class="sxs-lookup"><span data-stu-id="c5a78-165">These files contain the following items that are used to configure the Bloomberg SFTP site in Step 2:</span></span>

   - <span data-ttu-id="c5a78-166">Clé publique SSH : cette clé permet de configurer le protocole SSH (Secure Shell) pour activer une connexion à distance sécurisée lorsque le connecteur se connecte au site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-166">SSH public key: This key is used to configure Secure Shell (SSH) to enable a secure remote login when the connector connects to the Bloomberg SFTP site.</span></span>

   - <span data-ttu-id="c5a78-167">Clé publique PGP : cette clé permet de configurer le chiffrement des données transférées à partir du site Bloomberg SFTP vers Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-167">PGP public key: This key is used to configure the encryption of data that's transferred from the Bloomberg SFTP site to Microsoft 365.</span></span>

   - <span data-ttu-id="c5a78-168">Adresse IP : le site Bloomberg SFTP est configuré pour accepter une demande de connexion uniquement à partir de cette adresse IP, utilisée par le connecteur de messages Bloomberg que vous créez à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="c5a78-168">IP address: The Bloomberg SFTP site is configured to accept a connection request only from this IP address, which is used by the Bloomberg Message connector that you create in Step 3.</span></span>

6. <span data-ttu-id="c5a78-169">Cliquez sur **Annuler** pour fermer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="c5a78-169">Click **Cancel** to close the wizard.</span></span> <span data-ttu-id="c5a78-170">Vous revenez à cet Assistant à l’étape 3 pour créer le connecteur.</span><span class="sxs-lookup"><span data-stu-id="c5a78-170">You come back to this wizard in Step 3 to create the connector.</span></span>

## <a name="step-2-configure-the-bloomberg-sftp-site"></a><span data-ttu-id="c5a78-171">Étape 2 : configurer le site Bloomberg SFTP</span><span class="sxs-lookup"><span data-stu-id="c5a78-171">Step 2: Configure the Bloomberg SFTP site</span></span>

> [!NOTE]
> <span data-ttu-id="c5a78-172">Comme indiqué précédemment, si votre organisation a déjà configuré un site Bloomberg SFTP pour archiver les données Bloomberg instantanées, vous n’avez pas besoin d’en configurer une autre.</span><span class="sxs-lookup"><span data-stu-id="c5a78-172">As previously stated, if you're organization has previously set up a Bloomberg SFTP site to archive Instant Bloomberg data, you don't have to set up another one.</span></span> <span data-ttu-id="c5a78-173">Vous pouvez spécifier le même site SFTP lors de la création du connecteur à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="c5a78-173">You can specify the same SFTP site when you create the connector in Step 3.</span></span>

<span data-ttu-id="c5a78-174">L’étape suivante consiste à utiliser les clés publiques SSH et PGP, ainsi que l’adresse IP que vous avez obtenue à l’étape 1, pour configurer l’authentification SSH et le chiffrement PGP pour le site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-174">The next step is to use the SSH and PGP public keys and the IP address that you obtained in Step 1 to configure SSH authentication and PGP encryption for the Bloomberg SFTP site.</span></span> <span data-ttu-id="c5a78-175">Cela permet au connecteur de messages Bloomberg que vous créez à l’étape 3 de se connecter au site Bloomberg SFTP et de transférer les données de message Bloomberg à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-175">This lets the Bloomberg Message connector that you create in Step 3 connect to the Bloomberg SFTP site and transfer Bloomberg Message data to Microsoft 365.</span></span> <span data-ttu-id="c5a78-176">Vous devez utiliser le support client Bloomberg pour configurer votre site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-176">You need to work with Bloomberg customer support to set up your Bloomberg SFTP site.</span></span> <span data-ttu-id="c5a78-177">Contactez le support technique de [client Bloomberg](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) pour obtenir de l’aide.</span><span class="sxs-lookup"><span data-stu-id="c5a78-177">Contact [Bloomberg customer support](https://service.bloomberg.com/portal/sessions/new?utm_source=bloomberg-menu&utm_medium=csc) for assistance.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5a78-178">Bloomberg recommande de joindre les trois fichiers que vous avez téléchargés à l’étape 1 à un message électronique et de les envoyer à leur équipe de support technique lorsqu’ils travaillent dessus pour configurer votre site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-178">Bloomberg recommends that you attach the three files that you downloaded in Step 1 to an email message and send it to their customer support team when working with them to set up your Bloomberg SFTP site.</span></span>

## <a name="step-3-create-a-bloomberg-message-connector"></a><span data-ttu-id="c5a78-179">Étape 3 : créer un connecteur de message Bloomberg</span><span class="sxs-lookup"><span data-stu-id="c5a78-179">Step 3: Create a Bloomberg Message connector</span></span>

<span data-ttu-id="c5a78-180">La dernière étape consiste à créer un connecteur de message Bloomberg dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-180">The last step is to create a Bloomberg Message connector in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="c5a78-181">Le connecteur utilise les informations que vous fournissez pour vous connecter au site Bloomberg SFTP et transférer les messages électroniques dans les boîtes aux lettres utilisateur correspondantes dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c5a78-181">The connector uses the information you provide to connect to the Bloomberg SFTP site and transfer email messages to the corresponding user mailbox boxes in Microsoft 365.</span></span>

1. <span data-ttu-id="c5a78-182">Accédez à [https://compliance.microsoft.com](https://compliance.microsoft.com) , puis cliquez sur **connecteurs de données** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="c5a78-182">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com) and click **Data connectors** in the left nav.</span></span>

2. <span data-ttu-id="c5a78-183">Sur la page **connecteurs de données** , sous **message Bloomberg**, cliquez sur **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="c5a78-183">On the **Data connectors** page under **Bloomberg Message**, click **View**.</span></span>

3. <span data-ttu-id="c5a78-184">Sur la page Description du produit **Bloomberg message** , cliquez sur **Ajouter un connecteur** .</span><span class="sxs-lookup"><span data-stu-id="c5a78-184">On the **Bloomberg Message** product description page, click **Add connector**</span></span>

4. <span data-ttu-id="c5a78-185">Sur la page **conditions de service** , cliquez sur **accepter**.</span><span class="sxs-lookup"><span data-stu-id="c5a78-185">On the **Terms of service** page, click **Accept**.</span></span>

5. <span data-ttu-id="c5a78-186">Sur la page **Ajouter des informations d’identification pour le site de Bloomberg SFTP** , sous étape 3, entrez les informations requises dans les zones suivantes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c5a78-186">On the **Add credentials for Bloomberg SFTP site** page, under Step 3, enter the required information in the following boxes and then click **Next**.</span></span>

      - <span data-ttu-id="c5a78-187">**Code de confirmation :** ID de votre organisation utilisé comme nom d’utilisateur pour le site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-187">**Firm code:** The ID for your organization that is used as the username for the Bloomberg SFTP site.</span></span>

      - <span data-ttu-id="c5a78-188">**Mot de passe :** Mot de passe du site Bloomberg SFTP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c5a78-188">**Password:** The password for your organization's Bloomberg SFTP site.</span></span>

      - <span data-ttu-id="c5a78-189">**URL sftp :** URL du site de Bloomberg SFTP (par exemple, sftp.bloomberg.com).</span><span class="sxs-lookup"><span data-stu-id="c5a78-189">**SFTP URL:** The URL for the Bloomberg SFTP site (for example, sftp.bloomberg.com).</span></span>

      - <span data-ttu-id="c5a78-190">**Port sftp :** Numéro de port du site Bloomberg SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-190">**SFTP port:** The port number for the Bloomberg SFTP site.</span></span> <span data-ttu-id="c5a78-191">Le connecteur utilise ce port pour se connecter au site SFTP.</span><span class="sxs-lookup"><span data-stu-id="c5a78-191">The connector uses this port to connect to the SFTP site.</span></span>

6. <span data-ttu-id="c5a78-192">Sur la page **mappage utilisateur** , activez le mappage utilisateur automatique et fournissez un mappage utilisateur personnalisé, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="c5a78-192">On the **User-mapping** page, enable automatic user mapping and provide custom user mapping as required</span></span>

7. <span data-ttu-id="c5a78-193">Cliquez sur **suivant**, vérifiez vos paramètres, puis cliquez sur préparer pour créer le connecteur.</span><span class="sxs-lookup"><span data-stu-id="c5a78-193">Click **Next**, review your settings, and then click prepare to create the connector.</span></span>

8. <span data-ttu-id="c5a78-194">Accédez à la page **connecteurs de données** pour voir la progression du processus d’importation pour le nouveau connecteur.</span><span class="sxs-lookup"><span data-stu-id="c5a78-194">Go to the **Data connectors** page to see the progress of the import process for the new connector.</span></span>

## <a name="known-issues"></a><span data-ttu-id="c5a78-195">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="c5a78-195">Known issues</span></span>

- <span data-ttu-id="c5a78-196">Le Threading du message Bloomberg message importé dans Microsoft 365 n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a78-196">Threading of Bloomberg Message email imported to Microsoft 365 isn't supported.</span></span> <span data-ttu-id="c5a78-197">Les messages individuels envoyés à une personne sont importés, mais ils ne sont pas présentés dans une conversation de thread.</span><span class="sxs-lookup"><span data-stu-id="c5a78-197">Individual messages sent to a person are imported, but they aren't presented in a threaded conversation.</span></span> <span data-ttu-id="c5a78-198">Microsoft s’efforce de prendre en charge le Threading dans les versions ultérieures du connecteur de données de message Bloomberg.</span><span class="sxs-lookup"><span data-stu-id="c5a78-198">Microsoft is working to support threading in later versions of the Bloomberg Message data connector.</span></span>