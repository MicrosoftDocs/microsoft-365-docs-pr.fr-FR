---
title: Mineurs et acquisition de compléments à partir du magasin
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
ms.custom: AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 737e8c86-be63-44d7-bf02-492fa7cd9c3f
description: Découvrez le règlement général sur la protection des données (RGPD) qui régit les données personnelles des mineurs.
ms.openlocfilehash: dcf2c98906830e0007747e2dd90e67b9dc85a5bb
ms.sourcegitcommit: 222fc3f8841de82b1b558f47db8a79aa5054d0ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/11/2020
ms.locfileid: "45103105"
---
# <a name="minors-and-acquiring-add-ins-from-the-store"></a><span data-ttu-id="9e441-103">Mineurs et acquisition de compléments à partir du magasin</span><span class="sxs-lookup"><span data-stu-id="9e441-103">Minors and acquiring add-ins from the Store</span></span>

<span data-ttu-id="9e441-104">Le règlement général sur la protection des données (RGPD) est un règlement de l’Union européenne qui devient effectif le 25 mai 2018.</span><span class="sxs-lookup"><span data-stu-id="9e441-104">The General Data Protection Regulation (GDPR) is a European Union regulation that becomes effective May 25, 2018.</span></span> <span data-ttu-id="9e441-105">Il donne aux utilisateurs des droits et la protection de leurs données.</span><span class="sxs-lookup"><span data-stu-id="9e441-105">It gives users rights to and protection of their data.</span></span> <span data-ttu-id="9e441-106">L’un des aspects du RGPD est que les mineurs ne peuvent pas avoir leurs données personnelles envoyées aux parties que leur parent ou tuteur n’a pas approuvées.</span><span class="sxs-lookup"><span data-stu-id="9e441-106">One of the aspects of the GDPR is that minors cannot have their personal data sent to parties that their parent or guardian hasn't approved.</span></span> <span data-ttu-id="9e441-107">L’âge spécifique défini comme un mineur dépend de la région où se trouve la personne.</span><span class="sxs-lookup"><span data-stu-id="9e441-107">The specific age defined as a minor depends on the region where the individual is located.</span></span>
  
<span data-ttu-id="9e441-108">Les régions dont la réglementation statutaire est relative au consentement parental incluent les États-Unis, la Corée du Sud, le Royaume-Uni et l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="9e441-108">Regions that have statutory regulations about parental consent include the United States, South Korea, the United Kingdom, and the European Union.</span></span> <span data-ttu-id="9e441-109">Pour ces régions, un mineur est bloqué (via Azure Active Directory) pour obtenir les nouveaux compléments Office à partir du Store et exécuter des compléments qui ont été précédemment acquis.</span><span class="sxs-lookup"><span data-stu-id="9e441-109">For those regions, a minor will be blocked (via Azure Active Directory) from getting any new Office add-ins from the Store and running add-ins that were previously acquired.</span></span> <span data-ttu-id="9e441-110">Pour les pays sans réglementation réglementaire, il n’y aura pas de restrictions de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="9e441-110">For countries without statutory regulations, there will be no download restrictions.</span></span>
  
<span data-ttu-id="9e441-111">Un utilisateur est considéré comme mineur en fonction des données spécifiées dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e441-111">A user is determined to be a minor based on data specified in Azure Active Directory.</span></span> <span data-ttu-id="9e441-112">L’administrateur de l’organisation est responsable de la déclaration du groupe d’âge légal et de l’autorisation parentale pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9e441-112">The organization admin is responsible for declaring the legal age group and the parental consent for that user.</span></span>
  
<span data-ttu-id="9e441-113">Si le parent/tuteur est accepté par un utilisateur secondaire à l’aide d’un complément spécifique, l’administrateur de l’organisation peut utiliser un déploiement centralisé pour déployer ce complément sur tous les mineurs qui ont le consentement.</span><span class="sxs-lookup"><span data-stu-id="9e441-113">If the parent/guardian consents to a minor using a specific add-In, then the organization admin can use centralized deployment to deploy that add-In to all minors who have consent.</span></span>
  
<span data-ttu-id="9e441-114">Pour être conforme à RGPD pour les mineurs, vous devez vous assurer que l’une des versions suivantes d’Office est déployée dans votre établissement scolaire ou votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9e441-114">To be GDPR compliant for minors you need to ensure that one of following builds of Office is deployed in your school/organization.</span></span>
 
 <span data-ttu-id="9e441-115">**Pour Word, Excel, PowerPoint et Project**:</span><span class="sxs-lookup"><span data-stu-id="9e441-115">**For Word, Excel, PowerPoint, and Project**:</span></span> 

|<span data-ttu-id="9e441-116">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="9e441-116">**Platform**</span></span> <br/> |<span data-ttu-id="9e441-117">**Numéro de build**</span><span class="sxs-lookup"><span data-stu-id="9e441-117">**Build number**</span></span> <br/> |
|:-----|:-----|
|<span data-ttu-id="9e441-118">Applications Microsoft 365 pour les entreprises (canal actuel)</span><span class="sxs-lookup"><span data-stu-id="9e441-118">Microsoft 365 Apps for enterprise (Current Channel)</span></span>  <br/> |<span data-ttu-id="9e441-119">9001,2138</span><span class="sxs-lookup"><span data-stu-id="9e441-119">9001.2138</span></span>   <br/> |
|<span data-ttu-id="9e441-120">Applications Microsoft 365 pour Enterprise (canal d’entreprise semi-annuel)</span><span class="sxs-lookup"><span data-stu-id="9e441-120">Microsoft 365 Apps for enterprise (Semi-Annual Enterprise Channel)</span></span>  <br/> |<span data-ttu-id="9e441-121">8431,2159</span><span class="sxs-lookup"><span data-stu-id="9e441-121">8431.2159</span></span>  <br/> |
|<span data-ttu-id="9e441-122">Office 2016 pour Windows</span><span class="sxs-lookup"><span data-stu-id="9e441-122">Office 2016 for Windows</span></span>  <br/> |<span data-ttu-id="9e441-123">16.0.4672.1000</span><span class="sxs-lookup"><span data-stu-id="9e441-123">16.0.4672.1000</span></span>  <br/> |
|<span data-ttu-id="9e441-124">Office 2013 pour Windows</span><span class="sxs-lookup"><span data-stu-id="9e441-124">Office 2013 for Windows</span></span>  <br/> |<span data-ttu-id="9e441-125">15.0.5023.1000</span><span class="sxs-lookup"><span data-stu-id="9e441-125">15.0.5023.1000</span></span>  <br/> |
|<span data-ttu-id="9e441-126">Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="9e441-126">Office 2016 for Mac</span></span>  <br/> |<span data-ttu-id="9e441-127">16.11.18020200</span><span class="sxs-lookup"><span data-stu-id="9e441-127">16.11.18020200</span></span>  <br/> |
|<span data-ttu-id="9e441-128">Office pour le web</span><span class="sxs-lookup"><span data-stu-id="9e441-128">Office for the web</span></span>  <br/> |<span data-ttu-id="9e441-129">S/O</span><span class="sxs-lookup"><span data-stu-id="9e441-129">N/A</span></span>  <br/> |
   
 <span data-ttu-id="9e441-130">**Pour Outlook**:</span><span class="sxs-lookup"><span data-stu-id="9e441-130">**For Outlook**:</span></span> 
  
|<span data-ttu-id="9e441-131">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="9e441-131">**Platform**</span></span> <br/> |<span data-ttu-id="9e441-132">**Numéro de build**</span><span class="sxs-lookup"><span data-stu-id="9e441-132">**Build number**</span></span> <br/> |
|:-----|:-----|
|<span data-ttu-id="9e441-133">Outlook 2016 pour Windows (MSI)</span><span class="sxs-lookup"><span data-stu-id="9e441-133">Outlook 2016 for Windows (MSI)</span></span>  <br/> |<span data-ttu-id="9e441-134">Générer non TBD</span><span class="sxs-lookup"><span data-stu-id="9e441-134">Build No TBD</span></span>  <br/> |
|<span data-ttu-id="9e441-135">Outlook 2016 pour Windows (C2R)</span><span class="sxs-lookup"><span data-stu-id="9e441-135">Outlook 2016 for Windows (C2R)</span></span>  <br/> |<span data-ttu-id="9e441-136">16.0.9323.1000</span><span class="sxs-lookup"><span data-stu-id="9e441-136">16.0.9323.1000</span></span>  <br/> |
|<span data-ttu-id="9e441-137">Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="9e441-137">Office 2016 for Mac</span></span>  <br/> |<span data-ttu-id="9e441-138">16.0.9318.1000</span><span class="sxs-lookup"><span data-stu-id="9e441-138">16.0.9318.1000</span></span>  <br/> |
|<span data-ttu-id="9e441-139">Outlook Mobile pour iOS</span><span class="sxs-lookup"><span data-stu-id="9e441-139">Outlook mobile for iOS</span></span>  <br/> |<span data-ttu-id="9e441-140">2.75.0</span><span class="sxs-lookup"><span data-stu-id="9e441-140">2.75.0</span></span>  <br/> |
|<span data-ttu-id="9e441-141">Outlook Mobile pour Android</span><span class="sxs-lookup"><span data-stu-id="9e441-141">Outlook mobile for Android</span></span>  <br/> |<span data-ttu-id="9e441-142">2.2.145</span><span class="sxs-lookup"><span data-stu-id="9e441-142">2.2.145</span></span>  <br/> |
|<span data-ttu-id="9e441-143">Outlook.com</span><span class="sxs-lookup"><span data-stu-id="9e441-143">Outlook.com</span></span>  <br/> |<span data-ttu-id="9e441-144">S/O</span><span class="sxs-lookup"><span data-stu-id="9e441-144">N/A</span></span>  <br/> |

 <span data-ttu-id="9e441-145">**Configuration requise pour Office 2013**</span><span class="sxs-lookup"><span data-stu-id="9e441-145">**Office 2013 requirements**</span></span>
  
<span data-ttu-id="9e441-146">Word, Excel et PowerPoint 2013 pour Windows prend en charge les mêmes vérifications de mineurs si la bibliothèque d’authentification Active Directory (ADAL) est activée.</span><span class="sxs-lookup"><span data-stu-id="9e441-146">Word, Excel, and PowerPoint 2013 for Windows will support the same minors checks if Active Directory Authentication Library (ADAL) is enabled.</span></span> <span data-ttu-id="9e441-147">Il existe deux options pour la conformité, comme expliqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="9e441-147">There are two options for compliance, as explained next.</span></span>
  
- <span data-ttu-id="9e441-148">**Activez Adal**.</span><span class="sxs-lookup"><span data-stu-id="9e441-148">**Enable ADAL**.</span></span> <span data-ttu-id="9e441-149">Cet article explique comment activer ADAL pour Office 2013 : utilisation de l' [authentification moderne Microsoft 365 avec les clients Office](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).</span><span class="sxs-lookup"><span data-stu-id="9e441-149">This article explains how to enable ADAL for Office 2013: [Using Microsoft 365 modern authentication with Office clients](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).</span></span><br/><span data-ttu-id="9e441-150">Vous devez également définir les clés de Registre pour activer ADAL, comme expliqué dans la rubrique [activation de l’authentification moderne pour Office 2013 sur les appareils Windows](../security-and-compliance/enable-modern-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="9e441-150">You also need to set the registry keys to enable ADAL as explained in [Enable Modern Authentication for Office 2013 on Windows devices](../security-and-compliance/enable-modern-authentication.md).</span></span><br/><span data-ttu-id="9e441-151">En outre, vous devez installer les mises à jour d’avril suivantes pour Office 2013 :</span><span class="sxs-lookup"><span data-stu-id="9e441-151">Additionally, you need to install the following April updates for Office 2013:</span></span>
    
  - [<span data-ttu-id="9e441-152">Description de la mise à jour de sécurité pour Office 2013:10 avril 2018</span><span class="sxs-lookup"><span data-stu-id="9e441-152">Description of the security update for Office 2013: April 10, 2018</span></span>](https://support.microsoft.com/help/4018330/description-of-the-security-update-for-office-2013-april-10-2018)
    
  - [<span data-ttu-id="9e441-153">2018 avril, mise à jour pour Office 2013 (KB4018333)</span><span class="sxs-lookup"><span data-stu-id="9e441-153">April 3, 2018, update for Office 2013 (KB4018333)</span></span>](https://support.microsoft.com/help/4018333/april-3-2018-update-for-office-2013-kb4018333)
    
- <span data-ttu-id="9e441-154">**N’activez pas Adal**.</span><span class="sxs-lookup"><span data-stu-id="9e441-154">**Don't enable ADAL**.</span></span> <span data-ttu-id="9e441-155">Si vous ne parvenez pas à activer ADAL dans Office 2013, nous vous recommandons d’utiliser la stratégie de groupe pour désactiver le magasin pour les clients Office.</span><span class="sxs-lookup"><span data-stu-id="9e441-155">If you're unable to enable ADAL in Office 2013, then our recommendation is to use Group Policy to turn off the Store for the Office clients.</span></span> <span data-ttu-id="9e441-156">Vous trouverez [ici](https://technet.microsoft.com/library/cc178992.aspx)des informations sur la façon de désactiver les paramètres de l’application pour Office.</span><span class="sxs-lookup"><span data-stu-id="9e441-156">Information on how to turn off the app for Office settings is located [here](https://technet.microsoft.com/library/cc178992.aspx).</span></span>

## <a name="related-articles"></a><span data-ttu-id="9e441-157">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="9e441-157">Related articles</span></span>

[<span data-ttu-id="9e441-158">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="9e441-158">Deploy add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)

[<span data-ttu-id="9e441-159">Gérer les compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="9e441-159">Manage add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center)
    
