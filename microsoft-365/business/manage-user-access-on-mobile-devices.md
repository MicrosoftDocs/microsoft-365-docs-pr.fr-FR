---
title: Gérer les accès des utilisateurs aux documents Office sur appareils mobiles
ms.author: sirkkuw
author: sirkkuw
manager: scotv
ms.audience: Admin
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: aa31319c-9196-48c9-a90b-4057e0494c7a
description: Découvrez les stratégies de protection qui peuvent aider à sécuriser l’accès aux applications Office à partir d’appareils mobiles.
ms.openlocfilehash: b49ec33f4899a25f92ffd9d7a25d3e435016749e
ms.sourcegitcommit: db1dfb2df2c2f7beced3b57bc772d106c189e88a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "33660325"
---
# <a name="manage-how-users-access-office-documents-on-mobile-devices"></a><span data-ttu-id="fa23e-103">Gérer les accès des utilisateurs aux documents Office sur appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="fa23e-103">Manage how users access Office documents on mobile devices</span></span>

 <span data-ttu-id="fa23e-p101">[] Les paramètres de stratégie qui contrôlent la manière dont les utilisateurs accèdent aux fichiers Office à partir de leur appareil mobile sont **désactivés** par défaut. Nous vous recommandons d'accepter les valeurs par défaut lors de l'installation pour créer des stratégies d'application pour Windows 10, iOS et Android qui s'appliquent à tous les utilisateurs. Vous pouvez créer des stratégies supplémentaires une fois l'installation terminée.</span><span class="sxs-lookup"><span data-stu-id="fa23e-p101">Policy settings that control how users access Office files from their mobile devices are **Off** by default. We recommend you accept the default values during setup to create application policies for Android, iOS, and Windows 10 that apply to all users. You can create more policies after setup completes.</span></span> 
  
## <a name="settings-that-control-how-users-access-office-files-on-mobile-devices"></a><span data-ttu-id="fa23e-107">Paramètres qui contrôlent la façon dont les utilisateurs accèdent aux fichiers Office sur appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="fa23e-107">Settings that control how users access Office files on mobile devices</span></span>

<span data-ttu-id="fa23e-108">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office :</span><span class="sxs-lookup"><span data-stu-id="fa23e-108">The following settings are available to manage how users access Office work files:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fa23e-109">Setting</span><span class="sxs-lookup"><span data-stu-id="fa23e-109">Setting</span></span>  <br/> |<span data-ttu-id="fa23e-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa23e-110">Description</span></span>  <br/> |
|<span data-ttu-id="fa23e-111">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="fa23e-111">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="fa23e-112">Si ce paramètre est **activé**, les utilisateurs doivent fournir une autre forme d'authentification, en plus de leur nom d'utilisateur et de leur mot de passe, pour pouvoir utiliser les applications Office sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="fa23e-112">If this settings is **On** users have to provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="fa23e-113">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="fa23e-113">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="fa23e-114">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="fa23e-114">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="fa23e-115">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="fa23e-115">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="fa23e-116">Ce paramètre détermine combien de temps un utilisateur peut être inactif avant d'être invité à se connecter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="fa23e-116">This setting determines how long a user can be idle before they are prompted to sign in again.</span></span>  <br/> |
|<span data-ttu-id="fa23e-117">Refuser l'accès aux fichiers de travail sur les appareils « jailbreakés » ou débridés</span><span class="sxs-lookup"><span data-stu-id="fa23e-117">Deny access to work files on jailbroken or rooted devices</span></span>  <br/> |<span data-ttu-id="fa23e-p102">Les utilisateurs intelligents peuvent avoir un appareil jailbreaké ou rooté. Cela signifie que l'utilisateur est en mesure de modifier le système d'exploitation, ce qui peut rendre l'appareil plus vulnérable aux logiciels malveillants. Ces appareils sont bloqués lorsque ce paramètre est **activé**.  </span><span class="sxs-lookup"><span data-stu-id="fa23e-p102">Clever users may have a device that is jailbroken or rooted. This means that the user can modify the operating system, which can make the device more subject to malware. These devices are blocked when this setting is **On**.  </span></span><br/> |
|<span data-ttu-id="fa23e-121">Ne pas autoriser les utilisateurs à copier le contenu des applications Office dans des applications personnelles</span><span class="sxs-lookup"><span data-stu-id="fa23e-121">Don't allow users to copy content from Office apps into personal apps</span></span>  <br/> |<span data-ttu-id="fa23e-122">Lorsque le paramètre est **activé**, l’utilisateur ne peut pas copier les informations d’un fichier de travail dans un fichier personnel.</span><span class="sxs-lookup"><span data-stu-id="fa23e-122">When the setting is **On**, the user can't copy information in a work file to a personal file.</span></span> <span data-ttu-id="fa23e-123">Si le paramètre est **désactivé**, l’utilisateur peut copier des informations à partir d’un fichier de travail vers une application personnelle ou un compte personnel.</span><span class="sxs-lookup"><span data-stu-id="fa23e-123">If the setting is **Off**, the user can copy information from a work file to a personal app or personal account.</span></span>  <br/> |
   

