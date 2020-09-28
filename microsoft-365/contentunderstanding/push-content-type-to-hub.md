---
title: Envoi de types de contenu vers un concentrateur
description: Découvrez comment diffuser des types de contenu vers un concentrateur
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: a852207bfd1a2a7643ce8895a533371d194954cf
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48295900"
---
# <a name="push-content-types-to-a-hub"></a><span data-ttu-id="51c73-103">Envoi de types de contenu vers un concentrateur</span><span class="sxs-lookup"><span data-stu-id="51c73-103">Push content types to a hub</span></span>

<span data-ttu-id="51c73-104">Pour rendre les types de contenu importants plus cohérents disponibles pour les bibliothèques et les listes SharePoint, vous pouvez les envoyer aux concentrateurs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="51c73-104">To make important content types more consistently available to SharePoint libraries and lists, you can push them to the hubs that you choose.</span></span> <span data-ttu-id="51c73-105">Cela les ajoute automatiquement aux nouvelles listes et bibliothèques créées sur les sites associés au concentrateur, ainsi qu’aux nouveaux sites ajoutés au Hub.</span><span class="sxs-lookup"><span data-stu-id="51c73-105">This automatically adds them to any new lists and libraries created on the sites associated with the hub, and to any new sites added to the hub.</span></span>

<span data-ttu-id="51c73-106">Pour que cette fonctionnalité fonctionne, les types de contenu en cours d’envoi doivent déjà être publiés.</span><span class="sxs-lookup"><span data-stu-id="51c73-106">For this feature to work, The content types being pushed must already be published.</span></span>

<span data-ttu-id="51c73-107">Pour envoyer des types de contenu vers des concentrateurs</span><span class="sxs-lookup"><span data-stu-id="51c73-107">To push content types to hubs</span></span>

1. <span data-ttu-id="51c73-108">Dans le centre d’administration SharePoint, développez **services de contenu**, puis cliquez sur Galerie de **types de contenu**.</span><span class="sxs-lookup"><span data-stu-id="51c73-108">In the SharePoint admin center, expand **Content services**, and then click **Content type gallery**.</span></span>

2. <span data-ttu-id="51c73-109">Cliquez sur le type de contenu que vous souhaitez envoyer aux hubs.</span><span class="sxs-lookup"><span data-stu-id="51c73-109">Click the content type that you want to push to hubs.</span></span>

3. <span data-ttu-id="51c73-110">Cliquez sur **modifier** dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="51c73-110">Click **Edit** in the command bar.</span></span>
 
4. <span data-ttu-id="51c73-111">Cliquez sur **choisir des sites hub**.</span><span class="sxs-lookup"><span data-stu-id="51c73-111">Click **Choose hub sites**.</span></span>
 
5. <span data-ttu-id="51c73-112">Sélectionnez les sites hub souhaités, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="51c73-112">Select the desired hub sites and then click **OK**.</span></span>
 
6. <span data-ttu-id="51c73-113">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="51c73-113">Click **Save**.</span></span>

<span data-ttu-id="51c73-114">Lorsque vous transmettez un type de contenu à un concentrateur existant & les sites associés existants pour la première fois, il peut prendre jusqu’à une heure après avoir consulté le Hub ou les sites associés pour que les paramètres soient mis à jour dans le site.</span><span class="sxs-lookup"><span data-stu-id="51c73-114">When pushing a content type to an existing hub & its existing associated sites for the first time, it can take up to an hour from when the hub or associated sites are visited, for the settings to update in the site.</span></span> <span data-ttu-id="51c73-115">Les nouvelles associations au hub ne nécessitent pas cette attente et les paramètres seront reflétés dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="51c73-115">Any new associations to the hub will not require this wait and will have the settings reflected in a few minutes.</span></span> 

<span data-ttu-id="51c73-116">Une fois cette configuration effectuée, le type de contenu avec ces paramètres sera disponible dans tout site nouvellement associé avec le Hub dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="51c73-116">Once this is configured, the content type with these settings will be available in any newly associated site with the hub in a few minutes.</span></span> <span data-ttu-id="51c73-117">Une fois la nouvelle liste ou bibliothèque créée, le type de contenu est ajouté automatiquement dans quelques minutes de création.</span><span class="sxs-lookup"><span data-stu-id="51c73-117">Once available, any new list or library created will have the content type automatically added to it within a few minutes of creation.</span></span> <span data-ttu-id="51c73-118">Un type de contenu push est ajouté à une bibliothèque de documents uniquement s’il est dérivé directement ou indirectement du type de contenu document, et un type de contenu est ajouté à une liste uniquement s’il ne dérive pas directement ou indirectement du type de contenu de document.</span><span class="sxs-lookup"><span data-stu-id="51c73-118">A pushed content type will be added to a document library only if it derives directly or indirectly from the Document content type, and a content type will be added to a list only if it does not derive from the Document content type directly or indirectly.</span></span>

## <a name="see-also"></a><span data-ttu-id="51c73-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51c73-119">See also</span></span>



  






