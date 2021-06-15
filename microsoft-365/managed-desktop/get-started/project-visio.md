---
title: Installer Microsoft Project ou Microsoft Visio sur Bureau géré Microsoft appareils
description: Informations sur l’installation Microsoft Project ou Microsoft Visio sur Bureau géré Microsoft appareils
keywords: Bureau géré Microsoft, Microsoft 365, Microsoft Project, Microsoft Visio
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
ms.topic: article
ms.localizationpriority: normal
ms.date: 03/07/2019
ms.collection: M365-modern-desktop
ms.openlocfilehash: 9fd46410877012d92e847ba7ff8b60cd5acceb1e
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925538"
---
# <a name="install-microsoft-project-or-microsoft-visio-on-microsoft-managed-desktop-devices"></a><span data-ttu-id="bb948-104">Installer Microsoft Project ou Microsoft Visio sur Bureau géré Microsoft appareils</span><span class="sxs-lookup"><span data-stu-id="bb948-104">Install Microsoft Project or Microsoft Visio on Microsoft Managed Desktop devices</span></span>

<span data-ttu-id="bb948-105">Microsoft Project et Microsoft Visio des étapes spécifiques doivent être installées sur Bureau géré Microsoft appareils.</span><span class="sxs-lookup"><span data-stu-id="bb948-105">Microsoft Project and Microsoft Visio require specific steps to be installed on Microsoft Managed Desktop devices.</span></span> <span data-ttu-id="bb948-106">Cette rubrique documente les conditions préalables et le processus d’installation de ces applications.</span><span class="sxs-lookup"><span data-stu-id="bb948-106">This topic documents the prerequisites and installation process for these applications.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bb948-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="bb948-107">Prerequisites</span></span>

<span data-ttu-id="bb948-108">Les administrateurs doivent vérifier qu’ils répondent aux conditions préalables ci-après :</span><span class="sxs-lookup"><span data-stu-id="bb948-108">Admins should verify that they meet these prerequisites:</span></span>
- <span data-ttu-id="bb948-109">**Quantités de licences** : le nombre correct de licences Microsoft Project et microsoft Visio licences doit être disponible pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bb948-109">**License quantities** - The correct amount of Microsoft Project and Microsoft Visio licenses must be available for your users.</span></span> <span data-ttu-id="bb948-110">Bureau géré Microsoft ne prend actuellement en charge que les versions 64 bits de ces applications.</span><span class="sxs-lookup"><span data-stu-id="bb948-110">Microsoft Managed Desktop currently only supports 64-bit versions of these applications.</span></span> 
- <span data-ttu-id="bb948-111">**Noms de licence** : les noms de licence appropriés pour ces applications sont les éléments ci-après :</span><span class="sxs-lookup"><span data-stu-id="bb948-111">**License names** - The appropriate license names for these applications are:</span></span>
    - <span data-ttu-id="bb948-112">**Microsoft Project** - Project Online Professionnel ou Project Online Premium</span><span class="sxs-lookup"><span data-stu-id="bb948-112">**Microsoft Project** - Project Online Professional or Project Online Premium</span></span>
    - <span data-ttu-id="bb948-113">**Microsoft Visio** - Visio Online Plan 2</span><span class="sxs-lookup"><span data-stu-id="bb948-113">**Microsoft Visio** - Visio Online Plan 2</span></span>
- <span data-ttu-id="bb948-114">**Portail d’entreprise** - Le Portail d’entreprise doit être disponible dans votre client pour que vos utilisateurs installent ces applications.</span><span class="sxs-lookup"><span data-stu-id="bb948-114">**Company Portal** -  The Company Portal must be available in your tenant for your users to install these applications.</span></span> <span data-ttu-id="bb948-115">Si le Portail d’entreprise n’est pas déployé dans votre client, voir [Portail d’entreprise](company-portal.md).</span><span class="sxs-lookup"><span data-stu-id="bb948-115">If the Company Portal isn’t deployed in your tenant, see [Company Portal](company-portal.md).</span></span>

## <a name="deploy-project-and-visio-for-microsoft-managed-desktop-devices"></a><span data-ttu-id="bb948-116">Déployer des Project et des Visio pour Bureau géré Microsoft appareils</span><span class="sxs-lookup"><span data-stu-id="bb948-116">Deploy Project and Visio for Microsoft Managed Desktop devices</span></span>
<span data-ttu-id="bb948-117">Bureau géré Microsoft ajoutera Microsoft Project et Microsoft Visio en tant que deux applications Win32 dans Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="bb948-117">Microsoft Managed Desktop will add Microsoft Project and Microsoft Visio as two Win32 Applications in Microsoft Intune.</span></span> <span data-ttu-id="bb948-118">Nous allons également créer deux groupes dans Azure Active Directory qui seront affectés à l’application correspondante avec l’intention « Disponible ».</span><span class="sxs-lookup"><span data-stu-id="bb948-118">We will also create two groups in Azure Active Directory which will be assigned to the corresponding application with the "Available" intent.</span></span> 

<span data-ttu-id="bb948-119">**Pour déployer Project et Visio** Ajoutez l’utilisateur au groupe approprié et l’application sera disponible dans le Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bb948-119">**To deploy Project and Visio** Add the user to the appropriate group and the application will become available in the Company Portal.</span></span> <span data-ttu-id="bb948-120">La synchronisation peut prendre quelques minutes, mais vos utilisateurs peuvent ensuite installer les applications à partir Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bb948-120">It may take a few minutes to sync, but then your users can install the apps from Company Portal.</span></span> 

<span data-ttu-id="bb948-121">Nom du groupe Azure AD</span><span class="sxs-lookup"><span data-stu-id="bb948-121">Azure AD Group name</span></span> | <span data-ttu-id="bb948-122">Quels utilisateurs attribuer ?</span><span class="sxs-lookup"><span data-stu-id="bb948-122">Which users to assign?</span></span>   
 --- | ---
<span data-ttu-id="bb948-123">Espace de travail moderne Office-Project_Install</span><span class="sxs-lookup"><span data-stu-id="bb948-123">Modern Workplace-Office-Project_Install</span></span> | <span data-ttu-id="bb948-124">Utilisateurs qui ont besoin de Project</span><span class="sxs-lookup"><span data-stu-id="bb948-124">Users needing Project</span></span>
<span data-ttu-id="bb948-125">Espace de travail moderne Office-Visio_Install</span><span class="sxs-lookup"><span data-stu-id="bb948-125">Modern Workplace-Office-Visio_Install</span></span> | <span data-ttu-id="bb948-126">Utilisateurs qui ont besoin de Visio</span><span class="sxs-lookup"><span data-stu-id="bb948-126">Users needing Visio</span></span>

## <a name="communicate-changes"></a><span data-ttu-id="bb948-127">Communiquer les modifications</span><span class="sxs-lookup"><span data-stu-id="bb948-127">Communicate changes</span></span>
<span data-ttu-id="bb948-128">Il est important pour les administrateurs informatiques de faire savoir à leurs utilisateurs comment installer Project et Visio.</span><span class="sxs-lookup"><span data-stu-id="bb948-128">It’s important for IT administrators to let their users know how to install Project and Visio.</span></span> <span data-ttu-id="bb948-129">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="bb948-129">This includes:</span></span> 
- <span data-ttu-id="bb948-130">Avertir les utilisateurs lorsque ces applications sont disponibles pour eux.</span><span class="sxs-lookup"><span data-stu-id="bb948-130">Notifying users when these applications are available to them.</span></span> 
- <span data-ttu-id="bb948-131">Instructions sur l’installation de ces applications à partir du Portail d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="bb948-131">Instructions on how to install these applications from the Company Portal.</span></span>
