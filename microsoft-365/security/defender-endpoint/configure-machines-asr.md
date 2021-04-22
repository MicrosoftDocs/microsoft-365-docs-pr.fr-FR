---
title: Optimiser le déploiement et les détections de règles asr
description: Optimisez vos règles de réduction de la surface d'attaque (ASR) pour identifier et empêcher les attaques de programmes malveillants classiques.
keywords: intégré, gestion Intune, Microsoft Defender pour le point de terminaison, Microsoft Defender, Windows Defender, réduction de la surface d'attaque, réduction de la surface d'attaque, réduction de la surface d'attaque, ligne de base de sécurité
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 91295135c833c6b403078bdfd517c7b84ec7d630
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51932846"
---
# <a name="optimize-asr-rule-deployment-and-detections"></a><span data-ttu-id="b4d60-104">Optimiser le déploiement et les détections de règles asr</span><span class="sxs-lookup"><span data-stu-id="b4d60-104">Optimize ASR rule deployment and detections</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b4d60-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b4d60-105">**Applies to:**</span></span>
- [<span data-ttu-id="b4d60-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4d60-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b4d60-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b4d60-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b4d60-108">Vous souhaitez faire l'expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b4d60-108">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="b4d60-109">[Inscrivez-vous à une version d'essai gratuite.](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="b4d60-109">[Sign up for a free trial](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink).</span></span>

<span data-ttu-id="b4d60-110">[Les règles de réduction de la surface](./attack-surface-reduction.md) d'attaque identifient et empêchent les attaques de programmes malveillants classiques.</span><span class="sxs-lookup"><span data-stu-id="b4d60-110">[Attack surface reduction (ASR) rules](./attack-surface-reduction.md) identify and prevent typical malware exploits.</span></span> <span data-ttu-id="b4d60-111">Ils contrôlent quand et comment du code potentiellement malveillant peut s'exécuter.</span><span class="sxs-lookup"><span data-stu-id="b4d60-111">They control when and how potentially malicious code can run.</span></span> <span data-ttu-id="b4d60-112">Par exemple, ils peuvent empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer les appels d'API Win32 à partir de macros Office et bloquer les processus qui s'exécutent à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="b4d60-112">For example, they can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, and block processes that run from USB drives.</span></span>

<span data-ttu-id="b4d60-113">![Carte de gestion de la surface d'attaque](images/secconmgmt_asr_card.png)</span><span class="sxs-lookup"><span data-stu-id="b4d60-113">![Attack surface management card](images/secconmgmt_asr_card.png)</span></span><br>
<span data-ttu-id="b4d60-114">*Carte de gestion de la surface d'attaque*</span><span class="sxs-lookup"><span data-stu-id="b4d60-114">*Attack surface management card*</span></span>

<span data-ttu-id="b4d60-115">La *carte de gestion de la surface* d'attaque est un point d'entrée vers les outils du Centre de sécurité Microsoft 365 que vous pouvez utiliser pour :</span><span class="sxs-lookup"><span data-stu-id="b4d60-115">The *Attack surface management card* is an entry point to tools in Microsoft 365 security center that you can use to:</span></span>

* <span data-ttu-id="b4d60-116">Comprendre comment les règles de la asr. sont actuellement déployées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4d60-116">Understand how ASR rules are currently deployed in your organization.</span></span>
* <span data-ttu-id="b4d60-117">Examinez les détections de la résurv et identifiez les détections éventuellement incorrectes.</span><span class="sxs-lookup"><span data-stu-id="b4d60-117">Review ASR detections and identify possible incorrect detections.</span></span>
* <span data-ttu-id="b4d60-118">Analysez l'impact des exclusions et générez la liste des chemins d'accès aux fichiers à exclure.</span><span class="sxs-lookup"><span data-stu-id="b4d60-118">Analyze the impact of exclusions and generate the list of file paths to exclude.</span></span>

<span data-ttu-id="b4d60-119">Sélectionnez **Go to attack surface management** Monitoring & reports > Attack surface reduction rules > Add  >  **exclusions**.</span><span class="sxs-lookup"><span data-stu-id="b4d60-119">Select **Go to attack surface management** > **Monitoring & reports > Attack surface reduction rules > Add exclusions**.</span></span> <span data-ttu-id="b4d60-120">À partir de là, vous pouvez accéder à d'autres sections du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b4d60-120">From there, you can navigate to other sections of Microsoft 365 security center.</span></span>

<span data-ttu-id="b4d60-121">![Onglet Ajouter des exclusions dans la page Règles de réduction de la surface d'attaque dans le Centre de sécurité Microsoft 365](images/secconmgmt_asr_m365exlusions.png)</span><span class="sxs-lookup"><span data-stu-id="b4d60-121">![Add exclusions tab in the Attack surface reduction rules page in Microsoft 365 security center](images/secconmgmt_asr_m365exlusions.png)</span></span><br>
<span data-ttu-id="b4d60-122">Onglet Ajouter des exclusions dans la page Règles de réduction de la surface d'attaque dans le Centre de sécurité *Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="b4d60-122">The ***Add exclusions** tab in the Attack surface reduction rules page in Microsoft 365 security center*</span></span>

> [!NOTE]
> <span data-ttu-id="b4d60-123">Pour accéder au Centre de sécurité Microsoft 365, vous avez besoin d'une licence Microsoft 365 E3 ou E5 et d'un compte qui a certains rôles sur Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4d60-123">To access Microsoft 365 security center, you need a Microsoft 365 E3 or E5 license and an account that has certain roles on Azure Active Directory.</span></span> <span data-ttu-id="b4d60-124">[En savoir plus sur les licences et autorisations requises.](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions)</span><span class="sxs-lookup"><span data-stu-id="b4d60-124">[Read about required licenses and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

<span data-ttu-id="b4d60-125">Pour plus d'informations sur le déploiement de règles asr dans le Centre de sécurité Microsoft 365, voir Surveiller et gérer le déploiement et les détections de règles [asr.](https://docs.microsoft.com/office365/securitycompliance/monitor-devices#monitor-and-manage-asr-rule-deployment-and-detections)</span><span class="sxs-lookup"><span data-stu-id="b4d60-125">For more information about ASR rule deployment in Microsoft 365 security center, see [Monitor and manage ASR rule deployment and detections](https://docs.microsoft.com/office365/securitycompliance/monitor-devices#monitor-and-manage-asr-rule-deployment-and-detections).</span></span>

<span data-ttu-id="b4d60-126">**Rubriques connexes**</span><span class="sxs-lookup"><span data-stu-id="b4d60-126">**Related topics**</span></span>

* [<span data-ttu-id="b4d60-127">Vérifier que vos appareils sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="b4d60-127">Ensure your devices are configured properly</span></span>](configure-machines.md)
* [<span data-ttu-id="b4d60-128">Obtenir des appareils intégrés à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4d60-128">Get devices onboarded to Microsoft Defender for Endpoint</span></span>](configure-machines-onboarding.md)
* [<span data-ttu-id="b4d60-129">Surveiller la conformité à la ligne de base de sécurité microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4d60-129">Monitor compliance to the Microsoft Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md)
