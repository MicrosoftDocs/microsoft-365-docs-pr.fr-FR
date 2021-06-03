---
title: Diffuser des Microsoft 365 Defender aux Hubs d’événements Azure
description: Découvrez comment configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers votre Hub d’événements.
keywords: exportation de données brutes, API de diffusion en continu, API, Hubs d’événements Azure, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
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
ms.openlocfilehash: e2ede14d6b93a61bc232d42b5926c6adb7c9585f
ms.sourcegitcommit: cc9e3cac6af23f20d7cc5ac6fc6f6e01bc3cc5c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52736323"
---
# <a name="configure-microsoft-365-defender-to-stream-advanced-hunting-events-to-your-azure-event-hubs"></a><span data-ttu-id="f108b-104">Configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers vos Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="f108b-104">Configure Microsoft 365 Defender to stream Advanced Hunting events to your Azure Event Hubs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="f108b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f108b-105">**Applies to:**</span></span>
- [<span data-ttu-id="f108b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f108b-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="before-you-begin"></a><span data-ttu-id="f108b-107">Avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="f108b-107">Before you begin:</span></span>

1. <span data-ttu-id="f108b-108">Créez [un hub d’événements](/azure/event-hubs/) dans votre client.</span><span class="sxs-lookup"><span data-stu-id="f108b-108">Create an [event hub](/azure/event-hubs/) in your tenant.</span></span>

2. <span data-ttu-id="f108b-109">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)allez à Abonnements > Votre abonnement > fournisseurs de ressources **> s’inscrire à Microsoft.Insights**.</span><span class="sxs-lookup"><span data-stu-id="f108b-109">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to **Subscriptions > Your subscription > Resource Providers > Register to Microsoft.Insights**.</span></span>

3. <span data-ttu-id="f108b-110">Créez un espace de noms Hub d’événements, sélectionnez **Hubs** d’événements > Ajoutez et sélectionnez le niveau de tarification, les unités de débit et la fonction de resserrement automatique adaptée à la charge attendue.</span><span class="sxs-lookup"><span data-stu-id="f108b-110">Create an Event Hub Namespace, go to **Event Hubs > Add** and select the pricing tier, throughput units and Auto-Inflate appropriate for expected load.</span></span> <span data-ttu-id="f108b-111">Pour plus d’informations, voir [Tarification - Hubs d’événements | Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/).</span><span class="sxs-lookup"><span data-stu-id="f108b-111">For more information, see [Pricing - Event Hubs | Microsoft Azure](https://azure.microsoft.com/en-us/pricing/details/event-hubs/).</span></span>  

4. <span data-ttu-id="f108b-112">Une fois l’espace de noms hub d’événements créé, vous devez ajouter le principal du service d’inscription d’application en tant que lecteur, récepteur de données Azure Event Hubs et utilisateur qui se connectera à Microsoft 365 Defender en tant que collaborateur (cette opération peut également être effectuée au niveau du groupe de ressources ou de l’abonnement).</span><span class="sxs-lookup"><span data-stu-id="f108b-112">Once the event hub namespace is created you will need to add the App Registration Service Principal as Reader, Azure Event Hubs Data Receiver and the user who will be logging into Microsoft 365 Defender as Contributor (this can also be done at Resource Group or Subscription level).</span></span> <span data-ttu-id="f108b-113">Accédez à l’espace de noms Hubs d'> contrôle d’accès **(IAM) >** ajouter et vérifier sous **Attributions de rôles**.</span><span class="sxs-lookup"><span data-stu-id="f108b-113">Go to **Event hubs namespace > Access control (IAM) > Add** and verify under **Role assignements**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="f108b-114">Activez la diffusion en continu des données brutes :</span><span class="sxs-lookup"><span data-stu-id="f108b-114">Enable raw data streaming:</span></span>

1. <span data-ttu-id="f108b-115">Connectez-vous au [centre de sécurité Microsoft 365 Defender](https://security.microsoft.com) en tant qu’administrateur général \* ou _\*_administrateur_ de sécurité \*\*.</span><span class="sxs-lookup"><span data-stu-id="f108b-115">Log in to the [Microsoft 365 Defender security center](https://security.microsoft.com) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="f108b-116">Go to the [Data export settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export).</span><span class="sxs-lookup"><span data-stu-id="f108b-116">Go to the [Data export settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export).</span></span>

3. <span data-ttu-id="f108b-117">Cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="f108b-117">Click on **Add**.</span></span>

4. <span data-ttu-id="f108b-118">Choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="f108b-118">Choose a name for your new settings.</span></span>

5. <span data-ttu-id="f108b-119">Choose **Forward events to Azure Event Hubs**.</span><span class="sxs-lookup"><span data-stu-id="f108b-119">Choose **Forward events to Azure Event Hubs**.</span></span>

6. <span data-ttu-id="f108b-120">Vous pouvez choisir d’exporter les données d’événement vers un hub d’événements unique ou d’exporter chaque table d’événements vers un hub d’événements différent dans votre espace de noms event hub.</span><span class="sxs-lookup"><span data-stu-id="f108b-120">You can select if you want to export the event data to a single event hub, or to export each event table to a different even hub in your event hub namespace.</span></span> 

7. <span data-ttu-id="f108b-121">Pour exporter les données d’événement vers un hub d’événements unique, entrez **le** nom de votre Hub d’événements et votre **ID de ressource Hub d’événements.**</span><span class="sxs-lookup"><span data-stu-id="f108b-121">To export the event data to a single event hub, Enter your **Event Hub name** and your **Event Hub resource ID**.</span></span>

   <span data-ttu-id="f108b-122">Pour obtenir votre ID de ressource **Event Hubs,** go to your Azure Event Hubs namespace page on [Azure](https://ms.portal.azure.com/)  >  **Properties** tab > copy the text under **Resource ID:**</span><span class="sxs-lookup"><span data-stu-id="f108b-122">To get your **Event Hubs resource ID**, go to your Azure Event Hubs namespace page on [Azure](https://ms.portal.azure.com/) > **Properties** tab > copy the text under **Resource ID**:</span></span>

   ![Image de l’ID1 de ressource du hub d’événements](images/event-hub-resource-id.png)

8. <span data-ttu-id="f108b-124">Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="f108b-124">Choose the events you want to stream and click **Save**.</span></span>

## <a name="the-schema-of-the-events-in-azure-event-hubs"></a><span data-ttu-id="f108b-125">Schéma des événements dans les Hubs d’événements Azure :</span><span class="sxs-lookup"><span data-stu-id="f108b-125">The schema of the events in Azure Event Hubs:</span></span>

```
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

- <span data-ttu-id="f108b-126">Chaque message de hub d’événements dans Azure Event Hubs contient la liste des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="f108b-126">Each event hub message in Azure Event Hubs contains list of records.</span></span>

- <span data-ttu-id="f108b-127">Chaque enregistrement contient le nom de l’événement, l’heure à Microsoft 365 Defender a reçu l’événement, le client qu’il appartient (vous recevez uniquement les événements de votre client) et l’événement au format JSON dans une propriété appelée **«** properties ».</span><span class="sxs-lookup"><span data-stu-id="f108b-127">Each record contains the event name, the time Microsoft 365 Defender received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "**properties**".</span></span>

- <span data-ttu-id="f108b-128">Pour plus d’informations sur le schéma des événements Microsoft 365 Defender, voir [vue d’ensemble de la recherche avancée.](../defender/advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="f108b-128">For more information about the schema of Microsoft 365 Defender events, see [Advanced Hunting overview](../defender/advanced-hunting-overview.md).</span></span>

- <span data-ttu-id="f108b-129">Dans la recherche avancée, la table **DeviceInfo** comporte une colonne nommée **MachineGroup** qui contient le groupe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f108b-129">In Advanced Hunting, the **DeviceInfo** table has a column named **MachineGroup** which contains the group of the device.</span></span> <span data-ttu-id="f108b-130">Ici, chaque événement est également décorée avec cette colonne.</span><span class="sxs-lookup"><span data-stu-id="f108b-130">Here every event will be decorated with this column as well.</span></span> 

9. <span data-ttu-id="f108b-131">Pour exporter chaque table d’événements vers un hub d’événements différent, laissez simplement le nom du **hub** d’événements vide et Microsoft 365 Defender fera le reste.</span><span class="sxs-lookup"><span data-stu-id="f108b-131">To export each event table to a different event hub, simply leave the **Event hub name** empty, and Microsoft 365 Defender will do the rest.</span></span>


## <a name="data-types-mapping"></a><span data-ttu-id="f108b-132">Mappage des types de données :</span><span class="sxs-lookup"><span data-stu-id="f108b-132">Data types mapping:</span></span>

<span data-ttu-id="f108b-133">Pour obtenir les types de données pour les propriétés d’événement, faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="f108b-133">To get the data types for event properties do the following:</span></span>

1. <span data-ttu-id="f108b-134">Connectez-vous [Microsoft 365 centre de sécurité et](https://security.microsoft.com) allez à la page Recherche [avancée.](https://security.microsoft.com/hunting-package)</span><span class="sxs-lookup"><span data-stu-id="f108b-134">Log in to [Microsoft 365 security center](https://security.microsoft.com) and go to [Advanced Hunting page](https://security.microsoft.com/hunting-package).</span></span>

2. <span data-ttu-id="f108b-135">Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="f108b-135">Run the following query to get the data types mapping for each event:</span></span>
 
   ```
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- <span data-ttu-id="f108b-136">Voici un exemple d’événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="f108b-136">Here is an example for Device Info event:</span></span> 

  ![Image de l’ID2 de ressource du hub d’événements](images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="f108b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f108b-138">Related topics</span></span>
- [<span data-ttu-id="f108b-139">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="f108b-139">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="f108b-140">Microsoft 365 API de diffusion en continu Defender</span><span class="sxs-lookup"><span data-stu-id="f108b-140">Microsoft 365 Defender streaming API</span></span>](raw-data-export.md)
- [<span data-ttu-id="f108b-141">Diffuser Microsoft 365 événements Defender sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="f108b-141">Stream Microsoft 365 Defender events to your Azure storage account</span></span>](raw-data-export-storage.md)
- [<span data-ttu-id="f108b-142">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="f108b-142">Azure Event Hubs documentation</span></span>](/azure/event-hubs/)
- [<span data-ttu-id="f108b-143">Résoudre les problèmes de connectivité : Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="f108b-143">Troubleshoot connectivity issues - Azure Event Hubs</span></span>](/azure/event-hubs/troubleshooting-guide)
