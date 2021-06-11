---
title: Diffuser des Microsoft 365 Defender dans Azure Event Hub
description: Découvrez comment configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers votre Hub d’événements.
keywords: exportation de données brutes, API de diffusion en continu, API, Hub d’événements Azure, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 6f5d04d35c8c4fec18e1a689c51ecbc32d416adf
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52903815"
---
# <a name="configure-microsoft-365-defender-to-stream-advanced-hunting-events-to-your-azure-event-hub"></a><span data-ttu-id="3b661-104">Configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers votre Hub d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="3b661-104">Configure Microsoft 365 Defender to stream Advanced Hunting events to your Azure Event Hub</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="3b661-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3b661-105">**Applies to:**</span></span>
- [<span data-ttu-id="3b661-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3b661-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="before-you-begin"></a><span data-ttu-id="3b661-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="3b661-107">Before you begin</span></span>

1. <span data-ttu-id="3b661-108">Créez [un hub d’événements](/azure/event-hubs/) dans votre client.</span><span class="sxs-lookup"><span data-stu-id="3b661-108">Create an [Event hub](/azure/event-hubs/) in your tenant.</span></span>

2. <span data-ttu-id="3b661-109">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)allez à Abonnements > Votre abonnement > fournisseurs de ressources **> s’inscrire à Microsoft.Insights**.</span><span class="sxs-lookup"><span data-stu-id="3b661-109">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to **Subscriptions > Your subscription > Resource Providers > Register to Microsoft.Insights**.</span></span>

3. <span data-ttu-id="3b661-110">Créez un espace de noms Hub d’événements, sélectionnez Hub d’événements **>** Ajoutez et sélectionnez le niveau de tarification, les unités de débit et la capacité de resserrement automatique en fonction de la charge attendue.</span><span class="sxs-lookup"><span data-stu-id="3b661-110">Create an Event Hub Namespace, go to **Event Hub > Add** and select the pricing tier, throughput units and Auto-Inflate appropriate for expected load.</span></span> <span data-ttu-id="3b661-111">Pour plus d’informations, voir [Tarification - Hub d’événements | Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/).</span><span class="sxs-lookup"><span data-stu-id="3b661-111">For more information, see [Pricing - Event Hub | Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/).</span></span>  

### <a name="add-contributor-permissions"></a><span data-ttu-id="3b661-112">Ajouter des autorisations de collaborateur</span><span class="sxs-lookup"><span data-stu-id="3b661-112">Add contributor permissions</span></span> 
<span data-ttu-id="3b661-113">Une fois l’espace de noms Hub d’événements créé, vous devez :</span><span class="sxs-lookup"><span data-stu-id="3b661-113">Once the Event Hub namespace is created you will need to:</span></span>
1. <span data-ttu-id="3b661-114">Définissez l’utilisateur qui se connectera à Microsoft 365 Defender en tant que collaborateur.</span><span class="sxs-lookup"><span data-stu-id="3b661-114">Define the user who will be logging into Microsoft 365 Defender as Contributor.</span></span>

2. <span data-ttu-id="3b661-115">Si vous vous connectez à une application, ajoutez le principal du service d’inscription de l’application en tant que lecteur, récepteur de données Azure Event Hub (cette procédure peut également être effectuée au niveau du groupe de ressources ou de l’abonnement).</span><span class="sxs-lookup"><span data-stu-id="3b661-115">If you are connecting to an application, add the App Registration Service Principal as Reader, Azure Event Hub Data Receiver (this can also be done at Resource Group or Subscription level).</span></span> 

    <span data-ttu-id="3b661-116">Accédez à l’espace de noms **Hubs d’événements > contrôle d’accès (IAM) > ajouter** et vérifier sous **attributions de rôles.**</span><span class="sxs-lookup"><span data-stu-id="3b661-116">Go to **Event hubs namespace > Access control (IAM) > Add** and verify under **Role assignments**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="3b661-117">Activer la diffusion en continu des données brutes</span><span class="sxs-lookup"><span data-stu-id="3b661-117">Enable raw data streaming</span></span>

1. <span data-ttu-id="3b661-118">Connectez-vous au [centre de sécurité Microsoft 365 Defender](https://security.microsoft.com) en tant qu’administrateur général \* ou _\*_administrateur_ de sécurité \*\*.</span><span class="sxs-lookup"><span data-stu-id="3b661-118">Log in to the [Microsoft 365 Defender security center](https://security.microsoft.com) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="3b661-119">Go to the [Streaming API settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export).</span><span class="sxs-lookup"><span data-stu-id="3b661-119">Go to the [Streaming API settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export).</span></span>

3. <span data-ttu-id="3b661-120">Cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="3b661-120">Click on **Add**.</span></span>

4. <span data-ttu-id="3b661-121">Choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="3b661-121">Choose a name for your new settings.</span></span>

5. <span data-ttu-id="3b661-122">Choose **Forward events to Azure Event Hub**.</span><span class="sxs-lookup"><span data-stu-id="3b661-122">Choose **Forward events to Azure Event Hub**.</span></span>

6. <span data-ttu-id="3b661-123">Vous pouvez choisir d’exporter les données d’événement vers un hub d’événements unique ou d’exporter chaque table d’événements vers un hub d’événements différent dans votre espace de noms Event Hub.</span><span class="sxs-lookup"><span data-stu-id="3b661-123">You can select if you want to export the event data to a single Event Hub, or to export each event table to a different event hub in your Event Hub namespace.</span></span> 

7. <span data-ttu-id="3b661-124">Pour exporter les données d’événement vers un hub d’événements unique, entrez votre nom de Hub d’événements **et** **votre ID de ressource Hub d’événements.**</span><span class="sxs-lookup"><span data-stu-id="3b661-124">To export the event data to a single Event Hub, enter your **Event Hub name** and your **Event Hub resource ID**.</span></span>

   <span data-ttu-id="3b661-125">Pour obtenir votre ID de ressource **Event Hub,** rendez-vous sur votre page d’espace de noms Azure Event Hub sous l’onglet [Propriétés Azure](https://ms.portal.azure.com/)> copier le texte sous  >   **L’ID de ressource**:</span><span class="sxs-lookup"><span data-stu-id="3b661-125">To get your **Event Hub resource ID**, go to your Azure Event Hub namespace page on [Azure](https://ms.portal.azure.com/) > **Properties** tab > copy the text under **Resource ID**:</span></span>

   ![Image de l’ID1 de la ressource Hub d’événements](../defender-endpoint/images/event-hub-resource-id.png)

8. <span data-ttu-id="3b661-127">Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="3b661-127">Choose the events you want to stream and click **Save**.</span></span>

## <a name="the-schema-of-the-events-in-azure-event-hub"></a><span data-ttu-id="3b661-128">Schéma des événements dans Le Hub d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="3b661-128">The schema of the events in Azure Event Hub</span></span>

```JSON
{
    "records": [
                    {
                        "time": "<The time Microsoft 365 Defender received the event>"
                        "tenantId": "<The Id of the tenant that the event belongs to>"
                        "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
                        "properties": { <Microsoft 365 Defender Advanced Hunting event as Json> }
                    }
                    ...
                ]
}
```

- <span data-ttu-id="3b661-129">Chaque message Event Hub dans Azure Event Hub contient la liste des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="3b661-129">Each Event Hub message in Azure Event Hub contains list of records.</span></span>

- <span data-ttu-id="3b661-130">Chaque enregistrement contient le nom de l’événement, l’heure à Microsoft 365 Defender a reçu l’événement, le client qu’il appartient (vous recevez uniquement les événements de votre client) et l’événement au format JSON dans une propriété appelée **«** properties ».</span><span class="sxs-lookup"><span data-stu-id="3b661-130">Each record contains the event name, the time Microsoft 365 Defender received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "**properties**".</span></span>

- <span data-ttu-id="3b661-131">Pour plus d’informations sur le schéma des événements Microsoft 365 Defender, voir [vue d’ensemble de la recherche avancée.](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="3b661-131">For more information about the schema of Microsoft 365 Defender events, see [Advanced Hunting overview](advanced-hunting-overview.md).</span></span>

- <span data-ttu-id="3b661-132">Dans la recherche avancée, la table **DeviceInfo** comporte une colonne nommée **MachineGroup** qui contient le groupe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3b661-132">In Advanced Hunting, the **DeviceInfo** table has a column named **MachineGroup** which contains the group of the device.</span></span> <span data-ttu-id="3b661-133">Ici, chaque événement est également décorée avec cette colonne.</span><span class="sxs-lookup"><span data-stu-id="3b661-133">Here every event will be decorated with this column as well.</span></span> 




## <a name="data-types-mapping"></a><span data-ttu-id="3b661-134">Mappage des types de données</span><span class="sxs-lookup"><span data-stu-id="3b661-134">Data types mapping</span></span>

<span data-ttu-id="3b661-135">Pour obtenir les types de données pour les propriétés d’événement, faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="3b661-135">To get the data types for event properties do the following:</span></span>

1. <span data-ttu-id="3b661-136">Connectez-vous [Microsoft 365 centre de sécurité et](https://security.microsoft.com) allez à la page Recherche [avancée.](https://security.microsoft.com/hunting-package)</span><span class="sxs-lookup"><span data-stu-id="3b661-136">Log in to [Microsoft 365 security center](https://security.microsoft.com) and go to [Advanced Hunting page](https://security.microsoft.com/hunting-package).</span></span>

2. <span data-ttu-id="3b661-137">Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="3b661-137">Run the following query to get the data types mapping for each event:</span></span>
 
   ```kusto
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- <span data-ttu-id="3b661-138">Voici un exemple d’événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="3b661-138">Here is an example for Device Info event:</span></span> 

  ![Image de l’ID2 de la ressource Hub d’événements](../defender-endpoint/images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="3b661-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b661-140">Related topics</span></span>
- [<span data-ttu-id="3b661-141">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="3b661-141">Overview of Advanced Hunting</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="3b661-142">Microsoft 365 API de diffusion en continu Defender</span><span class="sxs-lookup"><span data-stu-id="3b661-142">Microsoft 365 Defender streaming API</span></span>](streaming-api.md)
- [<span data-ttu-id="3b661-143">Diffuser Microsoft 365 événements Defender sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="3b661-143">Stream Microsoft 365 Defender events to your Azure storage account</span></span>](streaming-api-storage.md)
- [<span data-ttu-id="3b661-144">Documentation Du Hub d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="3b661-144">Azure Event Hub documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="3b661-145">Résoudre les problèmes de connectivité - Hub d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="3b661-145">Troubleshoot connectivity issues - Azure Event Hub</span></span>](/azure/event-hubs/troubleshooting-guide)
