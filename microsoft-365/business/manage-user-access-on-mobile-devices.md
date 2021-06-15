---
title: Gérer les accès des utilisateurs aux documents Office sur appareils mobiles
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
manager: scotv
audience: Admin
ms.topic: conceptual
f1_keywords:
- O365E_BCSSetup4OfficeMobile
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: aa31319c-9196-48c9-a90b-4057e0494c7a
description: Découvrez les stratégies de protection qui vous permettent de gérer la façon dont les utilisateurs accèdent Office applications et les fichiers de travail à partir d’appareils mobiles.
ms.openlocfilehash: 7602b712f2dfc3ba369fd76979baaaa8d5da5c5c
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925276"
---
# <a name="manage-how-users-access-office-documents-on-mobile-devices"></a><span data-ttu-id="1c2d4-103">Gérer les accès des utilisateurs aux documents Office sur appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1c2d4-103">Manage how users access Office documents on mobile devices</span></span>

<span data-ttu-id="1c2d4-104">Cet article s’applique aux Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="1c2d4-105">[] Les paramètres de stratégie qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office à partir de leur appareil mobile sont **désactivés** par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-105">Policy settings that control how users access Office files from their mobile devices are **Off** by default.</span></span> <span data-ttu-id="1c2d4-106">Nous vous recommandons d’accepter les valeurs par défaut lors de l’installation pour créer des stratégies d’application pour Android, iOS et Windows 10 qui s’appliquent à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-106">We recommend that you accept the default values during setup to create application policies for Android, iOS, and Windows 10 that apply to all users.</span></span> <span data-ttu-id="1c2d4-107">Vous pouvez créer des stratégies supplémentaires une fois l'installation terminée.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-107">You can create more policies after setup completes.</span></span> 
  
## <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="1c2d4-108">Paramètres qui contrôlent la façon dont les utilisateurs accèdent aux fichiers Office sur appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="1c2d4-108">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="1c2d4-109">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :</span><span class="sxs-lookup"><span data-stu-id="1c2d4-109">The following settings are available to manage how users access Office work files:</span></span>

|<span data-ttu-id="1c2d4-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1c2d4-110">Setting</span></span>  <br/> |<span data-ttu-id="1c2d4-111">Description</span><span class="sxs-lookup"><span data-stu-id="1c2d4-111">Description</span></span>  <br/> |
|:-----|:-----|
|<span data-ttu-id="1c2d4-112">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="1c2d4-112">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="1c2d4-113">Si ce paramètre est sur **,** les utilisateurs doivent fournir une autre forme d’authentification, en plus de leur nom d’utilisateur et mot de passe, avant de pouvoir utiliser des applications Office sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-113">If this setting is **On**, users must provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="1c2d4-114">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="1c2d4-114">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="1c2d4-115">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-115">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="1c2d4-116">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="1c2d4-116">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="1c2d4-117">Ce paramètre détermine la durée pendant combien de temps un utilisateur peut être inactif avant d’être invité à se ré-inscrire.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-117">This setting determines how long a user can be idle before they're prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="1c2d4-118">Refuser l'accès aux fichiers de travail sur les appareils « jailbreakés » ou débridés</span><span class="sxs-lookup"><span data-stu-id="1c2d4-118">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="1c2d4-119">Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-119">Clever users may have a device that is jailbroken or rooted.</span></span> <span data-ttu-id="1c2d4-120">Cela signifie que l’utilisateur peut modifier le système d’exploitation, ce qui peut rendre l’appareil plus susceptible d’être malveillant.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-120">This means that the user can modify the operating system, which can make the device more susceptible to malware.</span></span> <span data-ttu-id="1c2d4-121">Ces appareils sont bloqués lorsque ce paramètre est **activé**.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-121">These devices are blocked when this setting is **On**.</span></span>  <br/> |
|<span data-ttu-id="1c2d4-122">Ne pas autoriser les utilisateurs à copier le contenu de Office applications dans des applications personnelles</span><span class="sxs-lookup"><span data-stu-id="1c2d4-122">Don't allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="1c2d4-123">Lorsque le paramètre est **sur ,** l’utilisateur ne peut pas copier les informations d’un fichier de travail dans un fichier personnel.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-123">When the setting is **On**, the user can't copy information in a work file to a personal file.</span></span> <span data-ttu-id="1c2d4-124">Si le paramètre est **Éteint,** l’utilisateur peut copier les informations d’un fichier de travail vers une application personnelle ou un compte personnel.</span><span class="sxs-lookup"><span data-stu-id="1c2d4-124">If the setting is **Off**, the user can copy information from a work file to a personal app or personal account.</span></span>  <br/> |
   

