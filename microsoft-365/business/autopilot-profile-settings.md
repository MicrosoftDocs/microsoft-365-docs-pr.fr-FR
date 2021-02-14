---
title: À propos des paramètres du profil AutoPilot
f1.keywords:
- NOCSH
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
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: Les profils AutoPilot vous aident à contrôler la façon dont Windows est installé sur les appareils des utilisateurs. Les profils contiennent des paramètres par défaut et facultatifs comme ignorer l’installation de Cortana.
ms.openlocfilehash: 100de5e9548f901008d3ae154ac5a237ef265ffb
ms.sourcegitcommit: 2d59b24b877487f3b84aefdc7b1e200a21009999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "44401031"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="61d40-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="61d40-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="61d40-105">Paramètres de profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="61d40-105">AutoPilot profile settings</span></span>

<span data-ttu-id="61d40-106">Vous pouvez utiliser les profils AutoPilot pour contrôler la façon dont Windows est installé sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="61d40-106">You can use AutoPilot profiles to control how Windows is installed on user devices.</span></span> <span data-ttu-id="61d40-107">Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="61d40-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="61d40-108">**Fonctionnalités autoPilot par défaut (obligatoires) qui sont définies automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="61d40-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="61d40-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="61d40-109">**Setting**</span></span>|<span data-ttu-id="61d40-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="61d40-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61d40-111">Ignorer l’inscription de Cortana, OneDrive et OEM</span><span class="sxs-lookup"><span data-stu-id="61d40-111">Skip Cortana, OneDrive, and OEM registration</span></span>  <br/> |<span data-ttu-id="61d40-112">Ignore l’installation d’applications grand public telles que Cortana et OneDrive personnel.</span><span class="sxs-lookup"><span data-stu-id="61d40-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="61d40-113">L’utilisateur de l’appareil peut les installer ultérieurement tant que l’utilisateur est un administrateur local sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="61d40-113">The device user can install these later as long as the user is a local admin on the device.</span></span> <span data-ttu-id="61d40-114">L’inscription du fabricant d’origine est ignorée, car l’appareil sera géré par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="61d40-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business Premium.</span></span>  <br/> |
|<span data-ttu-id="61d40-115">Expérience de signature avec la marque de votre entreprise</span><span class="sxs-lookup"><span data-stu-id="61d40-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="61d40-116">Si votre entreprise dispose d’une marque Ajouter votre marque de société à la page de signature [Microsoft 365,](https://docs.microsoft.com/microsoft-365/admin/setup/customize-sign-in-page)l’utilisateur de l’appareil aura cette expérience lors de la signature.</span><span class="sxs-lookup"><span data-stu-id="61d40-116">If your company has a [Add your company branding to Microsoft 365 Sign In page](https://docs.microsoft.com/microsoft-365/admin/setup/customize-sign-in-page), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="61d40-117">Inscription automatique mdm avec des comptes AAD configurés.</span><span class="sxs-lookup"><span data-stu-id="61d40-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="61d40-118">L’identité de l’utilisateur est gérée par Azure Active Directory et les utilisateurs se connectent à Windows et Microsoft 365 avec leurs informations d’identification Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="61d40-118">The user identity will be managed by Azure Active Directory, and users will sign in to Windows and Microsoft 365 with their Microsoft 365 Business Premium credentials.</span></span>  <br/> |
   
 <span data-ttu-id="61d40-119">**Paramètres facultatifs :**</span><span class="sxs-lookup"><span data-stu-id="61d40-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="61d40-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="61d40-120">**Setting**</span></span>|<span data-ttu-id="61d40-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="61d40-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61d40-122">Ignorer les paramètres de confidentialité (par défaut)</span><span class="sxs-lookup"><span data-stu-id="61d40-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="61d40-123">Si cette option est définie sur **On,** l’utilisateur de l’appareil ne verra pas le contrat de licence pour l’appareil et Windows lorsqu’il se connecté pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="61d40-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="61d40-124">Ne pas autoriser l’utilisateur à devenir l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="61d40-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="61d40-125">Si cette option est définie sur **Activé,** l’utilisateur de l’appareil ne pourra pas installer d’applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="61d40-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span><br/> |
   
