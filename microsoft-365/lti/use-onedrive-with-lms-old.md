---
title: Utiliser l OneDrive Learning opérabilité des outils de gestion
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
description: Créez et classez des devoirs, créez et organisez du contenu de cours et collaborez sur des fichiers en temps réel avec la nouvelle application d’interopérabilité OneDrive Learning Tools.
ms.openlocfilehash: 0e437ed4b05b9968ee1e853f668787eed5351fb5
ms.sourcegitcommit: a4c93a4c7d7db08fe3b032b58d5c7dbbb9476e90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2021
ms.locfileid: "53256953"
---
# <a name="use-microsoft-onedrive-lti-with-canvas"></a><span data-ttu-id="fd834-103">Utiliser Microsoft OneDrive LTI avec Canvas</span><span class="sxs-lookup"><span data-stu-id="fd834-103">Use Microsoft OneDrive LTI with Canvas</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fd834-104">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="fd834-104">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd834-105">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="fd834-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

## <a name="integrate-with-canvas"></a><span data-ttu-id="fd834-106">Intégration à Canvas</span><span class="sxs-lookup"><span data-stu-id="fd834-106">Integrate with Canvas</span></span>

<span data-ttu-id="fd834-107">La personne qui effectue cette intégration doit être un administrateur de Canvas et un administrateur du Microsoft 365 client.</span><span class="sxs-lookup"><span data-stu-id="fd834-107">The person who performs this integration should be an admin of Canvas and an admin of the Microsoft 365 tenant.</span></span>

1. <span data-ttu-id="fd834-108">Connectez-vous au portail Microsoft Azure avec le compte d’administrateur client.</span><span class="sxs-lookup"><span data-stu-id="fd834-108">Sign in to the Microsoft Azure portal with the tenant admin account.</span></span> <span data-ttu-id="fd834-109">L’administrateur client Azure doit également avoir le rôle d’administrateur de groupe.</span><span class="sxs-lookup"><span data-stu-id="fd834-109">The Azure tenant administrator should also have the Group administrator role.</span></span>

    ![Administrateur de groupe mis en surbrill](../media/lti-media/lti-group-admin.png)

2. <span data-ttu-id="fd834-111">Connectez-vous au portail Microsoft [OneDrive LTI.](https://odltiappnl.azurewebsites.net/admin)</span><span class="sxs-lookup"><span data-stu-id="fd834-111">Sign in to the Microsoft [OneDrive LTI portal](https://odltiappnl.azurewebsites.net/admin).</span></span>

3. <span data-ttu-id="fd834-112">Acceptez les autorisations pour terminer la sign-in.</span><span class="sxs-lookup"><span data-stu-id="fd834-112">Accept the permissions to complete the sign-in.</span></span>

    ![accepter les autorisations](../media/lti-media/lti-permissions.png)

4. <span data-ttu-id="fd834-114">Sélectionnez **Ajouter un client LTI.**</span><span class="sxs-lookup"><span data-stu-id="fd834-114">Select **Add LTI Tenant**.</span></span>

     ![ajouter un client LTI](../media/lti-media/lti-add-tenant.png)

5. <span data-ttu-id="fd834-116">Sélectionnez **plateforme consommateur LTI** en **tant que zone** de dessin dans la zone de dropdown.</span><span class="sxs-lookup"><span data-stu-id="fd834-116">Select **LTI Consumer Platform** as **Canvas** from the dropdown.</span></span>

6. <span data-ttu-id="fd834-117">Sélectionnez **l’URL de base** de la zone de dessin, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="fd834-117">Select **Canvas Base URL** and then select **Next**.</span></span>

    ![sélectionner Canvas et ajouter une URL de base](../media/lti-media/lti-canvas-base-url.png)

   <span data-ttu-id="fd834-119">L’écran suivant affiche les champs qui vous sont confidentiels.</span><span class="sxs-lookup"><span data-stu-id="fd834-119">The next screen shows fields that are confidential to you.</span></span>

7. <span data-ttu-id="fd834-120">Sélectionner **Suivant** à partir de ??</span><span class="sxs-lookup"><span data-stu-id="fd834-120">Select **Next** from ??</span></span> <span data-ttu-id="fd834-121">page.</span><span class="sxs-lookup"><span data-stu-id="fd834-121">page.</span></span> <span data-ttu-id="fd834-122">LES RÉVISEURS PEUVENT-ILS REMPLIR LE VIDE ICI ?</span><span class="sxs-lookup"><span data-stu-id="fd834-122">CAN REVIEWERS FILL IN THE BLANK HERE?</span></span>

8. <span data-ttu-id="fd834-123">Sélectionnez **Suivant** dans l’écran qui affiche les informations confidentielles pour vous.</span><span class="sxs-lookup"><span data-stu-id="fd834-123">Select **Next** in the screen that shows information that's confidential to you.</span></span>

   <span data-ttu-id="fd834-124">L’écran final du portail Azure affiche les étapes suivantes pour ajouter votre instance de canvas.</span><span class="sxs-lookup"><span data-stu-id="fd834-124">The final screen of the Azure portal shows the next steps for adding your Canvas instance.</span></span>

9. <span data-ttu-id="fd834-125">Copiez les clés de développeur à partir de cet écran.</span><span class="sxs-lookup"><span data-stu-id="fd834-125">Copy the Developer Keys from this screen.</span></span> <span data-ttu-id="fd834-126">Vous l’utiliserez lorsque vous créerez l’instance canvas.</span><span class="sxs-lookup"><span data-stu-id="fd834-126">You'll use when you create the Canvas instance.</span></span>

## <a name="add-the-canvas-instance"></a><span data-ttu-id="fd834-127">Ajouter l’instance canvas</span><span class="sxs-lookup"><span data-stu-id="fd834-127">Add the Canvas instance</span></span>

1. <span data-ttu-id="fd834-128">Dans votre instance de canvas, désélectionnez **les clés de** développeur  >  **d’administration.**</span><span class="sxs-lookup"><span data-stu-id="fd834-128">In your Canvas instance, deselect **Admin** > **Developer Keys**.</span></span>

2. <span data-ttu-id="fd834-129">Choose **LTI Key** in the dropdown on **Developer Key**.</span><span class="sxs-lookup"><span data-stu-id="fd834-129">Choose **LTI Key** in the dropdown on **Developer Key**.</span></span>

   ![Obtenir les clés de développement LTI](../media/lti-media/lti-developer-keys.png)

3. <span data-ttu-id="fd834-131">Collez les clés de développeur ici.</span><span class="sxs-lookup"><span data-stu-id="fd834-131">Paste the developer keys here.</span></span>

     ![Coller les clés de développeur](../media/lti-media/lti-developer-keys.png)

   <span data-ttu-id="fd834-133">La clé est créée en mode **OFF**</span><span class="sxs-lookup"><span data-stu-id="fd834-133">The key gets created in **OFF** mode</span></span>

   ![Clés de développeur créées en mode Hors](../media/lti-media/lti-copy-developer-keys.png)

4. <span data-ttu-id="fd834-135">Copiez le texte mis en surbrillant.</span><span class="sxs-lookup"><span data-stu-id="fd834-135">Copy the highlighted text.</span></span>
    <span data-ttu-id="fd834-136">Il sert d’ID client dans Microsoft OneDrive portail LTI.</span><span class="sxs-lookup"><span data-stu-id="fd834-136">This serves as Client ID in Microsoft OneDrive LTI portal.</span></span>

5. <span data-ttu-id="fd834-137">Collez le texte dans le **champ ID client** Microsoft OneDrive portail LTI, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="fd834-137">Paste the text into the **Client ID** field in Microsoft OneDrive LTI portal, and then select **Next**.</span></span>

6. <span data-ttu-id="fd834-138">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="fd834-138">Select **Save**.</span></span>

7. <span data-ttu-id="fd834-139">Affichez les paramètres en sélectionnant **Afficher les locataires LTI.**</span><span class="sxs-lookup"><span data-stu-id="fd834-139">View the settings by selecting **View LTI Tenants**.</span></span>
