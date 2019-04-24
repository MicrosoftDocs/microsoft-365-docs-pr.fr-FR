---
title: Configuration requise pour les applications de bureau géré Microsoft
description: ''
keywords: Microsoft maNaged Desktop, Microsoft 365, service, documentation
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 01/08/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: de6cc7d77e023a9d41961e5fbcce060f1bb659ae
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278334"
---
# <a name="microsoft-managed-desktop-app-requirements"></a><span data-ttu-id="51148-103">Configuration requise pour les applications de bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="51148-103">Microsoft Managed Desktop app requirements</span></span>

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreeement for MMD. do not delete.-->

<!--Application addendum -->
 
<span data-ttu-id="51148-104">Les applications métier que vous souhaitez déployer sur des appareils de bureau gérés Microsoft doivent répondre aux exigences de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="51148-104">Line-of-business applications that you want to deploy to Microsoft Managed Desktop devices must meet the requirements in this topic.</span></span> 

## <a name="application-condition"></a><span data-ttu-id="51148-105">Condition de l'application</span><span class="sxs-lookup"><span data-stu-id="51148-105">Application condition</span></span>

<span data-ttu-id="51148-106">Il est important que les applications n'aient pas d'impact négatif sur l'environnement de bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51148-106">It’s important that applications don’t adversely impact the Microsoft Managed Desktop environment.</span></span> <span data-ttu-id="51148-107">Les conditions suivantes doivent être satisfaites pour que Microsoft puisse le déployer.</span><span class="sxs-lookup"><span data-stu-id="51148-107">The following are the requirements that an application must meet in order for Microsoft to deploy it.</span></span> <span data-ttu-id="51148-108">Pour une application ou un pilote donné, Microsoft peut renoncer aux exigences fournies dans le présent document.</span><span class="sxs-lookup"><span data-stu-id="51148-108">For any given application or driver, Microsoft may waive any requirement provided herein.</span></span> <span data-ttu-id="51148-109">Microsoft peut décider de supprimer une application ou un pilote qui a un impact négatif sur les performances et la fiabilité des appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51148-109">Microsoft may decide to remove any application or driver that negatively impacts performance and reliability of Microsoft Managed Desktop devices.</span></span>

## <a name="deployable-using-microsoft-technologies"></a><span data-ttu-id="51148-110">Déployable à l'aide des technologies Microsoft</span><span class="sxs-lookup"><span data-stu-id="51148-110">Deployable using Microsoft technologies</span></span>

<span data-ttu-id="51148-111">Microsoft maNaged Desktop utilise Intune, Microsoft Store et Microsoft Store pour les entreprises pour déployer des applications.</span><span class="sxs-lookup"><span data-stu-id="51148-111">Microsoft Managed Desktop uses Intune,  Microsoft Store, and  Microsoft Store for Business to deploy applications.</span></span> <span data-ttu-id="51148-112">Par conséquent, les applications doivent être empaquetées de manière à pouvoir être déployées par la version actuelle de ces services.</span><span class="sxs-lookup"><span data-stu-id="51148-112">Consequently, applications must be packaged in a manner able to be deployed by the then-current version of those services.</span></span>

## <a name="prohibited-app-classes"></a><span data-ttu-id="51148-113">Classes d'application interDites</span><span class="sxs-lookup"><span data-stu-id="51148-113">Prohibited app classes</span></span>

<span data-ttu-id="51148-114">Certains types d'application ne sont pas autorisés sur les appareils de bureau géré Microsoft:</span><span class="sxs-lookup"><span data-stu-id="51148-114">Certain application types are not permitted on Microsoft Managed Desktop devices:</span></span>
- <span data-ttu-id="51148-115">logiciels antivirus, de sécurité ou d'audit tiers</span><span class="sxs-lookup"><span data-stu-id="51148-115">3rd party anti-virus, security, or audit software</span></span>
- <span data-ttu-id="51148-116">navigateurs Web tiers</span><span class="sxs-lookup"><span data-stu-id="51148-116">3rd party web browsers</span></span>
- <span data-ttu-id="51148-117">Versions de Microsoft Office antérieures à Office 365 Pro plus</span><span class="sxs-lookup"><span data-stu-id="51148-117">Versions of Microsoft Office prior to Office 365 Pro Plus</span></span>
- <span data-ttu-id="51148-118">Applications qui installent ou regroupent d'autres logiciels tiers</span><span class="sxs-lookup"><span data-stu-id="51148-118">Applications that install or bundle other 3rd party software</span></span>

## <a name="restricted-app-behaviors"></a><span data-ttu-id="51148-119">Comportements d'application restreinte</span><span class="sxs-lookup"><span data-stu-id="51148-119">Restricted app behaviors</span></span>

<span data-ttu-id="51148-120">Certains comportements d'application peuvent être préjudiciables à l'expérience utilisateur ou présenter un risque de sécurité aux appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51148-120">Certain application behaviors can either be detrimental to user experience or present a security risk to Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="51148-121">Les applications ne doivent pas présenter les comportements ou caractéristiques suivants:</span><span class="sxs-lookup"><span data-stu-id="51148-121">Applications shall not exhibit the following behaviors or characteristics:</span></span> 

<span data-ttu-id="51148-122">Expérience utilisateur:</span><span class="sxs-lookup"><span data-stu-id="51148-122">User Experience:</span></span>
- <span data-ttu-id="51148-123">Installer des services d'arrière-plan ou générer des processus d'arrière-plan de longue durée d'exécution</span><span class="sxs-lookup"><span data-stu-id="51148-123">Install background services or spawn long-running background processes</span></span>
- <span data-ttu-id="51148-124">S'ajouter au chemin de démarrage de Windows</span><span class="sxs-lookup"><span data-stu-id="51148-124">Add itself to the Windows startup path</span></span>

<span data-ttu-id="51148-125">Sécurité :</span><span class="sxs-lookup"><span data-stu-id="51148-125">Security:</span></span>
- <span data-ttu-id="51148-126">Appeler des API Windows ou Office ou prendre des dépendances sur des structures de données Windows ou Office internes</span><span class="sxs-lookup"><span data-stu-id="51148-126">Call undocumented Windows or Office APIs or take dependencies on internal Windows or Office data structures</span></span>
- <span data-ttu-id="51148-127">Agir en tant que magasin d'applications ou disposer d'un gestionnaire d'extensions intégré</span><span class="sxs-lookup"><span data-stu-id="51148-127">Act as an app store or have built-in extension manager</span></span>
- <span data-ttu-id="51148-128">Élever les privilèges de l'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="51148-128">Elevate the end user’s privileges</span></span>
- <span data-ttu-id="51148-129">Ont des failles de sécurité connues</span><span class="sxs-lookup"><span data-stu-id="51148-129">Have known security vulnerabilities</span></span>
- <span data-ttu-id="51148-130">Signé à l'aide d'un certificat qui ne se cumule pas vers une racine approuvée</span><span class="sxs-lookup"><span data-stu-id="51148-130">Signed using a certificate which doesn’t roll up to a trusted root</span></span>
- <span data-ttu-id="51148-131">Chiffrer ou restreindre l'accès aux données de l'utilisateur final</span><span class="sxs-lookup"><span data-stu-id="51148-131">Encrypt or restrict access to end-user data</span></span>
- <span data-ttu-id="51148-132">Modifier le code du système d'exploitation au moment de l'exécution</span><span class="sxs-lookup"><span data-stu-id="51148-132">Modify operating system code at run time</span></span>

## <a name="driver-deployment"></a><span data-ttu-id="51148-133">Déploiement de pilotes</span><span class="sxs-lookup"><span data-stu-id="51148-133">Driver deployment</span></span>

<span data-ttu-id="51148-134">À moins qu'un pilote ne soit disponible dans Windows Update ou qu'il soit signé séparément par le laboratoire de la qualité du matériel Windows (WHQL), Microsoft doit approuver un pilote pour que Microsoft déploie le pilote sur les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51148-134">Unless a driver is available in Windows Update or is separately signed by Windows Hardware Quality Lab (WHQL), Microsoft must approve a driver before Microsoft will deploy the driver to Microsoft Managed Desktop devices.</span></span>
