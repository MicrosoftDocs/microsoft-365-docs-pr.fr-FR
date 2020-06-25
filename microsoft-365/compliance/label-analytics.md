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
ms.custom:
- seo-marvel-apr2020
description: Découvrez comment identifier rapidement les étiquettes de rétention et les étiquettes de confidentialité utilisées le plus souvent et l’endroit où elles sont appliquées.
ms.openlocfilehash: 89ccdce54b0d7e6146260037b8dcb085631b408e
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44817503"
---
# <a name="view-label-usage-with-label-analytics"></a><span data-ttu-id="cb3e1-103">Afficher l’utilisation d’étiquette grâce à la page Analyse des étiquettes</span><span class="sxs-lookup"><span data-stu-id="cb3e1-103">View label usage with label analytics</span></span>

<span data-ttu-id="cb3e1-104">Après avoir créé vos étiquettes de rétention et vos étiquettes de sensibilité, vous souhaiterez voir comment ils sont utilisés au sein de votre client.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-104">After you create your retention labels and sensitivity labels, you’ll want to see how they’re being used across your tenant.</span></span> <span data-ttu-id="cb3e1-105">Les portails Centre de conformité Microsoft 365 et Centre de sécurité Microsoft 365 sont dotés d’une page intitulée Analyse des étiquettes. Elle indique les étiquettes les plus utilisées et leurs types d’applications.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-105">With label analytics in the Microsoft 365 compliance center and Microsoft 365 security center, you can quickly see which labels are used the most and where they’re being applied.</span></span>

<span data-ttu-id="cb3e1-106">Par exemple, avec analytique étiquette, vous pouvez afficher:</span><span class="sxs-lookup"><span data-stu-id="cb3e1-106">For example, with label analytics, you can view the:</span></span>

- <span data-ttu-id="cb3e1-107">Le nombre total de rétention étiquettes et les étiquettes de sensibilité appliquées au contenu.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-107">Total number of retention labels and sensitivity labels applied to content.</span></span>
- <span data-ttu-id="cb3e1-108">Les étiquettes supérieures et le nombre de compte pour lequel chaque étiquette a été appliquée.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-108">Top labels and the count of how many times each label was applied.</span></span>
- <span data-ttu-id="cb3e1-109">Les emplacements où les étiquettes sont appliquées et le nombre pour chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-109">Locations where labels are applied and the count for each location.</span></span>
- <span data-ttu-id="cb3e1-110">Compter le nombre de fichiers et des dossiers pour lesquels l’étiquette de rétention a été modifiée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-110">Count for how many files and folders had their retention label changed or removed.</span></span>

<span data-ttu-id="cb3e1-111">Vous trouverez analytique étiquette dans la [centre de conformité de Microsoft 365](https://compliance.microsoft.com/labelanalytics) ou [centre de sécurité Microsoft 365](https://security.microsoft.com/labelanalytics) > **Classification**  >  \*\* Étiquettes analytique\*\*.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-111">You can find label analytics in the [Microsoft 365 compliance center](https://compliance.microsoft.com/labelanalytics) or [Microsoft 365 security center](https://security.microsoft.com/labelanalytics) > **Classification** > **Label analytics**.</span></span>

![Page analytique étiquette](../media/label-analytics-page.png)

## <a name="sensitivity-label-usage"></a><span data-ttu-id="cb3e1-113">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="cb3e1-113">Sensitivity label usage</span></span>

<span data-ttu-id="cb3e1-114">Les données sur l’utilisation de la sensibilité étiquette sont extraite des rapports pour Azure Information Protection-pour plus d’informations, voir [Central de création de rapports de Protection Informations Azure](https://docs.microsoft.com/azure/information-protection/reports-aip).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-114">The data on sensitivity label usage is pulled from the reports for Azure Information Protection – for more information, see [Central reporting for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/reports-aip).</span></span>

<span data-ttu-id="cb3e1-115">Notez que les rapports de Protection d’Informations Azure Information ont des[conditions préalables](/azure/information-protection/reports-aip#prerequisites) qui s’appliquent également à l’analytique d’étiquette sur les étiquettes de niveau de confidentialité dans le centre de conformité de Microsoft 365 et centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-115">Note that the Azure Information Protection reports have [prerequisites](/azure/information-protection/reports-aip#prerequisites) that also apply to label analytics on sensitivity labels in the Microsoft 365 compliance center and Microsoft 365 security center.</span></span> <span data-ttu-id="cb3e1-116">Par exemple, vous avez besoin d’un abonnement Azure qui inclut le journal Analytique, car ces rapports sont le résultat de l’envoi d’informations d’événements d’audit d’une protection à partir de scanneurs et Azure Information Protection clients vers un emplacement centralisé basé sur Azure journal Service Analytique.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-116">For example, you need an Azure subscription that includes the Log Analytics because these reports are a result of sending information protection audit events from Azure Information Protection clients and scanners to a centralized location based on Azure Log Analytics service.</span></span>

<span data-ttu-id="cb3e1-117">Usage d’étiquettes de niveau de confidentialité:</span><span class="sxs-lookup"><span data-stu-id="cb3e1-117">For sensitivity label usage:</span></span>

- <span data-ttu-id="cb3e1-118">Il n’existe aucune latence dans les données.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-118">There is no latency in the data.</span></span> <span data-ttu-id="cb3e1-119">Il s’agit d’un rapport en temps réel.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-119">This is a real-time report.</span></span>
- <span data-ttu-id="cb3e1-120">Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-120">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="cb3e1-121">Le rapport indique où les étiquettes de niveau de confidentialité sont appliquées par application (tandis que les étiquettes de rétention sont affichées par emplacement).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-121">The report shows where sensitivity labels are applied per app (whereas retention labels are shown per location).</span></span>

![Rapport d’usage d’étiquettes de niveau de confidentialité](../media/sensitivity-label-usage-report.png)

## <a name="retention-label-usage"></a><span data-ttu-id="cb3e1-123">Usage d’étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="cb3e1-123">Retention label usage</span></span>

<span data-ttu-id="cb3e1-124">Ce rapport affiche un aperçu rapide de ce que sont les étiquettes supérieures et où elles sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-124">This report shows a quick view of what the top labels are and where they’re applied.</span></span> <span data-ttu-id="cb3e1-125">Pour plus d’informations sur l’intitulé de contenu dans SharePoint et OneDrive, voir [Afficher l’activité des étiquettes pour les documents](view-label-activity-for-documents.md).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-125">For more detailed information on how content in SharePoint and OneDrive is labeled, see [View label activity for documents](view-label-activity-for-documents.md).</span></span>

<span data-ttu-id="cb3e1-126">Usage d’étiquette de rétention:</span><span class="sxs-lookup"><span data-stu-id="cb3e1-126">For retention label usage:</span></span>

- <span data-ttu-id="cb3e1-127">Les données sont regroupées de manière hebdomadaire, aussi cela peut prendre jusqu'à sept jours pour que les données s’affichent dans le rapport.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-127">Data is aggregated weekly, so it may take up to seven days for data to appear in the report.</span></span>
- <span data-ttu-id="cb3e1-128">Pour afficher le nombre de chaque étiquette supérieure, pointez sur le graphique à barres et lire l’info-bulle qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-128">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="cb3e1-129">Le rapport indique où les étiquettes de rétention sont appliquées par emplacement (tandis que les étiquettes de sensibilité sont affichées par application).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-129">The report shows where retention labels are applied per location (whereas sensitivity labels are shown per app).</span></span>
- <span data-ttu-id="cb3e1-130">Pour les étiquettes de rétention, il s’agit d’une synthèse des données à tout-moment dans votre client ; elles ne sont pas filtrées pour une plage de dates spécifique.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-130">For retention labels, this is a summary of the all-time data in your tenant; it’s not filtered to a specific date range.</span></span> <span data-ttu-id="cb3e1-131">En revanche, l’[étiquette d’activité Explorer](view-label-activity-for-documents.md) affiche les données 30 derniers jours uniquement.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-131">By contrast, the [Label Activity Explorer](view-label-activity-for-documents.md) shows data from only the past 30 days.</span></span>

![Rapport d’usage d’étiquette de rétention](../media/retention-label-usage-report.png)

## <a name="view-all-content-with-a-specific-retention-label"></a><span data-ttu-id="cb3e1-133">Afficher tout le contenu portant une étiquette de rétention spécifique</span><span class="sxs-lookup"><span data-stu-id="cb3e1-133">View all content with a specific retention label</span></span>

<span data-ttu-id="cb3e1-134">Dans le rapport d’utilisation d’étiquette de rétention, vous pouvez rapidement explorer tout le contenu associé à cette étiquette appliquée.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-134">From the retention label usage report, you can quickly explore all content with that label applied.</span></span> <span data-ttu-id="cb3e1-135">(Notez que nous travaillons actuellement sur cette fonctionnalité, afin que le processus prenne plus d’étapes pour afficher tout le contenu étiqueté).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-135">(Note that we're currently working on this feature, so that it will take fewer steps to view all the labeled content.)</span></span>

<span data-ttu-id="cb3e1-136">Tout d’abord, choisissez **Afficher les détails** en bas du rapport.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-136">First, choose **View Details** at the bottom of the report.</span></span>

![Option Afficher les détails en bas de rapport d’utilisation d’étiquette de rétention](../media/retention-label-usage-view-details.png)

<span data-ttu-id="cb3e1-138">Puis choisissez une étiquette de rétention > **Explorer les éléments** dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-138">Then choose a retention label > **Explore items** in the right pane.</span></span>

![Explorer l’option éléments dans le volet droit](../media/retention-label-usage-explore-items.png)

<span data-ttu-id="cb3e1-140">Pour cette étiquette, vous pouvez choisir l’onglet**activité**pour consulter un nombre d’éléments associé à cette étiquette selon l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-140">For that label, you can choose the **Activity** tab to view a count of items with that label by location.</span></span>

![Onglet activité pour une étiquette de rétention](../media/retention-label-usage-activity-tab.png)

<span data-ttu-id="cb3e1-142">Vous pouvez également choisir l’onglet**éléments avec cette étiquette**. Ensuite, vous pouvez explorer des emplacements spécifiques :</span><span class="sxs-lookup"><span data-stu-id="cb3e1-142">You can also choose the **Items with this label** tab. Then you can drill into specific locations:</span></span>

- <span data-ttu-id="cb3e1-143">Pour Exchange Online, consultez la liste de boîtes aux lettres avec le nombre d’éléments étiquetés dans chaque boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-143">For Exchange Online, you see a list of mailboxes with the count of labeled items in each mailbox.</span></span>
- <span data-ttu-id="cb3e1-144">Pour SharePoint Online et OneDrive Entreprise, vous voyez une liste de collections de sites et les comptes OneDrive avec le nombre d’éléments étiquetés dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-144">For SharePoint Online and OneDrive for Business, you see a list of site collections and OneDrive accounts with the count of labeled items in each location.</span></span>

<span data-ttu-id="cb3e1-145">Lorsque vous choisissez une collection de boîte aux lettres ou un site, vous pouvez afficher une liste d’éléments associé à cette étiquette rétention dans cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-145">When you choose a mailbox or site collection, you can view a list of items with that retention label in that location.</span></span>

![Les éléments de cet onglet d’étiquette affichant tous les éléments comportant cette étiquette rétention](../media/retention-label-usage-content-explorer.png)

## <a name="permissions"></a><span data-ttu-id="cb3e1-147">Autorisations</span><span class="sxs-lookup"><span data-stu-id="cb3e1-147">Permissions</span></span>

<span data-ttu-id="cb3e1-148">Pour afficher analytique étiquette, vous devez être affecté parmi les rôles suivants dans Azure Active Directory :</span><span class="sxs-lookup"><span data-stu-id="cb3e1-148">To view label analytics, you must be assigned one of the following roles in Azure Active Directory:</span></span>

- <span data-ttu-id="cb3e1-149">Administrateur général</span><span class="sxs-lookup"><span data-stu-id="cb3e1-149">Global administrator</span></span>
- <span data-ttu-id="cb3e1-150">Administrateur de conformité</span><span class="sxs-lookup"><span data-stu-id="cb3e1-150">Compliance administrator</span></span>
- <span data-ttu-id="cb3e1-151">Administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="cb3e1-151">Security administrator</span></span>
- <span data-ttu-id="cb3e1-152">Lecteur Sécurité</span><span class="sxs-lookup"><span data-stu-id="cb3e1-152">Security reader</span></span>

<span data-ttu-id="cb3e1-153">Par ailleurs, notez que ces rapports utilisent Azure Monitor pour stocker les données dans un espace de travail journal Analytique appartenant à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb3e1-153">In addition, note these reports use Azure Monitor to store the data in a Log Analytics workspace that your organization owns.</span></span> <span data-ttu-id="cb3e1-154">Par conséquent, l’utilisateur doit être ajouté en tant que lecteur à l’espace de travail Azure Monitor qui détient les données. Pour plus d’informations, voir [Autorisations nécessaires pour les analyses Azure Information Protection](https://docs.microsoft.com/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span><span class="sxs-lookup"><span data-stu-id="cb3e1-154">Therefore, the user should be added as a reader to the Azure Monitoring workspace that holds the data - for more information, see [Permissions required for Azure Information Protection analytics](https://docs.microsoft.com/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span></span>

