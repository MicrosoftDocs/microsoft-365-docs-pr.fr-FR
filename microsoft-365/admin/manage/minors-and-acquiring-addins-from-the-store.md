---
title: Mineurs et acquisition de modules dans le Store
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
description: Découvrez les réglementations du Règlement général sur la protection des données (R GDPR) qui régissent les données personnelles des mineurs.
ms.openlocfilehash: a738e22a0ac0b995c8e44fcf4cc5a2eb47375be5
ms.sourcegitcommit: 555d756c69ac9031d1fb928f2e1f9750beede066
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/29/2020
ms.locfileid: "47306550"
---
# <a name="minors-and-acquiring-add-ins-from-the-store"></a><span data-ttu-id="50984-103">Mineurs et acquisition de modules dans le Store</span><span class="sxs-lookup"><span data-stu-id="50984-103">Minors and acquiring add-ins from the Store</span></span>

<span data-ttu-id="50984-104">Le Règlement général sur la protection des données (R GDPR) est une réglementation de l’Union européenne qui entre en vigueur le 25 mai 2018.</span><span class="sxs-lookup"><span data-stu-id="50984-104">The General Data Protection Regulation (GDPR) is a European Union regulation that becomes effective May 25, 2018.</span></span> <span data-ttu-id="50984-105">Il accorde aux utilisateurs des droits et une protection de leurs données.</span><span class="sxs-lookup"><span data-stu-id="50984-105">It gives users rights to and protection of their data.</span></span> <span data-ttu-id="50984-106">L’un des aspects du R GDPR est que les mineurs ne peuvent pas avoir leurs données personnelles envoyées aux parties que leur parent ou leur guardian n’a pas approuvées.</span><span class="sxs-lookup"><span data-stu-id="50984-106">One of the aspects of the GDPR is that minors cannot have their personal data sent to parties that their parent or guardian hasn't approved.</span></span> <span data-ttu-id="50984-107">L’âge spécifique défini comme mineur dépend de la région où se trouve la personne.</span><span class="sxs-lookup"><span data-stu-id="50984-107">The specific age defined as a minor depends on the region where the individual is located.</span></span>
  
<span data-ttu-id="50984-108">Les régions qui ont des réglementations légales sur le consentement parental sont les États-Unis, la Corée du Sud, le Royaume-Uni et l’Union européenne.</span><span class="sxs-lookup"><span data-stu-id="50984-108">Regions that have statutory regulations about parental consent include the United States, South Korea, the United Kingdom, and the European Union.</span></span> <span data-ttu-id="50984-109">Pour ces régions, une mineure sera bloquée (via Azure Active Directory) pour obtenir de nouveaux modules office à partir du Windows Store et l’exécution de ceux qui ont été acquis précédemment.</span><span class="sxs-lookup"><span data-stu-id="50984-109">For those regions, a minor will be blocked (via Azure Active Directory) from getting any new Office add-ins from the Store and running add-ins that were previously acquired.</span></span> <span data-ttu-id="50984-110">Pour les pays sans réglementation statutaire, il n’y aura aucune restriction de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="50984-110">For countries without statutory regulations, there will be no download restrictions.</span></span>
  
<span data-ttu-id="50984-111">Un utilisateur est déterminé comme mineur en fonction des données spécifiées dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50984-111">A user is determined to be a minor based on data specified in Azure Active Directory.</span></span> <span data-ttu-id="50984-112">L’administrateur de l’organisation est responsable de la déclaration du groupe d’âge légal et du consentement parental de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50984-112">The organization admin is responsible for declaring the legal age group and the parental consent for that user.</span></span>
  
<span data-ttu-id="50984-113">Si le parent/guardian consent à un mineur à l’aide d’un add-In spécifique, l’administrateur de l’organisation peut utiliser le déploiement centralisé pour déployer ce module sur tous les mineurs qui ont le consentement.</span><span class="sxs-lookup"><span data-stu-id="50984-113">If the parent/guardian consents to a minor using a specific add-In, then the organization admin can use centralized deployment to deploy that add-In to all minors who have consent.</span></span>
  
<span data-ttu-id="50984-114">Pour être conforme au R GDPR pour les mineurs, vous devez vous assurer que l’une des builds suivantes d’Office est déployée dans votre établissement scolaire/organisation.</span><span class="sxs-lookup"><span data-stu-id="50984-114">To be GDPR compliant for minors you need to ensure that one of following builds of Office is deployed in your school/organization.</span></span>
 
 <span data-ttu-id="50984-115">**Pour Word, Excel, PowerPoint et Project**:</span><span class="sxs-lookup"><span data-stu-id="50984-115">**For Word, Excel, PowerPoint, and Project**:</span></span> 

|<span data-ttu-id="50984-116">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="50984-116">**Platform**</span></span> <br/> |<span data-ttu-id="50984-117">**Numéro de build**</span><span class="sxs-lookup"><span data-stu-id="50984-117">**Build number**</span></span> <br/> |
|:-----|:-----|
|<span data-ttu-id="50984-118">Applications Microsoft 365 pour les entreprises (canal actuel)</span><span class="sxs-lookup"><span data-stu-id="50984-118">Microsoft 365 Apps for enterprise (Current Channel)</span></span>  <br/> |<span data-ttu-id="50984-119">9001.2138</span><span class="sxs-lookup"><span data-stu-id="50984-119">9001.2138</span></span>   <br/> |
|<span data-ttu-id="50984-120">Applications Microsoft 365 pour les entreprises (canal d’entreprise semi-annuel)</span><span class="sxs-lookup"><span data-stu-id="50984-120">Microsoft 365 Apps for enterprise (Semi-Annual Enterprise Channel)</span></span>  <br/> |<span data-ttu-id="50984-121">8431.2159</span><span class="sxs-lookup"><span data-stu-id="50984-121">8431.2159</span></span>  <br/> |
|<span data-ttu-id="50984-122">Office 2016 pour Windows</span><span class="sxs-lookup"><span data-stu-id="50984-122">Office 2016 for Windows</span></span>  <br/> |<span data-ttu-id="50984-123">16.0.4672.1000</span><span class="sxs-lookup"><span data-stu-id="50984-123">16.0.4672.1000</span></span>  <br/> |
|<span data-ttu-id="50984-124">Office 2013 pour Windows</span><span class="sxs-lookup"><span data-stu-id="50984-124">Office 2013 for Windows</span></span>  <br/> |<span data-ttu-id="50984-125">15.0.5023.1000</span><span class="sxs-lookup"><span data-stu-id="50984-125">15.0.5023.1000</span></span>  <br/> |
|<span data-ttu-id="50984-126">Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="50984-126">Office 2016 for Mac</span></span>  <br/> |<span data-ttu-id="50984-127">16.11.18020200</span><span class="sxs-lookup"><span data-stu-id="50984-127">16.11.18020200</span></span>  <br/> |
|<span data-ttu-id="50984-128">Office pour le web</span><span class="sxs-lookup"><span data-stu-id="50984-128">Office for the web</span></span>  <br/> |<span data-ttu-id="50984-129">S/O</span><span class="sxs-lookup"><span data-stu-id="50984-129">N/A</span></span>  <br/> |
   
 <span data-ttu-id="50984-130">**Pour Outlook**:</span><span class="sxs-lookup"><span data-stu-id="50984-130">**For Outlook**:</span></span> 
  
|<span data-ttu-id="50984-131">**Plateforme**</span><span class="sxs-lookup"><span data-stu-id="50984-131">**Platform**</span></span> <br/> |<span data-ttu-id="50984-132">**Numéro de build**</span><span class="sxs-lookup"><span data-stu-id="50984-132">**Build number**</span></span> <br/> |
|:-----|:-----|
|<span data-ttu-id="50984-133">Outlook 2016 pour Windows (MSI)</span><span class="sxs-lookup"><span data-stu-id="50984-133">Outlook 2016 for Windows (MSI)</span></span>  <br/> |<span data-ttu-id="50984-134">Build No TBD</span><span class="sxs-lookup"><span data-stu-id="50984-134">Build No TBD</span></span>  <br/> |
|<span data-ttu-id="50984-135">Outlook 2016 pour Windows (C2R)</span><span class="sxs-lookup"><span data-stu-id="50984-135">Outlook 2016 for Windows (C2R)</span></span>  <br/> |<span data-ttu-id="50984-136">16.0.9323.1000</span><span class="sxs-lookup"><span data-stu-id="50984-136">16.0.9323.1000</span></span>  <br/> |
|<span data-ttu-id="50984-137">Office 2016 pour Mac</span><span class="sxs-lookup"><span data-stu-id="50984-137">Office 2016 for Mac</span></span>  <br/> |<span data-ttu-id="50984-138">16.0.9318.1000</span><span class="sxs-lookup"><span data-stu-id="50984-138">16.0.9318.1000</span></span>  <br/> |
|<span data-ttu-id="50984-139">Outlook Mobile pour iOS</span><span class="sxs-lookup"><span data-stu-id="50984-139">Outlook mobile for iOS</span></span>  <br/> |<span data-ttu-id="50984-140">2.75.0</span><span class="sxs-lookup"><span data-stu-id="50984-140">2.75.0</span></span>  <br/> |
|<span data-ttu-id="50984-141">Outlook Mobile pour Android</span><span class="sxs-lookup"><span data-stu-id="50984-141">Outlook mobile for Android</span></span>  <br/> |<span data-ttu-id="50984-142">2.2.145</span><span class="sxs-lookup"><span data-stu-id="50984-142">2.2.145</span></span>  <br/> |
|<span data-ttu-id="50984-143">Outlook.com</span><span class="sxs-lookup"><span data-stu-id="50984-143">Outlook.com</span></span>  <br/> |<span data-ttu-id="50984-144">S/O</span><span class="sxs-lookup"><span data-stu-id="50984-144">N/A</span></span>  <br/> |

 <span data-ttu-id="50984-145">**Conditions requises pour Office 2013**</span><span class="sxs-lookup"><span data-stu-id="50984-145">**Office 2013 requirements**</span></span>
  
<span data-ttu-id="50984-146">Word, Excel et PowerPoint 2013 pour Windows 2013 ront les mêmes contrôles mineurs si la bibliothèque d’authentification Active Directory (ADAL) est activée.</span><span class="sxs-lookup"><span data-stu-id="50984-146">Word, Excel, and PowerPoint 2013 for Windows will support the same minors checks if Active Directory Authentication Library (ADAL) is enabled.</span></span> <span data-ttu-id="50984-147">Il existe deux options de conformité, comme expliqué ci-après.</span><span class="sxs-lookup"><span data-stu-id="50984-147">There are two options for compliance, as explained next.</span></span>
  
- <span data-ttu-id="50984-148">**Activer ADAL**.</span><span class="sxs-lookup"><span data-stu-id="50984-148">**Enable ADAL**.</span></span> <span data-ttu-id="50984-149">Cet article explique comment activer ADAL pour Office 2013 : utilisation de [l’authentification moderne Microsoft 365 avec les clients Office.](https://docs.microsoft.com/microsoft-365/enterprise/modern-auth-for-office-2013-and-2016)</span><span class="sxs-lookup"><span data-stu-id="50984-149">This article explains how to enable ADAL for Office 2013: [Using Microsoft 365 modern authentication with Office clients](https://docs.microsoft.com/microsoft-365/enterprise/modern-auth-for-office-2013-and-2016).</span></span><br/><span data-ttu-id="50984-150">Vous devez également définir les clés de Registre pour activer ADAL, comme expliqué dans Activer l’authentification moderne pour [Office 2013 sur les appareils Windows.](../security-and-compliance/enable-modern-authentication.md)</span><span class="sxs-lookup"><span data-stu-id="50984-150">You also need to set the registry keys to enable ADAL as explained in [Enable Modern Authentication for Office 2013 on Windows devices](../security-and-compliance/enable-modern-authentication.md).</span></span><br/><span data-ttu-id="50984-151">En outre, vous devez installer les mises à jour d’avril suivantes pour Office 2013 :</span><span class="sxs-lookup"><span data-stu-id="50984-151">Additionally, you need to install the following April updates for Office 2013:</span></span>
    
  - [<span data-ttu-id="50984-152">Description de la mise à jour de sécurité pour Office 2013 : 10 avril 2018</span><span class="sxs-lookup"><span data-stu-id="50984-152">Description of the security update for Office 2013: April 10, 2018</span></span>](https://support.microsoft.com/help/4018330/description-of-the-security-update-for-office-2013-april-10-2018)
    
  - [<span data-ttu-id="50984-153">3 avril 2018, mise à jour pour Office 2013 (KB4018333)</span><span class="sxs-lookup"><span data-stu-id="50984-153">April 3, 2018, update for Office 2013 (KB4018333)</span></span>](https://support.microsoft.com/help/4018333/april-3-2018-update-for-office-2013-kb4018333)
    
- <span data-ttu-id="50984-154">**N’activez pas ADAL**.</span><span class="sxs-lookup"><span data-stu-id="50984-154">**Don't enable ADAL**.</span></span> <span data-ttu-id="50984-155">Si vous ne parvenez pas à activer ADAL dans Office 2013, il est recommandé d’utiliser une stratégie de groupe pour désactiver le Store pour les clients Office.</span><span class="sxs-lookup"><span data-stu-id="50984-155">If you're unable to enable ADAL in Office 2013, then our recommendation is to use Group Policy to turn off the Store for the Office clients.</span></span> <span data-ttu-id="50984-156">Des informations sur la façon de désactiver les paramètres de l’application pour Office sont disponibles [ici.](https://technet.microsoft.com/library/cc178992.aspx)</span><span class="sxs-lookup"><span data-stu-id="50984-156">Information on how to turn off the app for Office settings is located [here](https://technet.microsoft.com/library/cc178992.aspx).</span></span>

## <a name="related-articles"></a><span data-ttu-id="50984-157">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="50984-157">Related articles</span></span>

[<span data-ttu-id="50984-158">Déployer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="50984-158">Deploy add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-deployment-of-add-ins)

[<span data-ttu-id="50984-159">Gérer des compléments dans le centre d’administration</span><span class="sxs-lookup"><span data-stu-id="50984-159">Manage add-ins in the admin center</span></span>](https://docs.microsoft.com/microsoft-365/admin/manage/manage-addins-in-the-admin-center)
    
