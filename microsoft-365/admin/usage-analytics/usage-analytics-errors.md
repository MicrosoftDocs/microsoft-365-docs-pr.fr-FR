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
description: Découvrez comment résoudre les problèmes liés à l’application de modèle d’analyse de l’utilisation de Microsoft 365.
ms.openlocfilehash: 4696dd0c5140cdc110781c226819fc64a90fae1b
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44402033"
---
# <a name="troubleshooting-microsoft-365-usage-analytics"></a><span data-ttu-id="70aca-103">Résolution des problèmes d’analyse de l’utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="70aca-103">Troubleshooting Microsoft 365 usage analytics</span></span>

<span data-ttu-id="70aca-104">Explorez la liste de messages d’erreur suivante pour obtenir de l’aide sur les problèmes les plus courants liés à l’analyse de l’utilisation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-104">Explore the following list of error messages to get help with the most common issues with Microsoft 365 usage analytics.</span></span>
  
    
## <a name="we-are-unable-to-process-your-request-you-have-to-first-subscribe-to-this-data-from-the-microsoft-365-admin-center"></a><span data-ttu-id="70aca-105">Nous ne sommes pas en mesure de traiter votre demande.</span><span class="sxs-lookup"><span data-stu-id="70aca-105">We are unable to process your request.</span></span> <span data-ttu-id="70aca-106">Vous devez d’abord vous abonner à ces données à partir du centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="70aca-106">You have to first subscribe to this data from the Microsoft 365 admin center</span></span>

 <span data-ttu-id="70aca-107">**Code d'erreur :** 422</span><span class="sxs-lookup"><span data-stu-id="70aca-107">**Error Code :** 422</span></span> 
  
 <span data-ttu-id="70aca-108">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-108">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-109">**Cause :** Avant de vous connecter à l’application, vous devez vous abonner aux données à partir du centre d’administration 365 de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70aca-109">**Cause:** Before you can connect to the app you have to subscribe to the data from the Microsoft 365 admin center.</span></span> <span data-ttu-id="70aca-110">Si cette étape n’est pas réalisée en premier, vous ne pourrez pas vous connecter à l’application de modèle, même si vous fournissez votre ID de client Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-110">If this step isn't done first, you won't be able to connect to the template app, even if you provide your Microsoft 365 tenant id.</span></span> 
  
 <span data-ttu-id="70aca-111">**Pour corriger cette erreur :** Pour vous abonner aux données, accédez à l’utilisation des rapports du centre d’administration \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> et recherchez la vignette Microsoft 365 utilisation analytique sur la page principale du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="70aca-111">**To fix this error:** To subscribe to the data, go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="70aca-112">Sélectionnez le bouton **prise en main** , puis, dans le volet **rapports** qui s’ouvre, activez la case à cocher créer des **données disponibles pour l’analyse de l’utilisation de Microsoft 365 pour Power bi** sur et **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="70aca-112">Select the **Get started** button and then in the **Reports** pane that opens, turn the **Make data available to Microsoft 365 usage analytics for Power BI** setting on and **Save**.</span></span>
  
## <a name="we-are-processing-your-data"></a><span data-ttu-id="70aca-113">Vos données sont en cours de traitement</span><span class="sxs-lookup"><span data-stu-id="70aca-113">We are processing your data</span></span>

 <span data-ttu-id="70aca-114">**Où le message suivant s’affiche :** Dans la vignette de l’analyse de l' **utilisation 365 de Microsoft** sur le tableau de bord d' **utilisation** dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-114">**Where you will see this message:** In the **Microsoft 365 usage analytics** tile on the **Usage** dashboard in the Microsoft 365 admin center.</span></span> 
  
 <span data-ttu-id="70aca-115">**Cause :** Lorsque vous [Choisissez d’afficher les données dans l’application de modèle](enable-usage-analytics.md) à partir du centre d’administration Microsoft 365, le système Microsoft 365 commence à générer des données d’utilisation historiques pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="70aca-115">**Cause:** When you [opt in to seeing data in the template app](enable-usage-analytics.md) from the Microsoft 365 admin center, the Microsoft 365 system starts generating historical usage data for your organization.</span></span> <span data-ttu-id="70aca-116">En fonction de la taille de votre locataire, cette étape peut prendre 2 à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="70aca-116">Depending on the size of your tenant, this step could take anywhere between 2 hours to 48 hours.</span></span> 
  
 <span data-ttu-id="70aca-117">**Pour résoudre ce problème :** Il s’agit d’un patient, mais si le message ne change pas pour que **vos données soient prêtes** après 3 jours, [contactez Microsoft 365 pour obtenir de l’aide à](../contact-support-for-business-products.md)la décision.</span><span class="sxs-lookup"><span data-stu-id="70aca-117">**To fix this:** Just be patient, but if the message does not change to **Your data is ready** after 3 days, [contact Microsoft 365 for business support](../contact-support-for-business-products.md).</span></span>
  
## <a name="we-are-unable-to-process-your-request-at-this-time-we-are-still-preparing-the-data-for-your-organization"></a><span data-ttu-id="70aca-118">Nous ne sommes pas en mesure de traiter votre demande pour le moment.</span><span class="sxs-lookup"><span data-stu-id="70aca-118">We are unable to process your request at this time.</span></span> <span data-ttu-id="70aca-119">Les données relatives à votre organisation sont en cours de préparation</span><span class="sxs-lookup"><span data-stu-id="70aca-119">We are still preparing the data for your organization</span></span>

 <span data-ttu-id="70aca-120">**Code d'erreur :** 423</span><span class="sxs-lookup"><span data-stu-id="70aca-120">**Error Code:** 423</span></span> 
  
 <span data-ttu-id="70aca-121">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-121">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-122">**Cause :** Lorsque vous [Choisissez d’afficher les données dans l’application de modèle](enable-usage-analytics.md) à partir du centre d’administration, le système Microsoft 365 commence à générer des données d’utilisation historiques pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="70aca-122">**Cause:** When you [opt in to seeing data in the template app](enable-usage-analytics.md) from the admin center, the Microsoft 365 system starts generating historical usage data for your organization.</span></span> <span data-ttu-id="70aca-123">En fonction de la taille de votre locataire, cette étape peut prendre 2 à 48 heures.</span><span class="sxs-lookup"><span data-stu-id="70aca-123">Depending on the size of your tenant, this step could take anywhere between 2 hours to 48 hours.</span></span> 
  
 <span data-ttu-id="70aca-124">**Pour résoudre ce problème :** Il s’agit d’un patient, mais si le message ne change pas en fonction de **vos données, il est prêt** de 3 jours après l’initiation, [Contactez le support technique de Microsoft 365](../contact-support-for-business-products.md).</span><span class="sxs-lookup"><span data-stu-id="70aca-124">**To fix this:** Just be patient, but if the message does not change to **Your data is ready** even 3 days since initiation, [contact Microsoft 365 for business support](../contact-support-for-business-products.md).</span></span>
  
## <a name="the-tenant-id-you-provided-is-not-in-the-correct-format"></a><span data-ttu-id="70aca-125">Le format de l'ID de locataire que vous avez fourni est incorrect</span><span class="sxs-lookup"><span data-stu-id="70aca-125">The tenant ID you provided is not in the correct format</span></span>

 <span data-ttu-id="70aca-126">**Code d'erreur :** 400</span><span class="sxs-lookup"><span data-stu-id="70aca-126">**Error Code:** 400</span></span> 
  
 <span data-ttu-id="70aca-127">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-127">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-p107">**Cause :** L'ID de locataire est un identificateur global unique (GUID) qui doit être au format xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. Toute autre chaîne saisie dans la zone d'entrée du locataire générera cette erreur.</span><span class="sxs-lookup"><span data-stu-id="70aca-p107">**Cause:** The tenant id is a guid and has to be in the format of xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. If you enter any other string in the tenant input box you will get this error.</span></span> 
  
 <span data-ttu-id="70aca-130">**Pour corriger cette erreur :** Accédez à l’utilisation des rapports du centre d’administration \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> et localisez la vignette de l’utilisation de Microsoft 365 sur la page principale du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="70aca-130">**To fix this error:** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="70aca-131">L'ID de locataire est répertorié sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="70aca-131">The tenant id is listed on the tile.</span></span> <span data-ttu-id="70aca-132">Vous pouvez le copier à partir de cet emplacement et le coller dans la boîte de dialogue pour vous connecter à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="70aca-132">You can copy it from here and paste it in the dialog box for connecting to the template app.</span></span> 
  
## <a name="the-tenant-id-you-provided-is-not-recognized-by-our-system"></a><span data-ttu-id="70aca-133">Notre système ne reconnaît pas l'ID de locataire que vous avez fourni</span><span class="sxs-lookup"><span data-stu-id="70aca-133">The tenant ID you provided is not recognized by our system</span></span>

 <span data-ttu-id="70aca-134">**Code d'erreur :** 404</span><span class="sxs-lookup"><span data-stu-id="70aca-134">**Error Code:** 404</span></span> 
  
 <span data-ttu-id="70aca-135">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-135">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-136">**Cause :** L'ID de locataire que vous avez fourni n'est pas valide ou n'existe pas.</span><span class="sxs-lookup"><span data-stu-id="70aca-136">**Cause:** The tenant id you provided is not valid or does not exist.</span></span> 
  
 <span data-ttu-id="70aca-137">**Pour corriger cette erreur :** Accédez à l’utilisation des rapports du centre d’administration \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> et localisez la vignette de l’utilisation de Microsoft 365 sur la page principale du tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="70aca-137">**To fix this error:** Go to the admin center \> **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> and locate the Microsoft 365 usage analytics tile on the main dashboard page.</span></span> <span data-ttu-id="70aca-138">L'ID de locataire est répertorié sur la vignette.</span><span class="sxs-lookup"><span data-stu-id="70aca-138">The tenant id is listed on the tile.</span></span> <span data-ttu-id="70aca-139">Vous pouvez le copier à partir de cet emplacement et le coller dans la boîte de dialogue pour vous connecter à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="70aca-139">You can copy it from here and paste it in the dialog box for connecting to the template app.</span></span> 
  
## <a name="please-re-enter-your-credentials-to-sign-in-to-power-bi-again"></a><span data-ttu-id="70aca-140">Entrez à nouveau vos informations d'identification pour vous connecter à Power BI</span><span class="sxs-lookup"><span data-stu-id="70aca-140">Please re-enter your credentials to sign in to Power BI again</span></span>

<span data-ttu-id="70aca-141">Code d'erreur : 302</span><span class="sxs-lookup"><span data-stu-id="70aca-141">Error Code: 302</span></span>
  
 <span data-ttu-id="70aca-142">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-142">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-143">**Cause :** Le code d'autorisation a échoué. Vous risquez d'être invité à entrer à nouveau vos informations d'identification.</span><span class="sxs-lookup"><span data-stu-id="70aca-143">**Cause:** The authorization code failed and may require you to enter your credentials again.</span></span> 
  
 <span data-ttu-id="70aca-144">**Pour résoudre ce problème :** Déconnectez-vous de Power BI, puis reconnectez-vous.</span><span class="sxs-lookup"><span data-stu-id="70aca-144">**To fix this error:** Sign out of Power BI, and then sign in again.</span></span> 
  
## <a name="you-do-not-have-the-right-authorization-to-access-to-this-data-to-be-able-to-gain-access-to-the-data-from-this-service-you-need-to-be-either-a-global-admin-or-any-one-of-the-product-admins"></a><span data-ttu-id="70aca-145">Vous ne disposez pas de l'autorisation adéquate pour accéder à ces données.</span><span class="sxs-lookup"><span data-stu-id="70aca-145">You do not have the right authorization to access to this data.</span></span> <span data-ttu-id="70aca-146">Pour accéder aux données à partir de ce service, vous devez être administrateur général ou administrateur de produit</span><span class="sxs-lookup"><span data-stu-id="70aca-146">To be able to gain access to the data from this service you need to be either a global admin or any one of the product admins</span></span>

 <span data-ttu-id="70aca-147">**Code d'erreur :** 403</span><span class="sxs-lookup"><span data-stu-id="70aca-147">**Error Code:** 403</span></span> 
  
 <span data-ttu-id="70aca-148">**Où le message suivant s’affiche :** Dans Power BI lorsque vous vous connectez à l’application de modèle d’analyse de l’utilisation de Microsoft 365 ou lorsque vous appelez directement les API de création de rapports Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="70aca-148">**Where you will see this message:** In Power BI when you are connecting to the Microsoft 365 Usage Analytics template app or when directly calling the Microsoft 365 Reporting APIs.</span></span> 
  
 <span data-ttu-id="70aca-149">**Cause :** Le code d’autorisation a échoué, car l’utilisateur qui a tenté de se connecter à l’application de modèle ne dispose pas du niveau d’autorisation approprié pour accéder à ces données.</span><span class="sxs-lookup"><span data-stu-id="70aca-149">**Cause:** The authorization code failed because the user who tried connecting to the template app does not have the right level of authorization to access this data.</span></span> 
  
 <span data-ttu-id="70aca-150">**Pour corriger cette erreur :** Fournissez les informations d’identification d’un utilisateur qui est soit un administrateur **général**, un administrateur **Exchange**, un **administrateur Skype entreprise**, un **administrateur SharePoint**, un **lecteur global** ou un **lecteur de rapports** pour se connecter à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="70aca-150">**To fix this error:** Provide the credentials of a user who is either a **Global admin**, **Exchange admin**, **Skype for Business admin**, **SharePoint admin**, **Global reader** or **Report reader** to connect to the template app.</span></span> <span data-ttu-id="70aca-151">Pour plus d’informations, consultez la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="70aca-151">See [About admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
## <a name="refresh-failed"></a><span data-ttu-id="70aca-152">L'actualisation a échoué</span><span class="sxs-lookup"><span data-stu-id="70aca-152">Refresh failed</span></span>

 <span data-ttu-id="70aca-153">**Où ce message s'affichera-t-il ?** E-mail de Power BI ou état d'échec dans l'historique d'actualisation.</span><span class="sxs-lookup"><span data-stu-id="70aca-153">**Where you will see this message:** Email from Power BI or failed status in the refresh history.</span></span> 
  
 <span data-ttu-id="70aca-154">**Cause :** Parfois, les informations d’identification de l’utilisateur qui s’est connecté à l’application de modèle sont réinitialisées, et elles ne sont pas mises à jour dans les paramètres de connexion de l’application de modèle, ce qui entraîne l’affichage des erreurs d’échec d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="70aca-154">**Cause:** Sometimes the credentials of the user who connected to the template app are reset, and not updated in the connection settings of the template app causing the user to see refresh failure errors.</span></span> 
  
 <span data-ttu-id="70aca-155">**Pour corriger cette erreur :** Dans Power BI, recherchez le jeu de données correspondant à l’application de modèle d’analyse de l’utilisation de Microsoft 365, sélectionnez **Schedule Refresh** et fournissez vos informations d’identification d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="70aca-155">**To fix this error:** In Power BI, find the dataset corresponding to the Microsoft 365 Usage Analytics template app, select **schedule refresh** and provide your admin credentials.</span></span> 
  
<span data-ttu-id="70aca-156">Si cela ne fonctionne pas, effacez le cache et recréez l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="70aca-156">If that doesn't work, clear the cache, and re-create the template app.</span></span>
  
  
