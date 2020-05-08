---
title: Activation de l'analyse de l'utilisation de Microsoft 365
f1.keywords:
- CSH
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9db96e9f-a622-4d5d-b134-09dcace55b6a
description: Découvrez comment commencer à collecter des données pour votre client à l’aide de l’application de modèle d’analyse de l’utilisation 365 de Microsoft dans Power BI.
ms.openlocfilehash: 386b64b1db15ba9f00450ac037a74bfc702e95ea
ms.sourcegitcommit: 7ff75a0f45371b247d975fc61cfa286f5b6f42f6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "44140682"
---
# <a name="enable-microsoft-365-usage-analytics"></a><span data-ttu-id="dc62d-103">Activation de l'analyse de l'utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="dc62d-103">Enable Microsoft 365 usage analytics</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="dc62d-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="dc62d-104">The admin center is changing.</span></span> <span data-ttu-id="dc62d-105">Si votre expérience ne correspond pas aux détails présentés ici, reportez-vous [à la rubrique à propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="dc62d-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="dc62d-106">Microsoft 365 l’analyse de l’utilisation est également disponible pour la communauté du gouvernement américain Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dc62d-106">Microsoft 365 usage analytics is also available for Microsoft 365 US Government Community.</span></span>
  
## <a name="steps-to-enable-microsoft-365-usage-analytics"></a><span data-ttu-id="dc62d-107">Étapes d’activation de l’analyse de l’utilisation 365 Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc62d-107">Steps to enable Microsoft 365 usage analytics</span></span>

<span data-ttu-id="dc62d-108">Pour commencer à utiliser l’analyse de l’utilisation de Microsoft 365, vous devez d’abord mettre les données à disposition dans le centre d’administration 365 Microsoft, puis lancer l’application de modèle dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="dc62d-108">To get started with Microsoft 365 usage analytics you must first make the data available in the Microsoft 365 admin center, then initiate the template app in Power BI.</span></span>
  
### <a name="get-power-bi"></a><span data-ttu-id="dc62d-109">Obtenir Power BI</span><span class="sxs-lookup"><span data-stu-id="dc62d-109">Get Power BI</span></span>

<span data-ttu-id="dc62d-110">Si vous ne disposez pas encore de Power BI, vous pouvez vous [inscrire à Power bi Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span><span class="sxs-lookup"><span data-stu-id="dc62d-110">If you don't already have Power BI, you can [sign up for Power BI Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span></span> <span data-ttu-id="dc62d-111">Sélectionnez **essayer gratuitement** pour vous inscrire pour une version d’évaluation ou **acheter maintenant** pour obtenir Power bi Pro.</span><span class="sxs-lookup"><span data-stu-id="dc62d-111">Select **Try free** to sign up for a trial, or **Buy now** to get Power BI Pro.</span></span>
  
  
<span data-ttu-id="dc62d-112">Vous pouvez également développer **Produits** pour acheter une version de Power BI.</span><span class="sxs-lookup"><span data-stu-id="dc62d-112">You can also expand **Products** to buy a version of Power BI.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc62d-113">Vous avez besoin d’une licence Power BI Pro pour installer, personnaliser et distribuer une application de modèle.</span><span class="sxs-lookup"><span data-stu-id="dc62d-113">You need a Power BI Pro license to install, customize, and distribute a template app.</span></span> <span data-ttu-id="dc62d-114">Pour plus d’informations, reportez-vous à la rubrique [conditions préalables](https://docs.microsoft.com/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="dc62d-114">For more information, please see [Prerequisites](https://docs.microsoft.com/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span></span>

<span data-ttu-id="dc62d-115">Vous avez besoin d’une licence Power BI Pro pour partager votre contenu, et les personnes avec lesquelles vous le partagez également, ou le contenu doit se trouver dans un espace de travail d’une [capacité étendue](https://docs.microsoft.com/power-bi/service-premium-what-is).</span><span class="sxs-lookup"><span data-stu-id="dc62d-115">You need a Power BI Pro license to share your content, and the people you share it with do too, or the content needs to be in a workspace in a [Premium capacity](https://docs.microsoft.com/power-bi/service-premium-what-is).</span></span> 
  
### <a name="enable-the-template-app"></a><span data-ttu-id="dc62d-116">Activer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="dc62d-116">Enable the template app</span></span>

<span data-ttu-id="dc62d-117">Pour activer l’application de modèle, vous devez être un **administrateur général**, un **lecteur de rapport**, un **administrateur Exchange**, un **administrateur Skype entreprise**ou un **administrateur SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-117">To enable the template app, you have to be either a **global administrator**, **report reader**, **Exchange administrator**, **Skype for Business administrator**, or **SharePoint administrator**.</span></span> 
  
<span data-ttu-id="dc62d-118">Pour plus d’informations, consultez la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="dc62d-118">See [About admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
1. <span data-ttu-id="dc62d-119">Dans le centre d’administration, accédez à la page **Rapports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Utilisation</a>.</span><span class="sxs-lookup"><span data-stu-id="dc62d-119">In the admin center, go to the **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> page.</span></span> 
    
2. <span data-ttu-id="dc62d-120">Sur la page **utilisation** , recherchez la carte d' **analyse d’utilisation Microsoft 365** , puis sélectionnez **prise en main**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-120">On the **Usage** page, locate the **Microsoft 365 usage analytics** card, and select **Get started**.</span></span>
    
3. <span data-ttu-id="dc62d-121">Dans le panneau rapports qui s’ouvre, définissez **mettre les données à la disposition de l’analyse de l’utilisation de Microsoft 365 pour Power bi** **à** \> l' **enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-121">On the Reports panel that opens, set **Make data available to Microsoft 365 usage analytics for Power BI** to **On** \> **Save**.</span></span> 
  
<span data-ttu-id="dc62d-122">Cette opération lance le processus de collecte de données et se termine dans les 2 à 48 heures suivant la taille de votre client.</span><span class="sxs-lookup"><span data-stu-id="dc62d-122">This initiates the data collection process and will complete in 2 to 48 hours depending on the size of your tenant.</span></span> <span data-ttu-id="dc62d-123">Le bouton **go to Power bi** est activé (il n’est plus grisé) une fois la collecte de données terminée.</span><span class="sxs-lookup"><span data-stu-id="dc62d-123">The **Go to Power BI** button will be enabled (no longer gray) when data collection is complete.</span></span> 
    
### <a name="initiate-the-template-app"></a><span data-ttu-id="dc62d-124">Lancer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="dc62d-124">Initiate the template app</span></span>

<span data-ttu-id="dc62d-125">Pour lancer l’application de modèle, vous devez être un **administrateur général**, un **lecteur de rapports**, un **administrateur Exchange**, un **administrateur Skype entreprise**ou un **administrateur SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-125">To initiate the template app, you have to be either a **global administrator**, **report reader**, **Exchange administrator**, **Skype for Business administrator**, or **SharePoint administrator**.</span></span> 
  
1. <span data-ttu-id="dc62d-126">Copiez l’ID de client et sélectionnez **accéder à Power bi**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-126">Copy the tenant Id and select **Go to Power BI**.</span></span>
    
2.  <span data-ttu-id="dc62d-127">Lorsque vous accédez à Power BI, connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="dc62d-127">When you get to Power BI, sign in.</span></span> <span data-ttu-id="dc62d-128">Sélectionnez applications->obtenir des applications à partir du menu de navigation.</span><span class="sxs-lookup"><span data-stu-id="dc62d-128">Select Apps->Get apps from the navigation menu.</span></span>    
  
3. <span data-ttu-id="dc62d-129">Dans l’onglet **apps** , tapez Microsoft 365 dans la zone de recherche, puis sélectionnez analyse \> **Get it now**de **l’utilisation de Microsoft 365** .</span><span class="sxs-lookup"><span data-stu-id="dc62d-129">In the **Apps** tab, type Microsoft 365 in the search box and then select **Microsoft 365 usage analytics** \> **Get it now**.</span></span>

    <span data-ttu-id="dc62d-130">[![Sélectionnez obtenir maintenant](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span><span class="sxs-lookup"><span data-stu-id="dc62d-130">[![Select Get it now](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span></span>
    
4.  <span data-ttu-id="dc62d-131">Une fois que l’application est installée.</span><span class="sxs-lookup"><span data-stu-id="dc62d-131">Once the app is installed.</span></span> <span data-ttu-id="dc62d-132">Cliquez sur la mosaïque pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="dc62d-132">Click on the tile to open it.</span></span>

5.  <span data-ttu-id="dc62d-133">Cliquez sur **Explorer l’application** pour afficher l’application avec des exemples de données.</span><span class="sxs-lookup"><span data-stu-id="dc62d-133">Click **Explore app** to view the app with sample data.</span></span> <span data-ttu-id="dc62d-134">Cliquez sur **se connecter** pour connecter l’application aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="dc62d-134">Click **Connect** to connect the app to your organization’s data.</span></span>

6.  <span data-ttu-id="dc62d-135">Une fois que vous avez cliqué sur **connexion**, dans l’écran **se connecter à l’utilisation de Microsoft 365** , tapez l’ID client que \> vous avez copié à l’étape (1) **suivant**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-135">After clicking **Connect**, on the **Connect to Microsoft 365 usage analytics** screen, type in the tenant Id you copied in step (1) \> **Next**.</span></span>
    
7. <span data-ttu-id="dc62d-136">Dans l’écran suivant, sélectionnez **oAuth2** comme \> **Sign in** **méthode d’authentification** .</span><span class="sxs-lookup"><span data-stu-id="dc62d-136">On the next screen, select **oAuth2** as the **Authentication method** \> **Sign in**.</span></span> <span data-ttu-id="dc62d-137">Si vous choisissez une autre méthode d’authentification, la connexion à l’application de modèle échouera.</span><span class="sxs-lookup"><span data-stu-id="dc62d-137">If you choose any other authentication method, the connection to the template app will fail.</span></span>
    
    ![Choose oAuth2 as authentication method](../../media/ac85a360-c278-4c60-8aa3-68f4828f1d96.png)
  
8. <span data-ttu-id="dc62d-139">Une fois l’application de modèle instanciée, le tableau de bord d’analyse de l’utilisation de Microsoft 365 sera disponible dans Power BI sur le Web.</span><span class="sxs-lookup"><span data-stu-id="dc62d-139">Once the template app is instantiated the Microsoft 365 usage analytics dashboard will be available in Power BI on the web.</span></span> <span data-ttu-id="dc62d-140">Le chargement initial du tableau de bord prend entre 2 et 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="dc62d-140">The initial loading of the dashboard will take between 2 to 30 minutes.</span></span>
  
<span data-ttu-id="dc62d-141">Les agrégats de niveau client seront disponibles dans tous les rapports.</span><span class="sxs-lookup"><span data-stu-id="dc62d-141">Tenant level aggregates will be available in all reports.</span></span> <span data-ttu-id="dc62d-142">**Les détails au niveau de l’utilisateur ne seront disponibles qu’après le 1er ou le 15 jour du mois civil après avoir**pris l’opt.</span><span class="sxs-lookup"><span data-stu-id="dc62d-142">**User-level details will only become available after the 1st or 15th day of the calendar month after opting in**.</span></span> <span data-ttu-id="dc62d-143">Cela aura un impact sur tous les rapports sous activité de l’utilisateur (voir [naviguer et utiliser les rapports de l’analyse de l’utilisation de Microsoft 365](navigate-and-utilize-reports.md) pour obtenir des conseils sur l’affichage et l’utilisation de ces rapports).</span><span class="sxs-lookup"><span data-stu-id="dc62d-143">This will impact all reports under User Activity (See [Navigate and utilize the reports in Microsoft 365 usage analytics](navigate-and-utilize-reports.md) for tips on how to view and use these reports).</span></span>
    
## <a name="make-the-collected-data-anonymous"></a><span data-ttu-id="dc62d-144">Anonymiser les données collectées</span><span class="sxs-lookup"><span data-stu-id="dc62d-144">Make the collected data anonymous</span></span>

<span data-ttu-id="dc62d-145">Pour anonymiser les données collectées pour tous les rapports, vous devez être administrateur général.</span><span class="sxs-lookup"><span data-stu-id="dc62d-145">To make the data that is collected for all reports anonymous, you have to be a global administrator.</span></span> <span data-ttu-id="dc62d-146">Cette opération masque les informations identifiables telles que les noms d’utilisateur, de groupe et de site dans les rapports et l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="dc62d-146">This will hide identifiable information such as user, group and site names in reports and in the template app .</span></span>
  
1. <span data-ttu-id="dc62d-147">Dans le centre d’administration, accédez aux **Settings** \> **paramètres**paramètres, puis sous l’onglet **services** , choisissez **rapports**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-147">In the admin center, go to the **Settings** \> **Settings**, and under **Services** tab, choose **Reports**.</span></span>
    
2. <span data-ttu-id="dc62d-148">Sélectionnez **rapports**, puis choisissez d' **afficher les identificateurs anonymes**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-148">Select **Reports**, and then choose to **Display anonymous identifiers**.</span></span> <span data-ttu-id="dc62d-149">Ce paramètre est appliqué à la fois aux rapports d’utilisation ainsi qu’à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="dc62d-149">This setting gets applied both to the usage reports as well as to the template app.</span></span>
  
3. <span data-ttu-id="dc62d-150">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="dc62d-150">Select **Save changes**.</span></span>
