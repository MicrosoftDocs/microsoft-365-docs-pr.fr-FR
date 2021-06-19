---
title: Diffuser Microsoft 365 Defender événements sur votre compte Storage client
description: Découvrez comment configurer des Microsoft 365 Defender pour diffuser des événements de recherche avancée vers Storage compte.
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
ms.openlocfilehash: 656387e60bac90c7e9de4852779948dabce0efe3
ms.sourcegitcommit: c70067b4ef9c6f8f04aca68c35bb5141857c4e4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53029656"
---
# <a name="configure-microsoft-365-defender-to-stream-advanced-hunting-events-to-your-storage-account"></a><span data-ttu-id="5ed71-104">Configurer Microsoft 365 Defender pour diffuser en continu des événements de recherche avancée sur votre compte Storage client</span><span class="sxs-lookup"><span data-stu-id="5ed71-104">Configure Microsoft 365 Defender to stream Advanced Hunting events to your Storage account</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="5ed71-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5ed71-105">**Applies to:**</span></span>
- [<span data-ttu-id="5ed71-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5ed71-106">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="before-you-begin"></a><span data-ttu-id="5ed71-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5ed71-107">Before you begin</span></span>

1. <span data-ttu-id="5ed71-108">Créez [un Storage dans](/azure/storage/common/storage-account-overview) votre client.</span><span class="sxs-lookup"><span data-stu-id="5ed71-108">Create a [Storage account](/azure/storage/common/storage-account-overview) in your tenant.</span></span>

2. <span data-ttu-id="5ed71-109">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)allez à Abonnements > Votre abonnement > fournisseurs de ressources **> inscrivez-vous à Microsoft.Informations**.</span><span class="sxs-lookup"><span data-stu-id="5ed71-109">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to **Subscriptions > Your subscription > Resource Providers > Register to Microsoft.Insights**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="5ed71-110">Activer la diffusion en continu des données brutes</span><span class="sxs-lookup"><span data-stu-id="5ed71-110">Enable raw data streaming</span></span>

1. <span data-ttu-id="5ed71-111">Connectez-vous au portail Microsoft 365 Defender ( ) en tant qu’administrateur général \* ou _\* Administrateur de sécurité <https://security.microsoft.com> \*\*.</span><span class="sxs-lookup"><span data-stu-id="5ed71-111">Log in to the Microsoft 365 Defender portal (<https://security.microsoft.com>) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="5ed71-112">Go to **Paramètres** \> **Microsoft 365 Defender** \> **Streaming API**.</span><span class="sxs-lookup"><span data-stu-id="5ed71-112">Go to **Settings** \> **Microsoft 365 Defender** \> **Streaming API**.</span></span> <span data-ttu-id="5ed71-113">Pour aller directement à la page de **l’API de** diffusion en continu, utilisez <https://security.microsoft.com/settings/mtp_settings/raw_data_export> .</span><span class="sxs-lookup"><span data-stu-id="5ed71-113">To go directly to the **Streaming API** page, use <https://security.microsoft.com/settings/mtp_settings/raw_data_export>.</span></span>

3. <span data-ttu-id="5ed71-114">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="5ed71-114">Click **Add**.</span></span>

4. <span data-ttu-id="5ed71-115">Dans le **programme volant Ajouter de nouveaux paramètres d’API** de diffusion en continu qui s’affiche, configurez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="5ed71-115">In the **Add new Streaming API settings** flyout that appears, configure the following settings:</span></span>
   1. <span data-ttu-id="5ed71-116">**Nom**: choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="5ed71-116">**Name**: Choose a name for your new settings.</span></span>
   2. <span data-ttu-id="5ed71-117">Sélectionnez **Les événements Forward à Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="5ed71-117">Select **Forward events to Azure Storage**.</span></span>
   3. <span data-ttu-id="5ed71-118">Dans la **Storage’ID** de ressource de compte qui s’affiche, tapez **votre ID de ressource Storage compte.**</span><span class="sxs-lookup"><span data-stu-id="5ed71-118">In the **Storage Account Resource ID** box that appears, type your **Storage Account Resource ID**.</span></span> <span data-ttu-id="5ed71-119">Pour obtenir votre ID de ressource de compte **Storage,** ouvrez le portail Azure à l’Storage, cliquez sur les comptes Storage pour copier le texte sous <https://portal.azure.com>  l’ID de ressource Storage \> \> compte. </span><span class="sxs-lookup"><span data-stu-id="5ed71-119">To get your **Storage Account Resource ID**, open the Azure portal at <https://portal.azure.com>, click **Storage accounts** \> go to the properties tab \> copy the text under **Storage Account Resource ID**.</span></span>

      ![Image de l’ID1 de ressource du hub d’événements](../defender-endpoint/images/storage-account-resource-id.png)

   4. <span data-ttu-id="5ed71-121">De retour sur le volet Ajouter **de nouveaux paramètres d’API** de diffusion en continu, choisissez les **types** d’événements que vous souhaitez diffuser en continu.</span><span class="sxs-lookup"><span data-stu-id="5ed71-121">Back on the **Add new Streaming API settings** flyout, choose the **Event types** that you want to stream.</span></span>

   <span data-ttu-id="5ed71-122">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="5ed71-122">When you're finished, click **Submit**.</span></span>

## <a name="the-schema-of-the-events-in-the-storage-account"></a><span data-ttu-id="5ed71-123">Schéma des événements dans le compte de Storage</span><span class="sxs-lookup"><span data-stu-id="5ed71-123">The schema of the events in the Storage account</span></span>

- <span data-ttu-id="5ed71-124">Un conteneur d’objets blob est créé pour chaque type d’événement :</span><span class="sxs-lookup"><span data-stu-id="5ed71-124">A blob container will be created for each event type:</span></span>

  ![Image de l’ID2 de ressource du hub d’événements](../defender-endpoint/images/storage-account-event-schema.png)

- <span data-ttu-id="5ed71-126">Le schéma de chaque ligne d’un objet blob est le JSON suivant :</span><span class="sxs-lookup"><span data-stu-id="5ed71-126">The schema of each row in a blob is the following JSON:</span></span>

  ```JSON
  {
          "time": "<The time Microsoft 365 Defender received the event>"
          "tenantId": "<Your tenant ID>"
          "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
          "properties": { <Microsoft 365 Defender Advanced Hunting event as Json> }
  }
  ```

- <span data-ttu-id="5ed71-127">Chaque objet blob contient plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="5ed71-127">Each blob contains multiple rows.</span></span>

- <span data-ttu-id="5ed71-128">Chaque ligne contient le nom de l’événement, le moment où Defender pour le point de terminaison a reçu l’événement, le client qu’il appartient (vous recevez uniquement les événements de votre client) et l’événement au format JSON dans une propriété appelée « properties ».</span><span class="sxs-lookup"><span data-stu-id="5ed71-128">Each row contains the event name, the time Defender for Endpoint received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "properties".</span></span>

- <span data-ttu-id="5ed71-129">Pour plus d’informations sur le schéma des événements Microsoft 365 Defender, voir [vue d’ensemble de la recherche avancée.](../defender/advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5ed71-129">For more information about the schema of Microsoft 365 Defender events, see [Advanced Hunting overview](../defender/advanced-hunting-overview.md).</span></span>

## <a name="data-types-mapping"></a><span data-ttu-id="5ed71-130">Mappage des types de données</span><span class="sxs-lookup"><span data-stu-id="5ed71-130">Data types mapping</span></span>

<span data-ttu-id="5ed71-131">Pour obtenir les types de données pour nos propriétés d’événements, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="5ed71-131">In order to get the data types for our events properties do the following:</span></span>

1. <span data-ttu-id="5ed71-132">Connectez-vous au portail Microsoft 365 Defender ( ) et <https://security.microsoft.com> allez au hunting advanced  \> **hunting**.</span><span class="sxs-lookup"><span data-stu-id="5ed71-132">Log in to the Microsoft 365 Defender portal (<https://security.microsoft.com>) and go to **Hunting** \> **Advanced hunting**.</span></span> <span data-ttu-id="5ed71-133">Pour aller directement à la page **de** recherche avancée, utilisez <security.microsoft.com/advanced-hunting>.</span><span class="sxs-lookup"><span data-stu-id="5ed71-133">To go directly to the **Advanced hunting** page, use <security.microsoft.com/advanced-hunting>.</span></span>

2. <span data-ttu-id="5ed71-134">Sous **l’onglet Requête,** exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="5ed71-134">On the **Query** tab, run the following query to get the data types mapping for each event:</span></span>

   ```text
   {EventType}
   | getschema
   | project ColumnName, ColumnType
   ```

- <span data-ttu-id="5ed71-135">Voici un exemple d’événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="5ed71-135">Here is an example for Device Info event:</span></span>

  ![Image de l’ID3 de ressource du hub d’événements](../defender-endpoint/images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="5ed71-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ed71-137">Related topics</span></span>

- [<span data-ttu-id="5ed71-138">Vue d’ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="5ed71-138">Overview of Advanced Hunting</span></span>](../defender/advanced-hunting-overview.md)
- [<span data-ttu-id="5ed71-139">Microsoft 365 Defender API de diffusion en continu</span><span class="sxs-lookup"><span data-stu-id="5ed71-139">Microsoft 365 Defender Streaming API</span></span>](streaming-api.md)
- [<span data-ttu-id="5ed71-140">Diffuser Microsoft 365 Defender événements sur votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="5ed71-140">Stream Microsoft 365 Defender events to your Azure storage account</span></span>](streaming-api-storage.md)
- [<span data-ttu-id="5ed71-141">Azure Storage Documentation du compte</span><span class="sxs-lookup"><span data-stu-id="5ed71-141">Azure Storage Account documentation</span></span>](/azure/storage/common/storage-account-overview)
