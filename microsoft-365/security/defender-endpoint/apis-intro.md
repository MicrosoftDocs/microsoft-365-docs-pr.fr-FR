---
title: Accéder aux API Microsoft Defender for Endpoint
ms.reviewer: ''
description: Découvrez comment utiliser les API pour automatiser les flux de travail et innover en fonction des fonctionnalités de Microsoft Defender ATP
keywords: api, api, wdatp, api ouverte, api microsoft defender atp, api publique, api pris en charge, alertes, appareil, utilisateur, domaine, ip, fichier, recherche avancée, requête
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 70a8ba9d3ff864ca58c856714b00f0e8feba933a
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51164752"
---
# <a name="access-the-microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="d6b67-104">Accéder aux API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d6b67-104">Access the Microsoft Defender for Endpoint APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="d6b67-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d6b67-105">**Applies to:**</span></span>
- [<span data-ttu-id="d6b67-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6b67-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="d6b67-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d6b67-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


<span data-ttu-id="d6b67-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d6b67-108">**Applies to:**</span></span> 
- [<span data-ttu-id="d6b67-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6b67-109">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="d6b67-110">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d6b67-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d6b67-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d6b67-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 



<span data-ttu-id="d6b67-112">Defender pour le point de terminaison expose la plupart de ses données et actions par le biais d’un ensemble d’API par programme.</span><span class="sxs-lookup"><span data-stu-id="d6b67-112">Defender for Endpoint exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="d6b67-113">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d6b67-113">Those APIs will enable you to automate workflows and innovate based on Defender for Endpoint capabilities.</span></span> <span data-ttu-id="d6b67-114">L’accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="d6b67-114">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="d6b67-115">Pour plus d’informations, voir flux de code [d’autorisation OAuth 2.0.](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)</span><span class="sxs-lookup"><span data-stu-id="d6b67-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="d6b67-116">Regardez cette vidéo pour obtenir une vue d’ensemble rapide des API de Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="d6b67-116">Watch this video for a quick overview of Defender for Endpoint's APIs.</span></span> 
>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4d73M]

<span data-ttu-id="d6b67-117">En règle générale, vous devez suivre les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="d6b67-117">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="d6b67-118">Créer une application AAD</span><span class="sxs-lookup"><span data-stu-id="d6b67-118">Create an AAD application</span></span>
- <span data-ttu-id="d6b67-119">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="d6b67-119">Get an access token using this application</span></span>
- <span data-ttu-id="d6b67-120">Utiliser le jeton pour accéder à l’API Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="d6b67-120">Use the token to access Defender for Endpoint API</span></span>


<span data-ttu-id="d6b67-121">Vous pouvez accéder à l’API Defender for Endpoint avec le contexte **d’application** ou **le contexte utilisateur.**</span><span class="sxs-lookup"><span data-stu-id="d6b67-121">You can access Defender for Endpoint API with **Application Context** or **User Context**.</span></span>

- <span data-ttu-id="d6b67-122">**Contexte de l’application : (recommandé)**</span><span class="sxs-lookup"><span data-stu-id="d6b67-122">**Application Context: (Recommended)**</span></span> <br>
    <span data-ttu-id="d6b67-123">Utilisé par les applications qui s’exécutent sans utilisateur inscrit.</span><span class="sxs-lookup"><span data-stu-id="d6b67-123">Used by apps that run without a signed-in user present.</span></span> <span data-ttu-id="d6b67-124">par exemple, les applications qui s’exécutent en tant que daemons ou services d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="d6b67-124">for example, apps that run as background services or daemons.</span></span>

    <span data-ttu-id="d6b67-125">Étapes à suivre pour accéder à l’API Defender pour Endpoint avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="d6b67-125">Steps that need to be taken to access Defender for Endpoint API with application context:</span></span>

  1. <span data-ttu-id="d6b67-126">Créez une application web AAD.</span><span class="sxs-lookup"><span data-stu-id="d6b67-126">Create an AAD Web-Application.</span></span>
  2. <span data-ttu-id="d6b67-127">Attribuez l’autorisation souhaitée à l’application, par exemple, « Lire les alertes » et « Isoler les ordinateurs ».</span><span class="sxs-lookup"><span data-stu-id="d6b67-127">Assign the desired permission to the application, for example, 'Read Alerts', 'Isolate Machines'.</span></span> 
  3. <span data-ttu-id="d6b67-128">Créez une clé pour cette application.</span><span class="sxs-lookup"><span data-stu-id="d6b67-128">Create a key for this Application.</span></span>
  4. <span data-ttu-id="d6b67-129">Obtenir un jeton à l’aide de l’application avec sa clé.</span><span class="sxs-lookup"><span data-stu-id="d6b67-129">Get token using the application with its key.</span></span>
  5. <span data-ttu-id="d6b67-130">Utiliser le jeton pour accéder à l’API Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="d6b67-130">Use the token to access Microsoft Defender ATP API</span></span>

     <span data-ttu-id="d6b67-131">Pour plus d’informations, voir [Obtenir l’accès avec le contexte de l’application.](exposed-apis-create-app-webapp.md)</span><span class="sxs-lookup"><span data-stu-id="d6b67-131">For more information, see [Get access with application context](exposed-apis-create-app-webapp.md).</span></span>


- <span data-ttu-id="d6b67-132">**Contexte utilisateur :**</span><span class="sxs-lookup"><span data-stu-id="d6b67-132">**User Context:**</span></span> <br>
    <span data-ttu-id="d6b67-133">Permet d’effectuer des actions dans l’API au nom d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6b67-133">Used to perform actions in the API on behalf of a user.</span></span>

    <span data-ttu-id="d6b67-134">Étapes à suivre pour accéder à l’API Defender pour Endpoint avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="d6b67-134">Steps to take to access Defender for Endpoint API with application context:</span></span>

  1. <span data-ttu-id="d6b67-135">Créez une application native AAD.</span><span class="sxs-lookup"><span data-stu-id="d6b67-135">Create AAD Native-Application.</span></span>
  2. <span data-ttu-id="d6b67-136">Attribuez l’autorisation souhaitée à l’application, par exemple « Lire les alertes » et « Isoler les ordinateurs » etc.</span><span class="sxs-lookup"><span data-stu-id="d6b67-136">Assign the desired permission to the application, e.g 'Read Alerts', 'Isolate Machines' etc.</span></span> 
  3. <span data-ttu-id="d6b67-137">Obtenir un jeton à l’aide de l’application avec les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d6b67-137">Get token using the application with user credentials.</span></span>
  4. <span data-ttu-id="d6b67-138">Utiliser le jeton pour accéder à l’API Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="d6b67-138">Use the token to access Microsoft Defender ATP API</span></span>

     <span data-ttu-id="d6b67-139">Pour plus d’informations, voir [Obtenir l’accès avec le contexte utilisateur.](exposed-apis-create-app-nativeapp.md)</span><span class="sxs-lookup"><span data-stu-id="d6b67-139">For more information, see [Get access with user context](exposed-apis-create-app-nativeapp.md).</span></span>


## <a name="related-topics"></a><span data-ttu-id="d6b67-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6b67-140">Related topics</span></span>
- [<span data-ttu-id="d6b67-141">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d6b67-141">Microsoft Defender for Endpoint APIs</span></span>](exposed-apis-list.md)
- [<span data-ttu-id="d6b67-142">Accéder à Microsoft Defender pour le point de terminaison avec le contexte de l’application</span><span class="sxs-lookup"><span data-stu-id="d6b67-142">Access Microsoft Defender for Endpoint with application context</span></span>](exposed-apis-create-app-webapp.md)
- [<span data-ttu-id="d6b67-143">Accéder à Microsoft Defender pour le point de terminaison avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="d6b67-143">Access Microsoft Defender for Endpoint with user context</span></span>](exposed-apis-create-app-nativeapp.md)
