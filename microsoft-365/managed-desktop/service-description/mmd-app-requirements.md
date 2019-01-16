---
title: Configuration requise de bureau Microsoft
description: ''
keywords: Service Microsoft de bureau, Microsoft 365, documentation
ms.service: m365-md
author: trudyha
ms.localizationpriority: normal
ms.date: 01/08/2019
ms.openlocfilehash: 6b6c6f6a2e719496578ac1d15c9b94a92a2ab492
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866823"
---
# <a name="microsoft-managed-desktop-app-requirements"></a><span data-ttu-id="03ec0-103">Configuration requise de bureau Microsoft</span><span class="sxs-lookup"><span data-stu-id="03ec0-103">Microsoft Managed Desktop app requirements</span></span>

<!--This topic is the target for aka.ms/app-req. This is aka link is used from EA agreeement for MMD. do not delete.-->

<!--Application addendum -->
 
<span data-ttu-id="03ec0-104">Line-of-business applications que vous souhaitez déployer sur les périphériques de bureau Microsoft doivent respecter les spécifications indiquées dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="03ec0-104">Line-of-business applications that you want to deploy to Microsoft Managed Desktop devices must meet the requirements in this topic.</span></span> 

## <a name="application-condition"></a><span data-ttu-id="03ec0-105">Condition d’application</span><span class="sxs-lookup"><span data-stu-id="03ec0-105">Application condition</span></span>

<span data-ttu-id="03ec0-p101">Il est important que les applications ne pas avoir un impact sur l’environnement de bureau Microsoft. Voici la configuration requise qu’une application dans l’ordre pour déployer Microsoft. Pour une application donnée ou le pilote, Microsoft renoncer à toutes les exigences fournies dans le présent document. Microsoft peut décider de supprimer une application ou un pilote qui affecte les performances et la fiabilité des périphériques de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03ec0-p101">It’s important that applications don’t adversely impact the Microsoft Managed Desktop environment. The following are the requirements that an application must meet in order for Microsoft to deploy it. For any given application or driver, Microsoft may waive any requirement provided herein. Microsoft may decide to remove any application or driver that negatively impacts performance and reliability of Microsoft Managed Desktop devices.</span></span>

## <a name="deployable-using-microsoft-technologies"></a><span data-ttu-id="03ec0-110">Peut être déployé à l’aide des technologies Microsoft</span><span class="sxs-lookup"><span data-stu-id="03ec0-110">Deployable using Microsoft technologies</span></span>

<span data-ttu-id="03ec0-p102">Ordinateur de bureau Microsoft utilise Intune, Microsoft Store et Microsoft Store for Business pour déployer des applications. Par conséquent, les applications doivent être empaquetées sous forme peuvent être déployés par la version en cours de ces services.</span><span class="sxs-lookup"><span data-stu-id="03ec0-p102">Microsoft Managed Desktop uses Intune,  Microsoft Store, and  Microsoft Store for Business to deploy applications. Consequently, applications must be packaged in a manner able to be deployed by the then-current version of those services.</span></span>

## <a name="prohibited-app-classes"></a><span data-ttu-id="03ec0-113">Classes d’application interdite</span><span class="sxs-lookup"><span data-stu-id="03ec0-113">Prohibited app classes</span></span>

<span data-ttu-id="03ec0-114">Certains types d’applications ne sont pas autorisés sur les périphériques de bureau Microsoft :</span><span class="sxs-lookup"><span data-stu-id="03ec0-114">Certain application types are not permitted on Microsoft Managed Desktop devices:</span></span>
- <span data-ttu-id="03ec0-115">logiciel d’audit, de sécurité ou antivirus 3ème partie</span><span class="sxs-lookup"><span data-stu-id="03ec0-115">3rd party anti-virus, security, or audit software</span></span>
- <span data-ttu-id="03ec0-116">navigateurs web de 3ème partie</span><span class="sxs-lookup"><span data-stu-id="03ec0-116">3rd party web browsers</span></span>
- <span data-ttu-id="03ec0-117">Versions de Microsoft Office avant d’Office 365 Pro Plus</span><span class="sxs-lookup"><span data-stu-id="03ec0-117">Versions of Microsoft Office prior to Office 365 Pro Plus</span></span>
- <span data-ttu-id="03ec0-118">Applications qui installent ou regroupent les autres logiciels tiers 3</span><span class="sxs-lookup"><span data-stu-id="03ec0-118">Applications that install or bundle other 3rd party software</span></span>

## <a name="restricted-app-behaviors"></a><span data-ttu-id="03ec0-119">Comportements d’application restreinte</span><span class="sxs-lookup"><span data-stu-id="03ec0-119">Restricted app behaviors</span></span>

<span data-ttu-id="03ec0-p103">Certains comportements d’application peuvent être préjudiciable que l’expérience utilisateur ou représenter un risque de sécurité pour les périphériques de bureau Microsoft. Les applications ne doivent pas comporter les comportements ou les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="03ec0-p103">Certain application behaviors can either be detrimental to user experience or present a security risk to Microsoft Managed Desktop devices. Applications shall not exhibit the following behaviors or characteristics:</span></span> 

<span data-ttu-id="03ec0-122">Expérience utilisateur :</span><span class="sxs-lookup"><span data-stu-id="03ec0-122">User Experience:</span></span>
- <span data-ttu-id="03ec0-123">Installer les services d’arrière-plan ou de lancer le processus de longue durée en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="03ec0-123">Install background services or spawn long-running background processes</span></span>
- <span data-ttu-id="03ec0-124">Ajouter le chemin d’accès de démarrage de Windows</span><span class="sxs-lookup"><span data-stu-id="03ec0-124">Add itself to the Windows startup path</span></span>

<span data-ttu-id="03ec0-125">Sécurité :</span><span class="sxs-lookup"><span data-stu-id="03ec0-125">Security:</span></span>
- <span data-ttu-id="03ec0-126">Appeler proposait Windows ou API Office ou prendre de dépendances sur les structures de données internes Windows ou Office</span><span class="sxs-lookup"><span data-stu-id="03ec0-126">Call undocumented Windows or Office APIs or take dependencies on internal Windows or Office data structures</span></span>
- <span data-ttu-id="03ec0-127">Agir comme un magasin d’applications ou gestionnaire d’extension intégrés</span><span class="sxs-lookup"><span data-stu-id="03ec0-127">Act as an app store or have built-in extension manager</span></span>
- <span data-ttu-id="03ec0-128">Élever les privilèges de l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="03ec0-128">Elevate the end user’s privileges</span></span>
- <span data-ttu-id="03ec0-129">Failles de sécurité connus</span><span class="sxs-lookup"><span data-stu-id="03ec0-129">Have known security vulnerabilities</span></span>
- <span data-ttu-id="03ec0-130">Signé à l’aide d’un certificat qui ne reportés sur une racine de confiance</span><span class="sxs-lookup"><span data-stu-id="03ec0-130">Signed using a certificate which doesn’t roll up to a trusted root</span></span>
- <span data-ttu-id="03ec0-131">Chiffrer ou restreindre l’accès aux données de l’utilisateur final</span><span class="sxs-lookup"><span data-stu-id="03ec0-131">Encrypt or restrict access to end-user data</span></span>
- <span data-ttu-id="03ec0-132">Modifier le code du système d’exploitation en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="03ec0-132">Modify operating system code at run time</span></span>

## <a name="driver-deployment"></a><span data-ttu-id="03ec0-133">Déploiement pilote</span><span class="sxs-lookup"><span data-stu-id="03ec0-133">Driver deployment</span></span>

<span data-ttu-id="03ec0-134">Sauf si un pilote est disponible dans Windows Update ou est signé séparément par Windows matériel qualité (WHQL), Microsoft doit approuver un pilote avant que Microsoft déploierez le pilote aux périphériques de bureau Microsoft.</span><span class="sxs-lookup"><span data-stu-id="03ec0-134">Unless a driver is available in Windows Update or is separately signed by Windows Hardware Quality Lab (WHQL), Microsoft must approve a driver before Microsoft will deploy the driver to Microsoft Managed Desktop devices.</span></span>
