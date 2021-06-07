---
title: Diffuser Microsoft 365 événements Defender à votre compte Stockage client
description: Découvrez comment configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée sur Stockage compte.
keywords: exportation de données brutes, API de diffusion en continu, API, Hubs d’événements, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
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
ms.openlocfilehash: 9ec8c286828fd6b551bf76c8340b58c9a1407bba
ms.sourcegitcommit: 83df0be7144c9c5d606f70b4efa65369e86693d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/05/2021
ms.locfileid: "52778208"
---
# <a name="configure--microsoft-365-defender-to-stream-advanced-hunting-events-to-your-storage-account"></a><span data-ttu-id="90490-104">Configurer Microsoft 365 Defender pour diffuser des événements de recherche avancée vers Stockage compte</span><span class="sxs-lookup"><span data-stu-id="90490-104">Configure  Microsoft 365 Defender to stream Advanced Hunting events to your Storage account</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="90490-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="90490-105">**Applies to:**</span></span>
- [<span data-ttu-id="90490-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="90490-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


## <a name="before-you-begin"></a><span data-ttu-id="90490-107">Avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="90490-107">Before you begin:</span></span>

1. <span data-ttu-id="90490-108">Créez [un Stockage dans](/azure/storage/common/storage-account-overview) votre client.</span><span class="sxs-lookup"><span data-stu-id="90490-108">Create a [Storage account](/azure/storage/common/storage-account-overview) in your tenant.</span></span>

2. <span data-ttu-id="90490-109">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)allez à Abonnements > Votre abonnement > fournisseurs de ressources **> s’inscrire à Microsoft.Insights**.</span><span class="sxs-lookup"><span data-stu-id="90490-109">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to **Subscriptions > Your subscription > Resource Providers > Register to Microsoft.Insights**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="90490-110">Activez la diffusion en continu des données brutes :</span><span class="sxs-lookup"><span data-stu-id="90490-110">Enable raw data streaming:</span></span>

1. <span data-ttu-id="90490-111">Connectez-vous [Microsoft 365 centre de sécurité Defender](https://security.microsoft.com) en tant qu’administrateur général \* ou _\*_administrateur_ de sécurité \*\*.</span><span class="sxs-lookup"><span data-stu-id="90490-111">Log in to [Microsoft 365 Defender security center](https://security.microsoft.com) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="90490-112">Go to [Data export settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export) in Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="90490-112">Go to [Data export settings page](https://security.microsoft.com/settings/mtp_settings/raw_data_export) in Microsoft Defender Security Center.</span></span>

3. <span data-ttu-id="90490-113">Cliquez sur **Ajouter des paramètres d’exportation de données.**</span><span class="sxs-lookup"><span data-stu-id="90490-113">Click on **Add data export settings**.</span></span>

4. <span data-ttu-id="90490-114">Choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="90490-114">Choose a name for your new settings.</span></span>

5. <span data-ttu-id="90490-115">Choose **Forward events to stockage Azure**.</span><span class="sxs-lookup"><span data-stu-id="90490-115">Choose **Forward events to Azure Storage**.</span></span>

6. <span data-ttu-id="90490-116">Tapez votre **ID Stockage de ressource de compte.**</span><span class="sxs-lookup"><span data-stu-id="90490-116">Type your **Storage Account Resource ID**.</span></span> <span data-ttu-id="90490-117">Pour obtenir votre ID de ressource de compte **Stockage,** go to your Stockage account page on [Azure portal](https://ms.portal.azure.com/) > properties tab > copy the text under Stockage Account Resource **ID:**</span><span class="sxs-lookup"><span data-stu-id="90490-117">In order to get your **Storage Account Resource ID**, go to your Storage account page on [Azure portal](https://ms.portal.azure.com/) > properties tab > copy the text under **Storage Account Resource ID**:</span></span>

   ![Image de l’ID1 de ressource du hub d’événements](images/storage-account-resource-id.png)

7. <span data-ttu-id="90490-119">Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="90490-119">Choose the events you want to stream and click **Save**.</span></span>

## <a name="the-schema-of-the-events-in-the-storage-account"></a><span data-ttu-id="90490-120">Schéma des événements dans le compte Stockage :</span><span class="sxs-lookup"><span data-stu-id="90490-120">The schema of the events in the Storage account:</span></span>

- <span data-ttu-id="90490-121">Un conteneur d’objets blob est créé pour chaque type d’événement :</span><span class="sxs-lookup"><span data-stu-id="90490-121">A blob container will be created for each event type:</span></span> 

  ![Image de l’ID2 de ressource du hub d’événements](images/storage-account-event-schema.png)

- <span data-ttu-id="90490-123">Le schéma de chaque ligne d’un objet blob est le JSON suivant :</span><span class="sxs-lookup"><span data-stu-id="90490-123">The schema of each row in a blob is the following JSON:</span></span> 

  ```
  {
          "time": "<The time Microsoft 365 Defender received the event>"
          "tenantId": "<Your tenant ID>"
          "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
          "properties": { <Microsoft 365 Defender Advanced Hunting event as Json> }
  }               
  ```

- <span data-ttu-id="90490-124">Chaque objet blob contient plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="90490-124">Each blob contains multiple rows.</span></span>

- <span data-ttu-id="90490-125">Chaque ligne contient le nom de l’événement, le moment où Defender pour le point de terminaison a reçu l’événement, le client qu’il appartient (vous recevez uniquement les événements de votre client) et l’événement au format JSON dans une propriété appelée « properties ».</span><span class="sxs-lookup"><span data-stu-id="90490-125">Each row contains the event name, the time Defender for Endpoint received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "properties".</span></span>

- <span data-ttu-id="90490-126">Pour plus d’informations sur le schéma des événements Microsoft 365 Defender, voir [vue d’ensemble de la recherche avancée.](../defender/advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="90490-126">For more information about the schema of Microsoft 365 Defender events, see [Advanced Hunting overview](../defender/advanced-hunting-overview.md).</span></span>


## <a name="data-types-mapping"></a><span data-ttu-id="90490-127">Mappage des types de données :</span><span class="sxs-lookup"><span data-stu-id="90490-127">Data types mapping:</span></span>

<span data-ttu-id="90490-128">Pour obtenir les types de données pour nos propriétés d’événements, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="90490-128">In order to get the data types for our events properties do the following:</span></span>

1. <span data-ttu-id="90490-129">Connectez-vous [Microsoft 365 centre de sécurité et](https://security.microsoft.com) allez à la page Recherche [avancée.](https://security.microsoft.com/hunting-package)</span><span class="sxs-lookup"><span data-stu-id="90490-129">Log in to [Microsoft 365 security center](https://security.microsoft.com) and go to [Advanced Hunting page](https://security.microsoft.com/hunting-package).</span></span>

2. <span data-ttu-id="90490-130">Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="90490-130">Run the following query to get the data types mapping for each event:</span></span> 

   ```
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- <span data-ttu-id="90490-131">Voici un exemple d’événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="90490-131">Here is an example for Device Info event:</span></span> 

  ![Image de l’ID3 de ressource du hub d’événements](images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="90490-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90490-133">Related topics</span></span>
- [<span data-ttu-id="90490-134">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="90490-134">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="90490-135">Microsoft 365 API de diffusion en continu defender</span><span class="sxs-lookup"><span data-stu-id="90490-135">Microsoft 365 Defender Streaming API</span></span>](raw-data-export.md)
- [<span data-ttu-id="90490-136">Diffuser Microsoft 365 événements Defender sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="90490-136">Stream Microsoft 365 Defender events to your Azure storage account</span></span>](raw-data-export-storage.md)
- [<span data-ttu-id="90490-137">stockage Azure Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="90490-137">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)
