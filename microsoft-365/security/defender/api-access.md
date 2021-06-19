---
title: Accéder aux API Microsoft 365 Defender de données
description: Découvrez comment accéder aux API Microsoft 365 Defender de données
keywords: accès, api, contexte d’application, contexte utilisateur, application aad, jeton d’accès
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 03fd82cd5dc24653b6d67fa47cc225d355bfac45
ms.sourcegitcommit: d904f04958a13a514ce10219ed822b9e4f74ca2d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "53028798"
---
# <a name="access-the-microsoft-365-defender-apis"></a><span data-ttu-id="d12e9-104">Accéder aux API Microsoft 365 Defender de données</span><span class="sxs-lookup"><span data-stu-id="d12e9-104">Access the Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="d12e9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d12e9-105">**Applies to:**</span></span>

- <span data-ttu-id="d12e9-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d12e9-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d12e9-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="d12e9-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d12e9-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="d12e9-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="d12e9-109">Microsoft 365 Defender expose la plupart de ses données et actions par le biais d’un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="d12e9-109">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="d12e9-110">Ces API vous aident à automatiser les flux de travail et à utiliser Microsoft 365 Defender fonctionnalités de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d12e9-110">These APIs help you automate workflows and make full use of Microsoft 365 Defender's capabilities.</span></span>

<span data-ttu-id="d12e9-111">En règle générale, vous devez suivre les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="d12e9-111">In general, you'll need to take the following steps to use the APIs:</span></span>

- <span data-ttu-id="d12e9-112">Créer une application Azure Active Directory application</span><span class="sxs-lookup"><span data-stu-id="d12e9-112">Create an Azure Active Directory application</span></span>
- <span data-ttu-id="d12e9-113">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="d12e9-113">Get an access token using this application</span></span>
- <span data-ttu-id="d12e9-114">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d12e9-114">Use the token to access the Microsoft 365 Defender API</span></span>

> [!NOTE]
> <span data-ttu-id="d12e9-115">L’accès à l’API nécessite une authentification OAuth2.0.</span><span class="sxs-lookup"><span data-stu-id="d12e9-115">API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="d12e9-116">Pour plus d’informations, [voir code d’autorisation OAuth 2.0 Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="d12e9-116">For more information, see [OAuth 2.0 Authorization Code Flow](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="d12e9-117">Une fois ces étapes accomplies, vous êtes prêt à accéder à l’API Microsoft 365 Defender à l’aide d’un contexte particulier.</span><span class="sxs-lookup"><span data-stu-id="d12e9-117">Once you've accomplished these steps, you're ready to access the Microsoft 365 Defender API using a particular context.</span></span>

## <a name="application-context-recommended"></a><span data-ttu-id="d12e9-118">Contexte de l’application (recommandé)</span><span class="sxs-lookup"><span data-stu-id="d12e9-118">Application context (Recommended)</span></span>

<span data-ttu-id="d12e9-119">Utilisez ce contexte pour les applications qui s’exécutent sans utilisateur inscrit, tels que les services d’arrière-plan ou les daemons.</span><span class="sxs-lookup"><span data-stu-id="d12e9-119">Use this context for apps that run without a signed-in user present, such as background services or daemons.</span></span>

1. <span data-ttu-id="d12e9-120">Créez une Azure Active Directory application web.</span><span class="sxs-lookup"><span data-stu-id="d12e9-120">Create an Azure Active Directory web application.</span></span>
2. <span data-ttu-id="d12e9-121">Attribuez les autorisations souhaitées à l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e9-121">Assign the desired permissions to the application.</span></span>
3. <span data-ttu-id="d12e9-122">Créez une clé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e9-122">Create a key for the application.</span></span>
4. <span data-ttu-id="d12e9-123">Obtenez un jeton de sécurité à l’aide de l’application et de sa clé.</span><span class="sxs-lookup"><span data-stu-id="d12e9-123">Get a security token using the application and its key.</span></span>
5. <span data-ttu-id="d12e9-124">Utilisez le jeton pour accéder à Microsoft 365 Defender API.</span><span class="sxs-lookup"><span data-stu-id="d12e9-124">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="d12e9-125">Pour plus d’informations, voir **[Créer une application pour accéder Microsoft 365 Defender sans utilisateur.](api-create-app-web.md)**</span><span class="sxs-lookup"><span data-stu-id="d12e9-125">For more information, see **[Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md)**.</span></span>

## <a name="user-context"></a><span data-ttu-id="d12e9-126">Contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="d12e9-126">User context</span></span>

<span data-ttu-id="d12e9-127">Utilisez ce contexte pour effectuer des actions au nom d’un seul utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d12e9-127">Use this context to perform actions on behalf of a single user.</span></span>

1. <span data-ttu-id="d12e9-128">Créez une Azure Active Directory application native.</span><span class="sxs-lookup"><span data-stu-id="d12e9-128">Create an Azure Active Directory native application.</span></span>
2. <span data-ttu-id="d12e9-129">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e9-129">Assign the desired permission to the application.</span></span>
3. <span data-ttu-id="d12e9-130">Obtenez un jeton de sécurité à l’aide des informations d’identification de l’utilisateur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e9-130">Get a security token using the user credentials for the application.</span></span>
4. <span data-ttu-id="d12e9-131">Utilisez le jeton pour accéder à Microsoft 365 Defender API.</span><span class="sxs-lookup"><span data-stu-id="d12e9-131">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="d12e9-132">Pour plus d’informations, voir **[Créer une application pour accéder Microsoft 365 Defender API au nom d’un utilisateur.](api-create-app-user-context.md)**</span><span class="sxs-lookup"><span data-stu-id="d12e9-132">For more information, see **[Create an app to access Microsoft 365 Defender APIs on behalf of a user](api-create-app-user-context.md)**.</span></span>

## <a name="partner-context"></a><span data-ttu-id="d12e9-133">Contexte du partenaire</span><span class="sxs-lookup"><span data-stu-id="d12e9-133">Partner context</span></span>

<span data-ttu-id="d12e9-134">Utilisez ce contexte lorsque vous devez fournir une application à de nombreux utilisateurs sur [plusieurs clients.](/azure/active-directory/develop/single-and-multi-tenant-apps)</span><span class="sxs-lookup"><span data-stu-id="d12e9-134">Use this context when you need to provide an app to many users across [multiple tenants](/azure/active-directory/develop/single-and-multi-tenant-apps).</span></span>

1. <span data-ttu-id="d12e9-135">Créez une Azure Active Directory application multi-client.</span><span class="sxs-lookup"><span data-stu-id="d12e9-135">Create an Azure Active Directory multi-tenant application.</span></span>
2. <span data-ttu-id="d12e9-136">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="d12e9-136">Assign the desired permission to the application.</span></span>
3. <span data-ttu-id="d12e9-137">Obtenir [le consentement de l’administrateur](/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) pour l’application auprès de chaque client.</span><span class="sxs-lookup"><span data-stu-id="d12e9-137">Get [admin consent](/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) for the app from each tenant.</span></span>
4. <span data-ttu-id="d12e9-138">Obtenez un jeton de sécurité à l’aide des informations d’identification de l’utilisateur en fonction de l’ID de locataire d’un client.</span><span class="sxs-lookup"><span data-stu-id="d12e9-138">Get a security token using user credentials based on a customer's tenant ID.</span></span>
5. <span data-ttu-id="d12e9-139">Utilisez le jeton pour accéder à Microsoft 365 Defender API.</span><span class="sxs-lookup"><span data-stu-id="d12e9-139">Use the token to access Microsoft 365 Defender API.</span></span>

<span data-ttu-id="d12e9-140">Pour plus d’informations, voir Créer une application avec un accès partenaire **[à Microsoft 365 Defender API.](api-partner-access.md)**</span><span class="sxs-lookup"><span data-stu-id="d12e9-140">For more information, see **[Create an app with partner access to Microsoft 365 Defender APIs](api-partner-access.md)**.</span></span>

## <a name="related-articles"></a><span data-ttu-id="d12e9-141">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="d12e9-141">Related articles</span></span>

- [<span data-ttu-id="d12e9-142">Microsoft 365 Defender Vue d’ensemble des API</span><span class="sxs-lookup"><span data-stu-id="d12e9-142">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="d12e9-143">Autorisation OAuth 2.0 pour la connexion de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="d12e9-143">OAuth 2.0 authorization for user sign in and API access</span></span>](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
- [<span data-ttu-id="d12e9-144">Gérer les secrets dans vos applications serveur avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="d12e9-144">Manage secrets in your server apps with Azure Key Vault</span></span>](/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="d12e9-145">Créer une application « Hello World » qui accède aux API Microsoft 365 de l’application</span><span class="sxs-lookup"><span data-stu-id="d12e9-145">Create a 'Hello world' application that accesses the Microsoft 365 APIs</span></span>](api-hello-world.md)