---
title: Installer Microsoft Project ou Microsoft Visio sur des appareils de bureau gérés Microsoft
description: Informations sur l’installation de Microsoft Project ou de Microsoft Visio sur des appareils de bureau gérés Microsoft
keywords: Microsoft Managed Desktop, Microsoft 365, Microsoft Project, Microsoft Visio
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
ms.localizationpriority: normal
ms.date: 03/07/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: c04bcdf846bafaa7838ef5932c8de595f5035992
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950531"
---
# <a name="install-microsoft-project-or-microsoft-visio-on-microsoft-managed-desktop-devices"></a><span data-ttu-id="2bf11-104">Installer Microsoft Project ou Microsoft Visio sur des appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="2bf11-104">Install Microsoft Project or Microsoft Visio on Microsoft Managed Desktop devices</span></span>

<span data-ttu-id="2bf11-105">Microsoft Project et Microsoft Visio nécessitent l’installation de procédures spécifiques sur les appareils de bureau gérés par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2bf11-105">Microsoft Project and Microsoft Visio require specific steps to be installed on Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="2bf11-106">Cette rubrique décrit les conditions préalables et le processus d’installation de ces applications.</span><span class="sxs-lookup"><span data-stu-id="2bf11-106">This topic documents the prerequisites and installation process for these applications.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2bf11-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="2bf11-107">Prerequisites</span></span>

<span data-ttu-id="2bf11-108">Les administrateurs doivent vérifier qu’ils satisfont aux conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="2bf11-108">Admins should verify that they meet these prerequisites:</span></span>
- <span data-ttu-id="2bf11-109">**Quantités de licences** : la quantité correcte de licences Microsoft Project et Microsoft Visio doit être disponible pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2bf11-109">**License quantities** - The correct amount of Microsoft Project and Microsoft Visio licenses must be available for your users.</span></span> <span data-ttu-id="2bf11-110">Microsoft Managed Desktop ne prend actuellement en charge que les versions 64 bits de ces applications.</span><span class="sxs-lookup"><span data-stu-id="2bf11-110">Microsoft Managed Desktop currently only supports 64-bit versions of these applications.</span></span> 
- <span data-ttu-id="2bf11-111">**Noms de licences** : les noms de licences appropriés pour ces applications sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2bf11-111">**License names** - The appropriate license names for these applications are:</span></span>
    - <span data-ttu-id="2bf11-112">**Microsoft Project** -Project Online professionnel ou Project Online Premium</span><span class="sxs-lookup"><span data-stu-id="2bf11-112">**Microsoft Project** - Project Online Professional or Project Online Premium</span></span>
    - <span data-ttu-id="2bf11-113">**Microsoft Visio** -Visio Online-plan 2</span><span class="sxs-lookup"><span data-stu-id="2bf11-113">**Microsoft Visio** - Visio Online Plan 2</span></span>
- <span data-ttu-id="2bf11-114">**Portail d’entreprise** : le portail de l’entreprise doit être disponible dans votre client pour permettre à vos utilisateurs d’installer ces applications.</span><span class="sxs-lookup"><span data-stu-id="2bf11-114">**Company Portal** -  The Company Portal must be available in your tenant for your users to install these applications.</span></span> <span data-ttu-id="2bf11-115">Si le portail d’entreprise n’est pas déployé dans votre client, reportez-vous à la rubrique [entreprise Portal](company-portal.md).</span><span class="sxs-lookup"><span data-stu-id="2bf11-115">If the Company Portal isn’t deployed in your tenant, see [Company Portal](company-portal.md).</span></span>

## <a name="deploy-project-and-visio-for-microsoft-managed-desktop-devices"></a><span data-ttu-id="2bf11-116">Déployer Project et Visio pour les appareils de bureau gérés Microsoft</span><span class="sxs-lookup"><span data-stu-id="2bf11-116">Deploy Project and Visio for Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="2bf11-117">Microsoft Managed Desktop ajoute Microsoft Project et Microsoft Visio sous la forme de deux applications Win32 dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="2bf11-117">Microsoft Managed Desktop will add Microsoft Project and Microsoft Visio as two Win32 Applications in Microsoft Intune.</span></span> <span data-ttu-id="2bf11-118">Nous allons également créer deux groupes dans Azure Active Directory qui seront affectés à l’application correspondante avec l’intention « disponible ».</span><span class="sxs-lookup"><span data-stu-id="2bf11-118">We will also create two groups in Azure Active Directory which will be assigned to the corresponding application with the "Available" intent.</span></span> 

<span data-ttu-id="2bf11-119">**Pour déployer Project et Visio** Ajoutez l’utilisateur au groupe approprié et l’application deviendra disponible dans le portail de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2bf11-119">**To deploy Project and Visio** Add the user to the appropriate group and the application will become available in the Company Portal.</span></span> <span data-ttu-id="2bf11-120">La synchronisation peut prendre quelques minutes, mais les utilisateurs peuvent alors installer les applications à partir du portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2bf11-120">It may take a few minutes to sync, but then your users can install the apps from Company Portal.</span></span> 

<span data-ttu-id="2bf11-121">Nom du groupe Azure AD</span><span class="sxs-lookup"><span data-stu-id="2bf11-121">Azure AD Group name</span></span> | <span data-ttu-id="2bf11-122">Quels utilisateurs affecter ?</span><span class="sxs-lookup"><span data-stu-id="2bf11-122">Which users to assign?</span></span>   
 --- | ---
<span data-ttu-id="2bf11-123">Espace de travail moderne-Bureau-Project_Install</span><span class="sxs-lookup"><span data-stu-id="2bf11-123">Modern Workplace-Office-Project_Install</span></span> | <span data-ttu-id="2bf11-124">Utilisateurs ayant besoin d’un projet</span><span class="sxs-lookup"><span data-stu-id="2bf11-124">Users needing Project</span></span>
<span data-ttu-id="2bf11-125">Espace de travail moderne-Bureau-Visio_Install</span><span class="sxs-lookup"><span data-stu-id="2bf11-125">Modern Workplace-Office-Visio_Install</span></span> | <span data-ttu-id="2bf11-126">Utilisateurs qui ont besoin de Visio</span><span class="sxs-lookup"><span data-stu-id="2bf11-126">Users needing Visio</span></span>

## <a name="communicate-changes"></a><span data-ttu-id="2bf11-127">Communication des modifications</span><span class="sxs-lookup"><span data-stu-id="2bf11-127">Communicate changes</span></span>
<span data-ttu-id="2bf11-128">Il est important que les administrateurs informatiques sachent comment installer Project et Visio.</span><span class="sxs-lookup"><span data-stu-id="2bf11-128">It’s important for IT administrators to let their users know how to install Project and Visio.</span></span> <span data-ttu-id="2bf11-129">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2bf11-129">This includes:</span></span> 
- <span data-ttu-id="2bf11-130">Avertir les utilisateurs lorsque ces applications sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2bf11-130">Notifying users when these applications are available to them.</span></span> 
- <span data-ttu-id="2bf11-131">Instructions sur l’installation de ces applications à partir du portail de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="2bf11-131">Instructions on how to install these applications from the Company Portal.</span></span>
