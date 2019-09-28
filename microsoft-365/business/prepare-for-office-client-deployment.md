---
title: Se préparer pour le déploiement du client Office par Microsoft 365 Entreprise
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.date: 10/31/2017
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: M365-subscription-management
ms.custom: OKR_SMB_M365
search.appverid:
- BCS160
- MET150
ms.assetid: ed34fff3-2881-4ed4-9906-1ba6bb8dd804
description: Découvrez comment installer automatiquement les applications Office 32 bits sur les ordinateurs Windows 10 et les maintenir à jour.
ms.openlocfilehash: fe1f946e4a216050e533604afa7c6e74e7b5980f
ms.sourcegitcommit: 6003d6da0a85c97357eb3dba3918eb145f381fe1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/27/2019
ms.locfileid: "37288392"
---
# <a name="prepare-for-office-client-deployment-by-microsoft-365-business"></a><span data-ttu-id="34464-103">Se préparer pour le déploiement du client Office par Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="34464-103">Prepare for Office client deployment by Microsoft 365 Business</span></span>

## <a name="prepare-to-automatically-install-office-apps-to-client-computers"></a><span data-ttu-id="34464-104">Préparer l'installation automatique d'applications Office sur des ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="34464-104">Prepare to automatically install Office apps to client computers</span></span>

<span data-ttu-id="34464-105">Vous pouvez utiliser Microsoft 365 Entreprise pour automatiquement installer et mettre à jour les applications Office 32 bits sur des ordinateurs Windows 10.</span><span class="sxs-lookup"><span data-stu-id="34464-105">You can use Microsoft 365 Business to automatically install the 32-bit Office apps to Windows 10 computers and keep them current with updates.</span></span>
  
<span data-ttu-id="34464-106">Il est préférable que l'ordinateur de l'utilisateur final fonctionne sous Windows 10 Business et :</span><span class="sxs-lookup"><span data-stu-id="34464-106">This works best if the end user's computer is on Windows 10 Business and:</span></span>
  
- <span data-ttu-id="34464-107">qu'aucune application de bureau Office (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access et OneDrive) ne soit installée.</span><span class="sxs-lookup"><span data-stu-id="34464-107">Doesn't have existing Office desktop apps (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access, and OneDrive).</span></span>
    
    <span data-ttu-id="34464-108">ou</span><span class="sxs-lookup"><span data-stu-id="34464-108">or</span></span>
    
- <span data-ttu-id="34464-109">comprenne une version « Démarrer en un clic » d'Office.</span><span class="sxs-lookup"><span data-stu-id="34464-109">Has an existing version of Click-to-Run Office installed.</span></span>
    
<span data-ttu-id="34464-p101">Pour déterminer si vous possédez la version « Démarrer en un clic » d'Office, dans une application Office, accédez à **Fichier** \> **Compte** ( **Compte Office** dans Outlook). Si Mises à jour pour Office se présente comme dans la figure suivante, cela signifie que l'installation a été effectuée à l'aide de « Démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="34464-p101">To determine if you have the Click-to-Run version of Office, in any Office app go to **File** \> **Account** ( **Office Account** in Outlook). If you see Office Updates as shown in the following figure, then the installation was done by using Click-to-Run.</span></span> 
  
![Screenshot of Office updates in Office app Account](media/e3439380-fa43-4ed6-ae5d-64851c297df5.png)
  
 <span data-ttu-id="34464-113">**Pour qui cette fonctionnalité est-elle utile ?**</span><span class="sxs-lookup"><span data-stu-id="34464-113">**Who will benefit from having this feature**</span></span>
  
<span data-ttu-id="34464-114">L'utilisateur final dont le PC :</span><span class="sxs-lookup"><span data-stu-id="34464-114">The end user whose PC:</span></span>
  
- <span data-ttu-id="34464-115">**est associé** à une licence d'utilisateur Windows 10 Business activeMicrosoft 365 Entreprise, comprend Windows 10 Creators Update et est inscrit à Azure Active Directory ;</span><span class="sxs-lookup"><span data-stu-id="34464-115">**Has**  a Windows 10 Business user license, an active Microsoft 365 Business license, Windows 10 Creators Update, and is joined to Azure Active Directory.</span></span> 
    
- <span data-ttu-id="34464-p102">**ne comprend pas** les applications Office 64 bits (par exemple, Word, Excel, Powerpoint). Si les applications Office 64 bits sont requises, cette fonctionnalité n'est pas adaptée, car il n'est alors pas possible de déclencher une version « Démarrer en un clic » 64 bits d'Office 2016 à partir de la console d'administration Microsoft 365 Entreprise ;</span><span class="sxs-lookup"><span data-stu-id="34464-p102">**Doesn't have** 64-bit Office apps (example: Word, Excel, Powerpoint). If 64-bit Office apps are required, then this feature is not a good fit because there is no support for triggering a 64-bit 2016 Click-to-Run version of Office from the Microsoft 365 Business admin console.</span></span> 
    
- <span data-ttu-id="34464-p103">**ne comprend** aucune application autonome Windows Installer 2016 (MSI) (par exemple Visio ou Project). Microsoft 365 Entreprise met à niveau Office vers la version « Démarrer en un clic » d'Office 2016 et cela ne fonctionne pas avec les applications autonomes Office 2016 MSI.</span><span class="sxs-lookup"><span data-stu-id="34464-p103">**Doesn't have** any 2016 Windows Installer (MSI) standalone apps (for example, Visio or Project). Microsoft 365 Business upgrades Office to the Click-to-Run version of Office 2016 and that doesn't work with with Office 2016 MSI standalone apps.</span></span> 
    
<span data-ttu-id="34464-120">Le tableau suivant décrit en détail les mesures que les utilisateurs finaux/administrateurs doivent éventuellement prendre, en fonction de leur situation de départ, pour pouvoir déployer la version 32 bits « Démarrer en un clic » d'Office à partir de la console d'administration Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="34464-120">The following table details what action the end users/admins may need to take, depending on their beginning state, to have a successful 32-bit Click-to-Run version of Office deployment from the Microsoft 365 Business admin console.</span></span>
  
|<span data-ttu-id="34464-121">**Situation de départ à l'installation d'Office**</span><span class="sxs-lookup"><span data-stu-id="34464-121">**Starting Office install status**</span></span>|<span data-ttu-id="34464-122">**Mesure à prendre avant d'installer Office Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="34464-122">**Action to take before Microsoft 365 Business Office install**</span></span>|<span data-ttu-id="34464-123">**État final**</span><span class="sxs-lookup"><span data-stu-id="34464-123">**End state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34464-124">Aucune suite Office installée</span><span class="sxs-lookup"><span data-stu-id="34464-124">No Office suite installed</span></span>  <br/> |<span data-ttu-id="34464-125">Aucun</span><span class="sxs-lookup"><span data-stu-id="34464-125">None</span></span>  <br/> |<span data-ttu-id="34464-126">Office 2016 32 bits installé à l'aide de la technologie « Démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="34464-126">Office 2016 32-bit is installed by using click-to-run</span></span>  <br/> |
|<span data-ttu-id="34464-127">Version 32 bits « Démarrer en un clic » d'Office présente (2016 ou versions antérieures) et aucune application autonome</span><span class="sxs-lookup"><span data-stu-id="34464-127">Existing Click-to-Run 32-bit version of Office (2016 or earlier) and no standalone apps</span></span>  <br/> |<span data-ttu-id="34464-128">Aucun</span><span class="sxs-lookup"><span data-stu-id="34464-128">None</span></span>  <br/> |<span data-ttu-id="34464-129">Mise à niveau vers la dernière version 32 bits « Démarrer en un clic » d'Office 2016, le cas échéant **\***</span><span class="sxs-lookup"><span data-stu-id="34464-129">Upgraded to the latest 32-bit Click-to-Run version of Office 2016, as needed **\***</span></span> <br/> |
|<span data-ttu-id="34464-130">Version 32 bits « Démarrer en un clic » d'Office présente et applications autonomes 32 ou 64 bits « Démarrer en un clic » d'Office (par exemple Visio, Project) présentes</span><span class="sxs-lookup"><span data-stu-id="34464-130">Existing Click-to-Run 32-bit version of Office and Click-to-Run 32- or 64-bit standalone Office apps (for example, Visio, Project)</span></span>  <br/> |<span data-ttu-id="34464-131">Aucun</span><span class="sxs-lookup"><span data-stu-id="34464-131">None</span></span>  <br/> |<span data-ttu-id="34464-p104">Les applications autonomes ne sont pas concernées. Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="34464-p104">Standalone apps are not affected. Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> |
|<span data-ttu-id="34464-134">Version 32 bits « Démarrer en un clic » d'Office présente et applications autonomes 32 ou 64 bits MSI (à l'exception de 2016) présentes</span><span class="sxs-lookup"><span data-stu-id="34464-134">Existing Click-to-Run 32-bit version of Office and any 32-bit or 64-bit (except 2016) MSI standalone Office apps</span></span>  <br/> |<span data-ttu-id="34464-135">Aucun</span><span class="sxs-lookup"><span data-stu-id="34464-135">None</span></span>  <br/> |<span data-ttu-id="34464-p105">Les applications autonomes ne sont pas concernées. Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="34464-p105">Standalone apps are not affected. Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> ||||
|<span data-ttu-id="34464-138">Version 64 bits « Démarrer en un clic » d'Office présente</span><span class="sxs-lookup"><span data-stu-id="34464-138">Any existing Click-to-Run 64-bit version of Office</span></span>  <br/> |<span data-ttu-id="34464-139">Désinstaller les applications 64 bits d'Office, si leur remplacement par les applications 32 bits d'Office ne pose aucun problème.</span><span class="sxs-lookup"><span data-stu-id="34464-139">Uninstall the 64-bit Office apps, if it is OK to replace it with 32-bit Office apps</span></span>  <br/> |<span data-ttu-id="34464-140">Si les applications 64 bits d'Office sont supprimées, la version 32 bits « Démarrer en un clic » d'Office 2016 est installée</span><span class="sxs-lookup"><span data-stu-id="34464-140">If Office 64-bit apps are removed, the Click-to-Run 32-bit version of Office 2016 is installed</span></span>  <br/> |
|<span data-ttu-id="34464-141">Installation MSI d'Office 2016 existante, avec ou sans applications autonomes</span><span class="sxs-lookup"><span data-stu-id="34464-141">An existing MSI install of Office 2016 with or without standalone apps</span></span>  <br/> |<span data-ttu-id="34464-142">Désinstaller la version MSI d'Office 2016.</span><span class="sxs-lookup"><span data-stu-id="34464-142">Uninstall MSI Office 2016.</span></span>  <br/> |<span data-ttu-id="34464-p106">La version 32 bits « Démarrer en un clic » d'Office 2016 est installée. Aucune modification apportée aux applications autonomes.</span><span class="sxs-lookup"><span data-stu-id="34464-p106">Click-to-Run 32-bit version of Office 2016 is installed. No change to standalone apps</span></span>  <br/> |
|<span data-ttu-id="34464-145">Installation MSI d'Office 2013 (ou version antérieure) présente et/ou des applications Office autonomes présentes</span><span class="sxs-lookup"><span data-stu-id="34464-145">Existing MSI install of Office 2013 (or earlier) and/or standalone Office apps</span></span>  <br/> |<span data-ttu-id="34464-146">Aucune</span><span class="sxs-lookup"><span data-stu-id="34464-146">None</span></span>  <br/> |<span data-ttu-id="34464-147">Coexistence de la version 32 bits « Démarrer en un clic » d'Office 2016 avec l'installation MSI d'Office préexistante (et les applications autonomes)</span><span class="sxs-lookup"><span data-stu-id="34464-147">Click-to-Run 32-bit version of Office 2016 with the pre-existing MSI Office install (and standalone apps) exist side-by-side</span></span>  <br/> |
||||
   
 <span data-ttu-id="34464-p107">**(\*) Remarque :** pas de mise à niveau vers la version 32 bits « Démarrer en un clic » d'Office 2016 en raison d'un bogue répertorié. La correction est en cours.</span><span class="sxs-lookup"><span data-stu-id="34464-p107">**(\*) Note:** Does not upgrade to Click-to-Run 32-bit version of Office 2016 due to a known bug. Fix is in progress.</span></span> 
  


