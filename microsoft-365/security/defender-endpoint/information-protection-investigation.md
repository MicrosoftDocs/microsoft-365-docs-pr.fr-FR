---
title: Utiliser des étiquettes de niveau de sensibilité pour hiérarchiser la réponse aux incidents
description: Découvrez comment utiliser des étiquettes de niveau de sensibilité pour hiérarchiser et examiner les incidents
keywords: informations, protection, données, perte, prévention, étiquettes, dlp, incident, examiner, examen
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: bff490edcc79bc8f96e65c8b27586ca8b54e5bce
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51186124"
---
# <a name="use-sensitivity-labels-to-prioritize-incident-response"></a><span data-ttu-id="15330-104">Utiliser des étiquettes de niveau de sensibilité pour hiérarchiser la réponse aux incidents</span><span class="sxs-lookup"><span data-stu-id="15330-104">Use sensitivity labels to prioritize incident response</span></span>  

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="15330-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="15330-105">**Applies to:**</span></span>
- [<span data-ttu-id="15330-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="15330-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="15330-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="15330-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="15330-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="15330-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="15330-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="15330-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


<span data-ttu-id="15330-110">Un cycle de vie classique des menaces avancées persistantes implique l’exfiltration des données.</span><span class="sxs-lookup"><span data-stu-id="15330-110">A typical advanced persistent threat lifecycle involves data exfiltration.</span></span> <span data-ttu-id="15330-111">Dans un incident de sécurité, il est important de pouvoir hiérarchiser les enquêtes dans les cas où les fichiers sensibles peuvent être insécurisés afin que les données et les informations d’entreprise soient protégées.</span><span class="sxs-lookup"><span data-stu-id="15330-111">In a security incident, it's important to have the ability to prioritize investigations where sensitive files may be jeopardy so that corporate data and information are protected.</span></span>

<span data-ttu-id="15330-112">Defender pour le point de terminaison facilite la hiérquisation des incidents de sécurité avec l’utilisation d’étiquettes de niveau de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="15330-112">Defender for Endpoint helps to make the prioritization of security incidents much simpler with the use of sensitivity labels.</span></span> <span data-ttu-id="15330-113">Les étiquettes de confidentialité identifient rapidement les incidents qui peuvent impliquer des appareils avec des informations sensibles telles que des informations confidentielles.</span><span class="sxs-lookup"><span data-stu-id="15330-113">Sensitivity labels quickly identify incidents that may involve devices with sensitive information such as confidential information.</span></span> 

## <a name="investigate-incidents-that-involve-sensitive-data"></a><span data-ttu-id="15330-114">Examiner les incidents impliquant des données sensibles</span><span class="sxs-lookup"><span data-stu-id="15330-114">Investigate incidents that involve sensitive data</span></span>
<span data-ttu-id="15330-115">Découvrez comment utiliser des étiquettes de sensibilité aux données pour hiérarchiser l’examen des incidents.</span><span class="sxs-lookup"><span data-stu-id="15330-115">Learn how to use data sensitivity labels to prioritize incident investigation.</span></span>

>[!NOTE]
><span data-ttu-id="15330-116">Les étiquettes sont détectées pour Windows 10, version 1809 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="15330-116">Labels are detected for Windows 10, version 1809 or later.</span></span>

1. <span data-ttu-id="15330-117">Dans le Centre de sécurité Microsoft Defender, sélectionnez **Incidents.**</span><span class="sxs-lookup"><span data-stu-id="15330-117">In Microsoft Defender Security Center, select **Incidents**.</span></span> 

2. <span data-ttu-id="15330-118">Faites défiler vers la droite pour voir la colonne **Sensibilité aux** données.</span><span class="sxs-lookup"><span data-stu-id="15330-118">Scroll to the right to see the **Data sensitivity** column.</span></span> <span data-ttu-id="15330-119">Cette colonne reflète les étiquettes de niveau de sensibilité observées sur les appareils liés aux incidents, ce qui indique si les fichiers sensibles peuvent être touchés par l’incident.</span><span class="sxs-lookup"><span data-stu-id="15330-119">This column reflects sensitivity labels that have been observed on devices related to the incidents providing an indication of whether sensitive files may be impacted by the incident.</span></span>

    ![Image de la colonne de sensibilité des données](images/data-sensitivity-column.png)

    <span data-ttu-id="15330-121">Vous pouvez également filtrer en fonction du **niveau de sensibilité des données**</span><span class="sxs-lookup"><span data-stu-id="15330-121">You can also filter based on **Data sensitivity**</span></span> 

    ![Image du filtre de sensibilité des données](images/data-sensitivity-filter.png)

3. <span data-ttu-id="15330-123">Ouvrez la page incident pour examiner plus en détail.</span><span class="sxs-lookup"><span data-stu-id="15330-123">Open the incident page to further investigate.</span></span>

    ![Image des détails de la page d’incident](images/incident-page.png)

4. <span data-ttu-id="15330-125">Sélectionnez **l’onglet Appareils** pour identifier les appareils stockant des fichiers avec des étiquettes de sensibilité.</span><span class="sxs-lookup"><span data-stu-id="15330-125">Select the **Devices** tab to identify devices storing files with sensitivity labels.</span></span>

    ![Image de l’onglet de l’appareil](images/investigate-devices-tab.png)
   

5. <span data-ttu-id="15330-127">Sélectionnez les appareils qui stockent des données sensibles et recherchez dans la chronologie pour identifier les fichiers qui peuvent être touchés, puis prenez les mesures appropriées pour vous assurer que les données sont protégées.</span><span class="sxs-lookup"><span data-stu-id="15330-127">Select the devices that store sensitive data and search through the timeline to identify which files may be impacted then take appropriate action to ensure that data is protected.</span></span> 

   <span data-ttu-id="15330-128">Vous pouvez affiner les événements affichés sur la chronologie de l’appareil en recherchant des étiquettes de sensibilité aux données.</span><span class="sxs-lookup"><span data-stu-id="15330-128">You can narrow down the events shown on the device timeline by searching for data sensitivity labels.</span></span> <span data-ttu-id="15330-129">Cela n’affichera que les événements associés aux fichiers qui ont ce nom d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="15330-129">Doing this will show only events associated with files that have said label name.</span></span>

    ![Image de la chronologie de l’appareil avec des résultats de recherche restreints en fonction de l’étiquette](images/machine-timeline-labels.png)


>[!TIP]
><span data-ttu-id="15330-131">Ces points de données sont également exposés par le biais de « DeviceFileEvents » dans le repérage avancé, ce qui permet aux requêtes avancées et à la détection de planifier la détection de prendre en compte les étiquettes de sensibilité et l’état de protection des fichiers.</span><span class="sxs-lookup"><span data-stu-id="15330-131">These data points are also exposed through the ‘DeviceFileEvents’ in advanced hunting, allowing advanced queries and schedule detection to take into account sensitivity labels and file protection status.</span></span> 
