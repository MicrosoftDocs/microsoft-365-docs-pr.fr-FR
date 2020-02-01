---
title: Se préparer pour le déploiement du client Office par Microsoft 365 Entreprise
f1.keywords:
- CSH
ms.author: sirkkuw
author: Sirkkuw
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
search.appverid:
- BCS160
- MET150
ms.assetid: ed34fff3-2881-4ed4-9906-1ba6bb8dd804
description: Découvrez comment installer automatiquement les applications Office 32 bits sur les ordinateurs Windows 10 et les maintenir à jour.
ms.openlocfilehash: fa5b2ce1852ebdb1e76c1fa844793fee56af3d68
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41593616"
---
# <a name="prepare-for-office-client-deployment-by-microsoft-365-business"></a><span data-ttu-id="fa2b2-103">Se préparer pour le déploiement du client Office par Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="fa2b2-103">Prepare for Office client deployment by Microsoft 365 Business</span></span>

## <a name="prepare-to-automatically-install-office-apps-to-client-computers"></a><span data-ttu-id="fa2b2-104">Préparer l'installation automatique d'applications Office sur des ordinateurs clients</span><span class="sxs-lookup"><span data-stu-id="fa2b2-104">Prepare to automatically install Office apps to client computers</span></span>

<span data-ttu-id="fa2b2-105">Vous pouvez utiliser Microsoft 365 entreprise pour installer automatiquement les applications Office 32 bits sur les ordinateurs Windows 10 et les garder à jour avec les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-105">You can use Microsoft 365 Business to automatically install the 32-bit Office apps on Windows 10 computers and keep them current with updates.</span></span>
  
<span data-ttu-id="fa2b2-106">L’installation automatique fonctionne mieux si l’ordinateur de l’utilisateur final est sur Windows 10 entreprise et :</span><span class="sxs-lookup"><span data-stu-id="fa2b2-106">Automatic installation works best if the end user's computer is on Windows 10 Business and:</span></span>
  
- <span data-ttu-id="fa2b2-107">qu'aucune application de bureau Office (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access et OneDrive) ne soit installée.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-107">Doesn't have existing Office desktop apps (Word, Excel, PowerPoint, Outlook, OneNote, Publisher, Access, and OneDrive).</span></span>
    
    <span data-ttu-id="fa2b2-108">ou</span><span class="sxs-lookup"><span data-stu-id="fa2b2-108">or</span></span>
    
- <span data-ttu-id="fa2b2-109">comprenne une version « Démarrer en un clic » d'Office.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-109">Has an existing version of Click-to-Run Office installed.</span></span>
    
<span data-ttu-id="fa2b2-110">Pour déterminer si vous possédez la version « Démarrer en un clic » d'Office, dans une application Office, accédez à **Fichier** \> **Compte** ( **Compte Office** dans Outlook).</span><span class="sxs-lookup"><span data-stu-id="fa2b2-110">To determine if you have the Click-to-Run version of Office, in any Office app go to **File** \> **Account** ( **Office Account** in Outlook).</span></span> <span data-ttu-id="fa2b2-111">Si vous voyez les **mises à jour d’Office** comme illustré dans la figure suivante, l’installation a été effectuée à l’aide d’Office « démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="fa2b2-111">If you see **Office Updates** as shown in the following figure, then the installation was done by using Click-to-Run.</span></span> 
  
![Screenshot of Office updates in Office app Account](media/e3439380-fa43-4ed6-ae5d-64851c297df5.png)
  
 <span data-ttu-id="fa2b2-113">**Qui tire parti de cette fonctionnalité ?**</span><span class="sxs-lookup"><span data-stu-id="fa2b2-113">**Who benefits from having this feature**</span></span>
  
<span data-ttu-id="fa2b2-114">L'utilisateur final dont le PC :</span><span class="sxs-lookup"><span data-stu-id="fa2b2-114">The end user whose PC:</span></span>
  
- <span data-ttu-id="fa2b2-115">**est associé** à une licence d'utilisateur Windows 10 Business activeMicrosoft 365 Entreprise, comprend Windows 10 Creators Update et est inscrit à Azure Active Directory ;</span><span class="sxs-lookup"><span data-stu-id="fa2b2-115">**Has**  a Windows 10 Business user license, an active Microsoft 365 Business license, Windows 10 Creators Update, and is joined to Azure Active Directory.</span></span> 
    
- <span data-ttu-id="fa2b2-116">**N’a pas** d’applications Office 64 bits (exemple : Word, Excel, PowerPoint).</span><span class="sxs-lookup"><span data-stu-id="fa2b2-116">**Doesn't have** 64-bit Office apps (example: Word, Excel, PowerPoint).</span></span> <span data-ttu-id="fa2b2-117">Si des applications Office 64 bits sont requises, cette fonctionnalité n’est pas adaptée, car il n’existe pas de prise en charge pour le déclenchement d’une version d’Office « démarrer en un clic » 64 2016 bits d’Office à partir de la console d’administration Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-117">If 64-bit Office apps are required, then this feature isn't a good fit because there's no support for triggering a 64-bit 2016 Click-to-Run version of Office from the Microsoft 365 Business admin console.</span></span> 
    
- <span data-ttu-id="fa2b2-118">**ne comprend** aucune application autonome Windows Installer 2016 (MSI) (par exemple Visio ou Project).</span><span class="sxs-lookup"><span data-stu-id="fa2b2-118">**Doesn't have** any 2016 Windows Installer (MSI) standalone apps (for example, Visio or Project).</span></span> <span data-ttu-id="fa2b2-119">Microsoft 365 Business met à niveau Office vers la version « démarrer en un clic » d’Office 2016 et cela ne fonctionne pas avec les applications autonomes MSI Office 2016.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-119">Microsoft 365 Business upgrades Office to the Click-to-Run version of Office 2016 and that doesn't work with Office 2016 MSI standalone apps.</span></span> 
    
<span data-ttu-id="fa2b2-120">Le tableau suivant indique les actions que les utilisateurs/administrateurs finaux peuvent avoir à effectuer, en fonction de leur état de démarrage, pour obtenir une version de déploiement d’Office « démarrer en un clic » de 32 bits à partir de la console d’administration Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-120">The following table shows what action the end users/admins may need to take, depending on their beginning state, to have a successful 32-bit Click-to-Run version of Office deployment from the Microsoft 365 Business admin console.</span></span>
  
|<span data-ttu-id="fa2b2-121">**Situation de départ à l'installation d'Office**</span><span class="sxs-lookup"><span data-stu-id="fa2b2-121">**Starting Office install status**</span></span>|<span data-ttu-id="fa2b2-122">**Mesure à prendre avant d'installer Office Microsoft 365 Entreprise**</span><span class="sxs-lookup"><span data-stu-id="fa2b2-122">**Action to take before Microsoft 365 Business Office install**</span></span>|<span data-ttu-id="fa2b2-123">**État final**</span><span class="sxs-lookup"><span data-stu-id="fa2b2-123">**End state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa2b2-124">Aucune suite Office installée</span><span class="sxs-lookup"><span data-stu-id="fa2b2-124">No Office suite installed</span></span>  <br/> |<span data-ttu-id="fa2b2-125">Aucun</span><span class="sxs-lookup"><span data-stu-id="fa2b2-125">None</span></span>  <br/> |<span data-ttu-id="fa2b2-126">Office 2016 32 bits est installé à l’aide d’Office « démarrer en un clic »</span><span class="sxs-lookup"><span data-stu-id="fa2b2-126">Office 2016 32-bit is installed by using Click-to-Run</span></span>  <br/> |
|<span data-ttu-id="fa2b2-127">Version 32 bits « Démarrer en un clic » d'Office présente (2016 ou versions antérieures) et aucune application autonome</span><span class="sxs-lookup"><span data-stu-id="fa2b2-127">Existing Click-to-Run 32-bit version of Office (2016 or earlier) and no standalone apps</span></span>  <br/> |<span data-ttu-id="fa2b2-128">Aucun</span><span class="sxs-lookup"><span data-stu-id="fa2b2-128">None</span></span>  <br/> |<span data-ttu-id="fa2b2-129">Mise à niveau vers la dernière version 32 bits « Démarrer en un clic » d'Office 2016, le cas échéant **\***</span><span class="sxs-lookup"><span data-stu-id="fa2b2-129">Upgraded to the latest 32-bit Click-to-Run version of Office 2016, as needed **\***</span></span> <br/> |
|<span data-ttu-id="fa2b2-130">Version d’Office « démarrer en un clic » d’Office « 32 démarrer en un clic » et « démarrer en un clic » 64 ou des applications Office « 32 démarrer en un clic » (par exemple, Visio, Project).</span><span class="sxs-lookup"><span data-stu-id="fa2b2-130">Existing Click-to-Run 32-bit version of Office and Click-to-Run 32-bit or 64-bit standalone Office apps (for example, Visio, Project)</span></span>  <br/> |<span data-ttu-id="fa2b2-131">Aucun</span><span class="sxs-lookup"><span data-stu-id="fa2b2-131">None</span></span>  <br/> |<span data-ttu-id="fa2b2-132">Les applications autonomes ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-132">Standalone apps aren't affected.</span></span> <span data-ttu-id="fa2b2-133">Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="fa2b2-133">Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> |
|<span data-ttu-id="fa2b2-134">Version 32 bits « Démarrer en un clic » d'Office présente et applications autonomes 32 ou 64 bits MSI (à l'exception de 2016) présentes</span><span class="sxs-lookup"><span data-stu-id="fa2b2-134">Existing Click-to-Run 32-bit version of Office and any 32-bit or 64-bit (except 2016) MSI standalone Office apps</span></span>  <br/> |<span data-ttu-id="fa2b2-135">Aucun</span><span class="sxs-lookup"><span data-stu-id="fa2b2-135">None</span></span>  <br/> |<span data-ttu-id="fa2b2-136">Les applications autonomes ne sont pas affectées.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-136">Standalone apps aren't affected.</span></span> <span data-ttu-id="fa2b2-137">Mise à niveau de la suite vers la version 32 bits « Démarrer en un clic » d'Office 2016</span><span class="sxs-lookup"><span data-stu-id="fa2b2-137">Suite is upgraded to Click-to-Run 32-bit version of Office 2016</span></span>  <br/> ||||
|<span data-ttu-id="fa2b2-138">Version 64 bits « Démarrer en un clic » d'Office présente</span><span class="sxs-lookup"><span data-stu-id="fa2b2-138">Any existing Click-to-Run 64-bit version of Office</span></span>  <br/> |<span data-ttu-id="fa2b2-139">Désinstaller les applications Office 64 bits, si vous voulez les remplacer par des applications Office 32 bits</span><span class="sxs-lookup"><span data-stu-id="fa2b2-139">Uninstall the 64-bit Office apps, if it's OK to replace them with 32-bit Office apps</span></span>  <br/> |<span data-ttu-id="fa2b2-140">Si les applications 64 bits d'Office sont supprimées, la version 32 bits « Démarrer en un clic » d'Office 2016 est installée</span><span class="sxs-lookup"><span data-stu-id="fa2b2-140">If Office 64-bit apps are removed, the Click-to-Run 32-bit version of Office 2016 is installed</span></span>  <br/> |
|<span data-ttu-id="fa2b2-141">Installation MSI d'Office 2016 existante, avec ou sans applications autonomes</span><span class="sxs-lookup"><span data-stu-id="fa2b2-141">An existing MSI install of Office 2016 with or without standalone apps</span></span>  <br/> |<span data-ttu-id="fa2b2-142">Désinstaller la version MSI d'Office 2016.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-142">Uninstall MSI Office 2016.</span></span>  <br/> |<span data-ttu-id="fa2b2-p106">La version 32 bits « Démarrer en un clic » d'Office 2016 est installée. Aucune modification apportée aux applications autonomes.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-p106">Click-to-Run 32-bit version of Office 2016 is installed. No change to standalone apps</span></span>  <br/> |
|<span data-ttu-id="fa2b2-145">Installation MSI d'Office 2013 (ou version antérieure) présente et/ou des applications Office autonomes présentes</span><span class="sxs-lookup"><span data-stu-id="fa2b2-145">Existing MSI install of Office 2013 (or earlier) and/or standalone Office apps</span></span>  <br/> |<span data-ttu-id="fa2b2-146">Aucune</span><span class="sxs-lookup"><span data-stu-id="fa2b2-146">None</span></span>  <br/> |<span data-ttu-id="fa2b2-147">Coexistence de la version 32 bits « Démarrer en un clic » d'Office 2016 avec l'installation MSI d'Office préexistante (et les applications autonomes)</span><span class="sxs-lookup"><span data-stu-id="fa2b2-147">Click-to-Run 32-bit version of Office 2016 with the pre-existing MSI Office install (and standalone apps) exist side-by-side</span></span>  <br/> |
||||
   
 <span data-ttu-id="fa2b2-148">**(\*) Remarque :** pas de mise à niveau vers la version 32 bits « Démarrer en un clic » d'Office 2016 en raison d'un bogue répertorié.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-148">**(\*) Note:** Does not upgrade to Click-to-Run 32-bit version of Office 2016 due to a known bug.</span></span> <span data-ttu-id="fa2b2-149">Un correctif est en cours.</span><span class="sxs-lookup"><span data-stu-id="fa2b2-149">A fix is in progress.</span></span> 
  