---
title: Balisage d’image dans SharePoint Syntex
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Présentation du balisage d’image dans SharePoint Syntex
ms.openlocfilehash: c6d7513db2fd6aadabe5d813f3b49073a8f8c933
ms.sourcegitcommit: 5e1b8c959a081022826fb09358730096248507ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2020
ms.locfileid: "48413733"
---
# <a name="image-tagging-in-sharepoint-syntex"></a><span data-ttu-id="7f4ca-103">Balisage d’image dans SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="7f4ca-103">Image tagging in SharePoint Syntex</span></span>

<span data-ttu-id="7f4ca-104">(Bientôt disponible)</span><span class="sxs-lookup"><span data-stu-id="7f4ca-104">(Coming soon)</span></span>

<span data-ttu-id="7f4ca-105">Le balisage d’image dans SharePoint Syntex permet aux utilisateurs de trouver des images en effectuant une recherche sur des balises d’image, puis de créer des flux de travail en fonction de balises d’image.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-105">With image tagging in SharePoint Syntex, users can find images through search by searching on image tags, and create workflows based on image tags.</span></span> <span data-ttu-id="7f4ca-106">Par défaut, le balisage de base des images est activé pour SharePoint et OneDrive.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-106">By default, basic image tagging is turned on for SharePoint and OneDrive.</span></span> <span data-ttu-id="7f4ca-107">Les images chargées dans l’un des emplacements sont automatiquement analysées et des balises valables sont appliquées, le cas échéant, à partir d’une liste de 37 balises de base.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-107">Images uploaded to either location are automatically scanned and applicable tags are applied, if available, from a list of 37 basic tags.</span></span> <span data-ttu-id="7f4ca-108">Les utilisateurs peuvent trouver des images en effectuant une recherche sur les balises d’images.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-108">Users can find images through search by searching on the image tags.</span></span>

<span data-ttu-id="7f4ca-109">Lorsqu’un utilisateur charge une image, le processus de balisage s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-109">When a user uploads an image, the  tagging process runs automatically.</span></span> <span data-ttu-id="7f4ca-110">Si une image est modifiée, le processus de balisage s’exécute à nouveau pour la mise à jour des balises.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-110">If an image is edited, the tagging process runs again to update the tags.</span></span>

<span data-ttu-id="7f4ca-111">Les utilisateurs disposant d’autorisations sur le fichier image peuvent consulter et modifier les balises dans le volet d’informations sur le fichier ou dans la page des résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-111">Users with permissions to the image file can see and edit the tags in the file information panel or in the search results page.</span></span> <span data-ttu-id="7f4ca-112">Dès qu’un utilisateur modifie les balises d’une image, le système n’effectue plus le balisage automatique de cette image, même en cas de modification.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-112">Once a user edits an image's tags, the system no longer auto-tags that image, even if it's edited.</span></span>

<span data-ttu-id="7f4ca-113">Si vous désactivez l’option de balisage, les images ne seront plus marquées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-113">If you turn tagging off, images will no longer be automatically tagged.</span></span> <span data-ttu-id="7f4ca-114">Les balises existantes ne seront pas supprimées.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-114">Existing tags won't be removed.</span></span>

> [!NOTE]
> <span data-ttu-id="7f4ca-115">Les balises générées par le système peuvent changer avec les mises à jour de l’image ou notre technologie de balises.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-115">System generated tags may change with updates to the image or our tag technology.</span></span>


## <a name="configure-image-tagging"></a><span data-ttu-id="7f4ca-116">Configurer le balisage d’image</span><span class="sxs-lookup"><span data-stu-id="7f4ca-116">Configure image tagging</span></span>

<span data-ttu-id="7f4ca-117">Après avoir [configuré SharePoint Syntex](set-up-content-understanding.md), vous pouvez configurer le balisage d’image dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-117">After you [set up SharePoint Syntex](set-up-content-understanding.md), you can configure image tagging in the Microsoft 365 admin center.</span></span>  

<span data-ttu-id="7f4ca-118">Pour activer ou désactiver le balisage d’images</span><span class="sxs-lookup"><span data-stu-id="7f4ca-118">To turn image tagging on or off</span></span>

1. <span data-ttu-id="7f4ca-119">Dans le Centre d’administration Microsoft 365, cliquez sur **Configuration**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-119">In the Microsoft 365 admin center, click **Setup**.</span></span>

2. <span data-ttu-id="7f4ca-120">Sous **Connaissances organisationnelles**, cliquez sur **Automatiser la compréhension de contenu**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-120">Under **Organizational knowledge**, click **Automate content understanding**.</span></span>

3. <span data-ttu-id="7f4ca-121">Cliquez sur **Gérer**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-121">Click **Manage**.</span></span>

4. <span data-ttu-id="7f4ca-122">Sous l’onglet **Balisage d'image**, cliquez sur **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-122">On the **Image tagging** tab, click **Edit**.</span></span>

5. <span data-ttu-id="7f4ca-123">Choisissez d’autoriser le **Balisage d’image** ou de le **Désactiver**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-123">Choose to allow **Basic tagging** or turn tagging **Off**.</span></span>

6. <span data-ttu-id="7f4ca-124">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="7f4ca-124">Click **Save**.</span></span>

    ![Capture d’écran du contrôle de balisage d’image](../media/content-understanding/sharepoint-syntex-image-tagging-control.png)
