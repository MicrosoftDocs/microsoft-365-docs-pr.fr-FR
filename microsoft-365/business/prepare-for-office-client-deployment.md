---
title: Préparer le déploiement Office client par Microsoft 365 entreprise
f1.keywords:
- CSH
ms.author: efrene
author: efrene
manager: scotv
ms.date: 10/31/2017
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: M365-subscription-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: ed34fff3-2881-4ed4-9906-1ba6bb8dd804
description: Découvrez comment installer automatiquement les applications Office 32 bits sur Windows 10 ordinateurs et les maintenir à jour.
ms.openlocfilehash: 843be426d817da1173769b3b66dc4c054179f0fd
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52924224"
---
# <a name="prepare-for-office-client-deployment-by-microsoft-365-for-business"></a><span data-ttu-id="7fdc2-103">Préparer le déploiement Office client par Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="7fdc2-103">Prepare for Office client deployment by Microsoft 365 for business</span></span>

<span data-ttu-id="7fdc2-104">Cet article s’applique aux Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-104">This article applies to Microsoft 365 Business Premium.</span></span>

## <a name="prepare-to-automatically-install-office-apps-to-client-computers"></a><span data-ttu-id="7fdc2-105">Préparer l'installation automatique d'applications Office sur des ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="7fdc2-105">Prepare to automatically install Office apps to client computers</span></span>

<span data-ttu-id="7fdc2-106">Vous pouvez utiliser Microsoft 365 Business Premium pour installer automatiquement les applications Office 32 bits sur Windows 10 ordinateurs et les tenir informés des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-106">You can use Microsoft 365 Business Premium to automatically install the 32-bit Office apps on Windows 10 computers and keep them current with updates.</span></span>
  
<span data-ttu-id="7fdc2-107">L’installation automatique fonctionne mieux si l’ordinateur de l’utilisateur final est Windows 10 Business et :</span><span class="sxs-lookup"><span data-stu-id="7fdc2-107">Automatic installation works best if the end user's computer is on Windows 10 Business and:</span></span>
  
- <span data-ttu-id="7fdc2-108">qu'aucune application de bureau Office (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access et OneDrive) ne soit installée.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-108">Doesn't have existing Office desktop apps (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access, and OneDrive).</span></span>
    
    <span data-ttu-id="7fdc2-109">ou</span><span class="sxs-lookup"><span data-stu-id="7fdc2-109">or</span></span>
    
- <span data-ttu-id="7fdc2-110">comprenne une version « Démarrer en un clic » d'Office.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-110">Has an existing version of Click-to-Run Office installed.</span></span>
    
<span data-ttu-id="7fdc2-111">Pour déterminer si vous possédez la version « Démarrer en un clic » d'Office, dans une application Office, accédez à **Fichier** \> **Compte** ( **Compte Office** dans Outlook).</span><span class="sxs-lookup"><span data-stu-id="7fdc2-111">To determine if you have the Click-to-Run version of Office, in any Office app go to **File** \> **Account** ( **Office Account** in Outlook).</span></span> <span data-ttu-id="7fdc2-112">Si vous voyez **Office mises à** jour comme illustré dans la figure suivante, l’installation s’est effectuée à l’aide de Click-to-Run.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-112">If you see **Office Updates** as shown in the following figure, then the installation was done by using Click-to-Run.</span></span> 
  
![Screenshot of Office updates in Office app Account](../media/e3439380-fa43-4ed6-ae5d-64851c297df5.png)
  
 <span data-ttu-id="7fdc2-114">**Qui avantages de cette fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="7fdc2-114">**Who benefits from having this feature**</span></span>
  
<span data-ttu-id="7fdc2-115">L'utilisateur final dont le PC :</span><span class="sxs-lookup"><span data-stu-id="7fdc2-115">The end user whose PC:</span></span>
  
- <span data-ttu-id="7fdc2-116">**Possède** une licence Windows 10 Business utilisateur, une licence active Microsoft 365 entreprise, Windows 10 Creators Update et est jointe à Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-116">**Has**  a Windows 10 Business user license, an active Microsoft 365 for business license, Windows 10 Creators Update, and is joined to Azure Active Directory.</span></span> 
    
- <span data-ttu-id="7fdc2-117">**N’a pas d’applications** Office 64 bits (par exemple, Word, Excel, PowerPoint).</span><span class="sxs-lookup"><span data-stu-id="7fdc2-117">**Doesn't have** 64-bit Office apps (example: Word, Excel, PowerPoint).</span></span> <span data-ttu-id="7fdc2-118">Si des applications Office 64 bits sont requises, cette fonctionnalité n’est pas adaptée, car il n’existe aucune prise en charge du déclenchement d’une version 64 bits 2016 « En un clic » de Office à partir de la console d’administration Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-118">If 64-bit Office apps are required, then this feature isn't a good fit because there's no support for triggering a 64-bit 2016 Click-to-Run version of Office from the Microsoft 365 for business admin console.</span></span> 
    
- <span data-ttu-id="7fdc2-119">**ne comprend** aucune application autonome Windows Installer 2016 (MSI) (par exemple Visio ou Project).</span><span class="sxs-lookup"><span data-stu-id="7fdc2-119">**Doesn't have** any 2016 Windows Installer (MSI) standalone apps (for example, Visio or Project).</span></span> <span data-ttu-id="7fdc2-120">Microsoft 365 mises à niveau pour les entreprises Office vers la version « En un clic » de Office 2016 et qui ne fonctionne pas avec les applications autonomes MSI Office 2016.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-120">Microsoft 365 for business upgrades Office to the Click-to-Run version of Office 2016 and that doesn't work with Office 2016 MSI standalone apps.</span></span> 
    
<span data-ttu-id="7fdc2-121">Le tableau suivant indique l’action que les utilisateurs finaux/administrateurs peuvent avoir besoin d’exécuter, en fonction de leur état de départ, pour obtenir une version 32 bits en un clic réussie du déploiement Office à partir de la console d’administration Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-121">The following table shows what action the end users/admins may need to take, depending on their beginning state, to have a successful 32-bit Click-to-Run version of Office deployment from the Microsoft 365 for business admin console.</span></span><br/>


|<span data-ttu-id="7fdc2-122">Situation de départ à l'installation d'Office</span><span class="sxs-lookup"><span data-stu-id="7fdc2-122">Starting Office install status</span></span>|<span data-ttu-id="7fdc2-123">Action à prendre avant Microsoft 365'installation Office entreprise</span><span class="sxs-lookup"><span data-stu-id="7fdc2-123">Action to take before Microsoft 365 for business Office install</span></span>|<span data-ttu-id="7fdc2-124">État final</span><span class="sxs-lookup"><span data-stu-id="7fdc2-124">End state</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7fdc2-125">Aucune suite Office installée</span><span class="sxs-lookup"><span data-stu-id="7fdc2-125">No Office suite installed</span></span>  <br/> |<span data-ttu-id="7fdc2-126">Aucune</span><span class="sxs-lookup"><span data-stu-id="7fdc2-126">None</span></span>  <br/> |<span data-ttu-id="7fdc2-127">Office 2016 32 bits est installé à l’aide de « Click-to-Run</span><span class="sxs-lookup"><span data-stu-id="7fdc2-127">Office 2016 32-bit is installed by using Click-to-Run</span></span>  <br/> |
|<span data-ttu-id="7fdc2-128">Version 32 bits « Démarrer en un clic » d'Office présente (2016 ou versions antérieures) et aucune application autonome</span><span class="sxs-lookup"><span data-stu-id="7fdc2-128">Existing Click-to-Run 32-bit version of Office (2016 or earlier) and no standalone apps</span></span>  <br/> |<span data-ttu-id="7fdc2-129">Aucune</span><span class="sxs-lookup"><span data-stu-id="7fdc2-129">None</span></span>  <br/> |<span data-ttu-id="7fdc2-130">Mise à niveau vers la dernière version 32 bits « Démarrer en un clic » d'Office 2016, le cas échéant **\***</span><span class="sxs-lookup"><span data-stu-id="7fdc2-130">Upgraded to the latest 32-bit Click-to-Run version of Office 2016, as needed **\***</span></span> <br/> |
|<span data-ttu-id="7fdc2-131">Version 32 bits « Click-to-Run » existante de Office et applications Office autonomes 32 bits ou 64 bits « Click-to-Run » (par exemple, Visio, Project)</span><span class="sxs-lookup"><span data-stu-id="7fdc2-131">Existing Click-to-Run 32-bit version of Office and Click-to-Run 32-bit or 64-bit standalone Office apps (for example, Visio, Project)</span></span>  <br/> |<span data-ttu-id="7fdc2-132">Aucun</span><span class="sxs-lookup"><span data-stu-id="7fdc2-132">None</span></span>  <br/> |<span data-ttu-id="7fdc2-133">Les applications autonomes ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-133">Standalone apps aren't affected.</span></span> <span data-ttu-id="7fdc2-134">Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="7fdc2-134">Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> |
|<span data-ttu-id="7fdc2-135">Version 32 bits « Démarrer en un clic » d'Office présente et applications autonomes 32 ou 64 bits MSI (à l'exception de 2016) présentes</span><span class="sxs-lookup"><span data-stu-id="7fdc2-135">Existing Click-to-Run 32-bit version of Office and any 32-bit or 64-bit (except 2016) MSI standalone Office apps</span></span>  <br/> |<span data-ttu-id="7fdc2-136">Aucune</span><span class="sxs-lookup"><span data-stu-id="7fdc2-136">None</span></span>  <br/> |<span data-ttu-id="7fdc2-137">Les applications autonomes ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-137">Standalone apps aren't affected.</span></span> <span data-ttu-id="7fdc2-138">Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="7fdc2-138">Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> |
|<span data-ttu-id="7fdc2-139">Version 64 bits « Démarrer en un clic » d'Office présente</span><span class="sxs-lookup"><span data-stu-id="7fdc2-139">Any existing Click-to-Run 64-bit version of Office</span></span>  <br/> |<span data-ttu-id="7fdc2-140">Désinstallez les applications Office 64 bits, s’il est acceptable de les remplacer par des applications Office 32 bits</span><span class="sxs-lookup"><span data-stu-id="7fdc2-140">Uninstall the 64-bit Office apps, if it's OK to replace them with 32-bit Office apps</span></span>  <br/> |<span data-ttu-id="7fdc2-141">Si les applications 64 bits d'Office sont supprimées, la version 32 bits « Démarrer en un clic » d'Office 2016 est installée</span><span class="sxs-lookup"><span data-stu-id="7fdc2-141">If Office 64-bit apps are removed, the Click-to-Run 32-bit version of Office 2016 is installed</span></span>  <br/> |
|<span data-ttu-id="7fdc2-142">Installation MSI d'Office 2016 existante, avec ou sans applications autonomes</span><span class="sxs-lookup"><span data-stu-id="7fdc2-142">An existing MSI install of Office 2016 with or without standalone apps</span></span>  <br/> |<span data-ttu-id="7fdc2-143">Désinstaller la version MSI d'Office 2016.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-143">Uninstall MSI Office 2016.</span></span>  <br/> |<span data-ttu-id="7fdc2-p106">La version 32 bits « Démarrer en un clic » d'Office 2016 est installée. Aucune modification apportée aux applications autonomes.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-p106">Click-to-Run 32-bit version of Office 2016 is installed. No change to standalone apps</span></span>  <br/> |
|<span data-ttu-id="7fdc2-146">Installation MSI d'Office 2013 (ou version antérieure) présente et/ou des applications Office autonomes présentes</span><span class="sxs-lookup"><span data-stu-id="7fdc2-146">Existing MSI install of Office 2013 (or earlier) and/or standalone Office apps</span></span>  <br/> |<span data-ttu-id="7fdc2-147">Aucune</span><span class="sxs-lookup"><span data-stu-id="7fdc2-147">None</span></span>  <br/> |<span data-ttu-id="7fdc2-148">Coexistence de la version 32 bits « Démarrer en un clic » d'Office 2016 avec l'installation MSI d'Office préexistante (et les applications autonomes)</span><span class="sxs-lookup"><span data-stu-id="7fdc2-148">Click-to-Run 32-bit version of Office 2016 with the pre-existing MSI Office install (and standalone apps) exist side-by-side</span></span>  <br/> |
||||
   
 <span data-ttu-id="7fdc2-149">**(\*) Remarque :** pas de mise à niveau vers la version 32 bits « Démarrer en un clic » d'Office 2016 en raison d'un bogue répertorié.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-149">**(\*) Note:** Does not upgrade to Click-to-Run 32-bit version of Office 2016 due to a known bug.</span></span> <span data-ttu-id="7fdc2-150">Un correctif est en cours.</span><span class="sxs-lookup"><span data-stu-id="7fdc2-150">A fix is in progress.</span></span> 
  
