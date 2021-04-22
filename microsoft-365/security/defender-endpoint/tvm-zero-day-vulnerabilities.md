---
title: 'Atténuer les vulnérabilités du jour zéro : gestion des menaces et des vulnérabilités'
description: Découvrez comment rechercher et atténuer les vulnérabilités « zero-day » dans votre environnement par le biais de la gestion des menaces et des vulnérabilités.
keywords: Microsoft Defender pour endpoint tvm zero day vulnerabilities, tvm, threat & vulnerability management, zero day, 0-day, mitigate 0 day vulnerabilities, vulnerable CVE
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: be508e646a67f01887814a0e72170e438ee86212
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51933060"
---
# <a name="mitigate-zero-day-vulnerabilities---threat-and-vulnerability-management"></a><span data-ttu-id="cb4f5-104">Atténuer les vulnérabilités du jour zéro : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="cb4f5-104">Mitigate zero-day vulnerabilities - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="cb4f5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cb4f5-105">**Applies to:**</span></span>

- [<span data-ttu-id="cb4f5-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="cb4f5-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="cb4f5-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="cb4f5-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="cb4f5-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cb4f5-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="cb4f5-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="cb4f5-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="cb4f5-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="cb4f5-111">Une vulnérabilité « zero-day » est une vulnérabilité publiquement divulguée pour laquelle aucune mise à jour de sécurité ou correctifs officiels n'a été publié.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-111">A zero-day vulnerability is a publicly disclosed vulnerability for which no official patches or security updates have been released.</span></span> <span data-ttu-id="cb4f5-112">Les vulnérabilités du jour zéro ont souvent des niveaux de gravité élevés et sont activement exploitées.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-112">Zero-day vulnerabilities often have high severity levels and are actively exploited.</span></span>

<span data-ttu-id="cb4f5-113">La gestion des menaces et des vulnérabilités affiche uniquement les vulnérabilités du jour zéro dont elle dispose d'informations.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-113">Threat and vulnerability management will only display zero-day vulnerabilities it has information about.</span></span>

## <a name="find-information-about-zero-day-vulnerabilities"></a><span data-ttu-id="cb4f5-114">Trouver des informations sur les vulnérabilités du jour zéro</span><span class="sxs-lookup"><span data-stu-id="cb4f5-114">Find information about zero-day vulnerabilities</span></span>

<span data-ttu-id="cb4f5-115">Une fois qu'une vulnérabilité zéro jour a été trouvée, les informations à ce sujet sont transmises via les expériences suivantes dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-115">Once a zero-day vulnerability has been found, information about it will be conveyed through the following experiences in the Microsoft Defender Security Center.</span></span>

### <a name="threat-and-vulnerability-management-dashboard"></a><span data-ttu-id="cb4f5-116">Tableau de bord de gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="cb4f5-116">Threat and vulnerability management dashboard</span></span>

<span data-ttu-id="cb4f5-117">Recherchez des recommandations avec une balise « zero-day » dans la carte « Recommandations de sécurité les plus importantes ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-117">Look for recommendations with a zero-day tag in the “Top security recommendations” card.</span></span>

![Recommandations les plus importantes avec une balise « zero-day ».](images/tvm-zero-day-top-security-recommendations.png)

<span data-ttu-id="cb4f5-119">Recherchez les principaux logiciels avec la balise « zero-day » dans la carte « Logiciels les plus vulnérables ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-119">Find top software with the zero-day tag in the "Top vulnerable software" card.</span></span>

![Logiciels les plus vulnérables avec une balise « zero-day ».](images/tvm-zero-day-top-software.png)

### <a name="weaknesses-page"></a><span data-ttu-id="cb4f5-121">Page Faiblesses</span><span class="sxs-lookup"><span data-stu-id="cb4f5-121">Weaknesses page</span></span>

<span data-ttu-id="cb4f5-122">Recherchez la vulnérabilité nommée « zero-day » ainsi qu'une description et des détails.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-122">Look for the named zero-day vulnerability along with a description and details.</span></span>

- <span data-ttu-id="cb4f5-123">Si un ID CVE est affecté à cette vulnérabilité, vous verrez l'étiquette « zero-day » en regard du nom CVE.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-123">If this vulnerability has a CVE-ID assigned, you’ll see the zero-day label next to the CVE name.</span></span>

- <span data-ttu-id="cb4f5-124">Si aucun ID CVE n’est affecté à cette vulnérabilité, vous la trouverez sous un nom interne temporaire qui ressemble à « TVM-XXXX-XXXX ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-124">If this vulnerability has no CVE-ID assigned, you'll find it under an internal, temporary name that looks like “TVM-XXXX-XXXX”.</span></span> <span data-ttu-id="cb4f5-125">Le nom sera mis à jour une fois qu’un ID CVE officiel a été affecté, mais le nom interne précédent peut toujours être recherché et trouvé dans le panneau latéral.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-125">The name will be updated once an official CVE-ID has been assigned, but the previous internal name will still be searchable and found in the side-panel.</span></span>

![Exemple de jour zéro pour CVE-2020-17087 dans la page faiblesses.](images/tvm-zero-day-weakness-name.png)

### <a name="software-inventory-page"></a><span data-ttu-id="cb4f5-127">Page Inventaire logiciel</span><span class="sxs-lookup"><span data-stu-id="cb4f5-127">Software inventory page</span></span>

<span data-ttu-id="cb4f5-128">Recherchez des logiciels avec la balise « zero-day ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-128">Look for software with the zero-day tag.</span></span> <span data-ttu-id="cb4f5-129">Filtrez par la balise « zero day » pour voir uniquement les logiciels avec des vulnérabilités zero-day.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-129">Filter by the "zero day" tag to only see software with zero-day vulnerabilities.</span></span>

![Exemple zero day de Windows Server 2016 dans la page d’inventaire logiciel.](images/tvm-zero-day-software-inventory.png)

### <a name="software-page"></a><span data-ttu-id="cb4f5-131">Page de logiciels</span><span class="sxs-lookup"><span data-stu-id="cb4f5-131">Software page</span></span>

<span data-ttu-id="cb4f5-132">Recherchez une balise zero-day pour chaque logiciel affecté par la vulnérabilité zero-day.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-132">Look for a zero-day tag for each software that has been affected by the zero–day vulnerability.</span></span>

![Exemple de jour zéro pour la page du logiciel Windows Server 2016.](images/tvm-zero-day-software-page.png)

### <a name="security-recommendations-page"></a><span data-ttu-id="cb4f5-134">Page Recommandations en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="cb4f5-134">Security recommendations page</span></span>

<span data-ttu-id="cb4f5-135">Affichez des suggestions claires sur les options de correction et d’atténuation, y compris les solutions de contournement si elles existent.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-135">View clear suggestions about remediation and mitigation options, including workarounds if they exist.</span></span> <span data-ttu-id="cb4f5-136">Filtrez par balise « zero day » pour voir uniquement les recommandations de sécurité concernant les vulnérabilités « zero-day ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-136">Filter by the "zero day" tag to only see security recommendations addressing zero-day vulnerabilities.</span></span>

<span data-ttu-id="cb4f5-137">S’il existe un logiciel avec une vulnérabilité zéro jour et des vulnérabilités supplémentaires à résoudre, vous recevrez une recommandation sur toutes les vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-137">If there's software with a zero-day vulnerability and additional vulnerabilities to address, you'll get one recommendation about all vulnerabilities.</span></span>

![Exemple zero day de Windows Server 2016 dans la page recommandations de sécurité.](images/tvm-zero-day-security-recommendation.png)

## <a name="addressing-zero-day-vulnerabilities"></a><span data-ttu-id="cb4f5-139">Résoudre les vulnérabilités du jour zéro</span><span class="sxs-lookup"><span data-stu-id="cb4f5-139">Addressing zero-day vulnerabilities</span></span>

<span data-ttu-id="cb4f5-140">Go to the security recommendation page and select a recommendation with a zero-day.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-140">Go to the security recommendation page and select a recommendation with a zero-day.</span></span> <span data-ttu-id="cb4f5-141">Un flyout s’ouvre avec des informations sur le jour zéro et d’autres vulnérabilités pour ce logiciel.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-141">A flyout will open with information about the zero-day and other vulnerabilities for that software.</span></span>

<span data-ttu-id="cb4f5-142">Il y aura un lien vers les options d’atténuation et les solutions de contournement si elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-142">There will be a link to mitigation options and workarounds if they are available.</span></span> <span data-ttu-id="cb4f5-143">Les solutions de contournement peuvent aider à réduire les risques posés par cette vulnérabilité zero-day jusqu’à ce qu’un correctif ou une mise à jour de sécurité puisse être déployé.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-143">Workarounds may help reduce the risk posed by this zero-day vulnerability until a patch or security update can be deployed.</span></span>

<span data-ttu-id="cb4f5-144">Ouvrez les options de correction et choisissez le type d'attention.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-144">Open remediation options and choose the attention type.</span></span> <span data-ttu-id="cb4f5-145">Une option de correction « attention requise » est recommandée pour les vulnérabilités du jour zéro, dans la mesure où une mise à jour n'a pas encore été publiée.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-145">An "attention required" remediation option is recommended for the zero-day vulnerabilities, since an update hasn't been released yet.</span></span> <span data-ttu-id="cb4f5-146">Vous ne pourrez pas sélectionner une date d'échéance, car aucune action spécifique n'est à effectuer.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-146">You won't be able to select a due date, since there's no specific action to perform.</span></span> <span data-ttu-id="cb4f5-147">S'il existe des vulnérabilités plus anciennes pour ce logiciel que vous souhaitez mettre à jour, vous pouvez remplacer l'option de correction « Attention requise » et choisir « mettre à jour ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-147">If there are older vulnerabilities for this software you wish to remediation, you can override the "attention required" remediation option and choose “update.”</span></span>

![Exemple de flyout zero day de Windows Server 2016 dans la page recommandations de sécurité.](images/tvm-zero-day-recommendation-flyout400.png)

## <a name="track-zero-day-remediation-activities"></a><span data-ttu-id="cb4f5-149">Suivre les activités de correction du jour zéro</span><span class="sxs-lookup"><span data-stu-id="cb4f5-149">Track zero-day remediation activities</span></span>

<span data-ttu-id="cb4f5-150">Go to the threat and vulnerability management [Remediation](tvm-remediation.md) page to view the remediation activity item.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-150">Go to the threat and vulnerability management [Remediation](tvm-remediation.md) page to view the remediation activity item.</span></span> <span data-ttu-id="cb4f5-151">Si vous avez choisi l'option de correction « Attention requise », il n'y aura aucune barre de progression, état du ticket ou date d'échéance, car il n'existe aucune action réelle que nous pouvons surveiller.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-151">If you chose the "attention required" remediation option, there will be no progress bar, ticket status, or due date since there's no actual action we can monitor.</span></span> <span data-ttu-id="cb4f5-152">Vous pouvez filtrer par type de correction, par exemple « mise à jour logicielle » ou « attention requise », pour voir tous les éléments d'activité dans la même catégorie.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-152">You can filter by remediation type, such as "software update" or "attention required," to see all activity items in the same category.</span></span>

## <a name="patching-zero-day-vulnerabilities"></a><span data-ttu-id="cb4f5-153">Correction des vulnérabilités du jour zéro</span><span class="sxs-lookup"><span data-stu-id="cb4f5-153">Patching zero-day vulnerabilities</span></span>

<span data-ttu-id="cb4f5-154">Lorsqu'un correctif est publié pour le jour zéro, la recommandation est modifiée en « Mise à jour » et une étiquette bleue en plus de celle-ci indique « Nouvelle mise à jour de sécurité pour le jour zéro ».</span><span class="sxs-lookup"><span data-stu-id="cb4f5-154">When a patch is released for the zero-day, the recommendation will be changed to “Update” and a blue label next to it that says “New security update for zero day.”</span></span> <span data-ttu-id="cb4f5-155">Il ne sera plus considérer comme un jour zéro, la balise « zero-day » sera supprimée de toutes les pages.</span><span class="sxs-lookup"><span data-stu-id="cb4f5-155">It will no longer consider as a zero-day, the zero-day tag will be removed from all pages.</span></span>

![Recommandation pour « Mettre à jour Microsoft Windows 10 » avec une nouvelle étiquette de correctif.](images/tvm-zero-day-patch.jpg)

## <a name="related-articles"></a><span data-ttu-id="cb4f5-157">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="cb4f5-157">Related articles</span></span>

- [<span data-ttu-id="cb4f5-158">Vue d'ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="cb4f5-158">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="cb4f5-159">Tableau de bord</span><span class="sxs-lookup"><span data-stu-id="cb4f5-159">Dashboard</span></span>](tvm-dashboard-insights.md)
- [<span data-ttu-id="cb4f5-160">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="cb4f5-160">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="cb4f5-161">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="cb4f5-161">Software inventory</span></span>](tvm-software-inventory.md)
- [<span data-ttu-id="cb4f5-162">Les vulnérabilités dans mon organisation</span><span class="sxs-lookup"><span data-stu-id="cb4f5-162">Vulnerabilities in my organization</span></span>](tvm-weaknesses.md)
