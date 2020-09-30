---
title: Balisage d’image dans SharePoint Syntex
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: Présentation du balisage d’image dans SharePoint Syntex
ms.openlocfilehash: 38b9ad6823aa5f63a4ddec87bab7fec52a37f163
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295899"
---
# <a name="image-tagging-in-sharepoint-syntex"></a><span data-ttu-id="cf1dd-103">Balisage d’image dans SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="cf1dd-103">Image tagging in SharePoint Syntex</span></span>

<span data-ttu-id="cf1dd-104">Par défaut, le balisage de base des images est activé pour SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-104">By default, basic image tagging is turned on for SharePoint and OneDrive.</span></span> <span data-ttu-id="cf1dd-105">Les images chargées dans l’un des emplacements sont automatiquement analysées et des balises valables sont appliquées, le cas échéant, à partir d’une liste de 37 balises de base.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-105">Images uploaded to either location are automatically scanned and applicable tags are applied, if available, from a list of 37 basic tags.</span></span> <span data-ttu-id="cf1dd-106">Les utilisateurs peuvent trouver des images en effectuant une recherche sur les balises d’images.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-106">Users can find images through search by searching on the image tags.</span></span>

<span data-ttu-id="cf1dd-107">Lorsqu’un utilisateur charge une image, le processus de balisage s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-107">When a user uploads an image, the  tagging process runs automatically.</span></span> <span data-ttu-id="cf1dd-108">Si une image est modifiée, le processus de balisage s’exécute à nouveau pour la mise à jour des balises.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-108">If an image is edited, the tagging process runs again to update the tags.</span></span>

<span data-ttu-id="cf1dd-109">Les utilisateurs disposant d’autorisations sur le fichier image peuvent consulter et modifier les balises dans le volet d’informations sur le fichier ou dans la page des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-109">Users with permissions to the image file can see and edit the tags in the file information panel or in the search results page.</span></span> <span data-ttu-id="cf1dd-110">Une fois qu’un utilisateur modifie les balises d’une image, le système n’effectue plus le balisage automatique sur cette image, même dans le cas où elle est modifiée.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-110">Once a user edits an image's tags, the system no longer performs auto-tagging on that image, even if it is edited.</span></span>

<span data-ttu-id="cf1dd-111">Si vous désactivez l’option de balisage, les images ne seront plus marquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-111">If you turn tagging off, images will no longer be automatically tagged.</span></span> <span data-ttu-id="cf1dd-112">Les balises existantes ne seront pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-112">Existing tags will not be removed.</span></span>

## <a name="configure-image-tagging"></a><span data-ttu-id="cf1dd-113">Configurer le balisage d’image</span><span class="sxs-lookup"><span data-stu-id="cf1dd-113">Configure image tagging</span></span>

<span data-ttu-id="cf1dd-114">Vous pouvez configurer le balisage d’images dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-114">You can configure image tagging in the Microsoft 365 admin center.</span></span>  

<span data-ttu-id="cf1dd-115">Pour activer ou désactiver le balisage d’images</span><span class="sxs-lookup"><span data-stu-id="cf1dd-115">To turn image tagging on or off</span></span>

1. <span data-ttu-id="cf1dd-116">Dans le Centre d’administration Microsoft 365, cliquez sur **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-116">In the Microsoft 365 admin center, click **Setup**.</span></span>

2. <span data-ttu-id="cf1dd-117">Sous **Connaissances organisationnelles**, cliquez sur **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-117">Under **Organizational knowledge**, click **Automate content understanding**.</span></span>

3. <span data-ttu-id="cf1dd-118">Cliquez sur **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-118">Click **Manage**.</span></span>

4. <span data-ttu-id="cf1dd-119">Sous l’onglet **Balisage d'image**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-119">On the **Image tagging** tab, click **Edit**.</span></span>

5. <span data-ttu-id="cf1dd-120">Choisissez d’autoriser le **Balisage d’image** ou de le **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-120">Choose to allow **Basic tagging** or turn tagging **Off**.</span></span>

6. <span data-ttu-id="cf1dd-121">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="cf1dd-121">Click **Save**.</span></span>

    ![Capture d’écran du contrôle de balisage d’image](../media/content-understanding/sharepoint-syntex-image-tagging-control.png)

## <a name="see-also"></a><span data-ttu-id="cf1dd-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf1dd-123">See also</span></span>

[<span data-ttu-id="cf1dd-124">Configurer la compréhension de contenu</span><span class="sxs-lookup"><span data-stu-id="cf1dd-124">Set up content understanding</span></span>](set-up-content-understanding.md)