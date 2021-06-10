---
title: À propos des paramètres du profil AutoPilot
f1.keywords:
- NOCSH
ms.author: efrene
author: efrene
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
description: Les profils AutoPilot vous aident à contrôler Windows l’installation des appareils des utilisateurs. Les profils contiennent des paramètres par défaut et facultatifs comme ignorer l’installation de Cortana.
ms.openlocfilehash: 86f8718131f0a0b93e18e65e39e02e7d65aded1a
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578504"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="90bd4-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="90bd4-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="90bd4-105">Paramètres de profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="90bd4-105">AutoPilot profile settings</span></span>

<span data-ttu-id="90bd4-106">Vous pouvez utiliser les profils AutoPilot pour contrôler la Windows sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="90bd4-106">You can use AutoPilot profiles to control how Windows is installed on user devices.</span></span> <span data-ttu-id="90bd4-107">Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="90bd4-107">The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="90bd4-108">**Fonctionnalités autoPilot par défaut (obligatoires) qui sont définies automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="90bd4-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="90bd4-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="90bd4-109">**Setting**</span></span>|<span data-ttu-id="90bd4-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="90bd4-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90bd4-111">Ignorer l’inscription de Cortana, OneDrive et OEM</span><span class="sxs-lookup"><span data-stu-id="90bd4-111">Skip Cortana, OneDrive, and OEM registration</span></span>  <br/> |<span data-ttu-id="90bd4-112">Ignore l’installation d’applications grand public telles que Cortana et les OneDrive.</span><span class="sxs-lookup"><span data-stu-id="90bd4-112">Skips the installation of consumer apps like Cortana and personal OneDrive.</span></span> <span data-ttu-id="90bd4-113">L’utilisateur de l’appareil peut les installer ultérieurement tant que l’utilisateur est un administrateur local sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="90bd4-113">The device user can install these later as long as the user is a local admin on the device.</span></span> <span data-ttu-id="90bd4-114">L’inscription du fabricant d’origine est ignorée, car l’appareil sera géré par Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="90bd4-114">The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business Premium.</span></span>  <br/> |
|<span data-ttu-id="90bd4-115">Expérience de signature avec la marque de votre entreprise</span><span class="sxs-lookup"><span data-stu-id="90bd4-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="90bd4-116">Si votre entreprise dispose d’une marque Ajouter votre marque à [Microsoft 365 page](../admin/setup/customize-sign-in-page.md)de Microsoft 365, l’utilisateur de l’appareil reçoit cette expérience lors de la signature.</span><span class="sxs-lookup"><span data-stu-id="90bd4-116">If your company has a [Add your company branding to Microsoft 365 Sign In page](../admin/setup/customize-sign-in-page.md), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="90bd4-117">Inscription automatique mdm avec des comptes AAD configurés.</span><span class="sxs-lookup"><span data-stu-id="90bd4-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="90bd4-118">L’identité de l’utilisateur est gérée par Azure Active Directory et les utilisateurs se connectent à Windows et Microsoft 365 avec leurs informations d Microsoft 365 Business Premium personnelles.</span><span class="sxs-lookup"><span data-stu-id="90bd4-118">The user identity will be managed by Azure Active Directory, and users will sign in to Windows and Microsoft 365 with their Microsoft 365 Business Premium credentials.</span></span>  <br/> |
   
 <span data-ttu-id="90bd4-119">**Paramètres facultatifs :**</span><span class="sxs-lookup"><span data-stu-id="90bd4-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="90bd4-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="90bd4-120">**Setting**</span></span>|<span data-ttu-id="90bd4-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="90bd4-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90bd4-122">Ignorer les paramètres de confidentialité (par défaut)</span><span class="sxs-lookup"><span data-stu-id="90bd4-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="90bd4-123">Si cette option est définie sur **On,** l’utilisateur de l’appareil ne verra pas le contrat de licence de l’appareil et Windows lors de sa première se connecté.</span><span class="sxs-lookup"><span data-stu-id="90bd4-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="90bd4-124">Ne pas autoriser l’utilisateur à devenir l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="90bd4-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="90bd4-125">Si cette option est définie sur **Activé,** l’utilisateur de l’appareil ne pourra pas installer d’applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="90bd4-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span><br/> |
