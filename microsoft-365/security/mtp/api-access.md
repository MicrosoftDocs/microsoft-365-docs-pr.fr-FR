---
title: Accéder aux API de protection contre les menaces Microsoft
description: Découvrez comment accéder aux API de protection contre les menaces Microsoft
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
ms.openlocfilehash: 653c359c324852719688a374a6e863df0a1909ba
ms.sourcegitcommit: 9a275a13af3e063e80ce1bd3cd8142a095db92d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2020
ms.locfileid: "47650302"
---
# <a name="access-the-microsoft-threat-protection-apis"></a><span data-ttu-id="71b09-104">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="71b09-104">Access the Microsoft Threat Protection APIs</span></span>

<span data-ttu-id="71b09-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="71b09-105">**Applies to:**</span></span>
- <span data-ttu-id="71b09-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="71b09-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="71b09-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="71b09-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="71b09-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="71b09-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


 <span data-ttu-id="71b09-109">La protection contre les menaces Microsoft expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="71b09-109">Microsoft Threat Protection exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="71b09-110">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="71b09-110">Those APIs will enable you to automate workflows and innovate based on  Microsoft Threat Protection capabilities.</span></span> <span data-ttu-id="71b09-111">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="71b09-111">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="71b09-112">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="71b09-112">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>


<span data-ttu-id="71b09-113">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="71b09-113">In general, you'll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="71b09-114">Créer une application AAD</span><span class="sxs-lookup"><span data-stu-id="71b09-114">Create an AAD application</span></span>
- <span data-ttu-id="71b09-115">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="71b09-115">Get an access token using this application</span></span>
- <span data-ttu-id="71b09-116">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="71b09-116">Use the token to access  Microsoft Threat Protection API</span></span>


<span data-ttu-id="71b09-117">Vous pouvez accéder à l’API de protection contre les menaces Microsoft avec le contexte de l' **application** ou le **contexte utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="71b09-117">You can access  Microsoft Threat Protection API with **Application Context** or **User Context**.</span></span>

- <span data-ttu-id="71b09-118">**Contexte de l’application : (recommandé)**</span><span class="sxs-lookup"><span data-stu-id="71b09-118">**Application Context: (Recommended)**</span></span> <br>
    <span data-ttu-id="71b09-119">Utilisé par les applications qui s’exécutent sans qu’aucun utilisateur ne soit connecté.</span><span class="sxs-lookup"><span data-stu-id="71b09-119">Used by apps that run without a signed-in user present.</span></span> <span data-ttu-id="71b09-120">par exemple, les applications qui s’exécutent en tant que services ou démons d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="71b09-120">for example, apps that run as background services or daemons.</span></span>

    <span data-ttu-id="71b09-121">Étapes à suivre pour accéder à l’API Microsoft Threat Protection avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="71b09-121">Steps that need to be taken to access  Microsoft Threat Protection API with application context:</span></span>

  1. <span data-ttu-id="71b09-122">Créer une application Web AAD.</span><span class="sxs-lookup"><span data-stu-id="71b09-122">Create an AAD Web-Application.</span></span>
  2. <span data-ttu-id="71b09-123">Attribuez l’autorisation souhaitée à l’exemple applicationFor, **incident. Read. All**, **AdvancedHunting. Read. All**.</span><span class="sxs-lookup"><span data-stu-id="71b09-123">Assign the desired permission to the applicationFor example, **Incident.Read.All**, **AdvancedHunting.Read.All**.</span></span> 
  3. <span data-ttu-id="71b09-124">Créez une clé pour cette application.</span><span class="sxs-lookup"><span data-stu-id="71b09-124">Create a key for this Application.</span></span>
  4. <span data-ttu-id="71b09-125">Obtenir un jeton à l’aide de l’application avec sa clé.</span><span class="sxs-lookup"><span data-stu-id="71b09-125">Get token using the application with its key.</span></span>
  5. <span data-ttu-id="71b09-126">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="71b09-126">Use the token to access  Microsoft Threat Protection API</span></span>

     <span data-ttu-id="71b09-127">Pour plus d’informations, consultez la rubrique [Get Access with application Context](api-create-app-web.md).</span><span class="sxs-lookup"><span data-stu-id="71b09-127">For more information, see [Get access with application context](api-create-app-web.md).</span></span>


- <span data-ttu-id="71b09-128">**Contexte utilisateur :**</span><span class="sxs-lookup"><span data-stu-id="71b09-128">**User Context:**</span></span> <br>
    <span data-ttu-id="71b09-129">Permet d’effectuer des actions dans l’API pour le compte d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71b09-129">Used to perform actions in the API on behalf of a user.</span></span>

    <span data-ttu-id="71b09-130">Étapes à suivre pour accéder à l’API Microsoft Threat Protection avec le contexte de l’application :</span><span class="sxs-lookup"><span data-stu-id="71b09-130">Steps that needs to be taken to access  Microsoft Threat Protection API with application context:</span></span>
  1. <span data-ttu-id="71b09-131">Créer une application native AAD.</span><span class="sxs-lookup"><span data-stu-id="71b09-131">Create AAD Native-Application.</span></span>
  2. <span data-ttu-id="71b09-132">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="71b09-132">Assign the desired permission to the application.</span></span> <span data-ttu-id="71b09-133">Par exemple, **incident. Read**, **AdvancedHunting. Read**.</span><span class="sxs-lookup"><span data-stu-id="71b09-133">For example, **Incident.Read**, **AdvancedHunting.Read**.</span></span>
  3. <span data-ttu-id="71b09-134">Obtenir un jeton à l’aide de l’application avec des informations d’identification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="71b09-134">Get token using the application with user credentials.</span></span>
  4. <span data-ttu-id="71b09-135">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="71b09-135">Use the token to access  Microsoft Threat Protection API</span></span>

     <span data-ttu-id="71b09-136">Pour plus d’informations, consultez la rubrique [Get Access with User Context](api-create-app-user-context.md).</span><span class="sxs-lookup"><span data-stu-id="71b09-136">For more information, see [Get access with user context](api-create-app-user-context.md).</span></span>


## <a name="related-topics"></a><span data-ttu-id="71b09-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b09-137">Related topics</span></span>
- [<span data-ttu-id="71b09-138">API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="71b09-138">Microsoft Threat Protection APIs</span></span>](api-supported.md)
- [<span data-ttu-id="71b09-139">Accéder à la protection contre les menaces Microsoft avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="71b09-139">Access  Microsoft Threat Protection with application context</span></span>](api-create-app-web.md)
- [<span data-ttu-id="71b09-140">Accéder à la protection contre les menaces Microsoft avec le contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="71b09-140">Access  Microsoft Threat Protection with user context</span></span>](api-create-app-user-context.md)
