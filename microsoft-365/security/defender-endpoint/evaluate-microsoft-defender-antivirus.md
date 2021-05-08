---
title: Évaluer l’antivirus Microsoft Defender
description: Les entreprises de toutes tailles peuvent utiliser ce guide pour évaluer et tester la protection offerte Antivirus Microsoft Defender dans Windows 10.
keywords: Antivirus Microsoft Defender, protection cloud, cloud, logiciel anti-programme malveillant, sécurité, defender, évaluer, tester, protection, comparer, protection en temps réel
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: Normal
author: denisebmsft
ms.author: deniseb
ms.custom: nextgen
ms.date: 09/03/2018
ms.reviewer: ''
manager: dansimp
ms.technology: mde
ms.topic: article
ms.openlocfilehash: 4f789ab80d48966d4cf922811d05d74882d728fe
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52274735"
---
# <a name="evaluate-microsoft-defender-antivirus"></a><span data-ttu-id="055e8-104">Évaluer l’antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="055e8-104">Evaluate Microsoft Defender Antivirus</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="055e8-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="055e8-105">**Applies to:**</span></span>

- [<span data-ttu-id="055e8-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="055e8-106">Microsoft Defender for Endpoint</span></span>](/microsoft-365/security/defender-endpoint/)

<span data-ttu-id="055e8-107">Utilisez ce guide pour déterminer dans quelle mesure Antivirus Microsoft Defender vous protège contre les virus, les programmes malveillants et les applications potentiellement indésirables.</span><span class="sxs-lookup"><span data-stu-id="055e8-107">Use this guide to determine how well Microsoft Defender Antivirus protects you from viruses, malware, and potentially unwanted applications.</span></span>

>[!TIP]
><span data-ttu-id="055e8-108">Vous pouvez également consulter le site web de démonstration microsoft Defender pour points de terminaison [sur demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) pour vérifier que les fonctionnalités suivantes fonctionnent et voir comment elles fonctionnent :</span><span class="sxs-lookup"><span data-stu-id="055e8-108">You can also visit the Microsoft Defender for Endpoint demo website at [demo.wd.microsoft.com](https://demo.wd.microsoft.com?ocid=cx-wddocs-testground) to confirm the following features are working and see how they work:</span></span>
>- <span data-ttu-id="055e8-109">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="055e8-109">Cloud-delivered protection</span></span>
>- <span data-ttu-id="055e8-110">Apprentissage rapide (y compris Bloquer à la première vue)</span><span class="sxs-lookup"><span data-stu-id="055e8-110">Fast learning (including Block at first sight)</span></span>
>- <span data-ttu-id="055e8-111">Blocage d’applications potentiellement indésirables</span><span class="sxs-lookup"><span data-stu-id="055e8-111">Potentially unwanted application blocking</span></span>

<span data-ttu-id="055e8-112">Il explique les fonctionnalités importantes de protection nouvelle génération de Antivirus Microsoft Defender disponibles pour les petites et grandes entreprises, et comment elles augmentent la détection et la protection contre les programmes malveillants sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="055e8-112">It explains the important next-generation protection features of Microsoft Defender Antivirus available for both small and large enterprises, and how they increase malware detection and protection across your network.</span></span>

<span data-ttu-id="055e8-113">Vous pouvez choisir de configurer et d’évaluer chaque paramètre indépendamment, ou tous en même temps.</span><span class="sxs-lookup"><span data-stu-id="055e8-113">You can choose to configure and evaluate each setting independently, or all at once.</span></span> <span data-ttu-id="055e8-114">Nous avons regroupé des paramètres similaires basés sur des scénarios d’évaluation classiques et incluons des instructions d’utilisation de PowerShell pour activer les paramètres.</span><span class="sxs-lookup"><span data-stu-id="055e8-114">We have grouped similar settings based upon typical evaluation scenarios, and include instructions for using PowerShell to enable the settings.</span></span>

<span data-ttu-id="055e8-115">Le guide est disponible au format PDF pour l’affichage hors connexion :</span><span class="sxs-lookup"><span data-stu-id="055e8-115">The guide is available in PDF format for offline viewing:</span></span>

- [<span data-ttu-id="055e8-116">Télécharger le guide au format PDF</span><span class="sxs-lookup"><span data-stu-id="055e8-116">Download the guide in PDF format</span></span>](https://www.microsoft.com/download/details.aspx?id=54795)

<span data-ttu-id="055e8-117">Vous pouvez également télécharger un PowerShell qui active automatiquement tous les paramètres décrits dans le guide.</span><span class="sxs-lookup"><span data-stu-id="055e8-117">You can also download a PowerShell that will enable all the settings described in the guide automatically.</span></span> <span data-ttu-id="055e8-118">Vous pouvez obtenir le script en même temps que le téléchargement PDF ci-dessus, ou individuellement à partir de la galerie PowerShell :</span><span class="sxs-lookup"><span data-stu-id="055e8-118">You can obtain the script alongside the PDF download above, or individually from PowerShell Gallery:</span></span>

- [<span data-ttu-id="055e8-119">Télécharger le script PowerShell pour configurer automatiquement les paramètres</span><span class="sxs-lookup"><span data-stu-id="055e8-119">Download the PowerShell script to automatically configure the settings</span></span>](https://www.powershellgallery.com/packages/WindowsDefender_InternalEvaluationSettings)

> [!IMPORTANT]
> <span data-ttu-id="055e8-120">Le guide est actuellement destiné à l’évaluation de la Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="055e8-120">The guide is currently intended for single-machine evaluation of Microsoft Defender Antivirus.</span></span> <span data-ttu-id="055e8-121">L’activation de tous les paramètres de ce guide peut ne pas convenir pour un déploiement réel.</span><span class="sxs-lookup"><span data-stu-id="055e8-121">Enabling all of the settings in this guide may not be suitable for real-world deployment.</span></span>
>
> <span data-ttu-id="055e8-122">Pour obtenir les dernières recommandations pour le déploiement et la surveillance réels des Antivirus Microsoft Defender sur un réseau, voir [Déployer Antivirus Microsoft Defender](deploy-manage-report-microsoft-defender-antivirus.md).</span><span class="sxs-lookup"><span data-stu-id="055e8-122">For the latest recommendations for real-world deployment and monitoring of Microsoft Defender Antivirus across a network, see [Deploy Microsoft Defender Antivirus](deploy-manage-report-microsoft-defender-antivirus.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="055e8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="055e8-123">Related topics</span></span>

- [<span data-ttu-id="055e8-124">Antivirus Microsoft Defender dans Windows 10</span><span class="sxs-lookup"><span data-stu-id="055e8-124">Microsoft Defender Antivirus in Windows 10</span></span>](microsoft-defender-antivirus-in-windows-10.md)
- [<span data-ttu-id="055e8-125">Déployer Antivirus Microsoft Defender</span><span class="sxs-lookup"><span data-stu-id="055e8-125">Deploy Microsoft Defender Antivirus</span></span>](deploy-manage-report-microsoft-defender-antivirus.md)