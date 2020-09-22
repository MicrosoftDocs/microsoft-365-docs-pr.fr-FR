---
title: Accéder aux API de protection contre les menaces Microsoft à l’aide de pour le compte de l’utilisateur
description: Découvrez comment accéder aux API de protection contre les menaces Microsoft à l’aide de pour le compte de l’utilisateur
keywords: accès, de la part de l’utilisateur, de l’API, de l’application, de l’utilisateur, du jeton d’accès, du jeton
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
ms.openlocfilehash: a62d90004d00e8c553f1b011e77b871df7cd94f4
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48197796"
---
# <a name="access-microsoft-threat-protection-apis-on-behalf-of-user"></a><span data-ttu-id="761e3-104">Accéder aux API de protection contre les menaces Microsoft pour le compte de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="761e3-104">Access Microsoft Threat Protection APIs on behalf of user</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="761e3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="761e3-105">**Applies to:**</span></span>
- <span data-ttu-id="761e3-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="761e3-106">Microsoft Threat Protection</span></span>

>[!IMPORTANT] 
><span data-ttu-id="761e3-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="761e3-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="761e3-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="761e3-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>


<span data-ttu-id="761e3-109">Cette page explique comment créer une application pour accéder par programme à Microsoft Threat Protection au nom d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="761e3-109">This page describes how to create an application to get programmatic access to Microsoft Threat Protection on behalf of a user.</span></span>

<span data-ttu-id="761e3-110">Si vous avez besoin d’un accès par programme à la protection Microsoft contre les menaces sans utilisateur, reportez-vous à la rubrique [créer une application pour accéder à la protection contre les menaces Microsoft sans utilisateur](api-create-app-web.md).</span><span class="sxs-lookup"><span data-stu-id="761e3-110">If you need programmatic access Microsoft Threat Protection without a user, refer to [Create an app to access Microsoft Threat Protection without a user](api-create-app-web.md).</span></span>

<span data-ttu-id="761e3-111">Si vous n’êtes pas certain de l’accès dont vous avez besoin, lisez l' [accès aux API de protection contre les menaces Microsoft](api-access.md).</span><span class="sxs-lookup"><span data-stu-id="761e3-111">If you are not sure which access you need, read the [Access the Microsoft Threat Protection APIs](api-access.md).</span></span>

<span data-ttu-id="761e3-112">La protection contre les menaces Microsoft expose une grande partie de ses données et actions via un ensemble d’API de programmation.</span><span class="sxs-lookup"><span data-stu-id="761e3-112">Microsoft Threat Protection exposes much of its data and actions through a set of programmatic APIs.</span></span> <span data-ttu-id="761e3-113">Ces API vous permettront d’automatiser les flux de travail et d’innover en fonction des fonctionnalités de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="761e3-113">Those APIs will enable you to automate work flows and innovate based on Microsoft Threat Protection capabilities.</span></span> <span data-ttu-id="761e3-114">L’accès à l’API nécessite l’authentification OAuth 2.0.</span><span class="sxs-lookup"><span data-stu-id="761e3-114">The API access requires OAuth2.0 authentication.</span></span> <span data-ttu-id="761e3-115">Pour plus d’informations, reportez-vous au [flux de code d’autorisation OAuth 2,0](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span><span class="sxs-lookup"><span data-stu-id="761e3-115">For more information, see [OAuth 2.0 Authorization Code Flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code).</span></span>

<span data-ttu-id="761e3-116">En règle générale, vous devez effectuer les étapes suivantes pour utiliser les API :</span><span class="sxs-lookup"><span data-stu-id="761e3-116">In general, you’ll need to take the following steps to use the APIs:</span></span>
- <span data-ttu-id="761e3-117">Créer une application AAD</span><span class="sxs-lookup"><span data-stu-id="761e3-117">Create an AAD application</span></span>
- <span data-ttu-id="761e3-118">Obtenir un jeton d’accès à l’aide de cette application</span><span class="sxs-lookup"><span data-stu-id="761e3-118">Get an access token using this application</span></span>
- <span data-ttu-id="761e3-119">Utiliser le jeton pour accéder à l’API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="761e3-119">Use the token to access Microsoft Threat Protection API</span></span>

<span data-ttu-id="761e3-120">Cette page explique comment créer une application AAD, obtenir un jeton d’accès à Microsoft Threat Protection et valider le jeton.</span><span class="sxs-lookup"><span data-stu-id="761e3-120">This page explains how to create an AAD application, get an access token to Microsoft Threat Protection and validate the token.</span></span>

>[!NOTE]
> <span data-ttu-id="761e3-121">Lors de l’accès à l’API de protection contre les menaces Microsoft pour le compte d’un utilisateur, vous aurez besoin de l’autorisation d’application et de l’autorisation utilisateur appropriées.</span><span class="sxs-lookup"><span data-stu-id="761e3-121">When accessing Microsoft Threat Protection API on behalf of a user, you will need the correct Application permission and user permission.</span></span>


>[!TIP]
> <span data-ttu-id="761e3-122">Si vous disposez de l’autorisation pour effectuer une action dans le portail, vous disposez de l’autorisation pour effectuer l’action dans l’API.</span><span class="sxs-lookup"><span data-stu-id="761e3-122">If you have the permission to perform an action in the portal, you have the permission to perform the action in the API.</span></span>

## <a name="create-an-app"></a><span data-ttu-id="761e3-123">Créer une application</span><span class="sxs-lookup"><span data-stu-id="761e3-123">Create an app</span></span>

1. <span data-ttu-id="761e3-124">Connectez-vous à [Azure](https://portal.azure.com) avec un utilisateur disposant du rôle **administrateur général** .</span><span class="sxs-lookup"><span data-stu-id="761e3-124">Log on to [Azure](https://portal.azure.com) with user that has **Global Administrator** role.</span></span>

2. <span data-ttu-id="761e3-125">Accédez à **Azure Active Directory**  >  **app Registrations**  >  **New Registration**.</span><span class="sxs-lookup"><span data-stu-id="761e3-125">Navigate to **Azure Active Directory** > **App registrations** > **New registration**.</span></span> 

   ![Image de Microsoft Azure et navigation de l’application](../../media/atp-azure-new-app2.png)

3. <span data-ttu-id="761e3-127">Dans l’inscription de, entrez les informations suivantes, puis cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="761e3-127">In the registration from, enter the following information then click **Register**.</span></span>

   ![Image de la fenêtre créer une application](../../media/nativeapp-create2.PNG)

   - <span data-ttu-id="761e3-129">**Nom :** Nom de votre application</span><span class="sxs-lookup"><span data-stu-id="761e3-129">**Name:** Your application name</span></span>
   - <span data-ttu-id="761e3-130">**Type d’application :** Client public</span><span class="sxs-lookup"><span data-stu-id="761e3-130">**Application type:** Public client</span></span>
   - <span data-ttu-id="761e3-131">**URI de redirection :**https://portal.azure.com</span><span class="sxs-lookup"><span data-stu-id="761e3-131">**Redirect URI:** https://portal.azure.com</span></span>

4. <span data-ttu-id="761e3-132">Pour permettre à votre application d’accéder à la protection contre les menaces Microsoft et de lui attribuer des autorisations, dans la page de votre application, sélectionnez autorisations de l' **API**  >  **Ajouter**une  >  **API mon organisation utilise** des >, tapez **protection Microsoft contre les menaces**, puis sélectionnez **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="761e3-132">To enable your app to access Microsoft Threat Protection and assign it permissions, on your application page, select **API Permissions** > **Add permission** > **APIs my organization uses** >, type **Microsoft Threat Protection**, and then select **Microsoft Threat Protection**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="761e3-133">La protection contre les menaces Microsoft ne s’affiche pas dans la liste d’origine.</span><span class="sxs-lookup"><span data-stu-id="761e3-133">Microsoft Threat Protection does not appear in the original list.</span></span> <span data-ttu-id="761e3-134">Vous devez commencer à écrire son nom dans la zone de texte pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="761e3-134">You need to start writing its name in the text box to see it appear.</span></span>

      ![Image de l’accès à l’API et de la sélection de l’API](../../media/apis-in-my-org-tab.PNG)

    - <span data-ttu-id="761e3-136">Sélectionnez **autorisations déléguées** > choisissez les autorisations appropriées pour votre scénario, par exemple, **incident. Read**, puis sélectionnez **Ajouter des autorisations**.</span><span class="sxs-lookup"><span data-stu-id="761e3-136">Choose **Delegated permissions** > Choose the relevant permissions for your scenario, e.g. **Incident.Read**, and then select **Add permissions**.</span></span>

      ![Image de l’accès à l’API et de la sélection de l’API](../../media/request-api-permissions-delegated.PNG)

     >[!IMPORTANT]
     ><span data-ttu-id="761e3-138">Vous devez sélectionner les autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="761e3-138">You need to select the relevant permissions.</span></span> 

    -  <span data-ttu-id="761e3-139">Pour déterminer les autorisations qui vous sont nécessaires, consultez la section **autorisations** dans l’API que vous souhaitez appeler.</span><span class="sxs-lookup"><span data-stu-id="761e3-139">To determine which permission you need, please look at the **Permissions** section in the API you are interested to call.</span></span>

    - <span data-ttu-id="761e3-140">Cliquez sur **accorder le consentement**</span><span class="sxs-lookup"><span data-stu-id="761e3-140">Click **Grant consent**</span></span>

      >[!NOTE]
      ><span data-ttu-id="761e3-141">Chaque fois que vous ajoutez une autorisation, vous devez cliquer sur **accorder le consentement** pour que la nouvelle autorisation prenne effet.</span><span class="sxs-lookup"><span data-stu-id="761e3-141">Every time you add permission you must click on **Grant consent** for the new permission to take effect.</span></span>

      ![Image des autorisations accorder](../../media/grant-consent-delegated.PNG)

6. <span data-ttu-id="761e3-143">Notez l’ID de votre application et votre ID de client :</span><span class="sxs-lookup"><span data-stu-id="761e3-143">Write down your application ID and your tenant ID:</span></span>

   - <span data-ttu-id="761e3-144">Sur la page de votre application, accédez à **vue d’ensemble** et copiez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="761e3-144">On your application page, go to **Overview** and copy the following:</span></span>

   ![Image de l’ID d’application créé](../../media/app-and-tenant-ids.png)


## <a name="get-an-access-token-using-powershell"></a><span data-ttu-id="761e3-146">Obtenir un jeton d’accès à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="761e3-146">Get an access token using PowerShell</span></span>

```
#Install the ADAL.PS package if it's not installed.
if(!(Get-Package adal.ps)) { Install-Package -Name adal.ps }

$authority = "https://login.windows.net/{tenant-id}" # replace {tenant-id} with your tenant ID.

$clientId = "{application-id}" #replace {application-id} with your application ID.

$redirectUri = "{redirect-uri}" # replace {redirect-uri} with your application redirect URI.

$resourceUrl = "https://api.security.microsoft.com"

$response = Get-ADALToken -Resource $resourceUrl -ClientId $clientId -RedirectUri $redirectUri -Authority $authority -PromptBehavior:Always
$response.AccessToken | clip
$response.AccessToken
```

## <a name="related-topics"></a><span data-ttu-id="761e3-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="761e3-147">Related topics</span></span>
- [<span data-ttu-id="761e3-148">Accéder aux API de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="761e3-148">Access the Microsoft Threat Protection APIs</span></span>](api-access.md)
- [<span data-ttu-id="761e3-149">Accéder à la protection contre les menaces Microsoft avec le contexte d’application</span><span class="sxs-lookup"><span data-stu-id="761e3-149">Access  Microsoft Threat Protection with application context</span></span>](api-create-app-web.md)
