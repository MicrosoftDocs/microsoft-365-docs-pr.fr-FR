---
title: Activation de l'analyse de l'utilisation de Microsoft 365
f1.keywords:
- CSH
ms.author: efrene
author: efrene
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
description: Découvrez comment commencer à collecter des données pour votre client à l’aide de l’application Microsoft 365 d’analyse de l’utilisation dans Power BI.
ms.openlocfilehash: 01923887b4af143d1490e14d59a6174700e6ae93
ms.sourcegitcommit: 17f0aada83627d9defa0acf4db03a2d58e46842f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "52635413"
---
# <a name="enable-microsoft-365-usage-analytics"></a><span data-ttu-id="012f6-103">Activation de l'analyse de l'utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="012f6-103">Enable Microsoft 365 usage analytics</span></span>

<span data-ttu-id="012f6-104">Microsoft 365'analyse de l’utilisation n’est pas encore disponible pour Microsoft 365 gouvernement américain Community.</span><span class="sxs-lookup"><span data-stu-id="012f6-104">Microsoft 365 usage analytics is not yet available for Microsoft 365 US Government Community.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="012f6-105">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="012f6-105">Before you begin</span></span>

<span data-ttu-id="012f6-106">Pour commencer à utiliser Microsoft 365 l’analyse de l’utilisation, vous devez d’abord rendre les données disponibles dans le Centre d’administration Microsoft 365, puis lancer l’application modèle dans Power BI.</span><span class="sxs-lookup"><span data-stu-id="012f6-106">To get started with Microsoft 365 usage analytics you must first make the data available in the Microsoft 365 admin center, then initiate the template app in Power BI.</span></span>
  
## <a name="get-power-bi"></a><span data-ttu-id="012f6-107">Obtenir Power BI</span><span class="sxs-lookup"><span data-stu-id="012f6-107">Get Power BI</span></span>

<span data-ttu-id="012f6-108">Si vous n’avez pas encore Power BI, vous pouvez vous inscrire [à Power BI Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span><span class="sxs-lookup"><span data-stu-id="012f6-108">If you don't already have Power BI, you can [sign up for Power BI Pro](https://go.microsoft.com/fwlink/p/?linkid=845347).</span></span> <span data-ttu-id="012f6-109">Sélectionnez **Essayer de** vous inscrire gratuitement à une version d’essai ou **achetez** maintenant pour obtenir Power BI Pro.</span><span class="sxs-lookup"><span data-stu-id="012f6-109">Select **Try free** to sign up for a trial, or **Buy now** to get Power BI Pro.</span></span>
  
  
<span data-ttu-id="012f6-110">Vous pouvez également développer **Produits** pour acheter une version de Power BI.</span><span class="sxs-lookup"><span data-stu-id="012f6-110">You can also expand **Products** to buy a version of Power BI.</span></span> 

> [!NOTE]
> <span data-ttu-id="012f6-111">Vous avez besoin d Power BI Pro licence pour installer, personnaliser et distribuer une application de modèle.</span><span class="sxs-lookup"><span data-stu-id="012f6-111">You need a Power BI Pro license to install, customize, and distribute a template app.</span></span> <span data-ttu-id="012f6-112">Pour plus d’informations, voir [Conditions préalables.](/power-bi/service-template-apps-install-distribute?source=docs#prerequisites)</span><span class="sxs-lookup"><span data-stu-id="012f6-112">For more information, please see [Prerequisites](/power-bi/service-template-apps-install-distribute?source=docs#prerequisites).</span></span>

<span data-ttu-id="012f6-113">Pour partager vos données, vous et les personnes avec qui vous partagez les données, vous avez besoin d’une licence Power BI Pro ou le contenu doit se trouver dans un espace de travail dans un [service Power BI premium](/power-bi/service-premium-what-is).</span><span class="sxs-lookup"><span data-stu-id="012f6-113">To share your data, both you and the people who you share the data with, need a Power BI Pro license, or the content needs to be in a workspace in a [Power BI premium service](/power-bi/service-premium-what-is).</span></span> 
  
## <a name="enable-the-template-app"></a><span data-ttu-id="012f6-114">Activer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="012f6-114">Enable the template app</span></span>

<span data-ttu-id="012f6-115">Pour activer l’application de modèle, vous devez être administrateur **général.**</span><span class="sxs-lookup"><span data-stu-id="012f6-115">To enable the template app, you have to be a **Global administrator**.</span></span>
  
<span data-ttu-id="012f6-116">Pour plus [d’informations, voir les rôles](../add-users/about-admin-roles.md) d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="012f6-116">See [about admin roles](../add-users/about-admin-roles.md) for more information.</span></span> 
  
1. <span data-ttu-id="012f6-117">Dans le Centre d’administration, allez dans **l’onglet Paramètres** \> **Services des paramètres** \> **de l’organisation.**</span><span class="sxs-lookup"><span data-stu-id="012f6-117">In the admin center, go to the **Settings** \> **Org settings** \> **Services** tab.</span></span> 
    
2. <span data-ttu-id="012f6-118">Sous **l’onglet Services,** sélectionnez **Rapports.**</span><span class="sxs-lookup"><span data-stu-id="012f6-118">On the **Services** tab, select  **Reports**.</span></span>
    
3. <span data-ttu-id="012f6-119">Dans le panneau Rapports qui s’ouvre, définissez Rendre les données de rapport disponibles Microsoft 365 **l’analyse** de l’utilisation Power BI sur **Sur** \> **enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="012f6-119">On the Reports panel that opens, set **Make report data available to Microsoft 365 usage analytics for Power BI** to **On** \> **Save**.</span></span> 
  
<span data-ttu-id="012f6-120">Le processus de collecte de données se terminera en 2 à 48 heures en fonction de la taille de votre client.</span><span class="sxs-lookup"><span data-stu-id="012f6-120">The data collection process will complete in two to 48 hours depending on the size of your tenant.</span></span> <span data-ttu-id="012f6-121">Le **bouton Go to Power BI** est activé (plus gris) lorsque la collecte de données est terminée.</span><span class="sxs-lookup"><span data-stu-id="012f6-121">The **Go to Power BI** button will be enabled (no longer gray) when data collection is complete.</span></span> 
    
## <a name="start-the-template-app"></a><span data-ttu-id="012f6-122">Démarrer l’application de modèle</span><span class="sxs-lookup"><span data-stu-id="012f6-122">Start the template app</span></span>

<span data-ttu-id="012f6-123">Pour démarrer l’application de modèle, vous devez être un administrateur **général,** un lecteur de **rapports,** un administrateur **Exchange,** un administrateur **Skype Entreprise** ou un **administrateur SharePoint.**</span><span class="sxs-lookup"><span data-stu-id="012f6-123">To start the template app, you have to be either a **global administrator**, **report reader**, **Exchange administrator**, **Skype for Business administrator**, or **SharePoint administrator**.</span></span> 
  
1. <span data-ttu-id="012f6-124">Copiez l’ID de client et **sélectionnez Power BI**.</span><span class="sxs-lookup"><span data-stu-id="012f6-124">Copy the tenant ID and select **Go to Power BI**.</span></span>
    
2.  <span data-ttu-id="012f6-125">Lorsque vous accédez à Power BI, connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="012f6-125">When you get to Power BI, sign in.</span></span> <span data-ttu-id="012f6-126">Sélectionnez **ensuite Applications** -> **Obtenir des applications** dans le menu de navigation.</span><span class="sxs-lookup"><span data-stu-id="012f6-126">Then **Select Apps**->**Get apps** from the navigation menu.</span></span>    
  
3. <span data-ttu-id="012f6-127">Dans **l’onglet** Applications, tapez Microsoft 365 dans la zone de recherche, puis sélectionnez Microsoft 365 **l’analyse de l’utilisation.** \> </span><span class="sxs-lookup"><span data-stu-id="012f6-127">In the **Apps** tab, type Microsoft 365 in the search box and then select **Microsoft 365 usage analytics** \> **Get it now**.</span></span>

    <span data-ttu-id="012f6-128">[![Sélectionnez Obtenir maintenant](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span><span class="sxs-lookup"><span data-stu-id="012f6-128">[![Select Get it now](../../media/78102250-9874-4a32-8365-436f13560b52.png)](https://app.powerbi.com/groups/me/getapps/services/cia_microsoft365.microsoft-365-usage-analytics)</span></span>
    
4.  <span data-ttu-id="012f6-129">Une fois l’application installée.</span><span class="sxs-lookup"><span data-stu-id="012f6-129">Once the app is installed.</span></span> <span data-ttu-id="012f6-130">Sélectionnez la vignette pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="012f6-130">Select the tile to open it.</span></span>

5.  <span data-ttu-id="012f6-131">Sélectionnez **Explorer l’application** pour afficher l’application avec des exemples de données.</span><span class="sxs-lookup"><span data-stu-id="012f6-131">Select **Explore app** to view the app with sample data.</span></span> <span data-ttu-id="012f6-132">Choisissez **Connecter** pour connecter l’application aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="012f6-132">Choose **Connect** to connect the app to your organization’s data.</span></span>

6.  <span data-ttu-id="012f6-133">Choisissez **Connecter**, sur **l’écran d’analyse** de l’utilisation Connecter à Microsoft 365, puis tapez l’ID de locataire (sans tirets) que vous avez copié à l’étape (1), puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="012f6-133">Choose **Connect**, on the **Connect to Microsoft 365 usage analytics** screen, then type in the tenant ID (without dashes) you copied in step (1), and select **Next**.</span></span>
    
7. <span data-ttu-id="012f6-134">Dans l’écran suivant, sélectionnez **OAuth2** en tant que méthode **d’authentification** \> **Sign in**.</span><span class="sxs-lookup"><span data-stu-id="012f6-134">On the next screen, select **OAuth2** as the **Authentication method** \> **Sign in**.</span></span> <span data-ttu-id="012f6-135">Si vous choisissez une autre méthode d’authentification, la connexion au modèle d’application échoue.</span><span class="sxs-lookup"><span data-stu-id="012f6-135">If you choose any other authentication method, the connection to the template app will fail.</span></span>
    
    ![Choisir un compte Microsoft comme méthode d’authentification](../../media/ab6f0463-c3f7-4088-a605-67c699fa86adnew.png)
  
8. <span data-ttu-id="012f6-137">Une fois l’application de modèle ins Microsoft 365 le tableau de bord d’analyse de l’utilisation sera disponible Power BI sur le web.</span><span class="sxs-lookup"><span data-stu-id="012f6-137">After the template app is instantiated the Microsoft 365 usage analytics dashboard will be available in Power BI on the web.</span></span> <span data-ttu-id="012f6-138">Le chargement initial du tableau de bord prend entre 2 et 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="012f6-138">The initial loading of the dashboard will take between 2 to 30 minutes.</span></span>
  
<span data-ttu-id="012f6-139">Les agrégats au niveau du client seront disponibles dans tous les rapports après l’avoir choisi.</span><span class="sxs-lookup"><span data-stu-id="012f6-139">Tenant level aggregates will be available in all reports after opting in.</span></span> <span data-ttu-id="012f6-140">Les détails au niveau de l’utilisateur ne seront disponibles que le 5 du mois calendaire suivant **après l’avoir choisi.**</span><span class="sxs-lookup"><span data-stu-id="012f6-140">**User-level details will only become available around the 5th of the next calendar month after opting in**.</span></span> <span data-ttu-id="012f6-141">Cela aura un impact sur [](navigate-and-utilize-reports.md) tous les rapports sous Activité de l’utilisateur (voir Naviguer et utiliser les rapports dans Microsoft 365'analyse de l’utilisation pour obtenir des conseils sur la façon d’afficher et d’utiliser ces rapports).</span><span class="sxs-lookup"><span data-stu-id="012f6-141">This will impact all reports under User Activity (See [Navigate and utilize the reports in Microsoft 365 usage analytics](navigate-and-utilize-reports.md) for tips on how to view and use these reports).</span></span>
    
## <a name="make-the-collected-data-anonymous"></a><span data-ttu-id="012f6-142">Anonymiser les données collectées</span><span class="sxs-lookup"><span data-stu-id="012f6-142">Make the collected data anonymous</span></span>

<span data-ttu-id="012f6-143">Pour anonymiser les données collectées pour tous les rapports, vous devez être administrateur général.</span><span class="sxs-lookup"><span data-stu-id="012f6-143">To make the data that is collected for all reports anonymous, you have to be a global administrator.</span></span> <span data-ttu-id="012f6-144">Cela masquera les informations identifiables telles que les noms d’utilisateur, de groupe et de site dans les rapports et dans l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="012f6-144">This will hide identifiable information such as user, group and site names in reports and in the template app .</span></span>
  
1. <span data-ttu-id="012f6-145">Dans le centre d’administration, allez à **l’Paramètres** Org Paramètres et sous \> l’onglet **Services,** choisissez **Rapports.**</span><span class="sxs-lookup"><span data-stu-id="012f6-145">In the admin center, go to the **Settings** \> **Org Settings**, and under **Services** tab, choose **Reports**.</span></span>
    
2. <span data-ttu-id="012f6-146">Sélectionnez **Rapports,** puis choisissez **d’afficher les identificateurs anonymes.**</span><span class="sxs-lookup"><span data-stu-id="012f6-146">Select **Reports**, and then choose to **Display anonymous identifiers**.</span></span> <span data-ttu-id="012f6-147">Ce paramètre est appliqué à la fois aux rapports d’utilisation et à l’application de modèle.</span><span class="sxs-lookup"><span data-stu-id="012f6-147">This setting gets applied both to the usage reports as well as to the template app.</span></span>
  
3. <span data-ttu-id="012f6-148">Sélectionnez **Enregistrer les modifications**.</span><span class="sxs-lookup"><span data-stu-id="012f6-148">Select **Save changes**.</span></span>

## <a name="related-content"></a><span data-ttu-id="012f6-149">Contenu associé</span><span class="sxs-lookup"><span data-stu-id="012f6-149">Related content</span></span>

<span data-ttu-id="012f6-150">[À propos de l’analyse de l’utilisation](usage-analytics.md) (article)</span><span class="sxs-lookup"><span data-stu-id="012f6-150">[About usage analytics](usage-analytics.md) (article)</span></span>\
<span data-ttu-id="012f6-151">[Obtenir la dernière version de l’analyse de l’utilisation](get-the-latest-version-of-usage-analytics.md) (article)</span><span class="sxs-lookup"><span data-stu-id="012f6-151">[Get the latest version of usage analytics](get-the-latest-version-of-usage-analytics.md) (article)</span></span>\
<span data-ttu-id="012f6-152">[Naviguer et utiliser les rapports dans l’analyse Microsoft 365'utilisation (article)](navigate-and-utilize-reports.md)</span><span class="sxs-lookup"><span data-stu-id="012f6-152">[Navigate and utilize the reports in Microsoft 365 usage analytics](navigate-and-utilize-reports.md) (article)</span></span>