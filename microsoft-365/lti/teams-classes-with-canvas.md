---
title: Utiliser Microsoft Teams classes avec Canvas
ms.author: v-cichur
author: cichur
manager: serdars
ms.reviewer: amitman
audience: admin
ms.topic: article
ms.service: o365-administration
f1.keywords:
- CSH
ms.collection: M365-modern-desktop
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Intégrer Microsoft Teams classes à Canvas
ms.openlocfilehash: 8e28cc8401dbf37d6e780b8f56dc300982abd0cc
ms.sourcegitcommit: 410f6e1c6cf53c3d9013b89d6e0b40a050ee9cad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2021
ms.locfileid: "53137678"
---
# <a name="use-microsoft-teams-classes-with-canvas"></a><span data-ttu-id="d9e85-103">Utiliser Microsoft Teams classes avec Canvas</span><span class="sxs-lookup"><span data-stu-id="d9e85-103">Use Microsoft Teams classes with Canvas</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9e85-104">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="d9e85-104">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d9e85-105">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="d9e85-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="d9e85-106">Microsoft Teams classes est une application Learning Tools Interoperability (LTI) qui permet aux enseignants et aux étudiants de naviguer facilement entre leur système de gestion Learning (LMS) et leur Teams.</span><span class="sxs-lookup"><span data-stu-id="d9e85-106">Microsoft Teams classes is a Learning Tools Interoperability (LTI) app that helps educators and students easily navigate between their Learning Management System (LMS) and Teams.</span></span> <span data-ttu-id="d9e85-107">Les utilisateurs peuvent accéder à leurs équipes de cours associées à leur cours directement à partir de leur LMS.</span><span class="sxs-lookup"><span data-stu-id="d9e85-107">Users can access their class teams associated with their course directly from within their LMS.</span></span>

## <a name="microsoft-office-365-admin"></a><span data-ttu-id="d9e85-108">Microsoft Office 365 Administrateur</span><span class="sxs-lookup"><span data-stu-id="d9e85-108">Microsoft Office 365 Admin</span></span>

<span data-ttu-id="d9e85-109">Avant de gérer l’intégration Microsoft Teams dans Instructure Canvas, il est important que l’application **Microsoft-Teams-Sync-for-Canvas** Azure de Canvas soit approuvée par l’administrateur Microsoft Office 365 de votre établissement dans votre client Microsoft Azure avant de terminer la configuration de l’administrateur canvas.</span><span class="sxs-lookup"><span data-stu-id="d9e85-109">Before managing the Microsoft Teams integration within Instructure Canvas, it is important to have Canvas’s **Microsoft-Teams-Sync-for-Canvas** Azure app approved by your institution’s Microsoft Office 365 admin in your Microsoft Azure tenant before completing the Canvas admin setup.</span></span>

1. <span data-ttu-id="d9e85-110">Connectez-vous à Canvas.</span><span class="sxs-lookup"><span data-stu-id="d9e85-110">Sign in to Canvas.</span></span>
 
2. <span data-ttu-id="d9e85-111">Sélectionnez **le lien** Administrateur dans la navigation globale, puis sélectionnez votre compte.</span><span class="sxs-lookup"><span data-stu-id="d9e85-111">Select the **Admin** link in the global navigation, and then select your account.</span></span>

3. <span data-ttu-id="d9e85-112">Dans la navigation de l’administrateur, **sélectionnez Paramètres** lien, puis l’onglet **Intégrations.**</span><span class="sxs-lookup"><span data-stu-id="d9e85-112">In the admin navigation, select the **Settings** link, and then the **Integrations** tab.</span></span> 

4. <span data-ttu-id="d9e85-113">Activez Microsoft Teams synchronisation en activer le basculement.</span><span class="sxs-lookup"><span data-stu-id="d9e85-113">Enable Microsoft Teams Sync by turning the toggle on.</span></span>

   ![teams-sync](media/teams-sync.png)

5. <span data-ttu-id="d9e85-115">Entrez le nom de votre client Microsoft et l’attribut de connexion.</span><span class="sxs-lookup"><span data-stu-id="d9e85-115">Enter your Microsoft tenant name and login attribute.</span></span> 

   <span data-ttu-id="d9e85-116">L’attribut de connexion sera utilisé pour associer l’utilisateur Canvas à un Azure Active Directory utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9e85-116">The login attribute will be used for associating the Canvas user with an Azure Active Directory user.</span></span> 

6. <span data-ttu-id="d9e85-117">Sélectionnez **Mettre à jour Paramètres** une fois terminé.</span><span class="sxs-lookup"><span data-stu-id="d9e85-117">Select **Update Settings** once done.</span></span>

7. <span data-ttu-id="d9e85-118">Pour approuver l’accès à l’application **Azure Microsoft-Teams-Sync-for-Canvas de Canvas,** sélectionnez le lien Accorder l’accès **client.**</span><span class="sxs-lookup"><span data-stu-id="d9e85-118">To approve access for Canvas’s **Microsoft-Teams-Sync-for-Canvas** Azure app, select the **Grant tenant access** link.</span></span> <span data-ttu-id="d9e85-119">Vous serez redirigé vers le point de terminaison de consentement de l’administrateur de la plateforme d’identités Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9e85-119">You'll be redirected to the Microsoft Identity Platform Admin Consent Endpoint.</span></span>

   ![autorisations](media/permissions.png)

8. <span data-ttu-id="d9e85-121">Sélectionnez **Accepter**.</span><span class="sxs-lookup"><span data-stu-id="d9e85-121">Select **Accept**.</span></span>
 
## <a name="canvas-admin"></a><span data-ttu-id="d9e85-122">Administrateur de zone de dessin</span><span class="sxs-lookup"><span data-stu-id="d9e85-122">Canvas Admin</span></span>

<span data-ttu-id="d9e85-123">Configurer l’Microsoft Teams’intégration LTI 1.3.</span><span class="sxs-lookup"><span data-stu-id="d9e85-123">Set up the Microsoft Teams LTI 1.3 Integration.</span></span>

<span data-ttu-id="d9e85-124">En tant qu’administrateur de zone de dessin, vous devez ajouter l’application Microsoft Teams classes LTI dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="d9e85-124">As a Canvas Admin, you'll need to add the Microsoft Teams classes LTI app within your environment.</span></span> <span data-ttu-id="d9e85-125">Notez l’ID client LTI de l’application.</span><span class="sxs-lookup"><span data-stu-id="d9e85-125">Make a note of the LTI Client ID for the app.</span></span>

 - <span data-ttu-id="d9e85-126">Microsoft Teams classes - 17000000000570</span><span class="sxs-lookup"><span data-stu-id="d9e85-126">Microsoft Teams classes - 170000000000570</span></span>

1. <span data-ttu-id="d9e85-127">Access **Admin settings**  >  **Apps**.</span><span class="sxs-lookup"><span data-stu-id="d9e85-127">Access **Admin settings** > **Apps**.</span></span>

2. <span data-ttu-id="d9e85-128">Sélectionnez **+ Application** pour ajouter Teams applications LTI.</span><span class="sxs-lookup"><span data-stu-id="d9e85-128">Select **+ App** to add the Teams LTI apps.</span></span> 
 
   ![external-apps](media/external-apps.png)

3. <span data-ttu-id="d9e85-130">Sélectionnez **par ID client pour** le type de configuration.</span><span class="sxs-lookup"><span data-stu-id="d9e85-130">Select **By Client ID** for configuration type.</span></span>

   ![ajouter une application](media/add-app.png)

4. <span data-ttu-id="d9e85-132">Entrez l’ID client fourni, puis sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="d9e85-132">Enter the Client ID provided, and then select **Submit**.</span></span>
   
   <span data-ttu-id="d9e85-133">Vous remarquerez que le nom Microsoft Teams’application LTI des classes pour l’ID client pour confirmation.</span><span class="sxs-lookup"><span data-stu-id="d9e85-133">You'll notice the Microsoft Teams classes LTI app name for the Client ID for confirmation.</span></span> 

5. <span data-ttu-id="d9e85-134">Sélectionnez **Installer**.</span><span class="sxs-lookup"><span data-stu-id="d9e85-134">Select **Install**.</span></span>

   <span data-ttu-id="d9e85-135">L Microsoft Teams’application LTI des classes sera ajoutée à la liste des applications externes.</span><span class="sxs-lookup"><span data-stu-id="d9e85-135">The Microsoft Teams classes LTI app will be added to the list of external apps.</span></span>
