---
title: Configuration d’un connecteur pour l’archivage des données WhatsApp dans Microsoft 365
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
description: Les administrateurs peuvent configurer un connecteur de télémessage pour importer et archiver des données WhatsApp dans Microsoft 365. Cela vous permet d’archiver des données provenant de sources de données tierces dans Microsoft 365 de sorte que vous puissiez utiliser les fonctionnalités de conformité telles que la conservation légale, la recherche de contenu et les stratégies de rétention pour gérer les données tierces de votre organisation.
ms.openlocfilehash: 072dd5c6ce47d5b7f7572e7ef27815efa2c97b32
ms.sourcegitcommit: d39694d7b2c98350b0d568dfd03fa0ef44ed4c1d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/10/2020
ms.locfileid: "46601911"
---
# <a name="set-up-a-connector-to-archive-whatsapp-data-preview"></a><span data-ttu-id="1aed8-104">Configuration d’un connecteur pour l’archivage des données WhatsApp (aperçu)</span><span class="sxs-lookup"><span data-stu-id="1aed8-104">Set up a connector to archive WhatsApp data (preview)</span></span>

<span data-ttu-id="1aed8-105">Utilisez le connecteur de Télémessage dans le centre de conformité Microsoft 365 pour importer et archiver des appels WhatsApp, des conversations, des pièces jointes, des fichiers et des messages supprimés.</span><span class="sxs-lookup"><span data-stu-id="1aed8-105">Use the TeleMessage connector in the Microsoft 365 compliance center to import and archive WhatsApp calls, chats, attachments, files, and deleted messages.</span></span> <span data-ttu-id="1aed8-106">Une fois que vous avez configuré et configuré un connecteur, celui-ci se connecte au compte de messagerie de votre organisation une fois par jour et importe la communication mobile des employés à l’aide de l’archiveur téléphonique des télémessages WhatsApp ou de l’archivage de Cloud WhatsApp sur les boîtes aux lettres de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-106">After you set up and configure a connector, it connects to your organization's TeleMessage account once every day, and imports the mobile communication of employees using the TeleMessage WhatsApp Phone Archiver or TeleMessage WhatsApp Cloud Archiver to mailboxes in Microsoft 365.</span></span>

<span data-ttu-id="1aed8-107">Une fois que les données WhatsApp sont stockées dans des boîtes aux lettres d’utilisateurs, vous pouvez appliquer des fonctionnalités de conformité de Microsoft 365 telles que la conservation pour litige, la recherche de contenu et les stratégies de rétention de Microsoft 365 aux données Verizon.</span><span class="sxs-lookup"><span data-stu-id="1aed8-107">After WhatsApp data is stored in user mailboxes, you can apply Microsoft 365 compliance features such as Litigation Hold, Content Search, and Microsoft 365 retention policies to Verizon data.</span></span> <span data-ttu-id="1aed8-108">Par exemple, vous pouvez rechercher des messages WhatsApp à l’aide de la recherche de contenu ou associer la boîte aux lettres qui contient des messages WhatsApp à un dépositaire dans un cas avancé de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="1aed8-108">For example, you can search WhatsApp messages using Content Search or associate the mailbox that contains WhatsApp messages with a custodian in an Advanced eDiscovery case.</span></span> <span data-ttu-id="1aed8-109">L’utilisation d’un connecteur WhatsApp pour importer et archiver des données dans Microsoft 365 peut aider votre organisation à respecter les stratégies gouvernementales et réglementaires.</span><span class="sxs-lookup"><span data-stu-id="1aed8-109">Using a WhatsApp connector to import and archive data in Microsoft 365 can help your organization stay compliant with government and regulatory policies.</span></span>

## <a name="overview-of-archiving-whatsapp-data"></a><span data-ttu-id="1aed8-110">Vue d’ensemble des données d’archivage WhatsApp</span><span class="sxs-lookup"><span data-stu-id="1aed8-110">Overview of archiving WhatsApp data</span></span>

<span data-ttu-id="1aed8-111">La vue d’ensemble suivante décrit le processus d’utilisation d’un connecteur pour archiver des données WhatsApp dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-111">The following overview explains the process of using a connector to archive WhatsApp data in Microsoft 365.</span></span>

![Flux de travail d’archivage WhatsApp](../media/WhatsAppConnectorWorkflow.png)

1. <span data-ttu-id="1aed8-113">Votre organisation utilise le télémessage pour configurer un connecteur d’archivage WhatsApp.</span><span class="sxs-lookup"><span data-stu-id="1aed8-113">Your organization works with TeleMessage to set up a WhatsApp Archiver connector.</span></span> <span data-ttu-id="1aed8-114">Pour plus d’informations, consultez la rubrique [WhatsApp archiver](https://www.telemessage.com/office365-activation-for-whatsapp-archiver).</span><span class="sxs-lookup"><span data-stu-id="1aed8-114">For more information, see [WhatsApp Archiver](https://www.telemessage.com/office365-activation-for-whatsapp-archiver).</span></span>

2. <span data-ttu-id="1aed8-115">Une fois toutes les 24 heures, les données WhatsApp de votre organisation sont copiées sur le site de Télémessage.</span><span class="sxs-lookup"><span data-stu-id="1aed8-115">Once every 24 hours, your organization’s WhatsApp data is copied to the TeleMessage site.</span></span>

3. <span data-ttu-id="1aed8-116">Le connecteur WhatsApp que vous créez dans le centre de conformité Microsoft 365 se connecte au site de Télémessage quotidiennement et transfère les données WhatsApp des dernières 24 heures vers un emplacement de stockage Azure sécurisé dans le Cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1aed8-116">The WhatsApp connector that you create in the Microsoft 365 compliance center connects to the TeleMessage site every day and transfers WhatsApp data from the previous 24 hours to a secure Azure Storage location in the Microsoft Cloud.</span></span> <span data-ttu-id="1aed8-117">Le connecteur convertit également les données de WhatsApp de contenu au format d’un message électronique.</span><span class="sxs-lookup"><span data-stu-id="1aed8-117">The connector also converts the content WhatsApp data to an email message format.</span></span>

4. <span data-ttu-id="1aed8-118">Le connecteur importe les données WhatsApp vers la boîte aux lettres d’un utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="1aed8-118">The connector imports WhatsApp data to the mailbox of a specific user.</span></span> <span data-ttu-id="1aed8-119">Un nouveau dossier nommé **WhatsApp archiver** est créé dans la boîte aux lettres de l’utilisateur spécifique et les éléments y sont importés.</span><span class="sxs-lookup"><span data-stu-id="1aed8-119">A new folder named **WhatsApp Archiver** is created in the specific user's mailbox and the items are imported to it.</span></span> <span data-ttu-id="1aed8-120">Le connecteur effectue ce mappage à l’aide de la valeur de la propriété d' *adresse de messagerie* de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1aed8-120">The connector does this mapping by using the value of the *User’s Email address* property.</span></span> <span data-ttu-id="1aed8-121">Chaque message WhatsApp contient cette propriété, qui est renseignée avec l’adresse de messagerie de chaque participant du message.</span><span class="sxs-lookup"><span data-stu-id="1aed8-121">Every WhatsApp message contains this property, which is populated with the email address of every participant of the message.</span></span>

   <span data-ttu-id="1aed8-122">Outre le mappage utilisateur automatique à l’aide de la valeur de la propriété d' *adresse de messagerie* de l’utilisateur, vous pouvez également implémenter un mappage personnalisé en téléchargeant un fichier de mappage CSV.</span><span class="sxs-lookup"><span data-stu-id="1aed8-122">In addition to automatic user mapping using the value of the *User’s Email address* property, you can also implement custom mapping by uploading a CSV mapping file.</span></span> <span data-ttu-id="1aed8-123">Ce fichier de mappage contient le numéro de téléphone mobile et l’adresse de messagerie Microsoft 365 correspondante pour les utilisateurs de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1aed8-123">This mapping file contains the mobile phone number and corresponding Microsoft 365 email address for users in your organization.</span></span> <span data-ttu-id="1aed8-124">Si vous activez le mappage utilisateur et le mappage personnalisés, pour chaque élément WhatsApp, le connecteur examine d’abord le fichier de mappage personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1aed8-124">If you enable both automatic user mapping and custom mapping, for every WhatsApp item the connector first looks at custom mapping file.</span></span> <span data-ttu-id="1aed8-125">S’il ne trouve pas un utilisateur Microsoft 365 valide correspondant au numéro de téléphone mobile d’un utilisateur, le connecteur utilise les valeurs de la propriété adresse de messagerie de l’élément qu’il tente d’importer.</span><span class="sxs-lookup"><span data-stu-id="1aed8-125">If it doesn't find a valid Microsoft 365 user that corresponds to a user's mobile phone number, the connector will use the values in the email address property of the item it's trying to import.</span></span> <span data-ttu-id="1aed8-126">Si le connecteur ne trouve pas d’utilisateur Microsoft 365 valide dans le fichier de mappage personnalisé ou dans la propriété adresse de messagerie de l’élément WhatsApp, l’élément n’est pas importé.</span><span class="sxs-lookup"><span data-stu-id="1aed8-126">If the connector doesn't find a valid Microsoft 365 user in either the custom mapping file or in the email address property of the WhatsApp item, the item won't be imported.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="1aed8-127">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="1aed8-127">Before you begin</span></span>

<span data-ttu-id="1aed8-128">La plupart des étapes d’implémentation nécessaires à l’archivage des données de communication WhatsApp sont externes à Microsoft 365 et doivent être terminées pour que vous puissiez créer le connecteur dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="1aed8-128">Many of the implementation steps required to archive WhatsApp communication data are external to Microsoft 365 and must be completed before you can create the connector in the compliance center.</span></span>

- <span data-ttu-id="1aed8-129">Commandez le [service archiver WhatsApp à partir du Télémessage](https://www.telemessage.com/mobile-archiver/order-mobile-archiver-for-o365) et obtenez un compte d’administration valide pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1aed8-129">Order the [WhatsApp Archiver service from TeleMessage](https://www.telemessage.com/mobile-archiver/order-mobile-archiver-for-o365) and get a valid administration account for your organization.</span></span> <span data-ttu-id="1aed8-130">Vous devez vous connecter à ce compte lorsque vous créez le connecteur dans le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="1aed8-130">You'll need to sign into this account when you create the connector in the compliance center.</span></span>

- <span data-ttu-id="1aed8-131">Inscrivez tous les utilisateurs qui requièrent l’archivage WhatsApp dans le compte de Télémessage.</span><span class="sxs-lookup"><span data-stu-id="1aed8-131">Register all users that require WhatsApp archiving in the TeleMessage account.</span></span> <span data-ttu-id="1aed8-132">Lors de l’inscription des utilisateurs, veillez à utiliser la même adresse de messagerie que celle utilisée pour leur compte Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-132">When registering users, be sure to use the same email address that's used for their Microsoft 365 account.</span></span>

- <span data-ttu-id="1aed8-133">Installez l’application d' [archivage de téléphone WhatsApp](https://www.telemessage.com/mobile-archiver/whatsapp-phone-archiver-2/) TeleMessage sur les téléphones mobiles de vos employés et activez-la.</span><span class="sxs-lookup"><span data-stu-id="1aed8-133">Install the TeleMessage [WhatsApp Phone Archiver app](https://www.telemessage.com/mobile-archiver/whatsapp-phone-archiver-2/) on the mobile phones of your employees and activate it.</span></span> <span data-ttu-id="1aed8-134">Vous pouvez également installer les applications métier WhatsApp ou WhatsApp normales sur les téléphones mobiles de vos employés et activer le service WhatsApp Cloud archiver en numérisant un code QR sur le site Web des télémessages.</span><span class="sxs-lookup"><span data-stu-id="1aed8-134">Alternatively, you can install the regular WhatsApp or WhatsApp Business apps on the mobile phones of your employees and activate the WhatsApp Cloud Archiver service by scanning a QR code on the TeleMessage website.</span></span> <span data-ttu-id="1aed8-135">Pour plus d’informations, consultez la rubrique [WhatsApp Cloud archiver](https://www.telemessage.com/mobile-archiver/whatsapp-archiver/whatsapp-cloud-archiver/).</span><span class="sxs-lookup"><span data-stu-id="1aed8-135">For more information, see [WhatsApp Cloud Archiver](https://www.telemessage.com/mobile-archiver/whatsapp-archiver/whatsapp-cloud-archiver/).</span></span>

- <span data-ttu-id="1aed8-136">Votre organisation doit consentir à autoriser le service d’importation Office 365 à accéder aux données de boîte aux lettres dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1aed8-136">Your organization must consent to allow the Office 365 Import service to access mailbox data in your organization.</span></span> <span data-ttu-id="1aed8-137">Vous devrez fournir ce consentement lors de la création du connecteur.</span><span class="sxs-lookup"><span data-stu-id="1aed8-137">You will need to provide this consent when you create the connector.</span></span> <span data-ttu-id="1aed8-138">Pour accepter cette demande, accédez à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), connectez-vous à l’aide des informations d’identification d’un administrateur général Office 365, puis acceptez la demande.</span><span class="sxs-lookup"><span data-stu-id="1aed8-138">To consent to this request, go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent), sign in with the credentials of an Office 365 global admin, and then accept the request.</span></span> <span data-ttu-id="1aed8-139">Vous devez effectuer cette étape avant de pouvoir créer un connecteur réseau Verizon.</span><span class="sxs-lookup"><span data-stu-id="1aed8-139">You have to complete this step before you can successfully create Verizon Network connector.</span></span>

- <span data-ttu-id="1aed8-140">L’utilisateur qui crée un connecteur réseau Verizon doit disposer du rôle d’exportation d’importation de boîte aux lettres dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1aed8-140">The user who creates a Verizon Network connector must be assigned the Mailbox Import Export role in Exchange Online.</span></span> <span data-ttu-id="1aed8-141">Cela est nécessaire pour ajouter des connecteurs dans la page **connecteurs de données** dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-141">This is required to add connectors in the **Data connectors** page in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="1aed8-142">Par défaut, ce rôle n’est affecté à aucun groupe de rôles dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1aed8-142">By default, this role isn't assigned to any role group in Exchange Online.</span></span> <span data-ttu-id="1aed8-143">Vous pouvez ajouter le rôle exportation d’importation de boîte aux lettres au groupe de rôles gestion de l’organisation dans Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1aed8-143">You can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> <span data-ttu-id="1aed8-144">Vous pouvez aussi créer un groupe de rôles, attribuer le rôle d’exportation d’importation de boîte aux lettres, puis ajouter les utilisateurs appropriés en tant que membres.</span><span class="sxs-lookup"><span data-stu-id="1aed8-144">Or you can create a role group, assign the Mailbox Import Export role, and then add the appropriate users as members.</span></span> <span data-ttu-id="1aed8-145">Pour plus d’informations, reportez-vous aux sections [créer des groupes de rôles](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) ou modifier des [groupes](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) de rôles dans l’article « gérer des groupes de rôles dans Exchange Online ».</span><span class="sxs-lookup"><span data-stu-id="1aed8-145">For more information, see the [Create role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#create-role-groups) or [Modify role groups](https://docs.microsoft.com/Exchange/permissions-exo/role-groups#modify-role-groups) sections in the article "Manage role groups in Exchange Online".</span></span>

## <a name="create-a-whatsapp-archiver-connector"></a><span data-ttu-id="1aed8-146">Créer un connecteur d’archivage WhatsApp</span><span class="sxs-lookup"><span data-stu-id="1aed8-146">Create a WhatsApp Archiver connector</span></span>

<span data-ttu-id="1aed8-147">Une fois que vous avez terminé les conditions préalables décrites dans la section précédente, vous pouvez créer le connecteur WhatsApp dans le centre de conformité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-147">After you've completed the prerequisites described in the previous section, you can create the WhatsApp connector in the Microsoft 365 compliance center.</span></span> <span data-ttu-id="1aed8-148">Le connecteur utilise les informations que vous fournissez pour vous connecter au site de Télémessage et transférer les données WhatsApp vers les boîtes aux lettres utilisateur correspondantes dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1aed8-148">The connector uses the information you provide to connect to the TeleMessage site and transfer the WhatsApp data to the corresponding user mailbox boxes in Microsoft 365.</span></span>

1. <span data-ttu-id="1aed8-149">Accédez à [https://compliance.microsoft.com](https://compliance.microsoft.com/) , puis cliquez sur **Data Connectors**  >  **WhatsApp archiver**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-149">Go to [https://compliance.microsoft.com](https://compliance.microsoft.com/) and then click **Data connectors** > **WhatsApp Archiver**.</span></span>

2. <span data-ttu-id="1aed8-150">Sur la page Description du produit **WhatsApp archiver** , cliquez sur **Ajouter un connecteur** .</span><span class="sxs-lookup"><span data-stu-id="1aed8-150">On the **WhatsApp Archiver** product description page, click **Add connector**</span></span>

3. <span data-ttu-id="1aed8-151">Sur la page **conditions de service** , cliquez sur **accepter**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-151">On the **Terms of service** page, click **Accept**.</span></span>

4. <span data-ttu-id="1aed8-152">Sur la page **connexion à un message** , sous étape 3, entrez les informations requises dans les zones suivantes, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-152">On the **Login to TeleMessage** page, under Step 3, enter the required information in the following boxes and then click **Next**.</span></span>

   - <span data-ttu-id="1aed8-153">**Nom d’utilisateur :** Nom d’utilisateur de votre Télémessage.</span><span class="sxs-lookup"><span data-stu-id="1aed8-153">**Username:** Your TeleMessage username.</span></span>

   - <span data-ttu-id="1aed8-154">**Mot de passe :** Mot de passe de votre Télémessage.</span><span class="sxs-lookup"><span data-stu-id="1aed8-154">**Password:** Your TeleMessage password.</span></span>

5. <span data-ttu-id="1aed8-155">Une fois le connecteur créé, vous pouvez fermer la fenêtre contextuelle et passer à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="1aed8-155">After the connector is created, you can close the pop-up window and go to the next page.</span></span>

6. <span data-ttu-id="1aed8-156">Sur la page mappage de l' **utilisateur** , activez mappage utilisateur automatique, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-156">On the **User mapping** page, enable automatic user mapping and click **Next**.</span></span> <span data-ttu-id="1aed8-157">Si vous avez besoin d’un mappage personnalisé, téléchargez un fichier CSV, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-157">In case you need custom mapping upload a CSV file, and click **Next**.</span></span>

7. <span data-ttu-id="1aed8-158">Fournissez le consentement de l’administrateur, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="1aed8-158">Provide admin consent and then click **Next**.</span></span>

   <span data-ttu-id="1aed8-159">Pour fournir le consentement de l’administrateur, vous devez être connecté avec les informations d’identification d’un administrateur général Office 365, puis accepter la demande de consentement.</span><span class="sxs-lookup"><span data-stu-id="1aed8-159">To provide admin consent, you must be signed in with the credentials of an Office 365 global admin, and then accept the consent request.</span></span> <span data-ttu-id="1aed8-160">Si vous n’êtes pas connecté en tant qu’administrateur général, vous pouvez accéder à [cette page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) et vous connecter à l’aide des informations d’identification d’administrateur général pour accepter la demande.</span><span class="sxs-lookup"><span data-stu-id="1aed8-160">If you aren't signed in as a global admin, you can go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=570d0bec-d001-4c4e-985e-3ab17fdc3073&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign-in using global admin credentials to accept the request.</span></span>

8. <span data-ttu-id="1aed8-161">Vérifiez vos paramètres, puis cliquez sur **Terminer** pour créer le connecteur.</span><span class="sxs-lookup"><span data-stu-id="1aed8-161">Review your settings, and then click **Finish** to create the connector.</span></span>

9. <span data-ttu-id="1aed8-162">Accédez à l’onglet Connecteurs de la page **connecteurs de données** pour voir la progression du processus d’importation pour le nouveau connecteur.</span><span class="sxs-lookup"><span data-stu-id="1aed8-162">Go to the Connectors tab in **Data connectors** page to see the progress of the import process for the new connector.</span></span>

## <a name="known-issues"></a><span data-ttu-id="1aed8-163">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="1aed8-163">Known issues</span></span>

- <span data-ttu-id="1aed8-164">Le connecteur n’importe pas d’élément d’une taille supérieure à 10 Mo.</span><span class="sxs-lookup"><span data-stu-id="1aed8-164">The connector doesn’t import any item larger than 10 MB.</span></span>