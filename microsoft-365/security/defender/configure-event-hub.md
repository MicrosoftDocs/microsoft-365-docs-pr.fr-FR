---
title: Configurer votre Hub d’événements
description: Découvrez comment configurer votre Hub d’événements
keywords: hub d’événements, configurer, informations
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
MS.technology: mde
ms.openlocfilehash: d28ad22721e22dfd0dc5962bd46bab2b45469781
ms.sourcegitcommit: 34c06715e036255faa75c66ebf95c12a85f8ef42
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "52985586"
---
# <a name="configure-your-event-hub"></a><span data-ttu-id="923bd-104">Configurer votre Hub d’événements</span><span class="sxs-lookup"><span data-stu-id="923bd-104">Configure your Event Hub</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="923bd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="923bd-105">**Applies to:**</span></span>
- [<span data-ttu-id="923bd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="923bd-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="923bd-107">Découvrez comment configurer votre Hub d’événements afin qu’il puisse inger des événements à partir Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="923bd-107">Learn how to configure your Event Hub so that it can ingest events from Microsoft 365 Defender.</span></span>


## <a name="setup-the-required-resource-provider-in-the-event-hub-subscription"></a><span data-ttu-id="923bd-108">Configurer le fournisseur de ressources requis dans l’abonnement Event Hub</span><span class="sxs-lookup"><span data-stu-id="923bd-108">Setup the required Resource Provider in the Event Hub subscription</span></span>


1. <span data-ttu-id="923bd-109">Connectez-vous au [Portail Azure](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="923bd-109">Sign in to the [Azure portal](https://portal.azure.com).</span></span>
1. <span data-ttu-id="923bd-110">Select **Subscriptions \> { Select the subscription the event hub will be ***deployed to***} Resource \> providers**.</span><span class="sxs-lookup"><span data-stu-id="923bd-110">Select **Subscriptions \> {***Select the subscription the event hub will be deployed to***} \> Resource providers**.</span></span>
1. <span data-ttu-id="923bd-111">Vérifiez que **le fournisseur Microsoft.Informations** est inscrit.</span><span class="sxs-lookup"><span data-stu-id="923bd-111">Verify that the **Microsoft.Insights** Provider is registered.</span></span> <span data-ttu-id="923bd-112">Sinon, inscrivez-le.</span><span class="sxs-lookup"><span data-stu-id="923bd-112">Otherwise, register it.</span></span>

![Image des fournisseurs de ressources dans Microsoft Azure](../../media/f893db7a7b1f7aa520e8b9257cc72562.png)

## <a name="setup-azure-active-directory-app-registration"></a><span data-ttu-id="923bd-114">Configuration de Azure Active Directory’inscription d’application</span><span class="sxs-lookup"><span data-stu-id="923bd-114">Setup Azure Active Directory App Registration</span></span>


><span data-ttu-id="923bd-115">! [REMARQUE] Vous devez avoir le rôle Administrateur ou Azure Active Directory (AAD) doit être définie pour autoriser les non-administrateurs à inscrire des applications.</span><span class="sxs-lookup"><span data-stu-id="923bd-115">![NOTE] You must have Administrator role or Azure Active Directory (AAD) must be set to allow non-Administrators to register apps.</span></span> <span data-ttu-id="923bd-116">Vous devez également avoir un rôle Propriétaire ou Administrateur d’accès utilisateur pour attribuer un rôle au principal de service.</span><span class="sxs-lookup"><span data-stu-id="923bd-116">You must also have an Owner or User Access Administrator role to assign the service principal a role.</span></span>  
><span data-ttu-id="923bd-117">Pour plus d’informations, voir Créer une application Azure AD & principal de service dans le [portail - Plateforme d’identités Microsoft Documents \| Microsoft](/azure/active-directory/develop/howto-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="923bd-117">For more information, see [Create an Azure AD app & service principal in the portal - Microsoft identity platform \| Microsoft Docs](/azure/active-directory/develop/howto-create-service-principal-portal).</span></span>

1. <span data-ttu-id="923bd-118">Créez une nouvelle inscription (qui crée par nature un principal de service) dans **\> Azure Active Directory’application Nouvelle \> inscription.**</span><span class="sxs-lookup"><span data-stu-id="923bd-118">Create a new registration (which inherently creates a service principal) in **Azure Active Directory \> App registrations \> New registration.**</span></span>

1. <span data-ttu-id="923bd-119">Remplissez le formulaire avec uniquement le nom (aucun URI de redirection n’est requis).</span><span class="sxs-lookup"><span data-stu-id="923bd-119">Fill out the form with just the Name (no Redirect URI is required).</span></span>

    ![Image de l’inscription d’une application](../../media/336bc84e6be23900c43232b4ef0c253c.png)

    ![Image des informations de vue d’ensemble](../../media/06ac04c4ff713c2065cec2ef2f99a294.png)

1. <span data-ttu-id="923bd-122">Créez une secret en cliquant sur **Certificats & Clés secrètes \> client Nouvelle :**</span><span class="sxs-lookup"><span data-stu-id="923bd-122">Create a secret by clicking on **Certificates & secrets \> New client secret**:</span></span>

    ![Image des certificats et des secrets](../../media/d2ef88d3d2310d2c60c294b569cdf02e.png)

>[!WARNING]
><span data-ttu-id="923bd-124">**Vous ne pourrez plus accéder à la secret client, veillez donc à l’enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="923bd-124">**You won't be able to access the client secret again so make sure to save it**.</span></span>

## <a name="setup-event-hub-namespace"></a><span data-ttu-id="923bd-125">Espace de noms Du Hub d’événements d’installation</span><span class="sxs-lookup"><span data-stu-id="923bd-125">Setup Event Hub namespace</span></span>


1. <span data-ttu-id="923bd-126">Créez un espace de noms Event Hub :</span><span class="sxs-lookup"><span data-stu-id="923bd-126">Create an Event Hub Namespace:</span></span>

    <span data-ttu-id="923bd-127">Go **to Event Hubs \> Add** and select the pricing tier, throughput units and Auto-Présoute (requires standard pricing and under features) appropriate for the load you are expecting.</span><span class="sxs-lookup"><span data-stu-id="923bd-127">Go **to Event Hubs \> Add** and select the pricing tier, throughput units and Auto-Inflate (requires standard pricing and under features) appropriate for the load you are expecting.</span></span>  
    <span data-ttu-id="923bd-128">Pour plus d’informations, voir [Tarification - Hubs \| d’événements Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/)</span><span class="sxs-lookup"><span data-stu-id="923bd-128">For more information, see [Pricing - Event Hubs \| Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/)</span></span>

    >[!NOTE]
    > <span data-ttu-id="923bd-129">Vous pouvez utiliser un hub d’événements existant, mais le débit et la mise à l’échelle sont définies au niveau de l’espace de noms. Il est donc recommandé de placer un hub d’événements dans son espace de noms.</span><span class="sxs-lookup"><span data-stu-id="923bd-129">You can use an existing event hub, but the throughput and scaling are set at the namespace level so it is recommended to place an event hub in itsown namespace.</span></span>

   ![Image de l’espace de noms Du Hub d’événements](../../media/ebc4ca37c342ad1da75c4aee4018e51a.png)

1. <span data-ttu-id="923bd-131">Vous aurez également besoin de l’ID de ressource de cet espace de noms Event Hub.</span><span class="sxs-lookup"><span data-stu-id="923bd-131">You will also need the Resource ID of this Event Hub Namespace.</span></span> <span data-ttu-id="923bd-132">Go to your Azure Event Hubs namespace page \> Properties.</span><span class="sxs-lookup"><span data-stu-id="923bd-132">Go to your Azure Event Hubs namespace page \> Properties.</span></span> <span data-ttu-id="923bd-133">Copiez le texte sous L’ID de ressource et enregistrez-le pour l’utiliser dans la section Configuration M365 ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="923bd-133">Copy the text under Resource ID and record it for use during the M365 Configuration section below.</span></span> 

    ![Image des propriétés](../../media/759498162a4e93cbf17c4130d704d164.png)

1. <span data-ttu-id="923bd-135">Une fois l’espace de noms Hub d’événements créé, vous devez ajouter le principal du service d’inscription d’application en tant que lecteur, récepteur de données Azure Event Hubs et utilisateur qui se connectera à Microsoft 365 Defender en tant que collaborateur (cette opération peut également être effectuée au niveau du groupe de ressources ou de l’abonnement).</span><span class="sxs-lookup"><span data-stu-id="923bd-135">Once the Event Hub Namespace is created you will need to add the App Registration Service Principal as Reader, Azure Event Hubs Data Receiver, and the user who will be logging into Microsoft 365 Defender as Contributor (this can also be done at Resource Group or Subscription level).</span></span>

    <span data-ttu-id="923bd-136">Cette tâche est effectuée dans **Event Hubs Namespace \> Access Control (IAM) \>** Add and verify under **Role assignments**:</span><span class="sxs-lookup"><span data-stu-id="923bd-136">This is done in **Event Hubs Namespace \> Access Control (IAM) \> Add** and verify under **Role assignments**:</span></span>

    ![Image du contrôle d’accès](../../media/9c9c29137b90d5858920202d87680d16.png)

## <a name="setup-event-hub"></a><span data-ttu-id="923bd-138">Configurer le Hub d’événements</span><span class="sxs-lookup"><span data-stu-id="923bd-138">Setup Event Hub</span></span>


<span data-ttu-id="923bd-139">**Option 1 :**</span><span class="sxs-lookup"><span data-stu-id="923bd-139">**Option 1:**</span></span>

<span data-ttu-id="923bd-140">Vous pouvez créer un Hub d’événements dans votre espace de noms et tous les types d’événements (Tables) que vous sélectionnez pour l’exportation seront écrits dans ce **hub** d’événements. </span><span class="sxs-lookup"><span data-stu-id="923bd-140">You can create an Event Hub within your Namespace and **all** the Event Types (Tables) you select to export will be written into this **one** Event Hub.</span></span>

<span data-ttu-id="923bd-141">**Option 2 :**</span><span class="sxs-lookup"><span data-stu-id="923bd-141">**Option 2:**</span></span>

<span data-ttu-id="923bd-142">Au lieu d’exporter tous les types d’événements (tables) dans un hub d’événements, vous pouvez exporter chaque table dans un hub d’événements différent à l’intérieur de votre espace de noms Event Hub (un Hub d’événements par type d’événement).</span><span class="sxs-lookup"><span data-stu-id="923bd-142">Instead of exporting all the Event Types (Tables) into one Event Hub, you can export each table into a different Event Hub inside your Event Hub Namespace (one Event Hub per Event Type).</span></span>  

<span data-ttu-id="923bd-143">Dans cette option, Microsoft 365 Defender créera des Hubs d’événements pour vous.</span><span class="sxs-lookup"><span data-stu-id="923bd-143">In this option, Microsoft 365 Defender will create Event Hubs for you.</span></span>  
>[!NOTE]
> <span data-ttu-id="923bd-144">Si vous utilisez un espace de  noms Event Hub qui ne fait pas partie d’un cluster Event Hub, vous ne pourrez choisir que jusqu’à 10 types d’événements (Tables) à exporter dans chaque Paramètres d’exportation que vous définissez, en raison d’une limite Azure de 10 hubs d’événements par espace de noms Event Hub.</span><span class="sxs-lookup"><span data-stu-id="923bd-144">If you are using an Event Hub Namespace that is **not** part of an Event Hub Cluster, you will only be able to choose up to 10 Event Types (Tables) to export in each Export Settings you define, due to an Azure limitation of 10 Event Hubs per Event Hub Namespace.</span></span>

<span data-ttu-id="923bd-145">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="923bd-145">For example:</span></span>

![Image de l’exemple de Hub d’événements](../../media/005c1f6c10c34420d387f594987f9ffe.png)

<span data-ttu-id="923bd-147">Si vous choisissez cette option, vous pouvez passer à la section Configurer [Microsoft 365 Defender pour envoyer des tables de courrier](#configure-microsoft-365-defender-to-send-email-tables) électronique.</span><span class="sxs-lookup"><span data-stu-id="923bd-147">If you choose this option, you can skip to the [Configure Microsoft 365 Defender to send email tables](#configure-microsoft-365-defender-to-send-email-tables) section.</span></span>

<span data-ttu-id="923bd-148">Créez un Hub d’événements dans votre espace de noms en sélectionnant **Hubs d’événements \> + Hub d’événements.**</span><span class="sxs-lookup"><span data-stu-id="923bd-148">Create an Event Hub within your Namespace by selecting **Event Hubs \> + Event Hub**.</span></span>

<span data-ttu-id="923bd-149">Le nombre de partitions autorise un débit supplémentaire via le parallélisme. Il est donc recommandé d’augmenter ce nombre en fonction de la charge que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="923bd-149">The Partition Count allows for additional throughput via parallelism, so it is recommended to increase this number based on the load you are expecting.</span></span>  
<span data-ttu-id="923bd-150">Les valeurs de rétention et de capture des messages par défaut de 1 et De sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="923bd-150">Default Message Retention and Capture values of 1 and Off are recommended.</span></span>

![Image de créer un Hub d’événements](../../media/1db04b8ec02a6298d7cc70419ac6e6a9.png)

<span data-ttu-id="923bd-152">Pour ce Hub d’événements (et non un espace de noms), vous devez configurer une stratégie d’accès partagé avec envoyer, écouter les revendications.</span><span class="sxs-lookup"><span data-stu-id="923bd-152">For this Event Hub (not namespace) you will need to configure a Shared Access Policy with Send, Listen Claims.</span></span> <span data-ttu-id="923bd-153">Cliquez sur vos stratégies d’accès partagé du Hub d’événements **\> \> +** Ajoutez-le, puis donnez-lui un nom de stratégie (non utilisé ailleurs) et vérifiez **Envoyer** et **écouter.**</span><span class="sxs-lookup"><span data-stu-id="923bd-153">Click on your **Event Hub \> Shared access policies \> + Add** and then give it a Policy name (not used elsewhere) and check **Send** and **Listen**.</span></span>

![Image des stratégies d’accès partagé](../../media/1867d13f46dc6a0f4cdae6cf00df24db.png)

## <a name="configure-microsoft-365-defender-to-send-email-tables"></a><span data-ttu-id="923bd-155">Configurer les Microsoft 365 Defender pour envoyer des tables de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="923bd-155">Configure Microsoft 365 Defender to send email tables</span></span>


### <a name="setup-microsoft-365-defender-send-email-tables-to-splunk-via-event-hub"></a><span data-ttu-id="923bd-156">Configurer Microsoft 365 Defender envoyer des tables de messagerie à Splunk via le Hub d’événements</span><span class="sxs-lookup"><span data-stu-id="923bd-156">Setup Microsoft 365 Defender send Email tables to Splunk via Event Hub</span></span>


1. <span data-ttu-id="923bd-157">Connectez-vous Microsoft 365 Defender avec <https://security.microsoft.com> un compte qui répond à toutes les exigences de rôle suivantes :</span><span class="sxs-lookup"><span data-stu-id="923bd-157">Login to Microsoft 365 Defender at <https://security.microsoft.com> with an account that meets all the following role requirements:</span></span>

    - <span data-ttu-id="923bd-158">Rôle de collaborateur au niveau de la ressource d’espace de noms *du* Hub d’événements ou supérieur pour le Hub d’événements vers qui vous allez exporter.</span><span class="sxs-lookup"><span data-stu-id="923bd-158">Contributor role at the Event Hub *Namespace* Resource level or higher for the Event Hub that you will be exporting to.</span></span> <span data-ttu-id="923bd-159">Sans cela, vous obtenez une erreur d’exportation lorsque vous essayez d’enregistrer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="923bd-159">Without this you will get an export error when you try to save the settings.</span></span>

    - <span data-ttu-id="923bd-160">Rôle d’administrateur global ou d’administrateur de sécurité sur le client lié à Microsoft 365 Defender azure.</span><span class="sxs-lookup"><span data-stu-id="923bd-160">Global Admin or Security Admin Role on the tenant tied to Microsoft 365 Defender and Azure.</span></span>

    ![Image du portail de sécurité](../../media/55d5b1c21dd58692fb12a6c1c35bd4fa.png)

1. <span data-ttu-id="923bd-162">Cliquez sur **Exportation de données \> brutes +Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="923bd-162">Click on **Raw Data Export \> +Add**.</span></span>

    <span data-ttu-id="923bd-163">Vous allez maintenant utiliser les données que vous avez enregistrées ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="923bd-163">You will now use the data that your recorded above.</span></span>

    <span data-ttu-id="923bd-164">**Nom**: il s’agit d’un environnement local qui doit être tout ce qui fonctionne dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="923bd-164">**Name**: This is local and should be whatever works in your environment.</span></span>

    <span data-ttu-id="923bd-165">**Forward events to event hub**: Select this checkbox.</span><span class="sxs-lookup"><span data-stu-id="923bd-165">**Forward events to event hub**: Select this checkbox.</span></span>

    <span data-ttu-id="923bd-166">**ID de ressource Event-Hub**: il s’agit de l’ID de ressource d’espace de noms Event Hub que vous avez enregistré ci-dessus lors de la configuration du Hub d’événements.</span><span class="sxs-lookup"><span data-stu-id="923bd-166">**Event-Hub Resource ID**: This is the Event Hub Namespace Resource ID you  recorded above when you setup the Event Hub.</span></span>

    <span data-ttu-id="923bd-167">**Nom du Hub** d’événements : si vous avez créé un Hub d’événements à l’intérieur de votre espace de noms Event Hub, collez le nom du Hub d’événements que vous avez enregistré ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="923bd-167">**Event-Hub name**:  If you created an Event Hub inside your Event Hub Namespace, paste the Event Hub  name you recorded above.</span></span>

    <span data-ttu-id="923bd-168">Si vous choisissez de laisser Microsoft 365 Defender créer des hubs d’événements par types d’événements (Tables) pour vous, laissez ce champ vide.</span><span class="sxs-lookup"><span data-stu-id="923bd-168">If you choose to let Microsoft 365 Defender to create Event Hubs per Event Types  (Tables) for you, leave this field empty.</span></span>

    <span data-ttu-id="923bd-169">**Types** d’événements : sélectionnez les tables de recherche avancée que vous souhaitez faire suivre au Hub d’événements, puis à votre application personnalisée.</span><span class="sxs-lookup"><span data-stu-id="923bd-169">**Event Types**: Select the Advanced Hunting tables that you want to forward to the Event Hub and then on to your custom app.</span></span> <span data-ttu-id="923bd-170">Les tables d’alerte sont Microsoft 365 Defender, les tables Périphériques sont de Microsoft Defender pour point de terminaison (PEPT) et les tables de messagerie sont de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="923bd-170">Alert tables are from Microsoft 365 Defender, Devices tables are from Microsoft Defender for Endpoint (EDR), and Email tables are from Microsoft Defender for Office 365.</span></span> <span data-ttu-id="923bd-171">Les événements de messagerie enregistrent toutes les transactions de messagerie.</span><span class="sxs-lookup"><span data-stu-id="923bd-171">Email Events records all Email Transactions.</span></span> <span data-ttu-id="923bd-172">Les événements URL (SafeLinks), Attachment (Safe Attachments) et POST Delivery Events (ZAP) sont également enregistrés et peuvent être joints aux événements de messagerie sur le champ NetworkMessageId.</span><span class="sxs-lookup"><span data-stu-id="923bd-172">The URL (SafeLinks), Attachment (Safe Attachments) and Post Delivery Events (ZAP) are also recorded and can be joined to the Email Events on the NetworkMessageId field.</span></span>

    ![Image des paramètres de l’API de diffusion en continu](../../media/3b2ad64b6ef0f88cf0175f8d57ef8b97.png)

1. <span data-ttu-id="923bd-174">Veillez à cliquer sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="923bd-174">Make sure to click **Submit**.</span></span>

### <a name="verify-that-the-events-are-being-exported-to-the-event-hub"></a><span data-ttu-id="923bd-175">Vérifier que les événements sont exportés vers le Hub d’événements</span><span class="sxs-lookup"><span data-stu-id="923bd-175">Verify that the events are being exported to the Event Hub</span></span>


<span data-ttu-id="923bd-176">Vous pouvez vérifier que les événements sont envoyés au Hub d’événements en exécutant une requête de recherche avancée de base.</span><span class="sxs-lookup"><span data-stu-id="923bd-176">You can verify that events are being sent to the Event Hub by running a basic Advanced Hunting query.</span></span> <span data-ttu-id="923bd-177">Sélectionnez **Une requête de recherche avancée \> \> et** entrez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="923bd-177">Select **Hunting \> Advanced Hunting \> Query** and enter the following query:</span></span>

```
EmailEvents
|joinkind=fullouterEmailAttachmentInfoonNetworkMessageId
|joinkind=fullouterEmailUrlInfoonNetworkMessageId
|joinkind=fullouterEmailPostDeliveryEventsonNetworkMessageId
|whereTimestamp\>ago(1h)
|count
```

<span data-ttu-id="923bd-178">Cela vous indique le nombre d’e-mails reçus au cours de la dernière heure, joints à tous les autres tableaux.</span><span class="sxs-lookup"><span data-stu-id="923bd-178">This will show you how many emails were received in the last hour joined across all the other tables.</span></span> <span data-ttu-id="923bd-179">Elle vous indique également si vous voyez des événements qui peuvent être exportés vers le hub d’événements.</span><span class="sxs-lookup"><span data-stu-id="923bd-179">It will also show you if you are seeing events that could be exported to the event hub.</span></span> <span data-ttu-id="923bd-180">Si ce nombre indique 0, vous ne verrez aucune donnée sortante vers le Hub d’événements.</span><span class="sxs-lookup"><span data-stu-id="923bd-180">If this count shows 0 then you won't see any data going out to the Event Hub.</span></span>

![Image de recherche avancée](../../media/c305e57dc6f72fa9eb035943f244738e.png)

<span data-ttu-id="923bd-182">Une fois que vous avez vérifié qu’il existe des données à exporter, vous pouvez afficher le Hub d’événements pour vérifier que les messages sont entrants.</span><span class="sxs-lookup"><span data-stu-id="923bd-182">Once you have verified there is data to export, you can view the Event Hub to verify that messages are incoming.</span></span> <span data-ttu-id="923bd-183">Cela peut prendre jusqu’à une heure.</span><span class="sxs-lookup"><span data-stu-id="923bd-183">This can take up to one hour.</span></span> 
 
1. <span data-ttu-id="923bd-184">Dans Azure, go to **Event Hubs \> Click on the Namespace Event \> Hubs Click on the Event \> Hub**.</span><span class="sxs-lookup"><span data-stu-id="923bd-184">In Azure, go to **Event Hubs \> Click on the Namespace \> Event Hubs \> Click on the Event Hub**.</span></span>  
1. <span data-ttu-id="923bd-185">Sous **Vue d’ensemble,** faites défiler vers le bas et dans le graphique Messages, vous devriez voir les messages entrants.</span><span class="sxs-lookup"><span data-stu-id="923bd-185">Under **Overview**, scroll down and in the Messages graph you should see Incoming Messages.</span></span> <span data-ttu-id="923bd-186">Si vous ne voyez aucun résultat, il n’y aura aucun message pour l’ing d’une application personnalisée.</span><span class="sxs-lookup"><span data-stu-id="923bd-186">If you don't see any results, then there will be no messages for your custom app to ingest.</span></span>

    ![Image de l’onglet Vue d’ensemble avec des messages](../../media/e88060e315d76e74269a3fc866df047f.png)
