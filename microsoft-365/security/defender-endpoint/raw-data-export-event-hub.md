---
title: Diffuser des événements Microsoft Defender for Endpoint vers des Hubs d’événements Azure
description: Découvrez comment configurer Microsoft Defender ATP pour diffuser des événements de recherche avancée vers votre Hub d’événements.
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
ms.openlocfilehash: 231ba79e1d66eee263b6c1a4335f0a7b54eeb75d
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51063870"
---
# <a name="configure-microsoft-defender-for-endpoint-to-stream-advanced-hunting-events-to-your-azure-event-hubs"></a><span data-ttu-id="156b9-104">Configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers vos Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="156b9-104">Configure Microsoft Defender for Endpoint to stream Advanced Hunting events to your Azure Event Hubs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="156b9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="156b9-105">**Applies to:**</span></span>

- [<span data-ttu-id="156b9-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="156b9-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="156b9-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="156b9-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="156b9-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="156b9-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="before-you-begin"></a><span data-ttu-id="156b9-109">Avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="156b9-109">Before you begin:</span></span>

1. <span data-ttu-id="156b9-110">Créez [un hub d’événements](https://docs.microsoft.com/azure/event-hubs/) dans votre client.</span><span class="sxs-lookup"><span data-stu-id="156b9-110">Create an [event hub](https://docs.microsoft.com/azure/event-hubs/) in your tenant.</span></span>

2. <span data-ttu-id="156b9-111">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)go to \*\*Subscriptions > Your subscription > Resource Providers > Register to **Microsoft.insights**.</span><span class="sxs-lookup"><span data-stu-id="156b9-111">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to \*\*Subscriptions > Your subscription > Resource Providers > Register to **Microsoft.insights**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="156b9-112">Activer la diffusion en continu des données brutes :</span><span class="sxs-lookup"><span data-stu-id="156b9-112">Enable raw data streaming:</span></span>

1. <span data-ttu-id="156b9-113">Connectez-vous au [Centre de](https://securitycenter.windows.com) sécurité Microsoft Defender en tant qu’administrateur général \* ou _\*_administrateur_ de sécurité \*\*.</span><span class="sxs-lookup"><span data-stu-id="156b9-113">Log in to the [Microsoft Defender Security Center](https://securitycenter.windows.com) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="156b9-114">Go to the [Data export settings page](https://securitycenter.windows.com/interoperability/dataexport) on Microsoft Defender Security Center.</span><span class="sxs-lookup"><span data-stu-id="156b9-114">Go to the [Data export settings page](https://securitycenter.windows.com/interoperability/dataexport) on Microsoft Defender Security Center.</span></span>

3. <span data-ttu-id="156b9-115">Cliquez sur **Ajouter des paramètres d’exportation de données.**</span><span class="sxs-lookup"><span data-stu-id="156b9-115">Click on **Add data export settings**.</span></span>

4. <span data-ttu-id="156b9-116">Choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="156b9-116">Choose a name for your new settings.</span></span>

5. <span data-ttu-id="156b9-117">Choose **Forward events to Azure Event Hubs**.</span><span class="sxs-lookup"><span data-stu-id="156b9-117">Choose **Forward events to Azure Event Hubs**.</span></span>

6. <span data-ttu-id="156b9-118">Tapez le **nom de vos Hubs d’événements** et votre ID de ressource Event **Hubs.**</span><span class="sxs-lookup"><span data-stu-id="156b9-118">Type your **Event Hubs name** and your **Event Hubs resource ID**.</span></span>

   <span data-ttu-id="156b9-119">Pour obtenir votre ID de ressource **Event Hubs,** rendez-vous sur votre page d’espace de noms Azure Event Hubs sous l’onglet Propriétés [d’Azure](https://ms.portal.azure.com/) > > copiez le texte sous **L’ID** de ressource :</span><span class="sxs-lookup"><span data-stu-id="156b9-119">In order to get your **Event Hubs resource ID**, go to your Azure Event Hubs namespace page on [Azure](https://ms.portal.azure.com/) > properties tab > copy the text under **Resource ID**:</span></span>

   ![Image de l’ID1 de ressource du hub d’événements](images/event-hub-resource-id.png)

7. <span data-ttu-id="156b9-121">Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="156b9-121">Choose the events you want to stream and click **Save**.</span></span>

## <a name="the-schema-of-the-events-in-azure-event-hubs"></a><span data-ttu-id="156b9-122">Schéma des événements dans les Hubs d’événements Azure :</span><span class="sxs-lookup"><span data-stu-id="156b9-122">The schema of the events in Azure Event Hubs:</span></span>

```
{
    "records": [
                    {
                        "time": "<The time WDATP received the event>"
                        "tenantId": "<The Id of the tenant that the event belongs to>"
                        "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
                        "properties": { <WDATP Advanced Hunting event as Json> }
                    }
                    ...
                ]
}
```

- <span data-ttu-id="156b9-123">Chaque message de hub d’événements dans Azure Event Hubs contient la liste des enregistrements.</span><span class="sxs-lookup"><span data-stu-id="156b9-123">Each event hub message in Azure Event Hubs contains list of records.</span></span>

- <span data-ttu-id="156b9-124">Chaque enregistrement contient le nom de l’événement, le moment où Microsoft Defender pour le point de terminaison a reçu l’événement, le client qu’il appartient (vous recevez uniquement les événements de votre client) et l’événement au format JSON dans une propriété appelée **«** properties ».</span><span class="sxs-lookup"><span data-stu-id="156b9-124">Each record contains the event name, the time Microsoft Defender for Endpoint received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "**properties**".</span></span>

- <span data-ttu-id="156b9-125">Pour plus d’informations sur le schéma des événements De Microsoft Defender pour point de [terminaison, voir vue d’ensemble de la recherche avancée.](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="156b9-125">For more information about the schema of Microsoft Defender for Endpoint events, see [Advanced Hunting overview](advanced-hunting-overview.md).</span></span>

- <span data-ttu-id="156b9-126">Dans la recherche avancée, la table **DeviceInfo** comporte une colonne nommée **MachineGroup** qui contient le groupe de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="156b9-126">In Advanced Hunting, the **DeviceInfo** table has a column named **MachineGroup** which contains the group of the device.</span></span> <span data-ttu-id="156b9-127">Ici, chaque événement est également décorée avec cette colonne.</span><span class="sxs-lookup"><span data-stu-id="156b9-127">Here every event will be decorated with this column as well.</span></span> <span data-ttu-id="156b9-128">Pour plus [d’informations,](machine-groups.md) voir Groupes d’appareils.</span><span class="sxs-lookup"><span data-stu-id="156b9-128">See [Device Groups](machine-groups.md) for more information.</span></span>

## <a name="data-types-mapping"></a><span data-ttu-id="156b9-129">Mappage des types de données :</span><span class="sxs-lookup"><span data-stu-id="156b9-129">Data types mapping:</span></span>

<span data-ttu-id="156b9-130">Pour obtenir les types de données pour les propriétés d’événement, faites les choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="156b9-130">To get the data types for event properties do the following:</span></span>

1. <span data-ttu-id="156b9-131">Connectez-vous [au Centre de](https://securitycenter.windows.com) sécurité Microsoft Defender et go to Advanced Hunting [page](https://securitycenter.windows.com/hunting-package).</span><span class="sxs-lookup"><span data-stu-id="156b9-131">Log in to [Microsoft Defender Security Center](https://securitycenter.windows.com) and go to [Advanced Hunting page](https://securitycenter.windows.com/hunting-package).</span></span>

2. <span data-ttu-id="156b9-132">Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="156b9-132">Run the following query to get the data types mapping for each event:</span></span>
 
   ```
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- <span data-ttu-id="156b9-133">Voici un exemple d’événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="156b9-133">Here is an example for Device Info event:</span></span> 

  ![Image de l’ID2 de ressource du hub d’événements](images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="156b9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="156b9-135">Related topics</span></span>
- [<span data-ttu-id="156b9-136">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="156b9-136">Overview of Advanced Hunting</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="156b9-137">API de diffusion en continu microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="156b9-137">Microsoft Defender for Endpoint streaming API</span></span>](raw-data-export.md)
- [<span data-ttu-id="156b9-138">Diffuser des événements Microsoft Defender for Endpoint vers votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="156b9-138">Stream Microsoft Defender for Endpoint events to your Azure storage account</span></span>](raw-data-export-storage.md)
- [<span data-ttu-id="156b9-139">Documentation Azure Event Hubs</span><span class="sxs-lookup"><span data-stu-id="156b9-139">Azure Event Hubs documentation</span></span>](https://docs.microsoft.com/azure/event-hubs/)
- [<span data-ttu-id="156b9-140">Résoudre les problèmes de connectivité : Hubs d’événements Azure</span><span class="sxs-lookup"><span data-stu-id="156b9-140">Troubleshoot connectivity issues - Azure Event Hubs</span></span>](https://docs.microsoft.com/azure/event-hubs/troubleshooting-guide)