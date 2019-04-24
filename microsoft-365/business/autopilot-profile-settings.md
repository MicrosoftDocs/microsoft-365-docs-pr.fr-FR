---
title: À propos des paramètres du profil AutoPilot
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: Les profils autoPilot vous permettent de contrôler la manière dont Windows est installé sur les appareils utilisateur. Les profils contiennent des paramètres par défaut et facultatifs, comme ignorer l'installation de Cortana.
ms.openlocfilehash: d43a15e5f3dc83596b5c23dd0ceb416b24810298
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32276938"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="537b9-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="537b9-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="537b9-105">Paramètres du profil autoPilot</span><span class="sxs-lookup"><span data-stu-id="537b9-105">AutoPilot profile settings</span></span>

<span data-ttu-id="537b9-106">Vous pouvez contrôler la façon dont Windows est installé sur les appareils utilisateur à l'aide des profils autoPilot.</span><span class="sxs-lookup"><span data-stu-id="537b9-106">You can control how Windows gets installed on user devices by using the AutoPilot profiles.</span></span> <span data-ttu-id="537b9-107">Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="537b9-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="537b9-108">**Les fonctionnalités de autoPilot par défaut (obligatoires) qui sont définies automatiquement:**</span><span class="sxs-lookup"><span data-stu-id="537b9-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="537b9-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="537b9-109">**Setting**</span></span>|<span data-ttu-id="537b9-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="537b9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="537b9-111">Ignorer Cortana, enregistrement OneDrive et OEM</span><span class="sxs-lookup"><span data-stu-id="537b9-111">Skip Cortana, OneDrive and OEM registration</span></span>  <br/> |<span data-ttu-id="537b9-112">Ignore l'installation des applications grand public telles que Cortana et OneDrive personnel.</span><span class="sxs-lookup"><span data-stu-id="537b9-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="537b9-113">L'utilisateur de l'appareil peut l'installer ultérieurement tant qu'il est administrateur local sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="537b9-113">The device user can install these later as long as he or she is a local admin on the device.</span></span> <span data-ttu-id="537b9-114">L'enregistrement du fabricant d'origine est ignoré car le périphérique sera géré par Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="537b9-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="537b9-115">Expérience de connexion avec la marque de votre entreprise</span><span class="sxs-lookup"><span data-stu-id="537b9-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="537b9-116">Si votre société dispose d'une [page de connexion Add Your Company to Office 365 Signing](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), l'utilisateur de l'appareil obtiendra cette expérience lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="537b9-116">If your company has a [Add your company branding to Office 365 Sign In page](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="537b9-117">Auto-inscriptions MDM avec comptes AAD configurés.</span><span class="sxs-lookup"><span data-stu-id="537b9-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="537b9-118">L'identité de l'utilisateur sera gérée par Azure Active Directory, et les utilisateurs se connecteront à Windows et Office 365 avec leurs informations d'identification d'entreprise Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="537b9-118">The user identity will be managed by Azure Active directory, and the users will sign into Windows and Office 365 with their Microsoft 365 Business credentials.</span></span>  <br/> |
   
 <span data-ttu-id="537b9-119">**Paramètres facultatifs:**</span><span class="sxs-lookup"><span data-stu-id="537b9-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="537b9-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="537b9-120">**Setting**</span></span>|<span data-ttu-id="537b9-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="537b9-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="537b9-122">Ignorer les paramètres de confidentialité (désActivés par défaut)</span><span class="sxs-lookup"><span data-stu-id="537b9-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="537b9-123">Si cette option est **activée**, l'utilisateur de l'appareil ne verra pas le contrat de licence du périphérique et de Windows lorsqu'il se connecte pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="537b9-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="537b9-124">Ne pas autoriser l'utilisateur à devenir l'administrateur local</span><span class="sxs-lookup"><span data-stu-id="537b9-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="537b9-125">Si cette option est **activée**, l'utilisateur de l'appareil ne peut pas installer d'applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="537b9-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span>  <br/> |
   
