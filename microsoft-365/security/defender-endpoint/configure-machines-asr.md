---
title: Optimiser le déploiement et les détections de règles asr
description: Optimisez vos règles de réduction de la surface d’attaque (ASR) pour identifier et empêcher les attaques de programmes malveillants classiques.
keywords: intégration, gestion Intune, Microsoft Defender pour le point de terminaison, Microsoft Defender, Windows Defender, réduction de la surface d’attaque, réduction de la surface d’attaque, réduction de la surface d’attaque, ligne de base de sécurité
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
ms.openlocfilehash: a5590e62e7838bb9f611320b6d0e5c573b2be084
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841557"
---
# <a name="optimize-asr-rule-deployment-and-detections"></a><span data-ttu-id="2fdb6-104">Optimiser le déploiement et les détections de règles asr</span><span class="sxs-lookup"><span data-stu-id="2fdb6-104">Optimize ASR rule deployment and detections</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="2fdb6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2fdb6-105">**Applies to:**</span></span>
- [<span data-ttu-id="2fdb6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2fdb6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="2fdb6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2fdb6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="2fdb6-108">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="2fdb6-108">Want to experience Defender for Endpoint?</span></span> <span data-ttu-id="2fdb6-109">[Inscrivez-vous à une version d’essai gratuite.](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-109">[Sign up for a free trial](https://www.microsoft.com/en-us/WindowsForBusiness/windows-atp?ocid=docs-wdatp-onboardconfigure-abovefoldlink).</span></span>

<span data-ttu-id="2fdb6-110">[Les règles de réduction de la surface](./attack-surface-reduction.md) d’attaque identifient et empêchent les attaques de programmes malveillants classiques.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-110">[Attack surface reduction (ASR) rules](./attack-surface-reduction.md) identify and prevent typical malware exploits.</span></span> <span data-ttu-id="2fdb6-111">Ils contrôlent quand et comment du code potentiellement malveillant peut s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-111">They control when and how potentially malicious code can run.</span></span> <span data-ttu-id="2fdb6-112">Par exemple, ils peuvent empêcher JavaScript ou VBScript de lancer un exécutable téléchargé, bloquer les appels d’API Win32 à partir de macros Office et bloquer les processus qui s’exécutent à partir de lecteurs USB.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-112">For example, they can prevent JavaScript or VBScript from launching a downloaded executable, block Win32 API calls from Office macros, and block processes that run from USB drives.</span></span>

<span data-ttu-id="2fdb6-113">![Carte de gestion de la surface d’attaque](images/secconmgmt_asr_card.png)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-113">![Attack surface management card](images/secconmgmt_asr_card.png)</span></span><br>
<span data-ttu-id="2fdb6-114">*Carte de gestion de la surface d’attaque*</span><span class="sxs-lookup"><span data-stu-id="2fdb6-114">*Attack surface management card*</span></span>

<span data-ttu-id="2fdb6-115">La *carte de gestion de la surface* d’attaque est un point d’entrée des outils Microsoft 365 centre de sécurité que vous pouvez utiliser pour :</span><span class="sxs-lookup"><span data-stu-id="2fdb6-115">The *Attack surface management card* is an entry point to tools in Microsoft 365 security center that you can use to:</span></span>

* <span data-ttu-id="2fdb6-116">Comprendre comment les règles de la asr. sont actuellement déployées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-116">Understand how ASR rules are currently deployed in your organization.</span></span>
* <span data-ttu-id="2fdb6-117">Examinez les détections de la résurv et identifiez les détections éventuellement incorrectes.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-117">Review ASR detections and identify possible incorrect detections.</span></span>
* <span data-ttu-id="2fdb6-118">Analysez l’impact des exclusions et générez la liste des chemins d’accès aux fichiers à exclure.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-118">Analyze the impact of exclusions and generate the list of file paths to exclude.</span></span>

<span data-ttu-id="2fdb6-119">Sélectionnez **Go to attack surface management** Monitoring & reports > Attack surface reduction rules > Add  >  **exclusions**.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-119">Select **Go to attack surface management** > **Monitoring & reports > Attack surface reduction rules > Add exclusions**.</span></span> <span data-ttu-id="2fdb6-120">À partir de là, vous pouvez accéder à d’autres sections du centre Microsoft 365 sécurité.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-120">From there, you can navigate to other sections of Microsoft 365 security center.</span></span>

<span data-ttu-id="2fdb6-121">![Onglet Ajouter des exclusions dans la page Règles de réduction de la surface d’attaque Microsoft 365 centre de sécurité](images/secconmgmt_asr_m365exlusions.png)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-121">![Add exclusions tab in the Attack surface reduction rules page in Microsoft 365 security center](images/secconmgmt_asr_m365exlusions.png)</span></span><br>
<span data-ttu-id="2fdb6-122">Onglet ***Ajouter des exclusions** dans la page Règles de réduction de la surface d’attaque Microsoft 365 centre de sécurité*</span><span class="sxs-lookup"><span data-stu-id="2fdb6-122">The ***Add exclusions** tab in the Attack surface reduction rules page in Microsoft 365 security center*</span></span>

> [!NOTE]
> <span data-ttu-id="2fdb6-123">Pour accéder Microsoft 365 centre de sécurité, vous avez besoin d’une licence Microsoft 365 E3 ou E5 et d’un compte qui a certains rôles sur Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2fdb6-123">To access Microsoft 365 security center, you need a Microsoft 365 E3 or E5 license and an account that has certain roles on Azure Active Directory.</span></span> <span data-ttu-id="2fdb6-124">[En savoir plus sur les licences et autorisations requises.](/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-124">[Read about required licenses and permissions](/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

<span data-ttu-id="2fdb6-125">Pour plus d’informations sur le déploiement de règles asr dans Microsoft 365 sécurité, voir Surveiller et gérer le déploiement et les détections de règles [asr.](/office365/securitycompliance/monitor-devices#monitor-and-manage-asr-rule-deployment-and-detections)</span><span class="sxs-lookup"><span data-stu-id="2fdb6-125">For more information about ASR rule deployment in Microsoft 365 security center, see [Monitor and manage ASR rule deployment and detections](/office365/securitycompliance/monitor-devices#monitor-and-manage-asr-rule-deployment-and-detections).</span></span>

<span data-ttu-id="2fdb6-126">**Rubriques connexes**</span><span class="sxs-lookup"><span data-stu-id="2fdb6-126">**Related topics**</span></span>

* [<span data-ttu-id="2fdb6-127">Vérifier que vos appareils sont correctement configurés</span><span class="sxs-lookup"><span data-stu-id="2fdb6-127">Ensure your devices are configured properly</span></span>](configure-machines.md)
* [<span data-ttu-id="2fdb6-128">Obtenir des appareils intégrés à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="2fdb6-128">Get devices onboarded to Microsoft Defender for Endpoint</span></span>](configure-machines-onboarding.md)
* [<span data-ttu-id="2fdb6-129">Surveiller la conformité à la ligne de base de sécurité microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="2fdb6-129">Monitor compliance to the Microsoft Defender for Endpoint security baseline</span></span>](configure-machines-security-baseline.md)
