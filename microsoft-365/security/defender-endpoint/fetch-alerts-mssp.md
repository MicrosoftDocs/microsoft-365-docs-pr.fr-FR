---
title: Récupérer des alertes à partir du client MSSP
description: Découvrez comment récupérer des alertes à partir d’un client
keywords: fournisseur de services de sécurité géré, mssp, configurer, intégration
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
ms.custom: api
ms.openlocfilehash: 456507533265bc085adc1008f3264e123569a6ca
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52770768"
---
# <a name="fetch-alerts-from-mssp-customer-tenant"></a><span data-ttu-id="95c42-104">Récupérer des alertes à partir du client MSSP</span><span class="sxs-lookup"><span data-stu-id="95c42-104">Fetch alerts from MSSP customer tenant</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="95c42-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="95c42-105">**Applies to:**</span></span>
- [<span data-ttu-id="95c42-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="95c42-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="95c42-107">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="95c42-107">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="95c42-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="95c42-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-mssp-support-abovefoldlink)

>[!NOTE]
><span data-ttu-id="95c42-109">Cette action est prise par le MSSP.</span><span class="sxs-lookup"><span data-stu-id="95c42-109">This action is taken by the MSSP.</span></span>


<span data-ttu-id="95c42-110">Il existe deux façons d’extraire des alertes :</span><span class="sxs-lookup"><span data-stu-id="95c42-110">There are two ways you can fetch alerts:</span></span>
- <span data-ttu-id="95c42-111">Utilisation de la méthode SIEM</span><span class="sxs-lookup"><span data-stu-id="95c42-111">Using the SIEM method</span></span>
- <span data-ttu-id="95c42-112">Utilisation des API</span><span class="sxs-lookup"><span data-stu-id="95c42-112">Using APIs</span></span>

## <a name="fetch-alerts-into-your-siem"></a><span data-ttu-id="95c42-113">Récupérer des alertes dans votre SIEM</span><span class="sxs-lookup"><span data-stu-id="95c42-113">Fetch alerts into your SIEM</span></span>

<span data-ttu-id="95c42-114">Pour récupérer des alertes dans votre système SIEM, vous devez suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="95c42-114">To fetch alerts into your SIEM system, you'll need to take the following steps:</span></span>

<span data-ttu-id="95c42-115">Étape 1 : Créer une application tierce</span><span class="sxs-lookup"><span data-stu-id="95c42-115">Step 1: Create a third-party application</span></span>

<span data-ttu-id="95c42-116">Étape 2 : Obtenir des jetons d’accès et d’actualisation à partir du client de votre client</span><span class="sxs-lookup"><span data-stu-id="95c42-116">Step 2: Get access and refresh tokens from your customer's tenant</span></span>
 
<span data-ttu-id="95c42-117">Étape 3 : autoriser votre application sur Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="95c42-117">Step 3: allow your application on Microsoft Defender Security Center</span></span>
 
### <a name="step-1-create-an-application-in-azure-active-directory-azure-ad"></a><span data-ttu-id="95c42-118">Étape 1 : Créer une application dans Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="95c42-118">Step 1: Create an application in Azure Active Directory (Azure AD)</span></span>
 
<span data-ttu-id="95c42-119">Vous devez créer une application et lui accorder des autorisations pour récupérer des alertes à partir du client Microsoft Defender for Endpoint de votre client.</span><span class="sxs-lookup"><span data-stu-id="95c42-119">You'll need to create an application and grant it permissions to fetch alerts from your customer's Microsoft Defender for Endpoint tenant.</span></span>

1. <span data-ttu-id="95c42-120">Connectez-vous au [portail Azure AD.](https://aad.portal.azure.com/)</span><span class="sxs-lookup"><span data-stu-id="95c42-120">Sign in to the [Azure AD portal](https://aad.portal.azure.com/).</span></span>

2. <span data-ttu-id="95c42-121">Sélectionnez **Azure Active Directory**  >  **inscriptions d’application.**</span><span class="sxs-lookup"><span data-stu-id="95c42-121">Select **Azure Active Directory** > **App registrations**.</span></span>
 
3. <span data-ttu-id="95c42-122">Cliquez **sur Nouvelle inscription.**</span><span class="sxs-lookup"><span data-stu-id="95c42-122">Click **New registration**.</span></span>

4. <span data-ttu-id="95c42-123">Spécifiez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="95c42-123">Specify the following values:</span></span>

    - <span data-ttu-id="95c42-124">Nom : \<Tenant_name\> Connecteur MSSP SIEM (remplacez Tenant_name par le nom complet du client)</span><span class="sxs-lookup"><span data-stu-id="95c42-124">Name: \<Tenant_name\> SIEM MSSP Connector (replace Tenant_name with the tenant display name)</span></span>
 
    - <span data-ttu-id="95c42-125">Types de comptes pris en charge : compte dans cet annuaire d’organisation uniquement</span><span class="sxs-lookup"><span data-stu-id="95c42-125">Supported account types: Account in this organizational directory only</span></span> 
    - <span data-ttu-id="95c42-126">URI de redirection : sélectionnez Web et tapez `https://<domain_name>/SiemMsspConnector` (remplacez <domain_name> par le nom du client)</span><span class="sxs-lookup"><span data-stu-id="95c42-126">Redirect URI: Select Web and type `https://<domain_name>/SiemMsspConnector`(replace <domain_name> with the tenant name)</span></span>

5. <span data-ttu-id="95c42-127">Cliquez sur **S'inscrire**.</span><span class="sxs-lookup"><span data-stu-id="95c42-127">Click **Register**.</span></span> <span data-ttu-id="95c42-128">L’application s’affiche dans la liste des applications que vous possédez.</span><span class="sxs-lookup"><span data-stu-id="95c42-128">The application is displayed in the list of applications you own.</span></span>

6. <span data-ttu-id="95c42-129">Sélectionnez l’application, puis cliquez sur **Vue d’ensemble.**</span><span class="sxs-lookup"><span data-stu-id="95c42-129">Select the application, then click **Overview**.</span></span>

7. <span data-ttu-id="95c42-130">Copiez la valeur du champ ID de **l’application (client)** dans un endroit sûr. Vous en aurez besoin à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="95c42-130">Copy the value from the **Application (client) ID** field to a safe place, you will need this in the next step.</span></span>

8. <span data-ttu-id="95c42-131">Sélectionnez **Certificat & secrets dans** le nouveau panneau d’application.</span><span class="sxs-lookup"><span data-stu-id="95c42-131">Select **Certificate & secrets** in the new application panel.</span></span>

9. <span data-ttu-id="95c42-132">Cliquez **sur Nouvelle secret client**.</span><span class="sxs-lookup"><span data-stu-id="95c42-132">Click **New client secret**.</span></span>

    - <span data-ttu-id="95c42-133">Description : entrez une description de la clé.</span><span class="sxs-lookup"><span data-stu-id="95c42-133">Description: Enter a description for the key.</span></span>
    - <span data-ttu-id="95c42-134">Expire : sélection **dans 1 an**</span><span class="sxs-lookup"><span data-stu-id="95c42-134">Expires: Select **In 1 year**</span></span>

 
10. <span data-ttu-id="95c42-135">Cliquez **sur** Ajouter , copiez la valeur de la question secrète client dans un endroit sûr. Vous en aurez besoin à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="95c42-135">Click **Add**, copy the value of the client secret to a safe place, you will need this in the next step.</span></span>
 

### <a name="step-2-get-access-and-refresh-tokens-from-your-customers-tenant"></a><span data-ttu-id="95c42-136">Étape 2 : Obtenir des jetons d’accès et d’actualisation à partir du client de votre client</span><span class="sxs-lookup"><span data-stu-id="95c42-136">Step 2: Get access and refresh tokens from your customer's tenant</span></span>
<span data-ttu-id="95c42-137">Cette section vous guide sur l’utilisation d’un script PowerShell pour obtenir les jetons du client de votre client.</span><span class="sxs-lookup"><span data-stu-id="95c42-137">This section guides you on how to use a PowerShell script to get the tokens from your customer's tenant.</span></span> <span data-ttu-id="95c42-138">Ce script utilise l’application de l’étape précédente pour obtenir les jetons d’accès et d’actualisation à l’aide du code d’autorisation OAuth Flow.</span><span class="sxs-lookup"><span data-stu-id="95c42-138">This script uses the application from the previous step to get the access and refresh tokens using the OAuth Authorization Code Flow.</span></span>

<span data-ttu-id="95c42-139">Après avoir fourni vos informations d’identification, vous devez donner votre consentement à l’application afin que l’application soit mise en service dans le client du client.</span><span class="sxs-lookup"><span data-stu-id="95c42-139">After providing your credentials, you'll need to grant consent to the application so that the application is provisioned in the customer's tenant.</span></span>


1. <span data-ttu-id="95c42-140">Créez un dossier et nommez-le : `MsspTokensAcquisition` .</span><span class="sxs-lookup"><span data-stu-id="95c42-140">Create a new folder and name it: `MsspTokensAcquisition`.</span></span>

2. <span data-ttu-id="95c42-141">Téléchargez [le module LoginBrowser.psm1](https://github.com/shawntabrizi/Microsoft-Authentication-with-PowerShell-and-MSAL/blob/master/Authorization%20Code%20Grant%20Flow/LoginBrowser.psm1) et enregistrez-le dans le `MsspTokensAcquisition` dossier.</span><span class="sxs-lookup"><span data-stu-id="95c42-141">Download the [LoginBrowser.psm1 module](https://github.com/shawntabrizi/Microsoft-Authentication-with-PowerShell-and-MSAL/blob/master/Authorization%20Code%20Grant%20Flow/LoginBrowser.psm1) and save it in the `MsspTokensAcquisition` folder.</span></span>

    >[!NOTE]
    ><span data-ttu-id="95c42-142">À la ligne 30, `authorzationUrl` remplacez par `authorizationUrl` .</span><span class="sxs-lookup"><span data-stu-id="95c42-142">In line 30, replace `authorzationUrl` with `authorizationUrl`.</span></span>

3. <span data-ttu-id="95c42-143">Créez un fichier avec le contenu suivant et enregistrez-le avec le nom `MsspTokensAcquisition.ps1` dans le dossier :</span><span class="sxs-lookup"><span data-stu-id="95c42-143">Create a file with the following content and save it with the name `MsspTokensAcquisition.ps1` in the folder:</span></span>
    ```
    param (
        [Parameter(Mandatory=$true)][string]$clientId,
        [Parameter(Mandatory=$true)][string]$secret,
        [Parameter(Mandatory=$true)][string]$tenantId
    )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12

    # Load our Login Browser Function
    Import-Module .\LoginBrowser.psm1

    # Configuration parameters
    $login = "https://login.microsoftonline.com"
    $redirectUri = "https://SiemMsspConnector"
    $resourceId = "https://graph.windows.net"

    Write-Host 'Prompt the user for his credentials, to get an authorization code'
    $authorizationUrl = ("{0}/{1}/oauth2/authorize?prompt=select_account&response_type=code&client_id={2}&redirect_uri={3}&resource={4}" -f
                        $login, $tenantId, $clientId, $redirectUri, $resourceId)
    Write-Host "authorzationUrl: $authorizationUrl"

    # Fake a proper endpoint for the Redirect URI
    $code = LoginBrowser $authorizationUrl $redirectUri

    # Acquire token using the authorization code

    $Body = @{
        grant_type = 'authorization_code'
        client_id = $clientId
        code = $code
        redirect_uri = $redirectUri
        resource = $resourceId
        client_secret = $secret
    }

    $tokenEndpoint = "$login/$tenantId/oauth2/token?"
    $Response = Invoke-RestMethod -Method Post -Uri $tokenEndpoint -Body $Body
    $token = $Response.access_token
    $refreshToken= $Response.refresh_token

    Write-Host " -----------------------------------  TOKEN ---------------------------------- "
    Write-Host $token

    Write-Host " -----------------------------------  REFRESH TOKEN ---------------------------------- "
    Write-Host $refreshToken 
    ```
4. <span data-ttu-id="95c42-144">Ouvrez une invite de commandes PowerShell avec élévation de niveaux dans le `MsspTokensAcquisition` dossier.</span><span class="sxs-lookup"><span data-stu-id="95c42-144">Open an elevated PowerShell command prompt in the `MsspTokensAcquisition` folder.</span></span>

5. <span data-ttu-id="95c42-145">Exécutez la commande suivante : `Set-ExecutionPolicy -ExecutionPolicy Bypass`</span><span class="sxs-lookup"><span data-stu-id="95c42-145">Run the following command: `Set-ExecutionPolicy -ExecutionPolicy Bypass`</span></span>

6. <span data-ttu-id="95c42-146">Entrez les commandes suivantes : `.\MsspTokensAcquisition.ps1 -clientId <client_id> -secret <app_key> -tenantId <customer_tenant_id>`</span><span class="sxs-lookup"><span data-stu-id="95c42-146">Enter the following commands: `.\MsspTokensAcquisition.ps1 -clientId <client_id> -secret <app_key> -tenantId <customer_tenant_id>`</span></span>
 
    - <span data-ttu-id="95c42-147">\<client_id\>Remplacez-le **par l’ID d’application (client)** obtenu à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="95c42-147">Replace \<client_id\> with the **Application (client) ID** you got from the previous step.</span></span>
    - <span data-ttu-id="95c42-148">Remplacez \<app_key\> par la secret client **que** vous avez créée à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="95c42-148">Replace \<app_key\> with the **Client Secret** you created from the previous step.</span></span>
    - <span data-ttu-id="95c42-149">Remplacez \<customer_tenant_id\> par l’ID de **locataire de votre client.**</span><span class="sxs-lookup"><span data-stu-id="95c42-149">Replace \<customer_tenant_id\> with your customer's **Tenant ID**.</span></span> 
 

7. <span data-ttu-id="95c42-150">Vous serez invité à fournir vos informations d’identification et votre consentement.</span><span class="sxs-lookup"><span data-stu-id="95c42-150">You'll be asked to provide your credentials and consent.</span></span> <span data-ttu-id="95c42-151">Ignorez la redirection de page.</span><span class="sxs-lookup"><span data-stu-id="95c42-151">Ignore the page redirect.</span></span>

8. <span data-ttu-id="95c42-152">Dans la fenêtre PowerShell, vous recevrez un jeton d’accès et un jeton d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="95c42-152">In the PowerShell window, you'll receive an access token and a refresh token.</span></span> <span data-ttu-id="95c42-153">Enregistrez le jeton d’actualisation pour configurer votre connecteur SIEM.</span><span class="sxs-lookup"><span data-stu-id="95c42-153">Save the refresh token to configure your SIEM connector.</span></span> 
 
### <a name="step-3-allow-your-application-on-microsoft-defender-security-center"></a><span data-ttu-id="95c42-154">Étape 3 : Autoriser votre application sur Centre de sécurité Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="95c42-154">Step 3: Allow your application on Microsoft Defender Security Center</span></span>
<span data-ttu-id="95c42-155">Vous devez autoriser l’application que vous avez créée dans Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="95c42-155">You'll need to allow the application you created in Microsoft Defender Security Center.</span></span>
 
<span data-ttu-id="95c42-156">Vous devez avoir l’autorisation Gérer les **paramètres système** du portail pour autoriser l’application.</span><span class="sxs-lookup"><span data-stu-id="95c42-156">You'll need to have **Manage portal system settings** permission to allow the application.</span></span> <span data-ttu-id="95c42-157">Dans le cas contraire, vous devrez demander à votre client d’autoriser l’application pour vous.</span><span class="sxs-lookup"><span data-stu-id="95c42-157">Otherwise, you'll need to request your customer to allow the application for you.</span></span>

1. <span data-ttu-id="95c42-158">Go to `https://securitycenter.windows.com?tid=<customer_tenant_id>` (replace \<customer_tenant_id\> with the customer's tenant ID.</span><span class="sxs-lookup"><span data-stu-id="95c42-158">Go to `https://securitycenter.windows.com?tid=<customer_tenant_id>` (replace \<customer_tenant_id\> with the customer's tenant ID.</span></span>

2. <span data-ttu-id="95c42-159">Cliquez **Paramètres**  >  **SIEM.**</span><span class="sxs-lookup"><span data-stu-id="95c42-159">Click **Settings** > **SIEM**.</span></span> 

3. <span data-ttu-id="95c42-160">Sélectionnez **l’onglet MSSP.**</span><span class="sxs-lookup"><span data-stu-id="95c42-160">Select the **MSSP** tab.</span></span>

4. <span data-ttu-id="95c42-161">Entrez **l’ID d’application** à partir de la première étape et votre **ID de client.**</span><span class="sxs-lookup"><span data-stu-id="95c42-161">Enter the **Application ID** from the first step and your **Tenant ID**.</span></span>

5. <span data-ttu-id="95c42-162">Cliquez **sur Autoriser l’application.**</span><span class="sxs-lookup"><span data-stu-id="95c42-162">Click **Authorize application**.</span></span> 

 
<span data-ttu-id="95c42-163">Vous pouvez maintenant télécharger le fichier de configuration approprié pour votre SIEM et vous connecter à l’API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="95c42-163">You can now download the relevant configuration file for your SIEM and connect to the Defender for Endpoint API.</span></span> <span data-ttu-id="95c42-164">Pour plus d’informations, voir [« Tirer des alertes vers vos outils SIEM](configure-siem.md)».</span><span class="sxs-lookup"><span data-stu-id="95c42-164">For more information, see, [Pull alerts to your SIEM tools](configure-siem.md).</span></span>
 

- <span data-ttu-id="95c42-165">Dans le fichier de configuration ArcSight /Splunk Authentication Properties, écrivez votre clé d’application manuellement en définir la valeur secrète.</span><span class="sxs-lookup"><span data-stu-id="95c42-165">In the ArcSight configuration file / Splunk Authentication Properties file, write your application key manually by setting the secret value.</span></span>
- <span data-ttu-id="95c42-166">Au lieu d’acquérir un jeton d’actualisation dans le portail, utilisez le script de l’étape précédente pour acquérir un jeton d’actualisation (ou l’acquérir par d’autres moyens).</span><span class="sxs-lookup"><span data-stu-id="95c42-166">Instead of acquiring a refresh token in the portal, use the script from the previous step to acquire a refresh token (or acquire it by other means).</span></span>

## <a name="fetch-alerts-from-mssp-customers-tenant-using-apis"></a><span data-ttu-id="95c42-167">Récupérer des alertes à partir du client MSSP client à l’aide des API</span><span class="sxs-lookup"><span data-stu-id="95c42-167">Fetch alerts from MSSP customer's tenant using APIs</span></span>
 
<span data-ttu-id="95c42-168">Pour plus d’informations sur la récupération des alertes à l’aide de l’API REST, voir [Extraire des alertes à l’aide de l’API REST.](pull-alerts-using-rest-api.md)</span><span class="sxs-lookup"><span data-stu-id="95c42-168">For information on how to fetch alerts using REST API, see [Pull alerts using REST API](pull-alerts-using-rest-api.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="95c42-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95c42-169">See also</span></span>
- [<span data-ttu-id="95c42-170">Accorder l’accès MSSP au portail</span><span class="sxs-lookup"><span data-stu-id="95c42-170">Grant MSSP access to the portal</span></span>](grant-mssp-access.md)
- [<span data-ttu-id="95c42-171">Accéder au portail client MSSP</span><span class="sxs-lookup"><span data-stu-id="95c42-171">Access the MSSP customer portal</span></span>](access-mssp-portal.md)
- [<span data-ttu-id="95c42-172">Configurer des notifications d’alerte</span><span class="sxs-lookup"><span data-stu-id="95c42-172">Configure alert notifications</span></span>](configure-mssp-notifications.md)
