---
title: Diffuser des événements Microsoft Defender for Endpoint vers votre compte de stockage
description: Découvrez comment configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers votre compte de stockage.
keywords: exportation de données brutes, API de diffusion en continu, API, Hubs d'événements, stockage Azure, compte de stockage, recherche avancée, partage de données brutes
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
ms.openlocfilehash: 19fe0c9c3dc6f2e4226a4aa9a6cd983bc95bae3a
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51688788"
---
# <a name="configure-microsoft-defender-for-endpoint-to-stream-advanced-hunting-events-to-your-storage-account"></a><span data-ttu-id="52494-104">Configurer Microsoft Defender pour le point de terminaison pour diffuser des événements de recherche avancée vers votre compte de stockage</span><span class="sxs-lookup"><span data-stu-id="52494-104">Configure Microsoft Defender for Endpoint to stream Advanced Hunting events to your Storage account</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="52494-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="52494-105">**Applies to:**</span></span>
- [<span data-ttu-id="52494-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="52494-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="52494-107">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="52494-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="52494-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="52494-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configuresiem-abovefoldlink) 

## <a name="before-you-begin"></a><span data-ttu-id="52494-109">Avant de commencer :</span><span class="sxs-lookup"><span data-stu-id="52494-109">Before you begin:</span></span>

1. <span data-ttu-id="52494-110">Créez [un compte de stockage](https://docs.microsoft.com/azure/storage/common/storage-account-overview) dans votre client.</span><span class="sxs-lookup"><span data-stu-id="52494-110">Create a [Storage account](https://docs.microsoft.com/azure/storage/common/storage-account-overview) in your tenant.</span></span>

2. <span data-ttu-id="52494-111">Connectez-vous à votre client [Azure,](https://ms.portal.azure.com/)allez à Abonnements > Votre abonnement > fournisseurs de ressources **> s'inscrire à Microsoft.insights**.</span><span class="sxs-lookup"><span data-stu-id="52494-111">Log in to your [Azure tenant](https://ms.portal.azure.com/), go to **Subscriptions > Your subscription > Resource Providers > Register to Microsoft.insights**.</span></span>

## <a name="enable-raw-data-streaming"></a><span data-ttu-id="52494-112">Activer la diffusion en continu des données brutes :</span><span class="sxs-lookup"><span data-stu-id="52494-112">Enable raw data streaming:</span></span>

1. <span data-ttu-id="52494-113">Connectez-vous [au portail Microsoft Defender pour points](https://securitycenter.windows.com) de terminaison en tant qu'administrateur \* Administrateur **général** _ ou _\*_Administrateur_ de sécurité \*\*.</span><span class="sxs-lookup"><span data-stu-id="52494-113">Log in to [Microsoft Defender for Endpoint portal](https://securitycenter.windows.com) as a ***Global Administrator** _ or _*_Security Administrator_\*\*.</span></span>

2. <span data-ttu-id="52494-114">Go to [Data export settings page](https://securitycenter.windows.com/interoperability/dataexport) on Microsoft Defender Security Center.</span><span class="sxs-lookup"><span data-stu-id="52494-114">Go to [Data export settings page](https://securitycenter.windows.com/interoperability/dataexport) on Microsoft Defender Security Center.</span></span>

3. <span data-ttu-id="52494-115">Cliquez sur **Ajouter des paramètres d'exportation de données.**</span><span class="sxs-lookup"><span data-stu-id="52494-115">Click on **Add data export settings**.</span></span>

4. <span data-ttu-id="52494-116">Choisissez un nom pour vos nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="52494-116">Choose a name for your new settings.</span></span>

5. <span data-ttu-id="52494-117">Choose **Forward events to Azure Storage**.</span><span class="sxs-lookup"><span data-stu-id="52494-117">Choose **Forward events to Azure Storage**.</span></span>

6. <span data-ttu-id="52494-118">Tapez votre **ID de ressource de compte de stockage.**</span><span class="sxs-lookup"><span data-stu-id="52494-118">Type your **Storage Account Resource ID**.</span></span> <span data-ttu-id="52494-119">Pour obtenir votre **ID** de ressource de compte de stockage, allez à la page de votre compte de stockage sur l'onglet Propriétés du portail [Azure](https://ms.portal.azure.com/) > > copiez le texte sous **L'ID** de ressource du compte de stockage :</span><span class="sxs-lookup"><span data-stu-id="52494-119">In order to get your **Storage Account Resource ID**, go to your Storage account page on [Azure portal](https://ms.portal.azure.com/) > properties tab > copy the text under **Storage account resource ID**:</span></span>

   ![Image de l'ID1 de ressource du hub d'événements](images/storage-account-resource-id.png)

7. <span data-ttu-id="52494-121">Choisissez les événements que vous souhaitez diffuser en continu, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="52494-121">Choose the events you want to stream and click **Save**.</span></span>

## <a name="the-schema-of-the-events-in-the-storage-account"></a><span data-ttu-id="52494-122">Schéma des événements dans le compte de stockage :</span><span class="sxs-lookup"><span data-stu-id="52494-122">The schema of the events in the Storage account:</span></span>

- <span data-ttu-id="52494-123">Un conteneur d'objets blob est créé pour chaque type d'événement :</span><span class="sxs-lookup"><span data-stu-id="52494-123">A blob container will be created for each event type:</span></span> 

  ![Image de l'ID2 de ressource du hub d'événements](images/storage-account-event-schema.png)

- <span data-ttu-id="52494-125">Le schéma de chaque ligne d'un objet blob est le JSON suivant :</span><span class="sxs-lookup"><span data-stu-id="52494-125">The schema of each row in a blob is the following JSON:</span></span> 

  ```
  {
          "time": "<The time WDATP received the event>"
          "tenantId": "<Your tenant ID>"
          "category": "<The Advanced Hunting table name with 'AdvancedHunting-' prefix>"
          "properties": { <WDATP Advanced Hunting event as Json> }
  }               
  ```

- <span data-ttu-id="52494-126">Chaque objet blob contient plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="52494-126">Each blob contains multiple rows.</span></span>

- <span data-ttu-id="52494-127">Chaque ligne contient le nom de l'événement, le moment où Defender pour le point de terminaison a reçu l'événement, le client qu'il appartient (vous recevez uniquement les événements de votre client) et l'événement au format JSON dans une propriété appelée « properties ».</span><span class="sxs-lookup"><span data-stu-id="52494-127">Each row contains the event name, the time Defender for Endpoint received the event, the tenant it belongs (you will only get events from your tenant), and the event in JSON format in a property called "properties".</span></span>

- <span data-ttu-id="52494-128">Pour plus d'informations sur le schéma des événements De Microsoft Defender pour point de [terminaison, voir vue d'ensemble de la recherche avancée.](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="52494-128">For more information about the schema of Microsoft Defender for Endpoint events, see [Advanced Hunting overview](advanced-hunting-overview.md).</span></span>

- <span data-ttu-id="52494-129">Dans la recherche avancée, la table **DeviceInfo** comporte une colonne nommée **MachineGroup** qui contient le groupe de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="52494-129">In Advanced Hunting, the **DeviceInfo** table has a column named **MachineGroup** which contains the group of the device.</span></span> <span data-ttu-id="52494-130">Ici, chaque événement est également décorée avec cette colonne.</span><span class="sxs-lookup"><span data-stu-id="52494-130">Here every event will be decorated with this column as well.</span></span> <span data-ttu-id="52494-131">Pour plus [d'informations,](machine-groups.md) voir Groupes d'appareils.</span><span class="sxs-lookup"><span data-stu-id="52494-131">See [Device Groups](machine-groups.md) for more information.</span></span>

## <a name="data-types-mapping"></a><span data-ttu-id="52494-132">Mappage des types de données :</span><span class="sxs-lookup"><span data-stu-id="52494-132">Data types mapping:</span></span>

<span data-ttu-id="52494-133">Pour obtenir les types de données pour nos propriétés d'événements, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="52494-133">In order to get the data types for our events properties do the following:</span></span>

1. <span data-ttu-id="52494-134">Connectez-vous [au Centre de](https://securitycenter.windows.com) sécurité Microsoft Defender et allez à la page Recherche [avancée.](https://securitycenter.windows.com/hunting-package)</span><span class="sxs-lookup"><span data-stu-id="52494-134">Log in to [Microsoft Defender Security Center](https://securitycenter.windows.com) and go to [Advanced Hunting page](https://securitycenter.windows.com/hunting-package).</span></span>

2. <span data-ttu-id="52494-135">Exécutez la requête suivante pour obtenir le mappage des types de données pour chaque événement :</span><span class="sxs-lookup"><span data-stu-id="52494-135">Run the following query to get the data types mapping for each event:</span></span> 

   ```
   {EventType}
   | getschema
   | project ColumnName, ColumnType 
   ```

- <span data-ttu-id="52494-136">Voici un exemple d'événement Device Info :</span><span class="sxs-lookup"><span data-stu-id="52494-136">Here is an example for Device Info event:</span></span> 

  ![Image de l'ID3 de ressource du hub d'événements](images/machine-info-datatype-example.png)

## <a name="related-topics"></a><span data-ttu-id="52494-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52494-138">Related topics</span></span>
- [<span data-ttu-id="52494-139">Vue d'ensemble du chasse avancée</span><span class="sxs-lookup"><span data-stu-id="52494-139">Overview of Advanced Hunting</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="52494-140">API de diffusion en continu microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="52494-140">Microsoft Defender for Endpoint Streaming API</span></span>](raw-data-export.md)
- [<span data-ttu-id="52494-141">Diffuser des événements Microsoft Defender for Endpoint vers votre compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="52494-141">Stream Microsoft Defender for Endpoint events to your Azure storage account</span></span>](raw-data-export-storage.md)
- [<span data-ttu-id="52494-142">Documentation du compte de stockage Azure</span><span class="sxs-lookup"><span data-stu-id="52494-142">Azure Storage Account documentation</span></span>](https://docs.microsoft.com/azure/storage/common/storage-account-overview)
