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
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 99bfbf81-e719-4630-9b0f-c187edfa1f8a
description: Les profils AutoPilot vous permettent de contrôler la manière dont Windows est installé sur les appareils utilisateur. Les profils contiennent des paramètres par défaut et facultatifs, comme ignorer l’installation de Cortana.
ms.openlocfilehash: 0c706d12ba262856ff40ea3bee57c64234fd77f7
ms.sourcegitcommit: 46644f9778bc70ab6d62783e0a1e60ba2eccc27f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/08/2020
ms.locfileid: "44165838"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="ee751-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="ee751-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="ee751-105">Paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="ee751-105">AutoPilot profile settings</span></span>

<span data-ttu-id="ee751-106">Vous pouvez utiliser les profils AutoPilot pour contrôler la façon dont Windows est installé sur les appareils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ee751-106">You can use AutoPilot profiles to control how Windows is installed on user devices.</span></span> <span data-ttu-id="ee751-107">Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="ee751-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="ee751-108">**Les fonctionnalités de AutoPilot par défaut (obligatoires) qui sont définies automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="ee751-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="ee751-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="ee751-109">**Setting**</span></span>|<span data-ttu-id="ee751-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee751-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee751-111">Ignorer l’inscription de Cortana, OneDrive et OEM</span><span class="sxs-lookup"><span data-stu-id="ee751-111">Skip Cortana, OneDrive, and OEM registration</span></span>  <br/> |<span data-ttu-id="ee751-112">Ignore l’installation des applications grand public telles que Cortana et OneDrive personnel.</span><span class="sxs-lookup"><span data-stu-id="ee751-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="ee751-113">L’utilisateur de l’appareil peut l’installer ultérieurement tant que l’utilisateur est un administrateur local sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee751-113">The device user can install these later as long as the user is a local admin on the device.</span></span> <span data-ttu-id="ee751-114">L’inscription du fabricant d’origine est ignorée car l’appareil est géré par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="ee751-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business Premium.</span></span>  <br/> |
|<span data-ttu-id="ee751-115">Expérience de connexion avec la marque de votre entreprise</span><span class="sxs-lookup"><span data-stu-id="ee751-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="ee751-116">Si votre société dispose d’une [page de connexion ajouter votre société à Microsoft 365](https://docs.microsoft.com/microsoft-365/admin/setup/customize-sign-in-page), l’utilisateur de l’appareil bénéficiera de cette expérience lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="ee751-116">If your company has a [Add your company branding to Microsoft 365 Sign In page](https://docs.microsoft.com/microsoft-365/admin/setup/customize-sign-in-page), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="ee751-117">Auto-inscriptions MDM avec comptes AAD configurés.</span><span class="sxs-lookup"><span data-stu-id="ee751-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="ee751-118">L’identité de l’utilisateur sera gérée par Azure Active Directory, et les utilisateurs se connecteront à Windows et à Microsoft 365 avec leurs informations d’identification Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="ee751-118">The user identity will be managed by Azure Active Directory, and users will sign in to Windows and Microsoft 365 with their Microsoft 365 Business Premium credentials.</span></span>  <br/> |
   
 <span data-ttu-id="ee751-119">**Paramètres facultatifs :**</span><span class="sxs-lookup"><span data-stu-id="ee751-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="ee751-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="ee751-120">**Setting**</span></span>|<span data-ttu-id="ee751-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee751-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ee751-122">Ignorer les paramètres de confidentialité (désactivés par défaut)</span><span class="sxs-lookup"><span data-stu-id="ee751-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="ee751-123">Si cette option est **activée**, l’utilisateur de l’appareil ne verra pas le contrat de licence du périphérique et de Windows lorsqu’il se connecte pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ee751-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="ee751-124">Ne pas autoriser l’utilisateur à devenir l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="ee751-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="ee751-125">Si cette option est **activée**, l’utilisateur de l’appareil ne peut pas installer d’applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="ee751-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span><br/> |
   
