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
description: Découvrez comment commencer à collecter des données pour votre client à l’aide de l’application de modèle d’analyse de l’utilisation 365 de Microsoft dans Power BI.
ms.openlocfilehash: cda5931e81f7ea13208825afa658f1c672a2f326
ms.sourcegitcommit: 34ebec8e2bd54ba3d4ccfd9724797665c965c17f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/13/2020
ms.locfileid: "49071454"
---
# <a name="enable-microsoft-365-usage-analytics"></a><span data-ttu-id="a8792-103">Activation de l'analyse de l'utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="a8792-103">Enable Microsoft 365 usage analytics</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="a8792-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="a8792-104">The admin center is changing.</span></span> <span data-ttu-id="a8792-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span><span class="sxs-lookup"><span data-stu-id="a8792-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet).</span></span>

::: moniker-end

<span data-ttu-id="a8792-106">L’analyse de l’utilisation de Microsoft 365 n’est pas encore disponible pour la communauté du gouvernement américain Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a8792-106">Microsoft 365 usage analytics is not yet available for Microsoft 365 US Government Community.</span></span>
  
## <a name="steps-to-enable-microsoft-365-usage-analytics"></a><span data-ttu-id="a8792-107">Étapes d’activation de l’analyse de l’utilisation 365 Microsoft</span><span class="sxs-lookup"><span data-stu-id="a8792-107">Steps to enable Microsoft 365 usage analytics</span></span>

<span data-ttu-id="a8792-108">Pour commencer à utiliser l’analyse de l’utilisation de Microsoft 365, vous devez d’abord mettre les données à disposition dans le centre d’administration 365 Microsoft, puis lancer l’application de modèle dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="a8792-108">To get started with Microsoft 365 usage analytics you must first make the data available in the Microsoft 365 admin center, then initiate the template app in Power BI.</span></span>
  
### <a name="get-power-bi"></a><span data-ttu-id="a8792-109">Obtenir Power BI</span><span class="sxs-lookup"><span data-stu-id="a8792-109">Get Power BI</span></span>

<span data-ttu-id="a8792-110">Si vous ne disposez pas encore de Power BI, vous pouvez vous [inscrire à Power bi Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span><span class="sxs-lookup"><span data-stu-id="a8792-110">If you don't already have Power BI, you can [sign up for Power BI Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span></span> <span data-ttu-id="a8792-111">Sélectionnez **essayer gratuitement** pour vous inscrire pour une version d’évaluation ou **acheter maintenant** pour obtenir Power bi Pro.</span><span class="sxs-lookup"><span data-stu-id="a8792-111">Select **Try free** to sign up for a trial, or **Buy now** to get Power BI Pro.</span></span>
  
  
<span data-ttu-id="a8792-112">Vous pouvez également développer **Produits** pour acheter une version de Power BI.</span><span class="sxs-lookup"><span data-stu-id="a8792-112">You can also expand **Products** to buy a version of Power BI.</span></span> 

> [!NOTE]
> <span data-ttu-id="a8792-113">Vous avez besoin d’une licence Power BI Pro pour installer, personnaliser et distribuer une application de modèle.</span><span class="sxs-lookup"><span data-stu-id="a8792-113">You need a Power BI Pro license to install, customize, and distribute a template app.</span></span> <span data-ttu-id="a8792-114">Pour plus d’informations, reportez-vous à la rubrique [conditions préalables](https://docs.microsoft.com/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a8792-114">For more information, please see [Prerequisites](https://docs.microsoft.com/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span></span>

<span data-ttu-id="a8792-115">Pour partager vos données, vous et les personnes avec lesquelles vous partagez des données, vous avez besoin d’une licence Power BI Pro ou le contenu doit se trouver dans un espace de travail dans un [service Power bi Premium](https://docs.microsoft.com/power-bi/service-premium-what-is).</span><span class="sxs-lookup"><span data-stu-id="a8792-115">To share your data, both you and the people who you share the data with, need a Power BI Pro license, or the content needs to be in a workspace in a [Power BI premium service](https://docs.microsoft.com/power-bi/service-premium-what-is).</span></span> 
  
### <a name="enable-the-template-app"></a><span data-ttu-id="a8792-116">Activer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="a8792-116">Enable the template app</span></span>

<span data-ttu-id="a8792-117">Pour activer l’application de modèle, vous devez être un **administrateur général**.</span><span class="sxs-lookup"><span data-stu-id="a8792-117">To enable the template app, you have to be a **Global administrator**.</span></span>
  
<span data-ttu-id="a8792-118">Pour plus d’informations, consultez la rubrique [à propos des rôles d’administrateur](../add-users/about-admin-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="a8792-118">See [about admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
1. <span data-ttu-id="a8792-119">Dans le centre d’administration, accédez à la page **Rapports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Utilisation</a>.</span><span class="sxs-lookup"><span data-stu-id="a8792-119">In the admin center, go to the **Reports** \> <a href="https://go.microsoft.com/fwlink/p/?linkid=2074756" target="_blank">Usage</a> page.</span></span> 
    
2. <span data-ttu-id="a8792-120">Sur la page **utilisation** , recherchez la carte d' **analyse d’utilisation Microsoft 365** , puis sélectionnez **prise en main**.</span><span class="sxs-lookup"><span data-stu-id="a8792-120">On the **Usage** page, locate the **Microsoft 365 usage analytics** card, and select **Get started**.</span></span>
    
3. <span data-ttu-id="a8792-121">Dans le panneau rapports qui s’ouvre, définissez **mettre les données à la disposition de l’analyse de l’utilisation de Microsoft 365 pour Power bi à l'** **On** \> **enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="a8792-121">On the Reports panel that opens, set **Make data available to Microsoft 365 usage analytics for Power BI** to **On** \> **Save**.</span></span> 
  
<span data-ttu-id="a8792-122">Le processus de collecte de données se terminera dans deux à 48 heures en fonction de la taille de votre client.</span><span class="sxs-lookup"><span data-stu-id="a8792-122">The data collection process will complete in two to 48 hours depending on the size of your tenant.</span></span> <span data-ttu-id="a8792-123">Le bouton **go to Power bi** est activé (il n’est plus grisé) une fois la collecte de données terminée.</span><span class="sxs-lookup"><span data-stu-id="a8792-123">The **Go to Power BI** button will be enabled (no longer gray) when data collection is complete.</span></span> 
    
### <a name="start-the-template-app"></a><span data-ttu-id="a8792-124">Démarrer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="a8792-124">Start the template app</span></span>

<span data-ttu-id="a8792-125">Pour démarrer l’application de modèle, vous devez être un **administrateur général** , un **lecteur de rapport** , un **administrateur Exchange** , un **administrateur Skype entreprise** ou un **administrateur SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="a8792-125">To start the template app, you have to be either a **global administrator** , **report reader** , **Exchange administrator** , **Skype for Business administrator** , or **SharePoint administrator**.</span></span> 
  
1. <span data-ttu-id="a8792-126">Copiez l’ID de client et sélectionnez **accéder à Power bi**.</span><span class="sxs-lookup"><span data-stu-id="a8792-126">Copy the tenant ID and select **Go to Power BI**.</span></span>
    
2.  <span data-ttu-id="a8792-127">Lorsque vous accédez à Power BI, connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="a8792-127">When you get to Power BI, sign in.</span></span> <span data-ttu-id="a8792-128">**Sélectionnez ensuite applications** -> **obtenir des applications** dans le menu de navigation.</span><span class="sxs-lookup"><span data-stu-id="a8792-128">Then **Select Apps**->**Get apps** from the navigation menu.</span></span>    
  
3. <span data-ttu-id="a8792-129">Dans l’onglet **apps** , tapez Microsoft 365 dans la zone de recherche, puis sélectionnez **analyse de l’utilisation de Microsoft 365** \> **Get it now**.</span><span class="sxs-lookup"><span data-stu-id="a8792-129">In the **Apps** tab, type Microsoft 365 in the search box and then select **Microsoft 365 usage analytics** \> **Get it now**.</span></span>

    <span data-ttu-id="a8792-130">[![Sélectionnez obtenir maintenant](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span><span class="sxs-lookup"><span data-stu-id="a8792-130">[![Select Get it now](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span></span>
    
4.  <span data-ttu-id="a8792-131">Une fois que l’application est installée.</span><span class="sxs-lookup"><span data-stu-id="a8792-131">Once the app is installed.</span></span> <span data-ttu-id="a8792-132">Sélectionnez la mosaïque pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="a8792-132">Select the tile to open it.</span></span>

5.  <span data-ttu-id="a8792-133">Sélectionnez **Explorer l’application** pour afficher l’application avec des exemples de données.</span><span class="sxs-lookup"><span data-stu-id="a8792-133">Select **Explore app** to view the app with sample data.</span></span> <span data-ttu-id="a8792-134">Sélectionnez **connecter** pour connecter l’application aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="a8792-134">Choose **Connect** to connect the app to your organization’s data.</span></span>

6.  <span data-ttu-id="a8792-135">Sélectionnez **connecter** , sur l’écran **se connecter à l’utilisation de Microsoft 365** , puis tapez l’ID de client (sans les tirets) que vous avez copié à l’étape (1), puis sélectionnez **suivant**.</span><span class="sxs-lookup"><span data-stu-id="a8792-135">Choose **Connect** , on the **Connect to Microsoft 365 usage analytics** screen, then type in the tenant ID (without dashes) you copied in step (1), and select **Next**.</span></span>
    
7. <span data-ttu-id="a8792-136">Dans l’écran suivant, sélectionnez **OAuth2** comme **méthode d’authentification** \> **Sign in**.</span><span class="sxs-lookup"><span data-stu-id="a8792-136">On the next screen, select **OAuth2** as the **Authentication method** \> **Sign in**.</span></span> <span data-ttu-id="a8792-137">Si vous choisissez une autre méthode d’authentification, la connexion à l’application de modèle échouera.</span><span class="sxs-lookup"><span data-stu-id="a8792-137">If you choose any other authentication method, the connection to the template app will fail.</span></span>
    
    ![Choisir un compte Microsoft comme méthode d’authentification](../../media/ab6f0463-c3f7-4088-a605-67c699fa86adnew.png)
  
8. <span data-ttu-id="a8792-139">Une fois l’application de modèle instanciée, le tableau de bord d’analyse de l’utilisation de Microsoft 365 sera disponible dans Power BI sur le Web.</span><span class="sxs-lookup"><span data-stu-id="a8792-139">After the template app is instantiated the Microsoft 365 usage analytics dashboard will be available in Power BI on the web.</span></span> <span data-ttu-id="a8792-140">Le chargement initial du tableau de bord prend entre 2 et 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="a8792-140">The initial loading of the dashboard will take between 2 to 30 minutes.</span></span>
  
<span data-ttu-id="a8792-141">Les agrégats de niveau client seront disponibles dans tous les rapports après avoir cliqué sur.</span><span class="sxs-lookup"><span data-stu-id="a8792-141">Tenant level aggregates will be available in all reports after opting in.</span></span> <span data-ttu-id="a8792-142">Les **Détails au niveau de l’utilisateur ne seront disponibles que dans le cinquième mois du calendrier suivant**.</span><span class="sxs-lookup"><span data-stu-id="a8792-142">**User-level details will only become available around the 5th of the next calendar month after opting in**.</span></span> <span data-ttu-id="a8792-143">Cela aura un impact sur tous les rapports sous activité de l’utilisateur (voir [naviguer et utiliser les rapports de l’analyse de l’utilisation de Microsoft 365](navigate-and-utilize-reports.md) pour obtenir des conseils sur l’affichage et l’utilisation de ces rapports).</span><span class="sxs-lookup"><span data-stu-id="a8792-143">This will impact all reports under User Activity (See [Navigate and utilize the reports in Microsoft 365 usage analytics](navigate-and-utilize-reports.md) for tips on how to view and use these reports).</span></span>
    
## <a name="make-the-collected-data-anonymous"></a><span data-ttu-id="a8792-144">Anonymiser les données collectées</span><span class="sxs-lookup"><span data-stu-id="a8792-144">Make the collected data anonymous</span></span>

<span data-ttu-id="a8792-145">Pour anonymiser les données collectées pour tous les rapports, vous devez être administrateur général.</span><span class="sxs-lookup"><span data-stu-id="a8792-145">To make the data that is collected for all reports anonymous, you have to be a global administrator.</span></span> <span data-ttu-id="a8792-146">Cette opération masque les informations identifiables telles que les noms d’utilisateur, de groupe et de site dans les rapports et l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="a8792-146">This will hide identifiable information such as user, group and site names in reports and in the template app .</span></span>
  
1. <span data-ttu-id="a8792-147">Dans le centre d’administration, accédez à **Settings** paramètres d' \> **organisation** paramètres, puis, sous l’onglet **services** , choisissez **rapports**.</span><span class="sxs-lookup"><span data-stu-id="a8792-147">In the admin center, go to the **Settings** \> **Org Settings** , and under **Services** tab, choose **Reports**.</span></span>
    
2. <span data-ttu-id="a8792-148">Sélectionnez **rapports** , puis choisissez d' **afficher les identificateurs anonymes**.</span><span class="sxs-lookup"><span data-stu-id="a8792-148">Select **Reports** , and then choose to **Display anonymous identifiers**.</span></span> <span data-ttu-id="a8792-149">Ce paramètre est appliqué à la fois aux rapports d’utilisation ainsi qu’à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="a8792-149">This setting gets applied both to the usage reports as well as to the template app.</span></span>
  
3. <span data-ttu-id="a8792-150">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="a8792-150">Select **Save changes**.</span></span>
