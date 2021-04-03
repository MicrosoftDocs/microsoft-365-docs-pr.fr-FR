---
title: Planifier les versions logicielles et logicielles de fin de prise en charge
description: Découvrez et planifiez les versions logicielles et logicielles qui ne sont plus pris en charge et qui ne reçoivent pas de mises à jour de sécurité.
keywords: gestion des menaces et des vulnérabilités, recommandation sur la sécurité tvm mdatp, recommandation en matière de cybersécurité, recommandation de sécurité actionnable
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 29adf8a542d97a981a07dac167343f3774aa5af4
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500151"
---
# <a name="plan-for-end-of-support-software-and-software-versions-with-threat-and-vulnerability-management"></a><span data-ttu-id="f093a-104">Planifier les versions logicielles et logicielles de fin de prise en charge avec la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="f093a-104">Plan for end-of-support software and software versions with threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="f093a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="f093a-105">**Applies to:**</span></span>

- [<span data-ttu-id="f093a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="f093a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="f093a-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="f093a-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="f093a-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f093a-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="f093a-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="f093a-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="f093a-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="f093a-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="f093a-111">EOS (End-of-support), également appelé end-of-life (EOL), pour les versions logicielles ou logicielles signifie qu’ils ne seront plus pris en charge ou pris en charge et ne recevront pas de mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f093a-111">End-of-support (EOS), otherwise known as end-of-life (EOL), for software or software versions means that they will no longer be supported or serviced, and will not receive security updates.</span></span> <span data-ttu-id="f093a-112">Lorsque vous utilisez des versions logicielles ou logicielles avec prise en charge terminée, vous exposez votre organisation aux vulnérabilités de sécurité, aux risques juridiques et financiers.</span><span class="sxs-lookup"><span data-stu-id="f093a-112">When you use software or software versions with ended support, you're exposing your organization to security vulnerabilities, legal, and financial risks.</span></span>

<span data-ttu-id="f093a-113">Il est essentiel que les administrateurs informatiques et de sécurité travaillent ensemble et s’assurent que l’inventaire logiciel de l’organisation est configuré pour obtenir des résultats optimaux, une conformité et un écosystème réseau sain.</span><span class="sxs-lookup"><span data-stu-id="f093a-113">It's crucial for Security and IT Administrators to work together and ensure that the organization's software inventory is configured for optimal results, compliance, and a healthy network ecosystem.</span></span> <span data-ttu-id="f093a-114">Ils doivent examiner les options de suppression ou de remplacement des applications qui ont atteint les versions de fin de prise en charge et de mise à jour qui ne sont plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f093a-114">They should examine the options to remove or replace apps that have reached end-of-support and update versions that are no longer supported.</span></span> <span data-ttu-id="f093a-115">Il est préférable de créer et d’implémenter un **plan** avant la fin des dates de support.</span><span class="sxs-lookup"><span data-stu-id="f093a-115">It's best to create and implement a plan **before** the end of support dates.</span></span>

## <a name="find-software-or-software-versions-that-are-no-longer-supported"></a><span data-ttu-id="f093a-116">Rechercher des versions logicielles ou logicielles qui ne sont plus pris en charge</span><span class="sxs-lookup"><span data-stu-id="f093a-116">Find software or software versions that are no longer supported</span></span>

1. <span data-ttu-id="f093a-117">Dans le menu gestion des menaces et des vulnérabilités, accédez aux [**recommandations en matière de sécurité.**](tvm-security-recommendation.md)</span><span class="sxs-lookup"><span data-stu-id="f093a-117">From the threat and vulnerability management menu, navigate to [**Security recommendations**](tvm-security-recommendation.md).</span></span>
2. <span data-ttu-id="f093a-118">Go to the **Filters** panel and look for the tags section.</span><span class="sxs-lookup"><span data-stu-id="f093a-118">Go to the **Filters** panel and look for the tags section.</span></span> <span data-ttu-id="f093a-119">Sélectionnez une ou plusieurs des options de balise EOS.</span><span class="sxs-lookup"><span data-stu-id="f093a-119">Select one or more of the EOS tag options.</span></span> <span data-ttu-id="f093a-120">Ensuite, **appliquez**.</span><span class="sxs-lookup"><span data-stu-id="f093a-120">Then **Apply**.</span></span>

    ![Screenshot tags that say EOS software, EOS versions, and Upcoming EOS versions.](images/tvm-eos-tag.png)

3. <span data-ttu-id="f093a-122">Vous verrez une liste de recommandations relatives aux logiciels dont la prise en charge est terminée, aux versions logicielles qui sont en fin de prise en charge ou aux versions dont la prise en charge sera prochainement terminée.</span><span class="sxs-lookup"><span data-stu-id="f093a-122">You'll see a list of recommendations related to software with ended support, software versions that are end of support, or versions with upcoming end of support.</span></span> <span data-ttu-id="f093a-123">Ces balises sont également visibles dans la page [d’inventaire](tvm-software-inventory.md) logiciel.</span><span class="sxs-lookup"><span data-stu-id="f093a-123">These tags are also visible in the [software inventory](tvm-software-inventory.md) page.</span></span>

    ![Recommandations avec la balise EOS.](images/tvm-eos-tags-column.png)

## <a name="list-of-versions-and-dates"></a><span data-ttu-id="f093a-125">Liste des versions et des dates</span><span class="sxs-lookup"><span data-stu-id="f093a-125">List of versions and dates</span></span>

<span data-ttu-id="f093a-126">Pour afficher la liste des versions qui ont atteint la fin de la prise en charge, ou qui ont pris fin ou bientôt prise en charge, ainsi que ces dates, suivez les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="f093a-126">To view a list of versions that have reached end of support, or end or support soon, and those dates, follow the below steps:</span></span>

1. <span data-ttu-id="f093a-127">Un message s’affiche dans le volant de recommandations de sécurité pour les logiciels dont les versions ont atteint la fin de la prise en charge ou qui arriveront bientôt à la fin du support.</span><span class="sxs-lookup"><span data-stu-id="f093a-127">A message will appear in the security recommendation flyout for software with versions that have reached end of support, or will reach end of support soon.</span></span>

    ![Capture d’écran du lien de distribution de version.](images/eos-upcoming-eos.png)

2. <span data-ttu-id="f093a-129">Sélectionnez **le lien de distribution** de version pour aller à la page d’accès au logiciel.</span><span class="sxs-lookup"><span data-stu-id="f093a-129">Select the **version distribution** link to go to the software drill-down page.</span></span> <span data-ttu-id="f093a-130">Vous pouvez y voir une liste filtrée de versions avec des balises les identifiant comme fin de support ou fin de support à venir.</span><span class="sxs-lookup"><span data-stu-id="f093a-130">There, you can see a filtered list of versions with tags identifying them as end of support, or upcoming end of support.</span></span>

    ![Capture d’écran de la page d’drilldown logicielle avec le logiciel de fin de support.](images/software-drilldown-eos.png)

3. <span data-ttu-id="f093a-132">Sélectionnez l’une des versions du tableau à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f093a-132">Select one of the versions in the table to open.</span></span> <span data-ttu-id="f093a-133">Par exemple, version 10.0.18362.1.</span><span class="sxs-lookup"><span data-stu-id="f093a-133">For example, version 10.0.18362.1.</span></span> <span data-ttu-id="f093a-134">Un volant s’affiche à la date de fin du support.</span><span class="sxs-lookup"><span data-stu-id="f093a-134">A flyout will appear with the end of support date.</span></span>

    ![Capture d’écran de la date de fin du support.](images/version-eos-date.png)

<span data-ttu-id="f093a-136">Une fois que vous avez identifié les logiciels et les versions logicielles vulnérables en raison de leur statut de fin de support, vous devez décider s’il faut les mettre à jour ou les supprimer de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f093a-136">Once you identify which software and software versions are vulnerable due to their end-of-support status, you must decide whether to update or remove them from your organization.</span></span> <span data-ttu-id="f093a-137">Cela réduit l’exposition de votre organisation aux vulnérabilités et aux menaces persistantes avancées.</span><span class="sxs-lookup"><span data-stu-id="f093a-137">Doing so will lower your organizations exposure to vulnerabilities and advanced persistent threats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f093a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f093a-138">Related topics</span></span>

- [<span data-ttu-id="f093a-139">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="f093a-139">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="f093a-140">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="f093a-140">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="f093a-141">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="f093a-141">Software inventory</span></span>](tvm-software-inventory.md)
