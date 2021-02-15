---
title: Résolution des problèmes d’analyse de l’utilisation de Microsoft 365
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: a73632a1-62c8-4a13-8115-913773b30f93
description: Découvrez comment résoudre les problèmes avec l’application modèle Analyse de l’utilisation de Microsoft 365.
ms.openlocfilehash: bf8e4ece7b1e310d91f418f5388cae9aa27f2aa7
ms.sourcegitcommit: e56894917d2aae05705c3b9447388d10e2156183
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48841434"
---
# <a name="troubleshooting-microsoft-365-usage-analytics"></a><span data-ttu-id="919ef-103">Résolution des problèmes d’analyse de l’utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="919ef-103">Troubleshooting Microsoft 365 usage analytics</span></span>

<span data-ttu-id="919ef-104">Explorez la liste suivante des messages d’erreur pour obtenir de l’aide sur les problèmes les plus courants avec l’analyse de l’utilisation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-104">Explore the following list of error messages to get help with the most common issues with Microsoft 365 usage analytics.</span></span>
  
    
## <a name="we-are-unable-to-process-your-request-you-have-to-first-subscribe-to-this-data-from-the-microsoft-365-admin-center"></a><span data-ttu-id="919ef-105">Nous ne sommes pas en mesure de traiter votre demande.</span><span class="sxs-lookup"><span data-stu-id="919ef-105">We are unable to process your request.</span></span> <span data-ttu-id="919ef-106">Vous devez d’abord vous abonner à ces données à partir du Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="919ef-106">You have to first subscribe to this data from the Microsoft 365 admin center</span></span>

 <span data-ttu-id="919ef-107">**Code d’erreur :** 422</span><span class="sxs-lookup"><span data-stu-id="919ef-107">**Error Code:** 422</span></span> 
  
 <span data-ttu-id="919ef-108">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-108">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-109">**Cause :** Avant de vous connecter à l’application, vous devez vous abonner aux données du Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-109">**Cause:** Before you can connect to the app, you have to subscribe to the data from the Microsoft 365 admin center.</span></span> <span data-ttu-id="919ef-110">Si cette étape n’est pas effectuée en premier, vous ne pourrez pas vous connecter à l’application de modèle, même si vous fournissez votre ID de client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-110">If this step isn't done first, you won't be able to connect to the template app, even if you provide your Microsoft 365 tenant ID.</span></span> 
  
 <span data-ttu-id="919ef-111">**Pour corriger cette erreur :** Pour vous abonner aux données, go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span><span class="sxs-lookup"><span data-stu-id="919ef-111">**To fix this error:** To subscribe to the data, go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="919ef-112">Sélectionnez **le** bouton Démarrer,  puis dans le volet Rapports qui s’ouvre, ouvrez le paramètre Rendre les données disponibles pour l’analyse de l’utilisation de **Microsoft 365** pour power BI et **enregistrez.**</span><span class="sxs-lookup"><span data-stu-id="919ef-112">Select the **Get started** button and then in the **Reports** pane that opens, turn the **Make data available to Microsoft 365 usage analytics for Power BI** setting on and **Save**.</span></span>
  
## <a name="we-are-processing-your-data"></a><span data-ttu-id="919ef-113">Vos données sont en cours de traitement</span><span class="sxs-lookup"><span data-stu-id="919ef-113">We are processing your data</span></span>

 <span data-ttu-id="919ef-114">**Où vous verrez ce message :** Dans la vignette Analyse de l’utilisation **de Microsoft 365** dans le tableau de bord Utilisation du Centre d’administration Microsoft 365. </span><span class="sxs-lookup"><span data-stu-id="919ef-114">**Where you will see this message:** In the **Microsoft 365 usage analytics** tile on the **Usage** dashboard in the Microsoft 365 admin center.</span></span> 
  
 <span data-ttu-id="919ef-115">**Cause :** Lorsque [vous](enable-usage-analytics.md) choisissez de voir les données dans l’application modèle à partir du Centre d’administration Microsoft 365, le système Microsoft 365 commence à générer des données d’utilisation historiques pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="919ef-115">**Cause:** When you [opt in to seeing data in the template app](enable-usage-analytics.md) from the Microsoft 365 admin center, the Microsoft 365 system starts generating historical usage data for your organization.</span></span> <span data-ttu-id="919ef-116">En fonction de la taille de votre locataire, cette étape peut prendre 2 à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="919ef-116">Depending on the size of your tenant, this step could take anywhere between 2 hours to 48 hours.</span></span> 
  
 <span data-ttu-id="919ef-117">**Pour résoudre ce problème :** Soyez patient, mais si le message  ne change pas à Vos données, vous êtes prêt après 3 jours, contactez le support [Microsoft 365 pour les entreprises.](../contact-support-for-business-products.md)</span><span class="sxs-lookup"><span data-stu-id="919ef-117">**To fix this:** Just be patient, but if the message does not change to **Your data is ready** after 3 days, [contact Microsoft 365 for business support](../contact-support-for-business-products.md).</span></span>
  
## <a name="we-are-unable-to-process-your-request-at-this-time-we-are-still-preparing-the-data-for-your-organization"></a><span data-ttu-id="919ef-118">Nous ne sommes pas en mesure de traiter votre demande pour le moment.</span><span class="sxs-lookup"><span data-stu-id="919ef-118">We are unable to process your request at this time.</span></span> <span data-ttu-id="919ef-119">Les données relatives à votre organisation sont en cours de préparation</span><span class="sxs-lookup"><span data-stu-id="919ef-119">We are still preparing the data for your organization</span></span>

 <span data-ttu-id="919ef-120">**Code d'erreur :** 423</span><span class="sxs-lookup"><span data-stu-id="919ef-120">**Error Code:** 423</span></span> 
  
 <span data-ttu-id="919ef-121">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-121">**Where you will see this message:** In Power BI, when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-122">**Cause :** Lorsque vous [choisissez de](enable-usage-analytics.md) voir les données dans le modèle d’application à partir du Centre d’administration, le système Microsoft 365 commence à générer des données d’utilisation historiques pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="919ef-122">**Cause:** When you [opt in to seeing data in the template app](enable-usage-analytics.md) from the admin center, the Microsoft 365 system starts generating historical usage data for your organization.</span></span> <span data-ttu-id="919ef-123">Selon la taille de votre client, cette étape peut prendre entre deux et 48 heures.</span><span class="sxs-lookup"><span data-stu-id="919ef-123">Depending on the size of your tenant, this step could take anywhere between two hours to 48 hours.</span></span> 
  
 <span data-ttu-id="919ef-124">**Pour résoudre ce problème :** Soyez patient, mais si le message  n’est pas ajouté à Vos données, même 3 jours après l’initiation, contactez le support [Microsoft 365 pour les entreprises.](../contact-support-for-business-products.md)</span><span class="sxs-lookup"><span data-stu-id="919ef-124">**To fix this:** Just be patient, but if the message does not change to **Your data is ready** even 3 days since initiation, [contact Microsoft 365 for business support](../contact-support-for-business-products.md).</span></span>
  
## <a name="the-tenant-id-you-provided-is-not-in-the-correct-format"></a><span data-ttu-id="919ef-125">Le format de l'ID de locataire que vous avez fourni est incorrect</span><span class="sxs-lookup"><span data-stu-id="919ef-125">The tenant ID you provided is not in the correct format</span></span>

 <span data-ttu-id="919ef-126">**Code d'erreur :** 400</span><span class="sxs-lookup"><span data-stu-id="919ef-126">**Error Code:** 400</span></span> 
  
 <span data-ttu-id="919ef-127">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-127">**Where you will see this message:** In Power BI, when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-128">**Cause :** L’ID de client est un GUID qui doit être au format xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.</span><span class="sxs-lookup"><span data-stu-id="919ef-128">**Cause:** The tenant ID is a guid and has to be in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx.</span></span> <span data-ttu-id="919ef-129">Si vous entrez une autre chaîne dans la zone d’entrée du client, vous obtenez cette erreur.</span><span class="sxs-lookup"><span data-stu-id="919ef-129">If you enter any other string in the tenant input box, you will get this error.</span></span> 
  
 <span data-ttu-id="919ef-130">**Pour corriger cette erreur :** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span><span class="sxs-lookup"><span data-stu-id="919ef-130">**To fix this error:** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="919ef-131">L’ID de client est répertorié sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="919ef-131">The tenant ID is listed on the tile.</span></span> <span data-ttu-id="919ef-132">Vous pouvez le copier à partir d’ici et le coller dans la boîte de dialogue pour vous connecter à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="919ef-132">You can copy it from here and paste it in the dialog box for connecting to the template app.</span></span> 
  
## <a name="the-tenant-id-you-provided-is-not-recognized-by-our-system"></a><span data-ttu-id="919ef-133">Notre système ne reconnaît pas l'ID de locataire que vous avez fourni</span><span class="sxs-lookup"><span data-stu-id="919ef-133">The tenant ID you provided is not recognized by our system</span></span>

 <span data-ttu-id="919ef-134">**Code d'erreur :** 404</span><span class="sxs-lookup"><span data-stu-id="919ef-134">**Error Code:** 404</span></span> 
  
 <span data-ttu-id="919ef-135">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-135">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-136">**Cause :** L’ID de locataire que vous avez fourni n’est pas valide ou n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="919ef-136">**Cause:** The tenant ID you provided is not valid or does not exist.</span></span> 
  
 <span data-ttu-id="919ef-137">**Pour corriger cette erreur :** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span><span class="sxs-lookup"><span data-stu-id="919ef-137">**To fix this error:** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="919ef-138">L’ID de client est répertorié sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="919ef-138">The tenant ID is listed on the tile.</span></span> <span data-ttu-id="919ef-139">Vous pouvez le copier à partir d’ici et le coller dans la boîte de dialogue pour vous connecter à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="919ef-139">You can copy it from here and paste it in the dialog box for connecting to the template app.</span></span> 
  
## <a name="please-re-enter-your-credentials-to-sign-in-to-power-bi-again"></a><span data-ttu-id="919ef-140">Entrez à nouveau vos informations d'identification pour vous connecter à Power BI</span><span class="sxs-lookup"><span data-stu-id="919ef-140">Please re-enter your credentials to sign in to Power BI again</span></span>

<span data-ttu-id="919ef-141">Code d'erreur : 302</span><span class="sxs-lookup"><span data-stu-id="919ef-141">Error Code: 302</span></span>
  
 <span data-ttu-id="919ef-142">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-142">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-143">**Cause :** Le code d'autorisation a échoué. Vous risquez d'être invité à entrer à nouveau vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="919ef-143">**Cause:** The authorization code failed and may require you to enter your credentials again.</span></span> 
  
 <span data-ttu-id="919ef-144">**Pour résoudre ce problème :** Déconnectez-vous de Power BI, puis reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="919ef-144">**To fix this error:** Sign out of Power BI, and then sign in again.</span></span> 
  
## <a name="you-do-not-have-the-right-authorization-to-access-to-this-data-to-be-able-to-gain-access-to-the-data-from-this-service-you-need-to-be-either-a-global-admin-or-any-one-of-the-product-admins"></a><span data-ttu-id="919ef-145">Vous ne disposez pas de l'autorisation adéquate pour accéder à ces données.</span><span class="sxs-lookup"><span data-stu-id="919ef-145">You do not have the right authorization to access to this data.</span></span> <span data-ttu-id="919ef-146">Pour accéder aux données à partir de ce service, vous devez être administrateur général ou administrateur de produit</span><span class="sxs-lookup"><span data-stu-id="919ef-146">To be able to gain access to the data from this service you need to be either a global admin or any one of the product admins</span></span>

 <span data-ttu-id="919ef-147">**Code d'erreur :** 403</span><span class="sxs-lookup"><span data-stu-id="919ef-147">**Error Code:** 403</span></span> 
  
 <span data-ttu-id="919ef-148">**Où vous verrez ce message :** Dans Power BI, lorsque vous vous connectez à l’application modèle Analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="919ef-148">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="919ef-149">**Cause :** Le code d’autorisation a échoué car l’utilisateur qui a tenté de se connecter à l’application modèle ne peut pas accéder à ces données avec le niveau d’autorisation le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="919ef-149">**Cause:** The authorization code failed because the user who tried connecting to the template app does not have the right level of authorization to access this data.</span></span> 
  
 <span data-ttu-id="919ef-150">**Pour corriger cette erreur :** Fournissez les informations d’identification d’un utilisateur qui est administrateur global,  **administrateur Exchange,** administrateur **Skype** Entreprise, administrateur **SharePoint,** lecteur global ou lecteur de rapports pour se connecter à l’application de modèle.  </span><span class="sxs-lookup"><span data-stu-id="919ef-150">**To fix this error:** Provide the credentials of a user who is either a **Global admin**, **Exchange admin**, **Skype for Business admin**, **SharePoint admin**, **Global reader** or **Report reader** to connect to the template app.</span></span> <span data-ttu-id="919ef-151">Pour plus [d’informations, voir](../add-users/about-admin-roles.md) à propos des rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="919ef-151">See [About admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
## <a name="refresh-failed"></a><span data-ttu-id="919ef-152">L'actualisation a échoué</span><span class="sxs-lookup"><span data-stu-id="919ef-152">Refresh failed</span></span>

 <span data-ttu-id="919ef-153">**Où ce message s'affichera-t-il ?** E-mail de Power BI ou état d'échec dans l'historique d'actualisation.</span><span class="sxs-lookup"><span data-stu-id="919ef-153">**Where you will see this message:** Email from Power BI or failed status in the refresh history.</span></span> 
  
 <span data-ttu-id="919ef-154">**Cause :** Parfois, les informations d’identification de l’utilisateur qui s’est connecté à l’application de modèle sont réinitialisées et ne sont pas mises à jour dans les paramètres de connexion de l’application de modèle, ce qui provoque des erreurs d’échec d’actualisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="919ef-154">**Cause:** Sometimes the credentials of the user who connected to the template app are reset, and not updated in the connection settings of the template app causing the user to see refresh failure errors.</span></span> 
  
 <span data-ttu-id="919ef-155">**Pour corriger cette erreur :** Dans Power BI, recherchez le jeu de données correspondant à  l’application modèle Analyse de l’utilisation de Microsoft 365, sélectionnez planifier l’actualisation et fournissez vos informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="919ef-155">**To fix this error:** In Power BI, find the dataset corresponding to the Microsoft 365 Usage Analytics template app, select **schedule refresh** and provide your admin credentials.</span></span> 
  
<span data-ttu-id="919ef-156">Si cela ne fonctionne pas, effacer le cache et re-créer l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="919ef-156">If that doesn't work, clear the cache, and re-create the template app.</span></span>
  
  
