---
title: Envoyer (push) des types de contenu à un hub
description: Découvrez comment envoyer (push) des types de contenu à un hub
ms.author: mikeplum
author: MikePlumleyMSFT
manager: serdars
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
ms.openlocfilehash: d64dd5ab49d371df075f1044024c12fbf78e265c
ms.sourcegitcommit: e7bf23df4852b78912229d1d38ec475223597f34
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49087606"
---
# <a name="push-content-types-to-a-hub"></a><span data-ttu-id="70636-103">Envoyer (push) des types de contenu à un hub</span><span class="sxs-lookup"><span data-stu-id="70636-103">Push content types to a hub</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4GyeV]  

</br>


<span data-ttu-id="70636-104">Pour mettre les types de contenu importants systématiquement à la disposition des bibliothèques et des listes SharePoint, vous pouvez les pousser vers les hubs de votre choix.</span><span class="sxs-lookup"><span data-stu-id="70636-104">To make important content types more consistently available to SharePoint libraries and lists, you can push them to the hubs that you choose.</span></span> <span data-ttu-id="70636-105">Cela permet de les ajouter automatiquement à toutes les listes et bibliothèques créées sur les sites associés au hub, ainsi qu’à tous les nouveaux sites ajoutés à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="70636-105">This automatically adds them to any new lists and libraries created on the sites associated with the hub, and to any new sites added to the hub.</span></span>

<span data-ttu-id="70636-106">Pour que cette fonctionnalité soit opérationnelle, les types de contenu envoyés par commande push doivent être déjà publiés.</span><span class="sxs-lookup"><span data-stu-id="70636-106">For this feature to work, The content types being pushed must already be published.</span></span>

<span data-ttu-id="70636-107">Pour envoyer (push) des types de contenu à un hub</span><span class="sxs-lookup"><span data-stu-id="70636-107">To push content types to hubs</span></span>

1. <span data-ttu-id="70636-108">Dans le Centre d’administration SharePoint, développez **Services de contenu**, puis cliquez sur **Galerie de types de contenus**.</span><span class="sxs-lookup"><span data-stu-id="70636-108">In the SharePoint admin center, expand **Content services**, and then click **Content type gallery**.</span></span>

2. <span data-ttu-id="70636-109">Cliquez sur le type de contenu à envoyer (push) à des hubs.</span><span class="sxs-lookup"><span data-stu-id="70636-109">Click the content type that you want to push to hubs.</span></span>

3. <span data-ttu-id="70636-110">Cliquez sur **Modifier** dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="70636-110">Click **Edit** in the command bar.</span></span>
 
4. <span data-ttu-id="70636-111">Cliquez sur **Choisir les sites hub**.</span><span class="sxs-lookup"><span data-stu-id="70636-111">Click **Choose hub sites**.</span></span>
 
5. <span data-ttu-id="70636-112">Sélectionnez les sites hub de votre choix, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="70636-112">Select the desired hub sites and then click **OK**.</span></span>
 
6. <span data-ttu-id="70636-113">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="70636-113">Click **Save**.</span></span>

<span data-ttu-id="70636-114">Lors du premier envoi (push) d’un type de contenu à un hub existant et à ses sites associés, la mise à jour des paramètres sur le site peut prendre jusqu’à une heure à compter de la visite du hub ou des sites associés.</span><span class="sxs-lookup"><span data-stu-id="70636-114">When pushing a content type to an existing hub & its existing associated sites for the first time, it can take up to an hour from when the hub or associated sites are visited, for the settings to update in the site.</span></span> <span data-ttu-id="70636-115">Pour les nouvelles associations au hub, ce temps d’attente ne sera pas nécessaires, et la prise en compte des paramètres ne prendra que quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="70636-115">Any new associations to the hub will not require this wait and will have the settings reflected in a few minutes.</span></span> 

<span data-ttu-id="70636-116">Une fois le système configuré, le type de contenu avec ces paramètres sera disponible dans tout site récemment associé avec le hub dans quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="70636-116">Once this is configured, the content type with these settings will be available in any newly associated site with the hub in a few minutes.</span></span> <span data-ttu-id="70636-117">Une fois disponible, le type de contenu est automatiquement ajouté à la nouvelle liste ou bibliothèque quelques minutes après la création de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="70636-117">Once available, any new list or library created will have the content type automatically added to it within a few minutes of creation.</span></span> <span data-ttu-id="70636-118">Un type de contenu envoyé (push) est ajouté à une bibliothèque de documents uniquement s’il provient directement ou indirectement du type de contenu Document. D’autre part, un type de contenu est ajouté à une liste uniquement s’il ne provient pas directement ou indirectement du type de contenu Document.</span><span class="sxs-lookup"><span data-stu-id="70636-118">A pushed content type will be added to a document library only if it derives directly or indirectly from the Document content type, and a content type will be added to a list only if it does not derive from the Document content type directly or indirectly.</span></span>

## <a name="see-also"></a><span data-ttu-id="70636-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70636-119">See also</span></span>



  






