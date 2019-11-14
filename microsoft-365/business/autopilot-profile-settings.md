---
title: À propos des paramètres du profil AutoPilot
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
f1_keywords:
- ZTDProfileSettings
- O365E_ZTDProfileSettings
- BCS365_ZTDProfileSettings
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: Les profils AutoPilot vous permettent de contrôler la manière dont Windows est installé sur les appareils utilisateur. Les profils contiennent des paramètres par défaut et facultatifs, comme ignorer l’installation de Cortana.
ms.openlocfilehash: 912a24e3d458986a4bcf7dcf903f80211996aca2
ms.sourcegitcommit: 8193b7da5b1a415835d02ca96883c351df7326ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38321782"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="cc6af-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="cc6af-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="cc6af-105">Paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="cc6af-105">AutoPilot profile settings</span></span>

<span data-ttu-id="cc6af-106">Vous pouvez utiliser les profils AutoPilot pour contrôler la façon dont Windows est installé sur les appareils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cc6af-106">You can use AutoPilot profiles to control how Windows is installed on user devices.</span></span> <span data-ttu-id="cc6af-107">Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="cc6af-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="cc6af-108">**Les fonctionnalités de AutoPilot par défaut (obligatoires) qui sont définies automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="cc6af-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="cc6af-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="cc6af-109">**Setting**</span></span>|<span data-ttu-id="cc6af-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc6af-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc6af-111">Ignorer l’inscription de Cortana, OneDrive et OEM</span><span class="sxs-lookup"><span data-stu-id="cc6af-111">Skip Cortana, OneDrive, and OEM registration</span></span>  <br/> |<span data-ttu-id="cc6af-112">Ignore l’installation des applications grand public telles que Cortana et OneDrive personnel.</span><span class="sxs-lookup"><span data-stu-id="cc6af-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="cc6af-113">L’utilisateur de l’appareil peut l’installer ultérieurement tant que l’utilisateur est un administrateur local sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cc6af-113">The device user can install these later as long as the user is a local admin on the device.</span></span> <span data-ttu-id="cc6af-114">L’enregistrement du fabricant d’origine est ignoré car le périphérique sera géré par Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="cc6af-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="cc6af-115">Expérience de connexion avec la marque de votre entreprise</span><span class="sxs-lookup"><span data-stu-id="cc6af-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="cc6af-116">Si votre société dispose d’une [page de connexion Add Your Company to Office 365 Signing](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), l’utilisateur de l’appareil obtiendra cette expérience lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="cc6af-116">If your company has a [Add your company branding to Office 365 Sign In page](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="cc6af-117">Auto-inscriptions MDM avec comptes AAD configurés.</span><span class="sxs-lookup"><span data-stu-id="cc6af-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="cc6af-118">L’identité de l’utilisateur sera gérée par Azure Active Directory, et les utilisateurs se connecteront à Windows et Office 365 avec leurs informations d’identification d’entreprise Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cc6af-118">The user identity will be managed by Azure Active Directory, and users will sign in to Windows and Office 365 with their Microsoft 365 Business credentials.</span></span>  <br/> |
   
 <span data-ttu-id="cc6af-119">**Paramètres facultatifs :**</span><span class="sxs-lookup"><span data-stu-id="cc6af-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="cc6af-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="cc6af-120">**Setting**</span></span>|<span data-ttu-id="cc6af-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc6af-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cc6af-122">Ignorer les paramètres de confidentialité (désactivés par défaut)</span><span class="sxs-lookup"><span data-stu-id="cc6af-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="cc6af-123">Si cette option est **activée**, l’utilisateur de l’appareil ne verra pas le contrat de licence du périphérique et de Windows lorsqu’il se connecte pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="cc6af-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="cc6af-124">Ne pas autoriser l’utilisateur à devenir l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="cc6af-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="cc6af-125">Si cette option est **activée**, l’utilisateur de l’appareil ne peut pas installer d’applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="cc6af-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span><br/> |
   
