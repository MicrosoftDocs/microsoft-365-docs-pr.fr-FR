---
title: Valider les nouveaux appareils
description: Avant de commander des appareils, obtenez l’un de chaque modèle et testez-le.
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: 772636fd72074c8fad30daa3eb25b785519e7772
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52246199"
---
# <a name="validate-new-devices"></a><span data-ttu-id="861c6-103">Valider les nouveaux appareils</span><span class="sxs-lookup"><span data-stu-id="861c6-103">Validate new devices</span></span>

<span data-ttu-id="861c6-104">Que vous débutiez dans Bureau géré Microsoft ou que vous êtes abonné à long terme, il est préférable de tester un exemple de tout modèle d’appareil que vous inscrivez pour la première fois dans le service.</span><span class="sxs-lookup"><span data-stu-id="861c6-104">Whether you're completely new to Microsoft Managed Desktop or a long-time subscriber, it's best to test an example of any device model you're enrolling in the service for the first time.</span></span> <span data-ttu-id="861c6-105">Cela est vrai si vous commandez de nouveaux appareils ou que vous en utilisez des appareils existants, y compris les appareils recommandés pour Bureau géré Microsoft sur le site Shop [Windows 10 Professionnel business devices.](https://www.microsoft.com/windowsforbusiness/view-all-devices)</span><span class="sxs-lookup"><span data-stu-id="861c6-105">This is true whether you're ordering brand-new devices or reusing existing ones, including devices recommended for Microsoft Managed Desktop on the [Shop Windows 10 Pro business devices](https://www.microsoft.com/windowsforbusiness/view-all-devices) site.</span></span> <span data-ttu-id="861c6-106">Sur ce site, affichez les appareils recommandés  pour une  utilisation avec le service en développez les fonctionnalités dans la zone Filtrer par **zone,** puis sélectionnez Bureau géré Microsoft .</span><span class="sxs-lookup"><span data-stu-id="861c6-106">At that site, view the devices recommended for use with the service by expanding **Features** in the **Filter by** area, and then selecting **Microsoft Managed Desktop**.</span></span> <span data-ttu-id="861c6-107">La validation des appareils garantit qu’ils offrent l’expérience utilisateur que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="861c6-107">Validating devices ensures that they'll deliver the user experience you expect.</span></span>

## <a name="validate-devices"></a><span data-ttu-id="861c6-108">Valider les appareils</span><span class="sxs-lookup"><span data-stu-id="861c6-108">Validate devices</span></span>

1. <span data-ttu-id="861c6-109">Prenez un ou plusieurs exemples de nouveaux modèles en suivant les étapes des articles suivants :</span><span class="sxs-lookup"><span data-stu-id="861c6-109">Take one or more examples of new models through the steps in the following articles:</span></span>
    - [<span data-ttu-id="861c6-110">Configurer les appareils Bureau géré Microsoft</span><span class="sxs-lookup"><span data-stu-id="861c6-110">Set up Microsoft Managed Desktop devices</span></span>](set-up-devices.md)
    - [<span data-ttu-id="861c6-111">Localiser l’expérience utilisateur</span><span class="sxs-lookup"><span data-stu-id="861c6-111">Localize the user experience</span></span>](localization.md)
    - [<span data-ttu-id="861c6-112">Expérience de première exécution avec le pilote automatique et la page état d’inscription</span><span class="sxs-lookup"><span data-stu-id="861c6-112">First-run experience with Autopilot and the Enrollment Status Page</span></span>](esp-first-run.md)
    - [<span data-ttu-id="861c6-113">Service d’emplacement Windows 10</span><span class="sxs-lookup"><span data-stu-id="861c6-113">Windows 10 location service</span></span>](device-location.md)
    - [<span data-ttu-id="861c6-114">Prise en main du contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="861c6-114">Get started with app control</span></span>](get-started-app-control.md)
    - [<span data-ttu-id="861c6-115">Déployer les applications sur les appareils</span><span class="sxs-lookup"><span data-stu-id="861c6-115">Deploy apps to devices</span></span>](deploy-apps.md)
2. <span data-ttu-id="861c6-116">Vérifiez que les expériences suivantes fonctionnent sans erreurs, erreurs ou invites :</span><span class="sxs-lookup"><span data-stu-id="861c6-116">Verify that the following experiences work without any failures, errors, or prompts:</span></span>
    - <span data-ttu-id="861c6-117">Expérience Autopilot après avoir rejoint le réseau et l’utilisateur s’est</span><span class="sxs-lookup"><span data-stu-id="861c6-117">The Autopilot experience after joining the network and the user signs in</span></span>
    - <span data-ttu-id="861c6-118">Si vous avez activé la [page](esp-first-run.md)État de l’inscription, cela fonctionne.</span><span class="sxs-lookup"><span data-stu-id="861c6-118">If you've enabled the [Enrollment Status Page](esp-first-run.md), it works.</span></span>
    - <span data-ttu-id="861c6-119">L’utilisateur peut se Office applications</span><span class="sxs-lookup"><span data-stu-id="861c6-119">User can sign into to Office applications</span></span>
    - <span data-ttu-id="861c6-120">OneDrive synchronisation des dossiers, notamment Windows Bureau, Documents et Images</span><span class="sxs-lookup"><span data-stu-id="861c6-120">OneDrive folders sync, including Windows Desktop, Documents, and Pictures</span></span>
    - <span data-ttu-id="861c6-121">L’appareil reçoit les mises à jour, les stratégies et les applications métier</span><span class="sxs-lookup"><span data-stu-id="861c6-121">Device receives updates, policies, and line-of-business applications</span></span>
3. <span data-ttu-id="861c6-122">Examinez les appareils signalés et la configuration matérielle requise dans le rapport [d’inventaire](../working-with-managed-desktop/device-inventory-report.md) des appareils pour vérifier qu’ils correspondent à ce que vous attendez.</span><span class="sxs-lookup"><span data-stu-id="861c6-122">Review the reported devices and hardware requirements in the [Device inventory report](../working-with-managed-desktop/device-inventory-report.md) to check that they match what you expect.</span></span>

<span data-ttu-id="861c6-123">Si des problèmes se produisent, vous pouvez demander [de l’aide](../working-with-managed-desktop/admin-support.md) dans le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="861c6-123">If any problems occur, you can [request support](../working-with-managed-desktop/admin-support.md) in the Admin portal.</span></span>

<span data-ttu-id="861c6-124">Si tout se passe bien, vous êtes prêt à commander le reste des appareils validés dont vous avez besoin pour votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="861c6-124">If everything goes well, you're ready to order the rest of the validated devices you need for your deployment.</span></span>