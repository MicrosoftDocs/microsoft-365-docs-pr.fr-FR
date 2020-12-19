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
ms.openlocfilehash: 5e01aaf2ee9255fd909b26278346fd4ccf54729a
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719237"
---
# <a name="access-the-microsoft-365-defender-apis"></a><span data-ttu-id="dba00-104">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dba00-104">Access the Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="dba00-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="dba00-105">**Applies to:**</span></span>

- <span data-ttu-id="dba00-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dba00-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dba00-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="dba00-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dba00-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="dba00-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="dba00-109">Microsoft 365 Defender expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="dba00-109">Microsoft 365 Defender exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="dba00-110">Ces API vous aident à automatiser les flux de travail et à utiliser pleinement les fonctionnalités de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="dba00-110">These APIs help you automate workflows and make full use of Microsoft 365 Defender's capabilities.</span></span>

<span data-ttu-id="dba00-111">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="dba00-111">In general, you'll need to take the following steps to use the APIs:</span></span>

- <span data-ttu-id="dba00-112">Créer une application Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="dba00-112">Create an Azure Active Directory application</span></span>
- <span data-ttu-id="dba00-113">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="dba00-113">Get an access token using this application</span></span>
- <span data-ttu-id="dba00-114">Utiliser le jeton pour accéder à l’API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dba00-114">Use the token to access the Microsoft 365 Defender API</span></span>

> [!NOTE]
> <span data-ttu-id="dba00-115">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="dba00-115">API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="dba00-116">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="dba00-116">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="dba00-117">Une fois que vous avez effectué ces étapes, vous êtes prêt à accéder à l’API Microsoft 365 Defender à l’aide d’un contexte particulier.</span><span class="sxs-lookup"><span data-stu-id="dba00-117">Once you've accomplished these steps, you're ready to access the Microsoft 365 Defender API using a particular context.</span></span>

## <a name="application-context-recommended"></a><span data-ttu-id="dba00-118">Contexte d’application (recommandé)</span><span class="sxs-lookup"><span data-stu-id="dba00-118">Application context (Recommended)</span></span>

<span data-ttu-id="dba00-119">Utilisez ce contexte pour les applications qui s’exécutent sans qu’un utilisateur connecté soit présent, tel que des services d’arrière-plan ou des démons.</span><span class="sxs-lookup"><span data-stu-id="dba00-119">Use this context for apps that run without a signed-in user present, such as background services or daemons.</span></span>

1. <span data-ttu-id="dba00-120">Créez une application Web Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dba00-120">Create an Azure Active Directory web application.</span></span>
2. <span data-ttu-id="dba00-121">Attribuez les autorisations souhaitées à l’application.</span><span class="sxs-lookup"><span data-stu-id="dba00-121">Assign the desired permissions to the application.</span></span>
3. <span data-ttu-id="dba00-122">Créez une clé pour l’application.</span><span class="sxs-lookup"><span data-stu-id="dba00-122">Create a key for the application.</span></span>
4. <span data-ttu-id="dba00-123">Obtenir un jeton de sécurité à l’aide de l’application et de sa clé.</span><span class="sxs-lookup"><span data-stu-id="dba00-123">Get a security token using the application and its key.</span></span>
5. <span data-ttu-id="dba00-124">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="dba00-124">Use the token to access  Microsoft 365 Defender API.</span></span>

<span data-ttu-id="dba00-125">Pour plus d’informations, consultez **[la rubrique créer une application pour accéder à Microsoft 365 Defender sans utilisateur](api-create-app-web.md)**.</span><span class="sxs-lookup"><span data-stu-id="dba00-125">For more information, see **[Create an app to access Microsoft 365 Defender without a user](api-create-app-web.md)**.</span></span>

## <a name="user-context"></a><span data-ttu-id="dba00-126">Contexte utilisateur</span><span class="sxs-lookup"><span data-stu-id="dba00-126">User context</span></span>

<span data-ttu-id="dba00-127">Utilisez ce contexte pour effectuer des actions au nom d’un utilisateur unique.</span><span class="sxs-lookup"><span data-stu-id="dba00-127">Use this context to perform actions on behalf of a single user.</span></span>

1. <span data-ttu-id="dba00-128">Créez une application native Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dba00-128">Create an Azure Active Directory native application.</span></span>
2. <span data-ttu-id="dba00-129">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="dba00-129">Assign the desired permission to the application.</span></span>
3. <span data-ttu-id="dba00-130">Obtenir un jeton de sécurité à l’aide des informations d’identification de l’utilisateur pour l’application.</span><span class="sxs-lookup"><span data-stu-id="dba00-130">Get a security token using the user credentials for the application.</span></span>
4. <span data-ttu-id="dba00-131">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="dba00-131">Use the token to access  Microsoft 365 Defender API.</span></span>

<span data-ttu-id="dba00-132">Pour plus d’informations, consultez **[la rubrique créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur](api-create-app-user-context.md)**.</span><span class="sxs-lookup"><span data-stu-id="dba00-132">For more information, see **[Create an app to access Microsoft 365 Defender APIs on behalf of a user](api-create-app-user-context.md)**.</span></span>

## <a name="partner-context"></a><span data-ttu-id="dba00-133">Contexte partenaire</span><span class="sxs-lookup"><span data-stu-id="dba00-133">Partner context</span></span>

<span data-ttu-id="dba00-134">Utilisez ce contexte lorsque vous devez fournir une application à de nombreux utilisateurs sur [plusieurs clients](https://docs.microsoft.com/azure/active-directory/develop/single-and-multi-tenant-apps).</span><span class="sxs-lookup"><span data-stu-id="dba00-134">Use this context when you need to provide an app to many users across [multiple tenants](https://docs.microsoft.com/azure/active-directory/develop/single-and-multi-tenant-apps).</span></span>

1. <span data-ttu-id="dba00-135">Créez une application mutualisée mutualisée d’Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dba00-135">Create an Azure Active Directory multi-tenant application.</span></span>
2. <span data-ttu-id="dba00-136">Attribuez l’autorisation souhaitée à l’application.</span><span class="sxs-lookup"><span data-stu-id="dba00-136">Assign the desired permission to the application.</span></span>
3. <span data-ttu-id="dba00-137">Obtenir le consentement de l' [administrateur](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) pour l’application de chaque client.</span><span class="sxs-lookup"><span data-stu-id="dba00-137">Get [admin consent](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent#requesting-consent-for-an-entire-tenant) for the app from each tenant.</span></span>
4. <span data-ttu-id="dba00-138">Obtenir un jeton de sécurité à l’aide des informations d’identification de l’utilisateur en fonction de l’ID de client d’un client.</span><span class="sxs-lookup"><span data-stu-id="dba00-138">Get a security token using user credentials based on a customer's tenant ID.</span></span>
5. <span data-ttu-id="dba00-139">Utilisez le jeton pour accéder à l’API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="dba00-139">Use the token to access  Microsoft 365 Defender API.</span></span>

<span data-ttu-id="dba00-140">Pour plus d’informations, consultez la rubrique **[créer une application avec un accès partenaire aux API Microsoft 365 Defender](api-partner-access.md)**.</span><span class="sxs-lookup"><span data-stu-id="dba00-140">For more information, see **[Create an app with partner access to Microsoft 365 Defender APIs](api-partner-access.md)**.</span></span>

## <a name="related-articles"></a><span data-ttu-id="dba00-141">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="dba00-141">Related articles</span></span>

- [<span data-ttu-id="dba00-142">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="dba00-142">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="dba00-143">Autorisation 2,0 OAuth pour l’authentification de l’utilisateur et l’accès à l’API</span><span class="sxs-lookup"><span data-stu-id="dba00-143">OAuth 2.0 authorization for user sign in and API access</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code)
- [<span data-ttu-id="dba00-144">Gérer les secrets dans vos applications serveur avec le coffre de clés Azure</span><span class="sxs-lookup"><span data-stu-id="dba00-144">Manage secrets in your server apps with Azure Key Vault</span></span>](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/)
- [<span data-ttu-id="dba00-145">Créer une application « Hello World » qui accède aux API Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="dba00-145">Create a 'Hello world' application that accesses the Microsoft 365 APIs</span></span>](api-hello-world.md)
