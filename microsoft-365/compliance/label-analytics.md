---
title: Afficher l’utilisation d’étiquette grâce à la page Analyse des étiquettes
f1.keywords:
- CSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Après avoir créé vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir comment ils sont utilisés au sein de votre client. Les portails Centre de conformité Microsoft 365 et Centre de sécurité Microsoft 365 sont dotés d’une page intitulée Analyse des étiquettes. Elle indique les étiquettes les plus utilisées et leurs types d’applications.
ms.openlocfilehash: 75eb86cb8671c81b80afc67b19d7c54830c4c401
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42072278"
---
# <a name="view-label-usage-with-label-analytics"></a><span data-ttu-id="e95e5-104">Afficher l’utilisation d’étiquette grâce à la page Analyse des étiquettes</span><span class="sxs-lookup"><span data-stu-id="e95e5-104">View label usage with label analytics</span></span>

<span data-ttu-id="e95e5-105">Après avoir créé vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir comment ils sont utilisés au sein de votre client.</span><span class="sxs-lookup"><span data-stu-id="e95e5-105">After you create your retention labels and sensitivity labels, you’ll want to see how they’re being used across your tenant.</span></span> <span data-ttu-id="e95e5-106">Les portails Centre de conformité Microsoft 365 et Centre de sécurité Microsoft 365 sont dotés d’une page intitulée Analyse des étiquettes. Elle indique les étiquettes les plus utilisées et leurs types d’applications.</span><span class="sxs-lookup"><span data-stu-id="e95e5-106">With label analytics in the Microsoft 365 compliance center and Microsoft 365 security center, you can quickly see which labels are used the most and where they’re being applied.</span></span>

<span data-ttu-id="e95e5-107">Par exemple, avec analytique étiquette, vous pouvez afficher:</span><span class="sxs-lookup"><span data-stu-id="e95e5-107">For example, with label analytics, you can view the:</span></span>

- <span data-ttu-id="e95e5-108">Le nombre total de rétention étiquettes et les étiquettes de sensibilité appliquées au contenu.</span><span class="sxs-lookup"><span data-stu-id="e95e5-108">Total number of retention labels and sensitivity labels applied to content.</span></span>
- <span data-ttu-id="e95e5-109">Les étiquettes supérieures et le nombre de compte pour lequel chaque étiquette a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="e95e5-109">Top labels and the count of how many times each label was applied.</span></span>
- <span data-ttu-id="e95e5-110">Les emplacements où les étiquettes sont appliquées et le nombre pour chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="e95e5-110">Locations where labels are applied and the count for each location.</span></span>
- <span data-ttu-id="e95e5-111">Compter le nombre de fichiers et des dossiers pour lesquels l’étiquette de rétention a été modifiée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="e95e5-111">Count for how many files and folders had their retention label changed or removed.</span></span>

<span data-ttu-id="e95e5-112">Vous trouverez analytique étiquette dans la [centre de conformité de Microsoft 365](https://compliance.microsoft.com/labelanalytics) ou [centre de sécurité Microsoft 365](https://security.microsoft.com/labelanalytics) > **Classification**  >  \*\* Étiquettes analytique\*\*.</span><span class="sxs-lookup"><span data-stu-id="e95e5-112">You can find label analytics in the [Microsoft 365 compliance center](https://compliance.microsoft.com/labelanalytics) or [Microsoft 365 security center](https://security.microsoft.com/labelanalytics) > **Classification** > **Label analytics**.</span></span>

![Page analytique étiquette](../media/label-analytics-page.png)

## <a name="sensitivity-label-usage"></a><span data-ttu-id="e95e5-114">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="e95e5-114">Sensitivity label usage</span></span>

<span data-ttu-id="e95e5-115">Les données sur l’utilisation de la sensibilité étiquette sont extraite des rapports pour Azure Information Protection-pour plus d’informations, voir [Central de création de rapports de Protection Informations Azure](https://docs.microsoft.com/azure/information-protection/reports-aip).</span><span class="sxs-lookup"><span data-stu-id="e95e5-115">The data on sensitivity label usage is pulled from the reports for Azure Information Protection – for more information, see [Central reporting for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/reports-aip).</span></span>

<span data-ttu-id="e95e5-116">Notez que les rapports de Protection d’Informations Azure Information ont des[conditions préalables](/azure/information-protection/reports-aip#prerequisites) qui s’appliquent également à l’analytique d’étiquette sur les étiquettes de niveau de confidentialité dans le centre de conformité de Microsoft 365 et centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e95e5-116">Note that the Azure Information Protection reports have [prerequisites](/azure/information-protection/reports-aip#prerequisites) that also apply to label analytics on sensitivity labels in the Microsoft 365 compliance center and Microsoft 365 security center.</span></span> <span data-ttu-id="e95e5-117">Par exemple, vous avez besoin d’un abonnement Azure qui inclut le journal Analytique, car ces rapports sont le résultat de l’envoi d’informations d’événements d’audit d’une protection à partir de scanneurs et Azure Information Protection clients vers un emplacement centralisé basé sur Azure journal Service Analytique.</span><span class="sxs-lookup"><span data-stu-id="e95e5-117">For example, you need an Azure subscription that includes the Log Analytics because these reports are a result of sending information protection audit events from Azure Information Protection clients and scanners to a centralized location based on Azure Log Analytics service.</span></span>

<span data-ttu-id="e95e5-118">Usage d’étiquettes de niveau de confidentialité:</span><span class="sxs-lookup"><span data-stu-id="e95e5-118">For sensitivity label usage:</span></span>

- <span data-ttu-id="e95e5-119">Il n’existe aucune latence dans les données.</span><span class="sxs-lookup"><span data-stu-id="e95e5-119">There is no latency in the data.</span></span> <span data-ttu-id="e95e5-120">Il s’agit d’un rapport en temps réel.</span><span class="sxs-lookup"><span data-stu-id="e95e5-120">This is a real-time report.</span></span>
- <span data-ttu-id="e95e5-121">Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e95e5-121">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="e95e5-122">Le rapport indique où les étiquettes de niveau de confidentialité sont appliquées par application (tandis que les étiquettes de rétention sont affichées par emplacement).</span><span class="sxs-lookup"><span data-stu-id="e95e5-122">The report shows where sensitivity labels are applied per app (whereas retention labels are shown per location).</span></span>

![Rapport d’usage d’étiquettes de niveau de confidentialité](../media/sensitivity-label-usage-report.png)

## <a name="retention-label-usage"></a><span data-ttu-id="e95e5-124">Usage d’étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="e95e5-124">Retention label usage</span></span>

<span data-ttu-id="e95e5-125">Ce rapport affiche un aperçu rapide de ce que sont les étiquettes supérieures et où elles sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="e95e5-125">This report shows a quick view of what the top labels are and where they’re applied.</span></span> <span data-ttu-id="e95e5-126">Pour plus d’informations sur l’intitulé de contenu dans SharePoint et OneDrive, voir [Afficher l’activité des étiquettes pour les documents](view-label-activity-for-documents.md).</span><span class="sxs-lookup"><span data-stu-id="e95e5-126">For more detailed information on how content in SharePoint and OneDrive is labeled, see [View label activity for documents](view-label-activity-for-documents.md).</span></span>

<span data-ttu-id="e95e5-127">Usage d’étiquette de rétention:</span><span class="sxs-lookup"><span data-stu-id="e95e5-127">For retention label usage:</span></span>

- <span data-ttu-id="e95e5-128">Les données sont regroupées de manière hebdomadaire, aussi cela peut prendre jusqu'à sept jours pour que les données s’affichent dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="e95e5-128">Data is aggregated weekly, so it may take up to seven days for data to appear in the report.</span></span>
- <span data-ttu-id="e95e5-129">Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e95e5-129">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="e95e5-130">Le rapport indique où les étiquettes de rétention sont appliquées par emplacement (tandis que les étiquettes de sensibilité sont affichées par application).</span><span class="sxs-lookup"><span data-stu-id="e95e5-130">The report shows where retention labels are applied per location (whereas sensitivity labels are shown per app).</span></span>
- <span data-ttu-id="e95e5-131">Pour les étiquettes de rétention, il s’agit d’une synthèse des données à tout-moment dans votre client ; elles ne sont pas filtrées pour une plage de dates spécifique.</span><span class="sxs-lookup"><span data-stu-id="e95e5-131">For retention labels, this is a summary of the all-time data in your tenant; it’s not filtered to a specific date range.</span></span> <span data-ttu-id="e95e5-132">En revanche, l’[étiquette d’activité Explorer](view-label-activity-for-documents.md) affiche les données 30 derniers jours uniquement.</span><span class="sxs-lookup"><span data-stu-id="e95e5-132">By contrast, the [Label Activity Explorer](view-label-activity-for-documents.md) shows data from only the past 30 days.</span></span>

![Rapport d’usage d’étiquette de rétention](../media/retention-label-usage-report.png)

## <a name="view-all-content-with-a-specific-retention-label"></a><span data-ttu-id="e95e5-134">Afficher tout le contenu portant une étiquette de rétention spécifique</span><span class="sxs-lookup"><span data-stu-id="e95e5-134">View all content with a specific retention label</span></span>

<span data-ttu-id="e95e5-135">Dans le rapport d’utilisation d’étiquette de rétention, vous pouvez rapidement explorer tout le contenu associé à cette étiquette appliquée.</span><span class="sxs-lookup"><span data-stu-id="e95e5-135">From the retention label usage report, you can quickly explore all content with that label applied.</span></span> <span data-ttu-id="e95e5-136">(Notez que nous travaillons actuellement sur cette fonctionnalité, afin que le processus prenne plus d’étapes pour afficher tout le contenu étiqueté).</span><span class="sxs-lookup"><span data-stu-id="e95e5-136">(Note that we're currently working on this feature, so that it will take fewer steps to view all the labeled content.)</span></span>

<span data-ttu-id="e95e5-137">Tout d’abord, choisissez **Afficher les détails** en bas du rapport.</span><span class="sxs-lookup"><span data-stu-id="e95e5-137">First, choose **View Details** at the bottom of the report.</span></span>

![Option Afficher les détails en bas de rapport d’utilisation d’étiquette de rétention](../media/retention-label-usage-view-details.png)

<span data-ttu-id="e95e5-139">Puis choisissez une étiquette de rétention > **Explorer les éléments** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="e95e5-139">Then choose a retention label > **Explore items** in the right pane.</span></span>

![Explorer l’option éléments dans le volet droit](../media/retention-label-usage-explore-items.png)

<span data-ttu-id="e95e5-141">Pour cette étiquette, vous pouvez choisir l’onglet**activité**pour consulter un nombre d’éléments associé à cette étiquette selon l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="e95e5-141">For that label, you can choose the **Activity** tab to view a count of items with that label by location.</span></span>

![Onglet activité pour une étiquette de rétention](../media/retention-label-usage-activity-tab.png)

<span data-ttu-id="e95e5-143">Vous pouvez également choisir l’onglet**éléments avec cette étiquette**. Ensuite, vous pouvez explorer des emplacements spécifiques :</span><span class="sxs-lookup"><span data-stu-id="e95e5-143">You can also choose the **Items with this label** tab. Then you can drill into specific locations:</span></span>

- <span data-ttu-id="e95e5-144">Pour Exchange Online, consultez la liste de boîtes aux lettres avec le nombre d’éléments étiquetés dans chaque boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="e95e5-144">For Exchange Online, you see a list of mailboxes with the count of labeled items in each mailbox.</span></span>
- <span data-ttu-id="e95e5-145">Pour SharePoint Online et OneDrive Entreprise, vous voyez une liste de collections de sites et les comptes OneDrive avec le nombre d’éléments étiquetés dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="e95e5-145">For SharePoint Online and OneDrive for Business, you see a list of site collections and OneDrive accounts with the count of labeled items in each location.</span></span>

<span data-ttu-id="e95e5-146">Lorsque vous choisissez une collection de boîte aux lettres ou un site, vous pouvez afficher une liste d’éléments associé à cette étiquette rétention dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="e95e5-146">When you choose a mailbox or site collection, you can view a list of items with that retention label in that location.</span></span>

![Les éléments de cet onglet d’étiquette affichant tous les éléments comportant cette étiquette rétention](../media/retention-label-usage-content-explorer.png)

## <a name="permissions"></a><span data-ttu-id="e95e5-148">Autorisations</span><span class="sxs-lookup"><span data-stu-id="e95e5-148">Permissions</span></span>

<span data-ttu-id="e95e5-149">Pour afficher analytique étiquette, vous devez être affecté parmi les rôles suivants dans Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="e95e5-149">To view label analytics, you must be assigned one of the following roles in Azure Active Directory:</span></span>

- <span data-ttu-id="e95e5-150">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="e95e5-150">Global administrator</span></span>
- <span data-ttu-id="e95e5-151">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="e95e5-151">Compliance administrator</span></span>
- <span data-ttu-id="e95e5-152">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="e95e5-152">Security administrator</span></span>
- <span data-ttu-id="e95e5-153">Lecteur Sécurité</span><span class="sxs-lookup"><span data-stu-id="e95e5-153">Security reader</span></span>

<span data-ttu-id="e95e5-154">Par ailleurs, notez que ces rapports utilisent Azure Monitor pour stocker les données dans un espace de travail journal Analytique appartenant à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e95e5-154">In addition, note these reports use Azure Monitor to store the data in a Log Analytics workspace that your organization owns.</span></span> <span data-ttu-id="e95e5-155">Par conséquent, l’utilisateur doit être ajouté en tant qu’un lecteur d’à l’espace de travail Azure surveillance que suspensions données-pour plus d’informations, voir [Autorisations nécessaires à analytique Protection Informations Azure](https://docs.microsoft.com/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span><span class="sxs-lookup"><span data-stu-id="e95e5-155">Therefore, the user should be added as a reader to the Azure Monitoring worksapce that holds the data - for more information, see [Permissions required for Azure Information Protection analytics](https://docs.microsoft.com/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span></span>

