---
title: Vue d’ensemble de la protection des informations dans Windows
ms.reviewer: ''
description: En savoir plus sur le fonctionnement de la protection des informations dans Windows pour identifier et protéger les informations sensibles
keywords: information, protection, dlp, données, perte, prévention, protéger
search.product: eADQiWindows 10XVcnh
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 803c0af0c495eedfd26023d4e71d98df6a1b1b64
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51904021"
---
# <a name="information-protection-in-windows-overview"></a><span data-ttu-id="9b4ee-104">Vue d’ensemble de la protection des informations dans Windows</span><span class="sxs-lookup"><span data-stu-id="9b4ee-104">Information protection in Windows overview</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="9b4ee-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9b4ee-105">**Applies to:**</span></span>

- [<span data-ttu-id="9b4ee-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="9b4ee-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="9b4ee-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9b4ee-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="9b4ee-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="9b4ee-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="9b4ee-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="9b4ee-110">La protection des informations fait partie intégrante de la suite Microsoft 365 Entreprise, offrant une protection intelligente pour garantir la sécurité des données sensibles tout en permettant la productivité sur le lieu de travail.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-110">Information protection is an integral part of Microsoft 365 Enterprise suite, providing intelligent protection to keep sensitive data secure while enabling productivity in the workplace.</span></span>


>[!TIP]
> <span data-ttu-id="9b4ee-111">Lisez notre billet de blog sur la façon dont Microsoft Defender pour point de terminaison (anciennement appelé Microsoft Defender ATP) s'intègre à Microsoft Information Protection pour découvrir, protéger et surveiller les données sensibles sur les appareils [Windows.](https://cloudblogs.microsoft.com/microsoftsecure/2019/01/17/windows-defender-atp-integrates-with-microsoft-information-protection-to-discover-protect-and-monitor-sensitive-data-on-windows-devices/)</span><span class="sxs-lookup"><span data-stu-id="9b4ee-111">Read our blog post about how Microsoft Defender for Endpoint (formerly known as Microsoft Defender ATP) integrates with Microsoft Information Protection to [discover, protect, and monitor sensitive data on Windows devices](https://cloudblogs.microsoft.com/microsoftsecure/2019/01/17/windows-defender-atp-integrates-with-microsoft-information-protection-to-discover-protect-and-monitor-sensitive-data-on-windows-devices/).</span></span>

<span data-ttu-id="9b4ee-112">Defender pour le point de terminaison applique les méthodes suivantes pour découvrir, classifier et protéger les données :</span><span class="sxs-lookup"><span data-stu-id="9b4ee-112">Defender for Endpoint applies the following methods to discover, classify, and protect data:</span></span>

- <span data-ttu-id="9b4ee-113">**Découverte de données** : identifier les données sensibles sur les appareils Windows à risque</span><span class="sxs-lookup"><span data-stu-id="9b4ee-113">**Data discovery** - Identify sensitive data on Windows devices at risk</span></span>
- <span data-ttu-id="9b4ee-114">**Classification des** données : classifiez automatiquement les données en fonction des stratégies MIP (Microsoft Information Protection) courantes gérées dans le Centre de sécurité et conformité Office 365 &.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-114">**Data classification** - Automatically classify data based on common Microsoft Information Protection (MIP) policies managed in Office 365 Security & Compliance Center.</span></span> <span data-ttu-id="9b4ee-115">La classification automatique vous permet de protéger les données sensibles même si l'utilisateur final ne les a pas classées manuellement.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-115">Auto-classification allows you to protect sensitive data even if the end user hasn’t manually classified it.</span></span>


## <a name="data-discovery-and-data-classification"></a><span data-ttu-id="9b4ee-116">Découverte de données et classification des données</span><span class="sxs-lookup"><span data-stu-id="9b4ee-116">Data discovery and data classification</span></span>

<span data-ttu-id="9b4ee-117">Defender pour le point de terminaison découvre automatiquement les fichiers avec des étiquettes de sensibilité et les fichiers qui contiennent des types d'informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-117">Defender for Endpoint automatically discovers files with sensitivity labels and files that contain sensitive information types.</span></span>

<span data-ttu-id="9b4ee-118">Les étiquettes de sensibilité classifient et aident à protéger le contenu sensible.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-118">Sensitivity labels classify and help protect sensitive content.</span></span>

<span data-ttu-id="9b4ee-119">Les types d'informations sensibles dans l'implémentation de la protection contre la perte de données Office 365 relèvent de deux catégories :</span><span class="sxs-lookup"><span data-stu-id="9b4ee-119">Sensitive information types in the Office 365 data loss prevention (DLP) implementation fall under two categories:</span></span>

- <span data-ttu-id="9b4ee-120">Par défaut</span><span class="sxs-lookup"><span data-stu-id="9b4ee-120">Default</span></span>
- <span data-ttu-id="9b4ee-121">Personnalisé</span><span class="sxs-lookup"><span data-stu-id="9b4ee-121">Custom</span></span>

<span data-ttu-id="9b4ee-122">Les types d'informations sensibles par défaut incluent des informations telles que des numéros de compte bancaire, des numéros de sécurité sociale ou des ID nationaux.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-122">Default sensitive information types include information such as bank account numbers, social security numbers, or national IDs.</span></span> <span data-ttu-id="9b4ee-123">Pour plus d'informations, voir [ce que le type d'informations sensibles recherche.](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)</span><span class="sxs-lookup"><span data-stu-id="9b4ee-123">For more information, see [What the sensitive information type look for](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for).</span></span>

<span data-ttu-id="9b4ee-124">Les types personnalisés sont ceux que vous définissez et sont conçus pour protéger un type différent d'informations sensibles (par exemple, les ID d'employé ou les numéros de projet).</span><span class="sxs-lookup"><span data-stu-id="9b4ee-124">Custom types are ones that you define and is designed to protect a different type of sensitive information (for example, employee IDs or project numbers).</span></span> <span data-ttu-id="9b4ee-125">Pour plus d'informations, [voir Créer un type d'informations sensibles personnalisé.](https://docs.microsoft.com/office365/securitycompliance/create-a-custom-sensitive-information-type)</span><span class="sxs-lookup"><span data-stu-id="9b4ee-125">For more information see, [Create a custom sensitive information type](https://docs.microsoft.com/office365/securitycompliance/create-a-custom-sensitive-information-type).</span></span>

<span data-ttu-id="9b4ee-126">Lorsqu'un fichier est créé ou modifié sur un appareil Windows, Defender for Endpoint analyse le contenu pour évaluer s'il contient des informations sensibles.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-126">When a file is created or edited on a  Windows device, Defender for Endpoint scans the content to evaluate if it contains sensitive information.</span></span>

<span data-ttu-id="9b4ee-127">Activer l'intégration Azure Information Protection de sorte que lorsqu'un fichier contenant des informations sensibles est découvert par Defender pour le point de terminaison à l'aide d'étiquettes ou de types d'informations, il est automatiquement transmis à Azure Information Protection à partir de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-127">Turn on the Azure Information Protection integration so that when a file that contains sensitive information is discovered by Defender for Endpoint though labels or information types, it is automatically forwarded to Azure Information Protection from the device.</span></span>

![Image de la page de paramètres avec Azure Information Protection](images/atp-settings-aip.png)

<span data-ttu-id="9b4ee-129">Les signaux signalés peuvent être vus dans le tableau de bord Azure Information Protection – Data Discovery.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-129">The reported signals can be viewed on the Azure Information Protection – Data discovery dashboard.</span></span>

## <a name="azure-information-protection---data-discovery-dashboard"></a><span data-ttu-id="9b4ee-130">Azure Information Protection - Tableau de bord de découverte de données</span><span class="sxs-lookup"><span data-stu-id="9b4ee-130">Azure Information Protection - Data discovery dashboard</span></span>

<span data-ttu-id="9b4ee-131">Ce tableau de bord présente une synthèse des informations de découverte des données découvertes par Defender pour Endpoint et Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-131">This dashboard presents a summarized discovery information of data discovered by both Defender for Endpoint and Azure Information Protection.</span></span> <span data-ttu-id="9b4ee-132">Les données de Defender pour le point de terminaison sont marquées avec type d'emplacement - Point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-132">Data from Defender for Endpoint is marked with Location Type - Endpoint.</span></span>

![Image d'Azure Information Protection - Découverte de données](images/azure-data-discovery.png)

<span data-ttu-id="9b4ee-134">Notez que la colonne Risque de l'appareil sur la droite, ce risque d'appareil est dérivé directement de Defender pour point de terminaison, indiquant le niveau de risque du périphérique de sécurité où le fichier a été découvert, en fonction des menaces de sécurité actives détectées par Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-134">Notice the Device Risk column on the right, this device risk is derived directly from Defender for Endpoint, indicating the risk level of the security device where the file was discovered, based on the active security threats detected by Defender for Endpoint.</span></span>

<span data-ttu-id="9b4ee-135">Cliquez sur un appareil pour afficher la liste des fichiers observés sur cet appareil, avec leurs étiquettes de niveau de sensibilité et leurs types d'informations.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-135">Click on a device to view a list of files observed on this device, with their sensitivity labels and information types.</span></span>

>[!NOTE]
><span data-ttu-id="9b4ee-136">Veuillez prévoir environ 15 à 20 minutes pour que la découverte du tableau de bord Azure Information Protection reflète les fichiers découverts.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-136">Please allow approximately 15-20 minutes for the Azure Information Protection Dashboard Discovery to reflect discovered files.</span></span>

## <a name="log-analytics"></a><span data-ttu-id="9b4ee-137">Log Analytics</span><span class="sxs-lookup"><span data-stu-id="9b4ee-137">Log Analytics</span></span>

<span data-ttu-id="9b4ee-138">La découverte de données basée sur Defender pour le point de terminaison est également disponible dans [Azure Log Analytics,](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview)où vous pouvez effectuer des requêtes complexes sur les données brutes.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-138">Data discovery based on Defender for Endpoint is also available in [Azure Log Analytics](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview), where you can perform complex queries over the raw data.</span></span>

<span data-ttu-id="9b4ee-139">Pour plus d'informations sur l'analyse d'Azure Information Protection, voir [Rapports centraux pour Azure Information Protection.](https://docs.microsoft.com/azure/information-protection/reports-aip)</span><span class="sxs-lookup"><span data-stu-id="9b4ee-139">For more information on Azure Information Protection analytics, see [Central reporting for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/reports-aip).</span></span>

<span data-ttu-id="9b4ee-140">Ouvrez Azure Log Analytics dans le portail Azure et ouvrez un générateur de requêtes (standard ou classique).</span><span class="sxs-lookup"><span data-stu-id="9b4ee-140">Open Azure Log Analytics in Azure portal and open a query builder (standard or classic).</span></span>

<span data-ttu-id="9b4ee-141">Pour afficher les données de Defender for Endpoint, effectuez une requête qui contient :</span><span class="sxs-lookup"><span data-stu-id="9b4ee-141">To view Defender for Endpoint data, perform a query that contains:</span></span>

```
InformationProtectionLogs_CL
| where Workload_s == "Windows Defender"
```

<span data-ttu-id="9b4ee-142">**Conditions préalables :**</span><span class="sxs-lookup"><span data-stu-id="9b4ee-142">**Prerequisites:**</span></span>

- <span data-ttu-id="9b4ee-143">Les clients doivent avoir un abonnement à Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-143">Customers must have a subscription for Azure Information Protection.</span></span>
- <span data-ttu-id="9b4ee-144">Activez l'intégration d'Azure Information Protection dans le Centre de sécurité Microsoft Defender :</span><span class="sxs-lookup"><span data-stu-id="9b4ee-144">Enable Azure Information Protection integration in Microsoft Defender Security Center:</span></span>
    - <span data-ttu-id="9b4ee-145">Go to **Settings** in Microsoft Defender Security Center, click on **Advanced Settings** under **General**.</span><span class="sxs-lookup"><span data-stu-id="9b4ee-145">Go to **Settings** in Microsoft Defender Security Center, click on **Advanced Settings** under **General**.</span></span>



