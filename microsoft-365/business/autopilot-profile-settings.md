---
title: À propos des paramètres du profil AutoPilot
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ZTDProfileSettings
- O365E_ZTDProfileSettings
- BCS365_ZTDProfileSettings
ms.service: o365-administration
localization_priority: Normal
ms.collection: Adm_O365
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
description: Profils de pilote vous aider à contrôler la façon dont Windows est installé sur les périphériques de l’utilisateur. Les profils contiennent par défaut et les paramètres facultatifs comme ignorer l’installation du Cortana.
ms.openlocfilehash: 5440286f1363780c87ab60514584c4addfeea0b2
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866865"
---
# <a name="about-autopilot-profile-settings"></a><span data-ttu-id="607d9-104">À propos des paramètres du profil AutoPilot</span><span class="sxs-lookup"><span data-stu-id="607d9-104">About AutoPilot Profile settings</span></span>

## <a name="autopilot-profile-settings"></a><span data-ttu-id="607d9-105">Paramètres de profil pilote</span><span class="sxs-lookup"><span data-stu-id="607d9-105">AutoPilot profile settings</span></span>

<span data-ttu-id="607d9-p102">Vous pouvez contrôler la façon dont Windows est installé sur les périphériques de l’utilisateur en utilisant les profils de pilote. Les profils contiennent les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="607d9-p102">You can control how Windows gets installed on user devices by using the AutoPilot profiles. The profiles contain the following settings.</span></span>
  
 <span data-ttu-id="607d9-108">**Pilote fonctionnalités par défaut (requis) qui sont définies automatiquement :**</span><span class="sxs-lookup"><span data-stu-id="607d9-108">**AutoPilot default features (required) that are set automatically:**</span></span>
  
|<span data-ttu-id="607d9-109">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="607d9-109">**Setting**</span></span>|<span data-ttu-id="607d9-110">**Description**</span><span class="sxs-lookup"><span data-stu-id="607d9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="607d9-111">Ignorer l’enregistrement OEM, OneDrive et Cortana</span><span class="sxs-lookup"><span data-stu-id="607d9-111">Skip Cortana, OneDrive and OEM registration</span></span>  <br/> |<span data-ttu-id="607d9-p103">Ignore l’installation des applications consommateur, telles que Cortana et OneDrive personnel. L’utilisateur de l’appareil peut installer ultérieurement tant qu’il est un administrateur local sur l’appareil. L’inscription du fabricant d’origine est ignorée car le périphérique sera géré par Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="607d9-p103">Skips the installation of consumer apps like Cortana and personal OneDrive. The device user can install these later as long as he or she is a local admin on the device. The original manufacturer registration is skipped because the device will be managed by Microsoft 365 Business.</span></span>  <br/> |
|<span data-ttu-id="607d9-115">Connecter l’expérience avec la marque de votre société</span><span class="sxs-lookup"><span data-stu-id="607d9-115">Sign in experience with your company brand</span></span>  <br/> |<span data-ttu-id="607d9-116">Si votre société possède une [personnalisation d’ajouter votre société pour Office 365 page de connexion](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), l’utilisateur d’appareil obtenez cette expérience lors de la connexion.</span><span class="sxs-lookup"><span data-stu-id="607d9-116">If your company has a [Add your company branding to Office 365 Sign In page](https://support.office.com/article/a1229cdb-ce19-4da5-90c7-2b9b146aef0a), the device user will get that experience when signing in.</span></span>  <br/> |
|<span data-ttu-id="607d9-117">Mobile Device Manager l’inscription automatique avec des comptes DAS configurés.</span><span class="sxs-lookup"><span data-stu-id="607d9-117">MDM auto-enrollment with configured AAD accounts.</span></span>  <br/> |<span data-ttu-id="607d9-118">Identité de l’utilisateur est gérée par Azure Active directory et les utilisateurs seront vous connecter à Windows et Office 365 avec leurs informations d’identification Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="607d9-118">The user identity will be managed by Azure Active directory, and the users will sign into Windows and Office 365 with their Microsoft 365 Business credentials.</span></span>  <br/> |
   
 <span data-ttu-id="607d9-119">**Paramètres facultatifs :**</span><span class="sxs-lookup"><span data-stu-id="607d9-119">**Optional settings:**</span></span>
  
|<span data-ttu-id="607d9-120">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="607d9-120">**Setting**</span></span>|<span data-ttu-id="607d9-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="607d9-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="607d9-122">Ignorer les paramètres de confidentialité (désactivé par défaut)</span><span class="sxs-lookup"><span data-stu-id="607d9-122">Skip privacy settings (Off by default)</span></span>  <br/> |<span data-ttu-id="607d9-123">Si cette option est définie sur **activé**, l’utilisateur d’appareil verrez pas le contrat de licence pour le périphérique et Windows lorsqu’il se connecte tout d’abord en.</span><span class="sxs-lookup"><span data-stu-id="607d9-123">If this option is set to **On**, the device user will not see the license agreement for the device and Windows when he or she first signs in.</span></span>  <br/> |
|<span data-ttu-id="607d9-124">Ne pas autoriser l’utilisateur de devenir l’administrateur local</span><span class="sxs-lookup"><span data-stu-id="607d9-124">Don't allow the user to become the local admin</span></span>  <br/> |<span data-ttu-id="607d9-125">Si cette option est définie sur **activé**, l’utilisateur du périphérique ne sera pas en mesure d’installer des applications personnelles, telles que Cortana.</span><span class="sxs-lookup"><span data-stu-id="607d9-125">If this option is set to **On**, the device user will not be able to install any personal apps, such as Cortana.</span></span>  <br/> |
   
