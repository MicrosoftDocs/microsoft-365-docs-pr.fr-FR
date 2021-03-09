---
title: Personnaliser les rapports dans l’analyse de l’utilisation de Microsoft 365
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
ms.assetid: 9b76065f-29b9-4b89-8059-c5f9db9ddbf6
description: Apprenez à personnaliser les rapports dans le navigateur et Power BI Desktop.
ms.openlocfilehash: 3c662dfa91939c68f0aa0a85c19a1fab003064bf
ms.sourcegitcommit: d3c1b08b3a8af29ef19ffe77da063920f28fe290
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "50572649"
---
# <a name="customize-the-reports-in-microsoft-365-usage-analytics"></a><span data-ttu-id="98010-103">Personnaliser les rapports dans l’analyse de l’utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="98010-103">Customize the reports in Microsoft 365 usage analytics</span></span>

::: moniker range="o365-21vianet"

> [!NOTE]
> <span data-ttu-id="98010-104">Le centre d’administration change.</span><span class="sxs-lookup"><span data-stu-id="98010-104">The admin center is changing.</span></span> <span data-ttu-id="98010-105">Si votre expérience ne correspond pas aux informations présentées ici, voir [À propos du nouveau centre d’administration Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="98010-105">If your experience doesn't match the details presented here, see [About the new Microsoft 365 admin center](https://docs.microsoft.com/microsoft-365/admin/microsoft-365-admin-center-preview?view=o365-21vianet&preserve-view=true).</span></span>

::: moniker-end

<span data-ttu-id="98010-106">L’analyse de l’utilisation de Microsoft 365 fournit un tableau de bord dans Power BI qui fournit des informations sur la façon dont les utilisateurs adoptent et utilisent Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="98010-106">Microsoft 365 usage analytics provides a dashboard in Power BI that offers insights into how users adopt and use Microsoft 365.</span></span> <span data-ttu-id="98010-107">Le tableau de bord n'est qu'un point de départ pour interagir avec les données d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="98010-107">The dashboard is just a starting point to interact with the usage data.</span></span> <span data-ttu-id="98010-108">Les rapports peuvent être personnalisés pour fournir des informations plus pertinentes.</span><span class="sxs-lookup"><span data-stu-id="98010-108">The reports can be customized for more personalized insights.</span></span>
  
<span data-ttu-id="98010-109">Vous pouvez également utiliser Power BI Desktop pour approfondir la personnalisation de vos rapports en les connectant à d'autres sources de données afin d'obtenir des informations plus pertinentes sur votre activité.</span><span class="sxs-lookup"><span data-stu-id="98010-109">You can also use the Power BI desktop to further customize your reports by connecting them to other data sources to gain richer insights about your business.</span></span>
  
## <a name="customizing-reports-in-the-browser"></a><span data-ttu-id="98010-110">Personnaliser les rapports dans le navigateur</span><span class="sxs-lookup"><span data-stu-id="98010-110">Customizing reports in the browser</span></span>

<span data-ttu-id="98010-111">Les deux exemples suivants montrent comment modifier un élément visuel existant et comment créer un élément visuel.</span><span class="sxs-lookup"><span data-stu-id="98010-111">The following two examples show how to modify an existing visual and how to create a new visual.</span></span>
  
### <a name="modify-an-existing-visual"></a><span data-ttu-id="98010-112">Modifier un élément visuel existant</span><span class="sxs-lookup"><span data-stu-id="98010-112">Modify an existing visual</span></span>

<span data-ttu-id="98010-113">Cet exemple montre comment modifier l’onglet **Activation** dans le rapport **Activation/Licences.**</span><span class="sxs-lookup"><span data-stu-id="98010-113">This example shows how to modify the **Activation** tab within the **Activation/Licensing** report.</span></span> 
  
1. <span data-ttu-id="98010-114">Dans le rapport **Activation/Licences,** sélectionnez **l’onglet Activation.**</span><span class="sxs-lookup"><span data-stu-id="98010-114">Within the **Activation/Licensing** report, select the **Activation** tab.</span></span>
    
2. <span data-ttu-id="98010-115">Entrez le mode d’édition en cliquant sur le bouton Modifier en haut via le bouton Plus de page dans le bouton Power  ![ ](../../media/d8da3c19-3f2d-4bf6-811e-faa804f74770.png) BI.</span><span class="sxs-lookup"><span data-stu-id="98010-115">Enter the edit mode by choosing the **Edit** button on the top through the ![The more page button in Power BI](../../media/d8da3c19-3f2d-4bf6-811e-faa804f74770.png) button.</span></span> 
    
    ![Click Edit report on the top right navigation](../../media/e2c16663-1fbd-4d7f-887c-0cbb891d3b3d.png)
  
3. <span data-ttu-id="98010-117">Dans la partie supérieure droite, sélectionnez **Dupliquer cette page.**</span><span class="sxs-lookup"><span data-stu-id="98010-117">On the top right, choose **Duplicate this page**.</span></span>
    
    ![Choose Duplicate this page](../../media/b2d18dcd-6b82-4ce7-ab79-1b24e3721309.png)
  
4. <span data-ttu-id="98010-119">En bas à droite, choisissez l’un des graphiques à barres affichant le nombre d’utilisateurs qui s’activent en fonction du système d’exploitation tel qu’Android, iOS, Mac, etc.</span><span class="sxs-lookup"><span data-stu-id="98010-119">In the bottom right, choose any of the bar-charts showing the count of users activating based on the OS such as Android, iOS, Mac, etc.</span></span>
    
5. <span data-ttu-id="98010-120">Dans la **zone Visualisations** à droite, afin de supprimer **Mac Count** de l’visuel, sélectionnez **le X** à côté de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="98010-120">In the **Visualizations** area to the right, in order to remove **Mac Count** from the visual, select the **X** next to it.</span></span>

    ![Supprimer le nombre de Mac](../../media/ce3d8358-df57-4f64-bd25-ac5be7fc8713.png)    
    
### <a name="create-a-new-visual"></a><span data-ttu-id="98010-122">Créer un élément visuel</span><span class="sxs-lookup"><span data-stu-id="98010-122">Create a new visual</span></span>

<span data-ttu-id="98010-123">L'exemple suivant montre comment créer un élément visuel pour assurer le suivi mensuel des nouveaux utilisateurs de Yammer.</span><span class="sxs-lookup"><span data-stu-id="98010-123">The following example shows how to create a new visual to track new Yammer users on monthly basis.</span></span>
  
1. <span data-ttu-id="98010-124">Go to the **Product Usage** report using the left nav and select the **Yammer** tab.</span><span class="sxs-lookup"><span data-stu-id="98010-124">Go to the **Product Usage** report using the left nav and select the **Yammer** tab.</span></span>
    
2. <span data-ttu-id="98010-125">Basculez en mode Édition en choisissant Le ![ bouton plus de page dans Power BI et ](../../media/d8da3c19-3f2d-4bf6-811e-faa804f74770.png) **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="98010-125">Switch to edit mode by choosing ![The more page button in Power BI](../../media/d8da3c19-3f2d-4bf6-811e-faa804f74770.png) and **Edit**.</span></span> 
    
3. <span data-ttu-id="98010-126">En bas de la page, sélectionnez le</span><span class="sxs-lookup"><span data-stu-id="98010-126">At the bottom of the page, select the</span></span> ![Bouton Ajouter une page dans Power BI](../../media/d3b8c117-17d4-4f53-b078-8fefc2155b24.png) <span data-ttu-id="98010-128">pour créer une page.</span><span class="sxs-lookup"><span data-stu-id="98010-128">to create a new page.</span></span>
  
4. <span data-ttu-id="98010-129">Dans la **zone Visualisations** à droite, choisissez le graphique **à** barres empilées (ligne supérieure, en premier à partir de la gauche).</span><span class="sxs-lookup"><span data-stu-id="98010-129">In the **Visualizations** area to the right, choose the **Stacked bar chart** (top row, first from left).</span></span>

    ![Sélectionner un graphique à barres](../../media/214c3fed-6eae-43e6-83fb-708a2d74406e.png)
    
5. <span data-ttu-id="98010-131">Sélectionnez la partie inférieure droite de cette visualisation et faites-la glisser pour la rendre plus grande.</span><span class="sxs-lookup"><span data-stu-id="98010-131">Select the bottom right of that visualization and drag to make it larger.</span></span>

6. <span data-ttu-id="98010-132">Dans la **zone Champs** à droite, développez **la** table Calendrier.</span><span class="sxs-lookup"><span data-stu-id="98010-132">In the **Fields** area to the right, expand the **Calendar** table.</span></span>

7. <span data-ttu-id="98010-133">Faites glisser **MonthName** vers la zone Champs, juste en-dessous du titre **Axe** de la zone **Visualisations**.</span><span class="sxs-lookup"><span data-stu-id="98010-133">Drag **MonthName** to the fields area, directly below the **Axis** heading in the **Visualizations** area.</span></span>
 
    ![Drag Month Name](../../media/bff99987-8c4b-4618-89fd-47df557b0ed7.png)
    
8. <span data-ttu-id="98010-135">Dans la zone **Champs** de droite, développez la table **TenantProductUsage**.</span><span class="sxs-lookup"><span data-stu-id="98010-135">In the **Fields** area to the right, expand the **TenantProductUsage** table.</span></span>

9. <span data-ttu-id="98010-136">Faites glisser **FirstTimeUsers** vers la zone Champs, juste en-dessous du titre **Valeur**.</span><span class="sxs-lookup"><span data-stu-id="98010-136">Drag **FirstTimeUsers** to the fields area, directly below the **Value** heading.</span></span>

10. <span data-ttu-id="98010-137">Faites glisser **Produit** vers la zone **Filtres**, juste en-dessous du titre **Filtres au niveau de l'élément visuel**.</span><span class="sxs-lookup"><span data-stu-id="98010-137">Drag **Product** to the **Filters** area, directly below the **Visual level filters** heading.</span></span>

11. <span data-ttu-id="98010-138">Dans la zone **Type de filtre** qui s'affiche, cochez la case **Yammer**.</span><span class="sxs-lookup"><span data-stu-id="98010-138">In the **Filter Type** area that appears, select the **Yammer** check box.</span></span>

    ![Cochez Yammer cocher](../../media/82e99730-0de9-42da-928a-76aab0c3e609.png)
  
12. <span data-ttu-id="98010-140">Juste en dessous de la liste des visualisations, choisissez **l’icône Format** de l’icône Format dans Power ![ BI Visualizaions ](../../media/ee0602f3-3df5-4930-b862-db1d90ae4ae2.png) .</span><span class="sxs-lookup"><span data-stu-id="98010-140">Just below the list of visualizations, choose the **Format** icon ![Format icon in Power BI Visualizaions](../../media/ee0602f3-3df5-4930-b862-db1d90ae4ae2.png).</span></span>

13. <span data-ttu-id="98010-141">Développez Titre et remplacez la valeur **Texte du titre** par **Nouveaux utilisateurs de Yammer par mois**.</span><span class="sxs-lookup"><span data-stu-id="98010-141">Expand Title and change the **Title Text** value to **First-Time Yammer Users by Month**.</span></span>
    
14. <span data-ttu-id="98010-142">Remplacez la valeur **Taille du texte** par **12**.</span><span class="sxs-lookup"><span data-stu-id="98010-142">Change the **Text Size** value to **12**.</span></span>
    
15. <span data-ttu-id="98010-143">Modifiez le titre de la nouvelle page en le éditant en bas à droite.</span><span class="sxs-lookup"><span data-stu-id="98010-143">Change the title of the new page by editing the name of the page on bottom right.</span></span>

16.  <span data-ttu-id="98010-144">Enregistrez le rapport en cliquant sur **Lecture en haut,** puis **enregistrez.**</span><span class="sxs-lookup"><span data-stu-id="98010-144">Save out the report by Clicking on **Reading View** on top and then **Save**.</span></span>
    
## <a name="customizing-the-reports-in-power-bi-desktop"></a><span data-ttu-id="98010-145">Personnaliser les rapports dans Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="98010-145">Customizing the reports in Power BI Desktop</span></span>

<span data-ttu-id="98010-p103">Pour la plupart des clients, la version web de Power BI suffit pour modifier les éléments visuels des rapports et des graphiques. Pour d'autres, en revanche, il peut être nécessaire de joindre ces données à d'autres sources de données afin d'obtenir des informations contextuelles plus pertinentes sur leur entreprise. Dans ce cas, ils peuvent utiliser Power BI Desktop pour personnaliser et créer des rapports supplémentaires. Vous pouvez télécharger [Power BI Desktop](https://go.microsoft.com/fwlink/p/?linkid=849797) gratuitement.</span><span class="sxs-lookup"><span data-stu-id="98010-p103">For most customers modifying the reports and chart visuals in Power BI web will be sufficient. For some however, there may be a need to join this data with other data sources to gain richer insights contextual to their own business, in which case they can customize and build additional reports using Power BI Desktop. You can download [Power BI Desktop](https://go.microsoft.com/fwlink/p/?linkid=849797) for free.</span></span> 
  
### <a name="use-the-reporting-apis"></a><span data-ttu-id="98010-149">Utiliser les API de création de rapports</span><span class="sxs-lookup"><span data-stu-id="98010-149">Use the reporting APIs</span></span>

<span data-ttu-id="98010-150">Vous pouvez commencer par vous connecter directement aux API de rapports ODATA à partir de Microsoft 365 qui sont à l’alimentation de ces rapports.</span><span class="sxs-lookup"><span data-stu-id="98010-150">You can start by connecting directly to the ODATA reporting APIs from Microsoft 365 that power these reports.</span></span>
  
1. <span data-ttu-id="98010-151">Accédez à **Obtenir des données** \> **Autres** \> **Flux ODATA** \> **Connexion**.</span><span class="sxs-lookup"><span data-stu-id="98010-151">Go to **get data** \> **Other** \> **ODATA Feed** \> **Connect**.</span></span>
    
2. <span data-ttu-id="98010-152">Dans la fenêtre URL, entrez « https:// <i></i> reports.office.com/pbi/v1.0/ \<tenantid\> »</span><span class="sxs-lookup"><span data-stu-id="98010-152">In the URL window enter "https://<i></i>reports.office.com/pbi/v1.0/\<tenantid\>"</span></span>
    
    <span data-ttu-id="98010-153">**REMARQUE :** Les API de création de rapports sont en prévisualisation et sont sujettes à modification jusqu’à leur mise en production.</span><span class="sxs-lookup"><span data-stu-id="98010-153">**NOTE:** The reporting APIs are in preview and are subject to change until they go into production.</span></span> 
  
    ![OData feed URL for Power BI desktop](../../media/c0ef967e-a454-4eba-bc8e-61e113170053.png)
  
3. <span data-ttu-id="98010-155">Entrez vos informations d’identification d’administrateur Microsoft 365 (organisation ou établissement scolaire) pour vous authentifier à Microsoft 365 lorsque vous y être invité.</span><span class="sxs-lookup"><span data-stu-id="98010-155">Enter your Microsoft 365 (organization or school) admin credentials to authenticate to Microsoft 365 when prompted.</span></span>
    
    <span data-ttu-id="98010-156">Consultez la [FAQ](usage-analytics.md#faq) pour plus d’informations sur les personnes autorisées à accéder aux rapports d’application du modèle Adoption de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="98010-156">See the [FAQ](usage-analytics.md#faq) for more information about who is allowed to access the Microsoft 365 Adoption template app reports.</span></span> 
    
4. <span data-ttu-id="98010-157">Une fois la connexion autorisée, la fenêtre du Navigateur affichera les jeux de données auxquels vous pouvez vous connecter.</span><span class="sxs-lookup"><span data-stu-id="98010-157">Once the connection is authorized, you will see the Navigator window that shows the datasets available to connect to.</span></span>
    
    <span data-ttu-id="98010-158">Sélectionnez tout et choisissez **Charger.**</span><span class="sxs-lookup"><span data-stu-id="98010-158">Select all and choose **Load**.</span></span>
    
    <span data-ttu-id="98010-159">Les données sont téléchargées dans votre instance de Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="98010-159">This will download the data into your Power BI Desktop.</span></span> <span data-ttu-id="98010-160">Enregistrez ce fichier pour pouvoir commencer à créer les rapports dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="98010-160">Save this file and then you can start creating the reports you need.</span></span>
    
    ![Valeurs ODATA disponibles dans l’API de rapports](../../media/545b4d17-dbbd-4cfc-b75a-a8b27283d438.png)
  
### <a name="use-the-microsoft-365-usage-analytics-template"></a><span data-ttu-id="98010-162">Utiliser le modèle d’analyse de l’utilisation de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="98010-162">Use the Microsoft 365 usage analytics template</span></span>

<span data-ttu-id="98010-163">Vous pouvez également utiliser le fichier de modèle Power BI qui correspond aux rapports d’analyse de l’utilisation de Microsoft 365 comme point de départ pour se connecter aux données.</span><span class="sxs-lookup"><span data-stu-id="98010-163">You can also use the Power BI template file that corresponds to the Microsoft 365 usage analytics reports as a starting point to connect to the data.</span></span> <span data-ttu-id="98010-164">L'avantage du fichier pbit est qu'il contient une chaîne de connexion déjà établie.</span><span class="sxs-lookup"><span data-stu-id="98010-164">The advantage of using the pbit file is that it has the connection string already established.</span></span> <span data-ttu-id="98010-165">Vous pouvez également tirer parti de toutes les mesures personnalisées créées, en plus des données renvoyées par le schéma de base.</span><span class="sxs-lookup"><span data-stu-id="98010-165">You can also take advantage of all the custom measures that are created, on top of the data that the base schema returns and build on it further.</span></span>
  
<span data-ttu-id="98010-166">Vous pouvez télécharger le fichier de modèle Power BI à partir du [Centre de téléchargement Microsoft.](https://download.microsoft.com/download/7/8/2/782ba8a7-8d89-4958-a315-dab04c3b620c/Microsoft%20365%20Usage%20Analytics.pbit)</span><span class="sxs-lookup"><span data-stu-id="98010-166">You can download the Power BI template file from the [Microsoft Download Center](https://download.microsoft.com/download/7/8/2/782ba8a7-8d89-4958-a315-dab04c3b620c/Microsoft%20365%20Usage%20Analytics.pbit).</span></span> <span data-ttu-id="98010-167">Après avoir téléchargé le fichier de modèle Power BI, suivez les étapes suivantes pour commencer :</span><span class="sxs-lookup"><span data-stu-id="98010-167">After you download the Power BI template file, follow these steps to get started:</span></span>
  
1. <span data-ttu-id="98010-168">Ouvrez le fichier pbit.</span><span class="sxs-lookup"><span data-stu-id="98010-168">Open the pbit file.</span></span>
    
2. <span data-ttu-id="98010-169">Entrez votre ID de locataire dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98010-169">Enter your tenant id value in the dialog.</span></span>
    
    ![Enter your tenant ID to open the pbit file](../../media/071ed0bf-8b9d-49c6-81fc-fd4c6cc85bd3.png)
  
3. <span data-ttu-id="98010-171">Entrez vos informations d’identification d’administrateur pour vous authentifier à Microsoft 365 lorsque vous y être invité.</span><span class="sxs-lookup"><span data-stu-id="98010-171">Enter your admin credentials to authenticate to Microsoft 365 when prompted.</span></span>
    
     <span data-ttu-id="98010-172">pour plus d’informations sur les personnes autorisées à accéder aux rapports d’analyse de l’utilisation de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="98010-172">for more information about who is allowed to access the Microsoft 365 usage analytics reports.</span></span> 
    
    <span data-ttu-id="98010-173">Une fois autorisées, les données seront actualisées dans le fichier Power BI.</span><span class="sxs-lookup"><span data-stu-id="98010-173">Once authorized, the data will be refreshed in the Power BI file.</span></span>
    
    <span data-ttu-id="98010-174">Le chargement des données peut prendre un certain temps. Au terme de celui-ci, vous pouvez enregistrer le fichier au format .pbix et continuer à personnaliser les rapports ou associer une source de données supplémentaire à ce rapport.</span><span class="sxs-lookup"><span data-stu-id="98010-174">Data load may take some time, once complete, you can save the file as a .pbix file and continue to customize the reports or bring an additional data source into this report.</span></span>
    
4. <span data-ttu-id="98010-p107">Suivez la documentation [Prise en main de Power BI](https://go.microsoft.com/fwlink/?linkid=849802) pour créer des rapports, les publier sur le service Power BI et les partager au sein de votre organisation. Pour poursuivre la personnalisation et le partage, des licences Power BI supplémentaires peuvent être nécessaires. Voir les [Conseils relatifs aux licences](https://go.microsoft.com/fwlink/p/?linkid=849803) Power BI pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="98010-p107">Follow [Getting started with Power BI](https://go.microsoft.com/fwlink/?linkid=849802) documentation to understand how to build reports, publish them to the Power BI service, and share with your organization. Following this path for customization and sharing may require additional Power BI licenses. See Power BI [licensing guidance](https://go.microsoft.com/fwlink/p/?linkid=849803) for details.</span></span> 
    

