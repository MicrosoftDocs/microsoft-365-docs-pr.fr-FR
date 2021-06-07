---
title: Explorateur d’API dans Microsoft Defender pour point de terminaison
ms.reviewer: ''
description: Utiliser l’Explorateur d’API pour créer et faire des requêtes API, tester et envoyer des demandes pour n’importe quelle API disponible
keywords: api, explorer, envoyer, demander, obtenir, publier,
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
ms.topic: conceptual
ms.technology: mde
ms.custom: api
ms.openlocfilehash: 6a5684d71d34b3efdfe915ae674b4fcb90342154
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52769796"
---
# <a name="api-explorer"></a><span data-ttu-id="a60cd-104">Explorateur d’API</span><span class="sxs-lookup"><span data-stu-id="a60cd-104">API Explorer</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="a60cd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a60cd-105">**Applies to:**</span></span>
- [<span data-ttu-id="a60cd-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a60cd-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)


<span data-ttu-id="a60cd-107">L’Explorateur d’API Microsoft Defender pour point de terminaison est un outil qui vous permet d’explorer différentes API Defender pour endpoint de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="a60cd-107">The Microsoft Defender for Endpoint API Explorer is a tool that helps you explore various Defender for Endpoint APIs interactively.</span></span> 

<span data-ttu-id="a60cd-108">L’Explorateur d’API facilite la construction et l’envoi de requêtes API, de test et d’envoi de requêtes pour n’importe quel point de terminaison de l’API Defender for Endpoint disponible.</span><span class="sxs-lookup"><span data-stu-id="a60cd-108">The API Explorer makes it easy to construct and do API queries, test, and send requests for any available Defender for Endpoint API endpoint.</span></span> <span data-ttu-id="a60cd-109">Utilisez l’Explorateur d’API pour prendre des mesures ou rechercher des données qui ne sont peut-être pas encore disponibles via l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a60cd-109">Use the API Explorer to take actions or find data that might not yet be available through the user interface.</span></span>

<span data-ttu-id="a60cd-110">L’outil est utile lors du développement d’applications.</span><span class="sxs-lookup"><span data-stu-id="a60cd-110">The tool is useful during app development.</span></span> <span data-ttu-id="a60cd-111">Il vous permet d’effectuer des requêtes API qui respectent vos paramètres d’accès utilisateur, ce qui réduit la nécessité de générer des jetons d’accès.</span><span class="sxs-lookup"><span data-stu-id="a60cd-111">It allows you to perform API queries that respect your user access settings, reducing the need to generate access tokens.</span></span>

<span data-ttu-id="a60cd-112">Vous pouvez également utiliser l’outil pour explorer la galerie d’exemples de requêtes, copier des exemples de code de résultat et générer des informations de débogage.</span><span class="sxs-lookup"><span data-stu-id="a60cd-112">You can also use the tool to explore the gallery of sample queries, copy result code samples, and generate debug information.</span></span>

<span data-ttu-id="a60cd-113">Avec l’Explorateur d’API, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="a60cd-113">With the API Explorer, you can:</span></span>

- <span data-ttu-id="a60cd-114">Exécuter des demandes pour n’importe quelle méthode et voir les réponses en temps réel</span><span class="sxs-lookup"><span data-stu-id="a60cd-114">Run requests for any method and see responses in real-time</span></span>
- <span data-ttu-id="a60cd-115">Parcourez rapidement les exemples d’API et découvrez les paramètres qu’ils supportent</span><span class="sxs-lookup"><span data-stu-id="a60cd-115">Quickly browse through the API samples and learn what parameters they support</span></span>
- <span data-ttu-id="a60cd-116">Effectuer des appels d’API en toute simplicité ; pas besoin de s’authentifier au-delà de la signature du portail de gestion</span><span class="sxs-lookup"><span data-stu-id="a60cd-116">Make API calls with ease; no need to authenticate beyond the management portal sign in</span></span>

## <a name="access-api-explorer"></a><span data-ttu-id="a60cd-117">Explorateur d’API Access</span><span class="sxs-lookup"><span data-stu-id="a60cd-117">Access API Explorer</span></span>

<span data-ttu-id="a60cd-118">Dans le menu de navigation de gauche, sélectionnez **Partenaires & API**  >  **Explorer.**</span><span class="sxs-lookup"><span data-stu-id="a60cd-118">From the left navigation menu, select **Partners & APIs** > **API Explorer**.</span></span>

## <a name="supported-apis"></a><span data-ttu-id="a60cd-119">API prise en charge</span><span class="sxs-lookup"><span data-stu-id="a60cd-119">Supported APIs</span></span>

<span data-ttu-id="a60cd-120">L’Explorateur d’API prend en charge toutes les API proposées par Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="a60cd-120">API Explorer supports all the APIs offered by Defender for Endpoint.</span></span>
  
<span data-ttu-id="a60cd-121">La liste des API prise en charge est disponible dans la [documentation des API.](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="a60cd-121">The list of supported APIs is available in the [APIs documentation](apis-intro.md).</span></span> 

## <a name="get-started-with-the-api-explorer"></a><span data-ttu-id="a60cd-122">Mise en place de l’Explorateur d’API</span><span class="sxs-lookup"><span data-stu-id="a60cd-122">Get started with the API Explorer</span></span>

1. <span data-ttu-id="a60cd-123">Dans le volet gauche se trouve une liste d’exemples de demandes que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a60cd-123">In the left pane, there is a list of sample requests that you can use.</span></span> 
2. <span data-ttu-id="a60cd-124">Suivez les liens et cliquez sur **Exécuter la requête.**</span><span class="sxs-lookup"><span data-stu-id="a60cd-124">Follow the links and click **Run query**.</span></span> 

<span data-ttu-id="a60cd-125">Certains exemples peuvent nécessiter la spécification d’un paramètre dans l’URL, par exemple, {machine- ID}.</span><span class="sxs-lookup"><span data-stu-id="a60cd-125">Some of the samples may require specifying a parameter in the URL, for example, {machine- ID}.</span></span>

## <a name="faq"></a><span data-ttu-id="a60cd-126">FAQ</span><span class="sxs-lookup"><span data-stu-id="a60cd-126">FAQ</span></span>

<span data-ttu-id="a60cd-127">**Ai-je besoin d’un jeton d’API pour utiliser l’Explorateur d’API ?**</span><span class="sxs-lookup"><span data-stu-id="a60cd-127">**Do I need to have an API token to use the API Explorer?**</span></span> <br>
<span data-ttu-id="a60cd-128">Les informations d’identification pour accéder à une API ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="a60cd-128">Credentials to access an API aren't needed.</span></span> <span data-ttu-id="a60cd-129">L’Explorateur d’API utilise le jeton du portail de gestion Defender for Endpoint chaque fois qu’il effectue une demande.</span><span class="sxs-lookup"><span data-stu-id="a60cd-129">The API Explorer uses the Defender for Endpoint management portal token whenever it makes a request.</span></span>

<span data-ttu-id="a60cd-130">Les informations d’authentification de l’utilisateur connecté sont utilisées pour vérifier que l’Explorateur d’API est autorisé à accéder aux données en votre nom.</span><span class="sxs-lookup"><span data-stu-id="a60cd-130">The logged-in user authentication credential is used to verify that the API Explorer is authorized to access data on your behalf.</span></span>

<span data-ttu-id="a60cd-131">Les demandes d’API spécifiques sont limitées en fonction de vos privilèges RBAC.</span><span class="sxs-lookup"><span data-stu-id="a60cd-131">Specific API requests are limited based on your RBAC privileges.</span></span> <span data-ttu-id="a60cd-132">Par exemple, une demande d'« indicateur d’soumission » est limitée au rôle d’administrateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="a60cd-132">For example, a request to "Submit indicator" is limited to the security admin role.</span></span> 
