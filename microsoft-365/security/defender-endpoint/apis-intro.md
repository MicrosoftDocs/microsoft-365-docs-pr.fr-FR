---
title: Accéder aux API Microsoft Defender pour point de terminaison.
ms.reviewer: ''
description: Découvrez comment utiliser les API pour automatiser les workflows et innover en fonction des fonctionnalités Microsoft Defender for Endpoint
keywords: apis, api, wdatp, open api, microsoft defender pour endpoint api, microsoft defender atp, public api, apis pris en charge, alertes, appareil, utilisateur, domaine, ip, fichier, chasse avancée, requête
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
ms.openlocfilehash: a91a401d5d57c7757bc043178c95dc42e7733b41
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52571828"
---
# <a name="access-the-microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="62307-104">Accéder aux API Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="62307-104">Access the Microsoft Defender for Endpoint APIs</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="62307-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="62307-105">**Applies to:**</span></span>
- [<span data-ttu-id="62307-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="62307-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="62307-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="62307-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)


<span data-ttu-id="62307-108">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="62307-108">**Applies to:**</span></span> 
- [<span data-ttu-id="62307-109">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="62307-109">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

> <span data-ttu-id="62307-110">Vous voulez faire l’expérience de Microsoft Defender pour Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="62307-110">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="62307-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="62307-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 



<span data-ttu-id="62307-112">Defender for Endpoint expose une grande partie de ses données et actions à travers un ensemble d’API programmatiques.</span><span class="sxs-lookup"><span data-stu-id="62307-112">Defender for Endpoint exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="62307-113">Ces API vous permettront d’automatiser les workflows et d’innover en fonction des fonctionnalités Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="62307-113">Those APIs will enable you to automate workflows and innovate based on Defender for Endpoint capabilities.</span></span> <span data-ttu-id="62307-114">L’accès api nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="62307-114">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="62307-115">Pour plus d’informations, [voir OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="62307-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="62307-116">Regardez cette vidéo pour un aperçu rapide des API defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="62307-116">Watch this video for a quick overview of Defender for Endpoint's APIs.</span></span> 
>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4d73M]

<span data-ttu-id="62307-117">En général, vous devrez prendre les mesures suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="62307-117">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="62307-118">Créer une [application AAD](/microsoft-365/security/defender-endpoint/exposed-apis-create-app-nativeapp)</span><span class="sxs-lookup"><span data-stu-id="62307-118">Create an [AAD application](/microsoft-365/security/defender-endpoint/exposed-apis-create-app-nativeapp)</span></span>
- <span data-ttu-id="62307-119">Obtenez un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="62307-119">Get an access token using this application</span></span>
- <span data-ttu-id="62307-120">Utilisez le jeton pour accéder à Defender pour l’API Endpoint</span><span class="sxs-lookup"><span data-stu-id="62307-120">Use the token to access Defender for Endpoint API</span></span>


<span data-ttu-id="62307-121">Vous pouvez accéder à Defender for Endpoint API avec le contexte **d’application ou** le **contexte utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="62307-121">You can access Defender for Endpoint API with **Application Context** or **User Context**.</span></span>

- <span data-ttu-id="62307-122">**Contexte d’application : (Recommandé)**</span><span class="sxs-lookup"><span data-stu-id="62307-122">**Application Context: (Recommended)**</span></span> <br>
    <span data-ttu-id="62307-123">Utilisé par les applications qui s’exécutent sans un utilisateur connecté présent.</span><span class="sxs-lookup"><span data-stu-id="62307-123">Used by apps that run without a signed-in user present.</span></span> <span data-ttu-id="62307-124">par exemple, les applications qui s’exécutent sous forme de services d’arrière-plan ou de démons.</span><span class="sxs-lookup"><span data-stu-id="62307-124">for example, apps that run as background services or daemons.</span></span>

    <span data-ttu-id="62307-125">Mesures à prendre pour accéder à Defender for Endpoint API avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="62307-125">Steps that need to be taken to access Defender for Endpoint API with application context:</span></span>

  1. <span data-ttu-id="62307-126">Créez une application Web AAD.</span><span class="sxs-lookup"><span data-stu-id="62307-126">Create an AAD Web-Application.</span></span>
  2. <span data-ttu-id="62307-127">Attribuez l’autorisation souhaitée à l’application, par exemple « Lire les alertes », « Isoler les machines ».</span><span class="sxs-lookup"><span data-stu-id="62307-127">Assign the desired permission to the application, for example, 'Read Alerts', 'Isolate Machines'.</span></span> 
  3. <span data-ttu-id="62307-128">Créez une clé pour cette application.</span><span class="sxs-lookup"><span data-stu-id="62307-128">Create a key for this Application.</span></span>
  4. <span data-ttu-id="62307-129">Obtenez un jeton en utilisant l’application avec sa clé.</span><span class="sxs-lookup"><span data-stu-id="62307-129">Get token using the application with its key.</span></span>
  5. <span data-ttu-id="62307-130">Utilisez le jeton pour accéder à l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="62307-130">Use the token to access the Microsoft Defender for Endpoint API</span></span>

     <span data-ttu-id="62307-131">Pour plus d’informations, voir [Obtenez l’accès avec le contexte de l’application](exposed-apis-create-app-webapp.md).</span><span class="sxs-lookup"><span data-stu-id="62307-131">For more information, see [Get access with application context](exposed-apis-create-app-webapp.md).</span></span>


- <span data-ttu-id="62307-132">**Contexte de l’utilisateur :**</span><span class="sxs-lookup"><span data-stu-id="62307-132">**User Context:**</span></span> <br>
    <span data-ttu-id="62307-133">Utilisé pour effectuer des actions dans l’API pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62307-133">Used to perform actions in the API on behalf of a user.</span></span>

    <span data-ttu-id="62307-134">Mesures à prendre pour accéder à Defender for Endpoint API avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="62307-134">Steps to take to access Defender for Endpoint API with application context:</span></span>

  1. <span data-ttu-id="62307-135">Créez l’application native AAD.</span><span class="sxs-lookup"><span data-stu-id="62307-135">Create AAD Native-Application.</span></span>
  2. <span data-ttu-id="62307-136">Attribuez l’autorisation souhaitée à l’application, par exemple « Lire les alertes », « Isoler les machines », etc.</span><span class="sxs-lookup"><span data-stu-id="62307-136">Assign the desired permission to the application, e.g 'Read Alerts', 'Isolate Machines' etc.</span></span> 
  3. <span data-ttu-id="62307-137">Obtenez un jeton à l’aide de l’application avec les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62307-137">Get token using the application with user credentials.</span></span>
  4. <span data-ttu-id="62307-138">Utilisez le jeton pour accéder à l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="62307-138">Use the token to access the Microsoft Defender for Endpoint API</span></span>

     <span data-ttu-id="62307-139">Pour plus d’informations, voir [Obtenez l’accès avec le contexte de l’utilisateur](exposed-apis-create-app-nativeapp.md).</span><span class="sxs-lookup"><span data-stu-id="62307-139">For more information, see [Get access with user context](exposed-apis-create-app-nativeapp.md).</span></span>


## <a name="related-topics"></a><span data-ttu-id="62307-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62307-140">Related topics</span></span>
- [<span data-ttu-id="62307-141">Microsoft Defender pour les API endpoint</span><span class="sxs-lookup"><span data-stu-id="62307-141">Microsoft Defender for Endpoint APIs</span></span>](exposed-apis-list.md)
- [<span data-ttu-id="62307-142">Accédez à Microsoft Defender pour Endpoint avec le contexte de l’application</span><span class="sxs-lookup"><span data-stu-id="62307-142">Access Microsoft Defender for Endpoint with application context</span></span>](exposed-apis-create-app-webapp.md)
- [<span data-ttu-id="62307-143">Accédez à Microsoft Defender pour Endpoint avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="62307-143">Access Microsoft Defender for Endpoint with user context</span></span>](exposed-apis-create-app-nativeapp.md)
