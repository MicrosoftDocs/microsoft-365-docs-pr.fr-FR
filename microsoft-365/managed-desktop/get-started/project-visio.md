---
title: Installer Microsoft Project ou Microsoft Visio sur des appareils de bureau gérés Microsoft
description: Informations sur l’installation de Microsoft Project ou de Microsoft Visio sur des appareils de bureau gérés Microsoft
keywords: Microsoft Managed Desktop, Microsoft 365, Microsoft Project, Microsoft Visio
ms.service: m365-md
author: jaimeo
ms.localizationpriority: normal
ms.date: 03/07/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: 30374e603350ecf9d5e5542263f004a22ccb0a67
ms.sourcegitcommit: 91ff1d4339f0f043c2b43997d87d84677c79e279
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2019
ms.locfileid: "36981705"
---
# <a name="install-microsoft-project-or-microsoft-visio-on-microsoft-managed-desktop-devices"></a><span data-ttu-id="f5e66-104">Installer Microsoft Project ou Microsoft Visio sur des appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5e66-104">Install Microsoft Project or Microsoft Visio on Microsoft Managed Desktop devices</span></span>

<span data-ttu-id="f5e66-105">Microsoft Project et Microsoft Visio nécessitent l’installation de procédures spécifiques sur les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f5e66-105">Microsoft Project and Microsoft Visio require specific steps to be installed on Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="f5e66-106">Cette rubrique décrit les conditions préalables et le processus d’installation de ces applications.</span><span class="sxs-lookup"><span data-stu-id="f5e66-106">This topic documents the prerequisites and installation process for these applications.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f5e66-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f5e66-107">Prerequisites</span></span>

<span data-ttu-id="f5e66-108">Les administrateurs doivent vérifier qu’ils satisfont aux conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5e66-108">Admins should verify that they meet these prerequisites:</span></span>
- <span data-ttu-id="f5e66-109">**Quantités de licences** : la quantité correcte de licences Microsoft Project et Microsoft Visio doit être disponible pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f5e66-109">**License quantities** - The correct amount of Microsoft Project and Microsoft Visio licenses must be available for your users.</span></span> <span data-ttu-id="f5e66-110">Microsoft Managed Desktop ne prend actuellement en charge que les versions 64 bits de ces applications.</span><span class="sxs-lookup"><span data-stu-id="f5e66-110">Microsoft Managed Desktop currently only supports 64-bit versions of these applications.</span></span> 
- <span data-ttu-id="f5e66-111">**Noms de licences** : les noms de licences appropriés pour ces applications sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f5e66-111">**License names** - The appropriate license names for these applications are:</span></span>
    - <span data-ttu-id="f5e66-112">**Microsoft Project** -Project Online professionnel ou Project Online Premium</span><span class="sxs-lookup"><span data-stu-id="f5e66-112">**Microsoft Project** - Project Online Professional or Project Online Premium</span></span>
    - <span data-ttu-id="f5e66-113">**Microsoft Visio** -Visio Online-plan 2</span><span class="sxs-lookup"><span data-stu-id="f5e66-113">**Microsoft Visio** - Visio Online Plan 2</span></span>
- <span data-ttu-id="f5e66-114">**Portail d’entreprise** : le portail de l’entreprise doit être disponible dans votre client pour permettre à vos utilisateurs d’installer ces applications.</span><span class="sxs-lookup"><span data-stu-id="f5e66-114">**Company Portal** -  The Company Portal must be available in your tenant for your users to install these applications.</span></span> <span data-ttu-id="f5e66-115">Si le portail d’entreprise n’est pas déployé dans votre client, reportez-vous à la rubrique [entreprise Portal](company-portal.md).</span><span class="sxs-lookup"><span data-stu-id="f5e66-115">If the Company Portal isn’t deployed in your tenant, see [Company Portal](company-portal.md).</span></span>

## <a name="deploy-project-and-visio-for-microsoft-managed-desktop-devices"></a><span data-ttu-id="f5e66-116">Déployer Project et Visio pour les appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="f5e66-116">Deploy Project and Visio for Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="f5e66-117">Une fois que vous avez soumis votre demande de support, le bureau géré Microsoft crée trois groupes Azure AD et trois déploiements d’application via Microsoft Intune pour déployer les applications sur votre client.</span><span class="sxs-lookup"><span data-stu-id="f5e66-117">After you submit your support request, Microsoft Managed Desktop will create three Azure AD groups and three application deployments through Microsoft Intune to deploy the apps to your tenant.</span></span>  

<span data-ttu-id="f5e66-118">**Pour déployer Project et Visio**</span><span class="sxs-lookup"><span data-stu-id="f5e66-118">**To deploy Project and Visio**</span></span>
1. <span data-ttu-id="f5e66-119">**Classer une demande de support** Les administrateurs informatiques doivent classer une demande de support pour mettre ces applications à disposition de leurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f5e66-119">**File a support request** IT administrators need to file a support request to make these applications available their users.</span></span> <span data-ttu-id="f5e66-120">Pour plus d’informations sur la façon de contacter le bureau géré Microsoft, consultez la rubrique [administrateur pris en charge pour Microsoft Managed Desktop](../working-with-managed-desktop/admin-support.md).</span><span class="sxs-lookup"><span data-stu-id="f5e66-120">For information on contacting Microsoft Managed Desktop, see [Admin support for Microsoft Managed Desktop](../working-with-managed-desktop/admin-support.md).</span></span>
2. <span data-ttu-id="f5e66-121">**Affecter des utilisateurs à de nouveaux groupes Azure ad** Le bureau géré Microsoft créera 3 groupes Azure AD dans votre client et 3 déploiements d’applications correspondants.</span><span class="sxs-lookup"><span data-stu-id="f5e66-121">**Assign users to new Azure AD groups** Microsoft Managed Desktop will create 3 Azure AD groups in your tenant and 3 corresponding application deployments.</span></span> <span data-ttu-id="f5e66-122">Les administrateurs informatiques doivent affecter les utilisateurs aux groupes appropriés.</span><span class="sxs-lookup"><span data-stu-id="f5e66-122">IT admins need to assign the users to the appropriate groups.</span></span>

>[!NOTE]
><span data-ttu-id="f5e66-123">Affectez des utilisateurs à un seul de ces groupes Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f5e66-123">Assign users to only one of these Azure AD groups.</span></span> 

<span data-ttu-id="f5e66-124">Nom du groupe Azure AD</span><span class="sxs-lookup"><span data-stu-id="f5e66-124">Azure AD Group name</span></span> | <span data-ttu-id="f5e66-125">Quels utilisateurs affecter ?</span><span class="sxs-lookup"><span data-stu-id="f5e66-125">Which users to assign?</span></span>   
 --- | ---
<span data-ttu-id="f5e66-126">Espace de travail moderne-Bureau-Project_Install</span><span class="sxs-lookup"><span data-stu-id="f5e66-126">Modern Workplace-Office-Project_Install</span></span> | <span data-ttu-id="f5e66-127">Les utilisateurs qui ont besoin d’un projet uniquement</span><span class="sxs-lookup"><span data-stu-id="f5e66-127">Users needing only Project</span></span>
<span data-ttu-id="f5e66-128">Espace de travail moderne-Bureau-Visio_Install</span><span class="sxs-lookup"><span data-stu-id="f5e66-128">Modern Workplace-Office-Visio_Install</span></span> | <span data-ttu-id="f5e66-129">Les utilisateurs qui ont uniquement besoin de Visio</span><span class="sxs-lookup"><span data-stu-id="f5e66-129">Users needing only Visio</span></span>
<span data-ttu-id="f5e66-130">Espace de travail moderne-Bureau-Visio_Project_Install</span><span class="sxs-lookup"><span data-stu-id="f5e66-130">Modern Workplace-Office-Visio_Project_Install</span></span> | <span data-ttu-id="f5e66-131">Utilisateurs ayant besoin à la fois de Project et de Visio</span><span class="sxs-lookup"><span data-stu-id="f5e66-131">Users needing both Project and Visio</span></span>

<span data-ttu-id="f5e66-132">Une fois affectées à ces groupes, les applications sont disponibles dans le portail de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f5e66-132">Once assigned to these groups, applications will be available in the Company Portal.</span></span> <span data-ttu-id="f5e66-133">La synchronisation peut prendre quelques minutes, mais les utilisateurs peuvent alors installer les applications à partir du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f5e66-133">It may take a few minutes to sync, but then your users can install the apps from Company Portal.</span></span> 

## <a name="communicate-changes"></a><span data-ttu-id="f5e66-134">Communication des modifications</span><span class="sxs-lookup"><span data-stu-id="f5e66-134">Communicate changes</span></span>
<span data-ttu-id="f5e66-135">Il est important que les administrateurs informatiques sachent comment installer Project et Visio.</span><span class="sxs-lookup"><span data-stu-id="f5e66-135">It’s important for IT administrators to let their users know how to install Project and Visio.</span></span> <span data-ttu-id="f5e66-136">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5e66-136">This includes:</span></span> 
- <span data-ttu-id="f5e66-137">Avertir les utilisateurs lorsque ces applications sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="f5e66-137">Notifying users when these applications are available to them.</span></span> 
- <span data-ttu-id="f5e66-138">Instructions sur l’installation de ces applications à partir du portail de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f5e66-138">Instructions on how to install these applications from the Company Portal.</span></span>

>[!NOTE]
><span data-ttu-id="f5e66-139">Les utilisateurs doivent fermer toutes les applications Office avant d’installer Microsoft Project ou Microsoft Visio à partir du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="f5e66-139">Users must close all Office applications before installing Microsoft Project or Microsoft Visio from Company Portal.</span></span> 
