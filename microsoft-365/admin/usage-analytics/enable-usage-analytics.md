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
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9db96e9f-a622-4d5d-b134-09dcace55b6a
description: Découvrez comment commencer à collecter des données pour votre client à l’aide de l’application modèle Analyse de l’utilisation de Microsoft 365 dans Power BI.
ms.openlocfilehash: 1ef50380041650763961ffbe6e01c63b26800ee3
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50913873"
---
# <a name="enable-microsoft-365-usage-analytics"></a><span data-ttu-id="2470b-103">Activation de l'analyse de l'utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2470b-103">Enable Microsoft 365 usage analytics</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="2470b-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="2470b-104">The admin center is changing.</span></span> <span data-ttu-id="2470b-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="2470b-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](../microsoft-365-admin-center-preview.md?preserve-view=true&view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="2470b-106">L’analyse de l’utilisation de Microsoft 365 n’est pas encore disponible pour la communauté Microsoft 365 pour le gouvernement américain.</span><span class="sxs-lookup"><span data-stu-id="2470b-106">Microsoft 365 usage analytics is not yet available for Microsoft 365 US Government Community.</span></span>
  
## <a name="steps-to-enable-microsoft-365-usage-analytics"></a><span data-ttu-id="2470b-107">Procédure d’analyse de l’utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2470b-107">Steps to enable Microsoft 365 usage analytics</span></span>

<span data-ttu-id="2470b-108">Pour commencer à utiliser l’analyse de l’utilisation de Microsoft 365, vous devez d’abord rendre les données disponibles dans le Centre d’administration Microsoft 365, puis lancer l’application modèle dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="2470b-108">To get started with Microsoft 365 usage analytics you must first make the data available in the Microsoft 365 admin center, then initiate the template app in Power BI.</span></span>
  
### <a name="get-power-bi"></a><span data-ttu-id="2470b-109">Obtenir Power BI</span><span class="sxs-lookup"><span data-stu-id="2470b-109">Get Power BI</span></span>

<span data-ttu-id="2470b-110">Si vous n’avez pas encore Power BI, vous pouvez vous [inscrire à Power BI Pro.](https://go.microsoft.com/fwlink/p/?linkid=845347)</span><span class="sxs-lookup"><span data-stu-id="2470b-110">If you don't already have Power BI, you can [sign up for Power BI Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span></span> <span data-ttu-id="2470b-111">Sélectionnez **Essayer gratuitement** de vous inscrire à une version d’essai ou achetez maintenant **pour** obtenir Power BI Pro.</span><span class="sxs-lookup"><span data-stu-id="2470b-111">Select **Try free** to sign up for a trial, or **Buy now** to get Power BI Pro.</span></span>
  
  
<span data-ttu-id="2470b-112">Vous pouvez également développer **Produits** pour acheter une version de Power BI.</span><span class="sxs-lookup"><span data-stu-id="2470b-112">You can also expand **Products** to buy a version of Power BI.</span></span> 

> [!NOTE]
> <span data-ttu-id="2470b-113">Vous avez besoin d’une licence Power BI Pro pour installer, personnaliser et distribuer une application de modèle.</span><span class="sxs-lookup"><span data-stu-id="2470b-113">You need a Power BI Pro license to install, customize, and distribute a template app.</span></span> <span data-ttu-id="2470b-114">Pour plus d’informations, voir [Conditions préalables.](/power-bi/service-template-apps-install-distribute?source=docs#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="2470b-114">For more information, please see [Prerequisites](/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span></span>

<span data-ttu-id="2470b-115">Pour partager vos données, vous et les personnes avec qui vous partagez les données, vous avez besoin d’une licence Power BI Pro ou le contenu doit se trouver dans un espace de travail dans un [service Premium Power BI.](/power-bi/service-premium-what-is)</span><span class="sxs-lookup"><span data-stu-id="2470b-115">To share your data, both you and the people who you share the data with, need a Power BI Pro license, or the content needs to be in a workspace in a [Power BI premium service](/power-bi/service-premium-what-is).</span></span> 
  
### <a name="enable-the-template-app"></a><span data-ttu-id="2470b-116">Activer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="2470b-116">Enable the template app</span></span>

<span data-ttu-id="2470b-117">Pour activer l’application de modèle, vous devez être administrateur **général.**</span><span class="sxs-lookup"><span data-stu-id="2470b-117">To enable the template app, you have to be a **Global administrator**.</span></span>
  
<span data-ttu-id="2470b-118">Pour plus [d’informations, voir](../add-users/about-admin-roles.md) les rôles d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2470b-118">See [about admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
1. <span data-ttu-id="2470b-119">Dans le centre d’administration, accédez à la page **Rapports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Utilisation</a>.</span><span class="sxs-lookup"><span data-stu-id="2470b-119">In the admin center, go to the **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> page.</span></span> 
    
2. <span data-ttu-id="2470b-120">Dans la page **Utilisation,** recherchez la carte d’analyse de l’utilisation **de Microsoft 365,** puis sélectionnez **Commencer.**</span><span class="sxs-lookup"><span data-stu-id="2470b-120">On the **Usage** page, locate the **Microsoft 365 usage analytics** card, and select **Get started**.</span></span>
    
3. <span data-ttu-id="2470b-121">Dans le panneau Rapports qui s’ouvre, définissez Rendre les données disponibles pour l’analyse de l’utilisation de **Microsoft 365** pour Power BI sur **Sur** \> **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="2470b-121">On the Reports panel that opens, set **Make data available to Microsoft 365 usage analytics for Power BI** to **On** \> **Save**.</span></span> 
  
<span data-ttu-id="2470b-122">Le processus de collecte de données se terminera en 2 à 48 heures en fonction de la taille de votre client.</span><span class="sxs-lookup"><span data-stu-id="2470b-122">The data collection process will complete in two to 48 hours depending on the size of your tenant.</span></span> <span data-ttu-id="2470b-123">Le **bouton Go to Power BI** est activé (et n’est plus gris) lorsque la collecte de données est terminée.</span><span class="sxs-lookup"><span data-stu-id="2470b-123">The **Go to Power BI** button will be enabled (no longer gray) when data collection is complete.</span></span> 
    
### <a name="start-the-template-app"></a><span data-ttu-id="2470b-124">Démarrer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="2470b-124">Start the template app</span></span>

<span data-ttu-id="2470b-125">Pour démarrer l’application de modèle, vous devez être administrateur **général,** lecteur de **rapports,** administrateur **Exchange,** administrateur **Skype** Entreprise ou **administrateur SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="2470b-125">To start the template app, you have to be either a **global administrator**, **report reader**, **Exchange administrator**, **Skype for Business administrator**, or **SharePoint administrator**.</span></span> 
  
1. <span data-ttu-id="2470b-126">Copiez l’ID de client et **sélectionnez Go to Power BI**.</span><span class="sxs-lookup"><span data-stu-id="2470b-126">Copy the tenant ID and select **Go to Power BI**.</span></span>
    
2.  <span data-ttu-id="2470b-127">Lorsque vous accédez à Power BI, connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="2470b-127">When you get to Power BI, sign in.</span></span> <span data-ttu-id="2470b-128">Sélectionnez **ensuite Applications** -> **Obtenir des applications** dans le menu de navigation.</span><span class="sxs-lookup"><span data-stu-id="2470b-128">Then **Select Apps**->**Get apps** from the navigation menu.</span></span>    
  
3. <span data-ttu-id="2470b-129">Dans **l’onglet** Applications, tapez Microsoft 365 dans la zone de recherche, puis sélectionnez Analyse de l’utilisation **de Microsoft 365** \> **Obtenez-le maintenant.**</span><span class="sxs-lookup"><span data-stu-id="2470b-129">In the **Apps** tab, type Microsoft 365 in the search box and then select **Microsoft 365 usage analytics** \> **Get it now**.</span></span>

    <span data-ttu-id="2470b-130">[![Sélectionnez Obtenir maintenant](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span><span class="sxs-lookup"><span data-stu-id="2470b-130">[![Select Get it now](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span></span>
    
4.  <span data-ttu-id="2470b-131">Une fois l’application installée.</span><span class="sxs-lookup"><span data-stu-id="2470b-131">Once the app is installed.</span></span> <span data-ttu-id="2470b-132">Sélectionnez la vignette pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="2470b-132">Select the tile to open it.</span></span>

5.  <span data-ttu-id="2470b-133">Sélectionnez **Explorer l’application** pour afficher l’application avec des exemples de données.</span><span class="sxs-lookup"><span data-stu-id="2470b-133">Select **Explore app** to view the app with sample data.</span></span> <span data-ttu-id="2470b-134">Choisissez **Se** connecter pour connecter l’application aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2470b-134">Choose **Connect** to connect the app to your organization’s data.</span></span>

6.  <span data-ttu-id="2470b-135">Choose **Connect**, on the **Connect to Microsoft 365 usage analytics** screen, then type in the tenant ID (without dashes) you copied in step (1), and select **Next**.</span><span class="sxs-lookup"><span data-stu-id="2470b-135">Choose **Connect**, on the **Connect to Microsoft 365 usage analytics** screen, then type in the tenant ID (without dashes) you copied in step (1), and select **Next**.</span></span>
    
7. <span data-ttu-id="2470b-136">Dans l’écran suivant, sélectionnez **OAuth2** en tant que méthode **d’authentification** \> **Sign in**.</span><span class="sxs-lookup"><span data-stu-id="2470b-136">On the next screen, select **OAuth2** as the **Authentication method** \> **Sign in**.</span></span> <span data-ttu-id="2470b-137">Si vous choisissez une autre méthode d’authentification, la connexion au modèle d’application échoue.</span><span class="sxs-lookup"><span data-stu-id="2470b-137">If you choose any other authentication method, the connection to the template app will fail.</span></span>
    
    ![Choisir un compte Microsoft comme méthode d’authentification](../../media/ab6f0463-c3f7-4088-a605-67c699fa86adnew.png)
  
8. <span data-ttu-id="2470b-139">Une fois l’application de modèle ins instantiée, le tableau de bord d’analyse de l’utilisation de Microsoft 365 sera disponible dans Power BI sur le web.</span><span class="sxs-lookup"><span data-stu-id="2470b-139">After the template app is instantiated the Microsoft 365 usage analytics dashboard will be available in Power BI on the web.</span></span> <span data-ttu-id="2470b-140">Le chargement initial du tableau de bord prend entre 2 et 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="2470b-140">The initial loading of the dashboard will take between 2 to 30 minutes.</span></span>
  
<span data-ttu-id="2470b-141">Les agrégats au niveau du client seront disponibles dans tous les rapports après l’avoir choisi.</span><span class="sxs-lookup"><span data-stu-id="2470b-141">Tenant level aggregates will be available in all reports after opting in.</span></span> <span data-ttu-id="2470b-142">Les détails au niveau de l’utilisateur ne seront disponibles qu’autour du 5 du mois calendaire suivant **après l’avoir choisi.**</span><span class="sxs-lookup"><span data-stu-id="2470b-142">**User-level details will only become available around the 5th of the next calendar month after opting in**.</span></span> <span data-ttu-id="2470b-143">Cela aura un impact sur tous les rapports sous Activité de l’utilisateur (voir Parcourir et utiliser les rapports dans l’analyse de l’utilisation de [Microsoft 365](navigate-and-utilize-reports.md) pour obtenir des conseils sur la façon d’afficher et d’utiliser ces rapports).</span><span class="sxs-lookup"><span data-stu-id="2470b-143">This will impact all reports under User Activity (See [Navigate and utilize the reports in Microsoft 365 usage analytics](navigate-and-utilize-reports.md) for tips on how to view and use these reports).</span></span>
    
## <a name="make-the-collected-data-anonymous"></a><span data-ttu-id="2470b-144">Anonymiser les données collectées</span><span class="sxs-lookup"><span data-stu-id="2470b-144">Make the collected data anonymous</span></span>

<span data-ttu-id="2470b-145">Pour anonymiser les données collectées pour tous les rapports, vous devez être administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2470b-145">To make the data that is collected for all reports anonymous, you have to be a global administrator.</span></span> <span data-ttu-id="2470b-146">Cela masquera les informations identifiables telles que les noms d’utilisateur, de groupe et de site dans les rapports et dans l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="2470b-146">This will hide identifiable information such as user, group and site names in reports and in the template app .</span></span>
  
1. <span data-ttu-id="2470b-147">Dans le Centre d’administration, sélectionnez **Paramètres** de l’organisation \> **paramètres,** puis sous **l’onglet Services,** choisissez **Rapports.**</span><span class="sxs-lookup"><span data-stu-id="2470b-147">In the admin center, go to the **Settings** \> **Org Settings**, and under **Services** tab, choose **Reports**.</span></span>
    
2. <span data-ttu-id="2470b-148">Sélectionnez **Rapports,** puis choisissez **d’afficher les identificateurs anonymes.**</span><span class="sxs-lookup"><span data-stu-id="2470b-148">Select **Reports**, and then choose to **Display anonymous identifiers**.</span></span> <span data-ttu-id="2470b-149">Ce paramètre est appliqué à la fois aux rapports d’utilisation et à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="2470b-149">This setting gets applied both to the usage reports as well as to the template app.</span></span>
  
3. <span data-ttu-id="2470b-150">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="2470b-150">Select **Save changes**.</span></span>