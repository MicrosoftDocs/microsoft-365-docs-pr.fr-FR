---
title: Noms de l’appareil
description: Comment Bureau géré Microsoft gestion des noms d’appareils
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
ms.openlocfilehash: adf4809e0d8dc29f170475435b19092abf2062fd
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893894"
---
# <a name="device-names"></a><span data-ttu-id="1ef35-103">Noms de l’appareil</span><span class="sxs-lookup"><span data-stu-id="1ef35-103">Device names</span></span>

<span data-ttu-id="1ef35-104">Bureau géré Microsoft utilise Windows Autopilot, Azure Active Directory et Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="1ef35-104">Microsoft Managed Desktop uses Windows Autopilot, Azure Active Directory, and Microsoft Intune.</span></span> <span data-ttu-id="1ef35-105">Pour que ces services fonctionnent ensemble en toute transparence, les appareils ont besoin de noms cohérents et normalisés.</span><span class="sxs-lookup"><span data-stu-id="1ef35-105">For these services to work together seamlessly, devices need consistent, standardized names.</span></span> <span data-ttu-id="1ef35-106">Bureau géré Microsoft un format de nom standardisé (au format *MMD-%RAND11)* lorsque les appareils sont inscrits.</span><span class="sxs-lookup"><span data-stu-id="1ef35-106">Microsoft Managed Desktop applies a standardized name format (of the form *MMD-%RAND11*) when devices are enrolled.</span></span> <span data-ttu-id="1ef35-107">Windows Autopilot attribue ces noms.</span><span class="sxs-lookup"><span data-stu-id="1ef35-107">Windows Autopilot assigns these names.</span></span> <span data-ttu-id="1ef35-108">Pour plus d’informations sur Autopilot, voir l’expérience de première expérience avec Autopilot et la page État de [l’inscription.](../get-started/esp-first-run.md)</span><span class="sxs-lookup"><span data-stu-id="1ef35-108">For more information about Autopilot, see [First-run experience with Autopilot and the Enrollment Status Page](../get-started/esp-first-run.md).</span></span>

## <a name="automated-name-changes"></a><span data-ttu-id="1ef35-109">Modifications automatiques de noms</span><span class="sxs-lookup"><span data-stu-id="1ef35-109">Automated name changes</span></span>

<span data-ttu-id="1ef35-110">Si un appareil est renommé ultérieurement, Bureau géré Microsoft le renommera automatiquement en un nouveau nom au format standardisé.</span><span class="sxs-lookup"><span data-stu-id="1ef35-110">If a device gets renamed later, Microsoft Managed Desktop will automatically rename it to a new name in the standardized format.</span></span> <span data-ttu-id="1ef35-111">Ce processus se produit toutes les quatre heures.</span><span class="sxs-lookup"><span data-stu-id="1ef35-111">This process occurs every four hours.</span></span> <span data-ttu-id="1ef35-112">Le changement de nom a lieu lors du prochain redémarrage de l’appareil par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ef35-112">The name change takes place the next time the user restarts the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ef35-113">Si votre environnement dépend de noms d’appareils spécifiques (par exemple, pour prendre en charge une configuration réseau particulière), vous devez examiner les options pour supprimer cette dépendance avant de vous inscrire à Bureau géré Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1ef35-113">If your environment depends on specific device names (for example, to support a particular network configuration), you should investigate options to remove that dependency before enrolling in Microsoft Managed Desktop.</span></span> <span data-ttu-id="1ef35-114">Si vous devez conserver la dépendance de nom, [](../working-with-managed-desktop/admin-support.md) vous pouvez envoyer une demande via le portail d’administration pour désactiver la fonction de changement de nom et utiliser le format de nom souhaité.</span><span class="sxs-lookup"><span data-stu-id="1ef35-114">If you must keep the name dependency, you can submit a request through the [Admin portal](../working-with-managed-desktop/admin-support.md) to disable the renaming function and use your desired name format.</span></span>