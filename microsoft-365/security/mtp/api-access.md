---
title: Accéder aux API Microsoft 365 Defender
description: Découvrez comment accéder aux API Microsoft 365 Defender
keywords: accès, API, contexte d’application, contexte utilisateur, application AAD, jeton d’accès
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: bf7a6a70cefda7bfac83d42f8e8dd6355c479914
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48845015"
---
# <a name="access-the-microsoft-365-defender-apis"></a><span data-ttu-id="ae073-104">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-104">Access the Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="ae073-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ae073-105">**Applies to:**</span></span>
- <span data-ttu-id="ae073-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="ae073-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="ae073-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ae073-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="ae073-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


 <span data-ttu-id="ae073-109">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="ae073-109">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="ae073-110">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="ae073-110">Those APIs will enable you to automate workflows and innovate based on  Microsoft 365 Defender capabilities.</span></span> <span data-ttu-id="ae073-111">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="ae073-111">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="ae073-112">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="ae073-112">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>


<span data-ttu-id="ae073-113">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="ae073-113">In general, you'll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="ae073-114">Créer une application AAD</span><span class="sxs-lookup"><span data-stu-id="ae073-114">Create an AAD application</span></span>
- <span data-ttu-id="ae073-115">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="ae073-115">Get an access token using this application</span></span>
- <span data-ttu-id="ae073-116">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-116">Use the token to access  Microsoft 365 Defender API</span></span>


<span data-ttu-id="ae073-117">Vous pouvez accéder à l’API Microsoft 365 Defender avec un **contexte d’application** ou un **contexte utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="ae073-117">You can access Microsoft 365 Defender API with **Application Context** or **User Context**.</span></span>

- <span data-ttu-id="ae073-118">**Contexte de l’application : (recommandé)**</span><span class="sxs-lookup"><span data-stu-id="ae073-118">**Application Context: (Recommended)**</span></span> <br>
    <span data-ttu-id="ae073-119">Utilisé par les applications qui s’exécutent sans qu’aucun utilisateur ne soit connecté.</span><span class="sxs-lookup"><span data-stu-id="ae073-119">Used by apps that run without a signed-in user present.</span></span> <span data-ttu-id="ae073-120">par exemple, les applications qui s’exécutent en tant que services ou démons d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ae073-120">for example, apps that run as background services or daemons.</span></span>

    <span data-ttu-id="ae073-121">Étapes à suivre pour accéder à l’API Microsoft 365 Defender avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="ae073-121">Steps that need to be taken to access  Microsoft 365 Defender API with application context:</span></span>

  1. <span data-ttu-id="ae073-122">Créer une application Web AAD.</span><span class="sxs-lookup"><span data-stu-id="ae073-122">Create an AAD Web-Application.</span></span>
  2. <span data-ttu-id="ae073-123">Attribuez l’autorisation souhaitée à l’exemple applicationFor, **incident. Read. All** , **AdvancedHunting. Read. All**.</span><span class="sxs-lookup"><span data-stu-id="ae073-123">Assign the desired permission to the applicationFor example, **Incident.Read.All** , **AdvancedHunting.Read.All**.</span></span> 
  3. <span data-ttu-id="ae073-124">Créez une clé pour cette application.</span><span class="sxs-lookup"><span data-stu-id="ae073-124">Create a key for this Application.</span></span>
  4. <span data-ttu-id="ae073-125">Obtenir un jeton à l’aide de l’application avec sa clé.</span><span class="sxs-lookup"><span data-stu-id="ae073-125">Get token using the application with its key.</span></span>
  5. <span data-ttu-id="ae073-126">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-126">Use the token to access  Microsoft 365 Defender API</span></span>

     <span data-ttu-id="ae073-127">Pour plus d’informations, consultez la rubrique [Get Access with application Context](api-create-app-web.md).</span><span class="sxs-lookup"><span data-stu-id="ae073-127">For more information, see [Get access with application context](api-create-app-web.md).</span></span>


- <span data-ttu-id="ae073-128">**Contexte utilisateur :**</span><span class="sxs-lookup"><span data-stu-id="ae073-128">**User Context:**</span></span> <br>
    <span data-ttu-id="ae073-129">Permet d’effectuer des actions dans l’API pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae073-129">Used to perform actions in the API on behalf of a user.</span></span>

    <span data-ttu-id="ae073-130">Étapes à suivre pour accéder à l’API Microsoft 365 Defender avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="ae073-130">Steps that needs to be taken to access  Microsoft 365 Defender API with application context:</span></span>
  1. <span data-ttu-id="ae073-131">Créer une application native AAD.</span><span class="sxs-lookup"><span data-stu-id="ae073-131">Create AAD Native-Application.</span></span>
  2. <span data-ttu-id="ae073-132">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="ae073-132">Assign the desired permission to the application.</span></span> <span data-ttu-id="ae073-133">Par exemple, **incident. Read** , **AdvancedHunting. Read**.</span><span class="sxs-lookup"><span data-stu-id="ae073-133">For example, **Incident.Read** , **AdvancedHunting.Read**.</span></span>
  3. <span data-ttu-id="ae073-134">Obtenir un jeton à l’aide de l’application avec des informations d’identification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae073-134">Get token using the application with user credentials.</span></span>
  4. <span data-ttu-id="ae073-135">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-135">Use the token to access  Microsoft 365 Defender API</span></span>

     <span data-ttu-id="ae073-136">Pour plus d’informations, consultez la rubrique [Get Access with User Context](api-create-app-user-context.md).</span><span class="sxs-lookup"><span data-stu-id="ae073-136">For more information, see [Get access with user context](api-create-app-user-context.md).</span></span>


## <a name="related-topics"></a><span data-ttu-id="ae073-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae073-137">Related topics</span></span>
- [<span data-ttu-id="ae073-138">API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae073-138">Microsoft 365 Defender APIs</span></span>](api-supported.md)
- [<span data-ttu-id="ae073-139">Accéder à Microsoft 365 Defender avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="ae073-139">Access  Microsoft 365 Defender with application context</span></span>](api-create-app-web.md)
- [<span data-ttu-id="ae073-140">Accéder à Microsoft 365 Defender avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="ae073-140">Access  Microsoft 365 Defender with user context</span></span>](api-create-app-user-context.md)
