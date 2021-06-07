---
title: Connexion des API Microsoft Defender for Endpoint Power BI
ms.reviewer: ''
description: Créez un rapport Power Business Intelligence (BI) sur les API Microsoft Defender for Endpoint.
keywords: api, api pris en charge, Power BI, rapports
search.product: eADQiWindows 10XVcnh
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 5c76784d78837c324922ffc25539746a4921e426
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769708"
---
# <a name="create-custom-reports-using-power-bi"></a><span data-ttu-id="249ef-104">Créer des rapports personnalisés à l’aide Power BI</span><span class="sxs-lookup"><span data-stu-id="249ef-104">Create custom reports using Power BI</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="249ef-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="249ef-105">**Applies to:**</span></span>
- [<span data-ttu-id="249ef-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="249ef-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="249ef-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="249ef-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


- <span data-ttu-id="249ef-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="249ef-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="249ef-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="249ef-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="249ef-110">Dans cette section, vous allez apprendre à créer un Power BI sur les API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="249ef-110">In this section you will learn create a Power BI report on top of Defender for Endpoint APIs.</span></span>

<span data-ttu-id="249ef-111">Le premier exemple montre comment connecter des Power BI à l’API de recherche avancée et le deuxième exemple illustre une connexion à nos API OData, telles que les actions de l’ordinateur ou les alertes.</span><span class="sxs-lookup"><span data-stu-id="249ef-111">The first example demonstrates how to connect Power BI to Advanced Hunting API and the second example demonstrates a connection to our OData APIs, such as Machine Actions or Alerts.</span></span>

## <a name="connect-power-bi-to-advanced-hunting-api"></a><span data-ttu-id="249ef-112">Connecter Power BI à l’API de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="249ef-112">Connect Power BI to Advanced Hunting API</span></span>

- <span data-ttu-id="249ef-113">Ouvrez Microsoft Power BI</span><span class="sxs-lookup"><span data-stu-id="249ef-113">Open Microsoft Power BI</span></span>

- <span data-ttu-id="249ef-114">Click **Get Data** Blank  >  **Query**</span><span class="sxs-lookup"><span data-stu-id="249ef-114">Click **Get Data** > **Blank Query**</span></span>

    ![Image de création d’une requête vide](images/power-bi-create-blank-query.png)

- <span data-ttu-id="249ef-116">Cliquez sur **Éditeur avancé**</span><span class="sxs-lookup"><span data-stu-id="249ef-116">Click **Advanced Editor**</span></span>

    ![Image de l’éditeur avancé ouvert](images/power-bi-open-advanced-editor.png)

- <span data-ttu-id="249ef-118">Copiez le texte ci-dessous et collez-le dans l’éditeur :</span><span class="sxs-lookup"><span data-stu-id="249ef-118">Copy the below and paste it in the editor:</span></span>

```
    let 
        AdvancedHuntingQuery = "DeviceEvents | where ActionType contains 'Anti' | limit 20",

        HuntingUrl = "https://api.securitycenter.microsoft.com/api/advancedqueries",

        Response = Json.Document(Web.Contents(HuntingUrl, [Query=[key=AdvancedHuntingQuery]])),

        TypeMap = #table(
            { "Type", "PowerBiType" },
            {
                { "Double",   Double.Type },
                { "Int64",    Int64.Type },
                { "Int32",    Int32.Type },
                { "Int16",    Int16.Type },
                { "UInt64",   Number.Type },
                { "UInt32",   Number.Type },
                { "UInt16",   Number.Type },
                { "Byte",     Byte.Type },
                { "Single",   Single.Type },
                { "Decimal",  Decimal.Type },
                { "TimeSpan", Duration.Type },
                { "DateTime", DateTimeZone.Type },
                { "String",   Text.Type },
                { "Boolean",  Logical.Type },
                { "SByte",    Logical.Type },
                { "Guid",     Text.Type }
            }),

        Schema = Table.FromRecords(Response[Schema]),
        TypedSchema = Table.Join(Table.SelectColumns(Schema, {"Name", "Type"}), {"Type"}, TypeMap , {"Type"}),
        Results = Response[Results],
        Rows = Table.FromRecords(Results, Schema[Name]),
        Table = Table.TransformColumnTypes(Rows, Table.ToList(TypedSchema, (c) => {c{0}, c{2}}))

    in Table

```

- <span data-ttu-id="249ef-119">Cliquez sur **Terminé**</span><span class="sxs-lookup"><span data-stu-id="249ef-119">Click **Done**</span></span>

- <span data-ttu-id="249ef-120">Cliquez sur **Modifier les informations d’identification**</span><span class="sxs-lookup"><span data-stu-id="249ef-120">Click **Edit Credentials**</span></span>

    ![Image de modification des informations d’identification0](images/power-bi-edit-credentials.png)

- <span data-ttu-id="249ef-122">Sélectionner un **compte d’organisation**  >  **pour se connecter**</span><span class="sxs-lookup"><span data-stu-id="249ef-122">Select **Organizational account** > **Sign in**</span></span>

    ![Image de l’ensemble des informations d’identification1](images/power-bi-set-credentials-organizational.png)

- <span data-ttu-id="249ef-124">Entrez vos informations d’identification et attendez d’être connexion</span><span class="sxs-lookup"><span data-stu-id="249ef-124">Enter your credentials and wait to be signed in</span></span>

- <span data-ttu-id="249ef-125">Cliquez **sur Connecter**</span><span class="sxs-lookup"><span data-stu-id="249ef-125">Click **Connect**</span></span>

    ![Image de l’ensemble des informations d’identification2](images/power-bi-set-credentials-organizational-cont.png)

- <span data-ttu-id="249ef-127">À présent, les résultats de votre requête s’affichent en tant que table et vous pouvez commencer à créer des visualisations au-dessus de celui-ci !</span><span class="sxs-lookup"><span data-stu-id="249ef-127">Now the results of your query will appear as table and you can start build visualizations on top of it!</span></span>

- <span data-ttu-id="249ef-128">Vous pouvez dupliquer cette table, la renommer et modifier la requête de recherche avancée à l’intérieur pour obtenir les données que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="249ef-128">You can duplicate this table, rename it and edit the Advanced Hunting query inside to get any data you would like.</span></span>

## <a name="connect-power-bi-to-odata-apis"></a><span data-ttu-id="249ef-129">Connecter Power BI aux API OData</span><span class="sxs-lookup"><span data-stu-id="249ef-129">Connect Power BI to OData APIs</span></span>

- <span data-ttu-id="249ef-130">La seule différence par rapport à l’exemple ci-dessus est la requête à l’intérieur de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="249ef-130">The only difference from the above example is the query inside the editor.</span></span> 

- <span data-ttu-id="249ef-131">Copiez le texte ci-dessous et collez-le dans l’éditeur pour tirer toutes les **actions de** l’ordinateur de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="249ef-131">Copy the below and paste it in the editor to pull all **Machine Actions** from your organization:</span></span>

```
    let

        Query = "MachineActions",

        Source = OData.Feed("https://api.securitycenter.microsoft.com/api/" & Query, null, [Implementation="2.0", MoreColumns=true])
    in
        Source

```

- <span data-ttu-id="249ef-132">Vous pouvez faire de même pour les alertes et les **ordinateurs.** </span><span class="sxs-lookup"><span data-stu-id="249ef-132">You can do the same for **Alerts** and **Machines**.</span></span>

- <span data-ttu-id="249ef-133">Vous pouvez également utiliser des requêtes OData pour les filtres de requêtes, voir [Utilisation de requêtes OData](exposed-apis-odata-samples.md)</span><span class="sxs-lookup"><span data-stu-id="249ef-133">You also can use OData queries for queries filters, see [Using OData Queries](exposed-apis-odata-samples.md)</span></span>


## <a name="power-bi-dashboard-samples-in-github"></a><span data-ttu-id="249ef-134">Power BI exemples de tableau de bord dans GitHub</span><span class="sxs-lookup"><span data-stu-id="249ef-134">Power BI dashboard samples in GitHub</span></span>
<span data-ttu-id="249ef-135">Pour plus d’informations, [voir Power BI modèles de rapport.](https://github.com/microsoft/MicrosoftDefenderATP-PowerBI)</span><span class="sxs-lookup"><span data-stu-id="249ef-135">For more information see the [Power BI report templates](https://github.com/microsoft/MicrosoftDefenderATP-PowerBI).</span></span>

## <a name="sample-reports"></a><span data-ttu-id="249ef-136">Exemples de rapports</span><span class="sxs-lookup"><span data-stu-id="249ef-136">Sample reports</span></span>
<span data-ttu-id="249ef-137">Affichez les exemples de rapport microsoft Defender pour Power BI de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="249ef-137">View the Microsoft Defender for Endpoint Power BI report samples.</span></span> <span data-ttu-id="249ef-138">Pour plus d’informations, voir [Parcourir les exemples de code.](https://docs.microsoft.com/samples/browse/?products=mdatp)</span><span class="sxs-lookup"><span data-stu-id="249ef-138">For more information, see [Browse code samples](https://docs.microsoft.com/samples/browse/?products=mdatp).</span></span>


## <a name="related-topic"></a><span data-ttu-id="249ef-139">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="249ef-139">Related topic</span></span>
- [<span data-ttu-id="249ef-140">API Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="249ef-140">Defender for Endpoint APIs</span></span>](apis-intro.md)
- [<span data-ttu-id="249ef-141">API de recherche avancée de menaces</span><span class="sxs-lookup"><span data-stu-id="249ef-141">Advanced Hunting API</span></span>](run-advanced-query-api.md)
- [<span data-ttu-id="249ef-142">Utilisation des requêtes OData</span><span class="sxs-lookup"><span data-stu-id="249ef-142">Using OData Queries</span></span>](exposed-apis-odata-samples.md)
