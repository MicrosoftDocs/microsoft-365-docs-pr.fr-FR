---
title: Ajouter un domaine
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment ajouter un autre domaine à votre abonnement.
ms.openlocfilehash: 16f6c4e416ede560d69014e320eb32c4453fd3f5
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702169"
---
# <a name="add-another-domain"></a><span data-ttu-id="c36fa-103">Ajouter un autre domaine</span><span class="sxs-lookup"><span data-stu-id="c36fa-103">Add another domain</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4dN8c?autoplay=false]

<span data-ttu-id="c36fa-104">Il se peut que votre société ait besoin de plusieurs noms de domaine à des fins différentes.</span><span class="sxs-lookup"><span data-stu-id="c36fa-104">Your company might need multiple domain names for different purposes.</span></span> <span data-ttu-id="c36fa-105">Par exemple, vous pouvez ajouter une orthographe différente du nom de votre société car les clients l’utilisent déjà et leurs communications n’ont pas pu vous joindre.</span><span class="sxs-lookup"><span data-stu-id="c36fa-105">For example, you might want to add a different spelling of your company name because customers are already using it and their communications have failed to reach you.</span></span>

## <a name="try-it"></a><span data-ttu-id="c36fa-106">Essayez !</span><span class="sxs-lookup"><span data-stu-id="c36fa-106">Try it!</span></span>

1. <span data-ttu-id="c36fa-107">Dans le centre d’administration Microsoft 365, sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-107">In the Microsoft 365 admin center, choose **Setup**.</span></span>
1. <span data-ttu-id="c36fa-108">Sous **obtenir votre configuration de domaine personnalisé**, sélectionnez **Afficher**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-108">Under **Get your custom domain set up**, select **View**.</span></span>
1. <span data-ttu-id="c36fa-109">Cliquez sur **gérer**, puis sur **Ajouter un domaine**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-109">Choose **Manage**, and then **Add domain**.</span></span>
1. <span data-ttu-id="c36fa-110">Entrez le nouveau nom de domaine que vous souhaitez ajouter, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-110">Enter the new domain name that you want to add, and then select **Next**.</span></span>
1. <span data-ttu-id="c36fa-111">Connectez-vous à votre bureau d’enregistrement de domaines, dans ce cas GoDaddy, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-111">Sign in to your domain registrar, in this case GoDaddy, and then select **Next**.</span></span>
1. <span data-ttu-id="c36fa-112">Si vous y êtes invité, connectez-vous à votre bureau d’enregistrement, puis choisissez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-112">If prompted, sign in to your registrar, and then choose **Authorize**.</span></span>
1. <span data-ttu-id="c36fa-113">Choisissez **Ajouter les enregistrements DNS pour moi**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-113">Choose **Add the DNS records for me**, and then select **Next**.</span></span>
1. <span data-ttu-id="c36fa-114">Choisissez les services pour votre nouveau domaine et désactivez les cases à cocher des services qui seront gérés par un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="c36fa-114">Choose the services for your new domain and clear the check boxes for any services that will be handled by a different domain.</span></span> <span data-ttu-id="c36fa-115">Par exemple, si vous souhaitez simplement utiliser le nouveau domaine pour le courrier électronique, choisissez **Exchange**, puis désactivez les cases à cocher de la gestion des appareils **Skype entreprise** et de la **gestion des appareils mobiles pour Office 365**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-115">For example, if you just want to use the new domain for email, choose **Exchange**, and clear the check boxes for **Skype for Business** and **Mobile Device Management for Office 365**.</span></span>
1. <span data-ttu-id="c36fa-116">Sélectionnez **suivant**, **autoriser**, **suivant**, puis **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-116">Select **Next**, **Authorize**, **Next**,and then **Finish**.</span></span> <span data-ttu-id="c36fa-117">Votre nouveau domaine a été ajouté.</span><span class="sxs-lookup"><span data-stu-id="c36fa-117">Your new domain has been added.</span></span>

<span data-ttu-id="c36fa-118">Pour recevoir des courriers électroniques dans votre nouveau domaine, vous devez ajouter un nouvel alias de messagerie pour chaque utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c36fa-118">To receive email at your new domain, you'll need to add a new email alias for each user:</span></span>

1. <span data-ttu-id="c36fa-119">Sélectionnez **utilisateurs**, **utilisateurs actifs**, puis sélectionnez l’utilisateur auquel le nouvel alias sera affecté.</span><span class="sxs-lookup"><span data-stu-id="c36fa-119">Select **Users**, **Active users**, and then select the user who will be assigned the new alias.</span></span>
1. <span data-ttu-id="c36fa-120">Choisissez **gérer les alias de messagerie**, puis **Ajoutez un alias**.</span><span class="sxs-lookup"><span data-stu-id="c36fa-120">Choose **Manage email aliases**, and then **Add an alias**.</span></span>
1. <span data-ttu-id="c36fa-121">Entrez le nom d’utilisateur, puis choisissez le nouveau domaine dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="c36fa-121">Enter the username, and then choose the new domain from the drop-down list.</span></span>
1. <span data-ttu-id="c36fa-122">Sélectionnez **enregistrer les modifications**, puis fermez la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c36fa-122">Select **Save changes**, and then close the window.</span></span>
1. <span data-ttu-id="c36fa-123">Répétez ces étapes pour chaque utilisateur qui doit recevoir des courriers électroniques sur le nouveau domaine.</span><span class="sxs-lookup"><span data-stu-id="c36fa-123">Repeat these steps for each user who should receive email at the new domain.</span></span>