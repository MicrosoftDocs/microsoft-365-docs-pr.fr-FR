---
title: Activer l'authentification moderne pour Office 2013 sur les appareils Windows
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
- okr_smb
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 7dc1c01a-090f-4971-9677-f1b192d6c910
description: Apprenez à définir des clés de registre pour permettre l’authentification moderne pour les appareils qui Microsoft Office 2013 installés.
ms.openlocfilehash: d358cb2ffb4284a51779e5a7c1dc894052b9ebc0
ms.sourcegitcommit: 0936f075a1205b8f8a71a7dd7761a2e2ce6167b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52572284"
---
# <a name="enable-modern-authentication-for-office-2013-on-windows-devices"></a><span data-ttu-id="f39af-103">Activer l'authentification moderne pour Office 2013 sur les appareils Windows</span><span class="sxs-lookup"><span data-stu-id="f39af-103">Enable Modern Authentication for Office 2013 on Windows devices</span></span>

<span data-ttu-id="f39af-104">[] Pour activer l'authentification moderne pour les appareils Windows sur lesquels Office 2013 est installé, vous devez définir des clés de Registre spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f39af-104">To enable modern authentication for any Windows devices that have Office 2013 installed, you need to set specific registry keys.</span></span>
  
## <a name="enable-modern-authentication-for-office-2013-clients"></a><span data-ttu-id="f39af-105">Activer l'authentification moderne pour les clients Office 2013</span><span class="sxs-lookup"><span data-stu-id="f39af-105">Enable modern authentication for Office 2013 clients</span></span>

> [!NOTE]
> <span data-ttu-id="f39af-106">L'authentification moderne est déjà activée pour les clients Office 2016. Vous n'avez pas besoin de définir de clés de Registre pour Office 2016.</span><span class="sxs-lookup"><span data-stu-id="f39af-106">Modern authentication is already enabled for Office 2016 clients, you do not need to set registry keys for Office 2016.</span></span> 
  
<span data-ttu-id="f39af-p101">Pour activer l'authentification moderne pour les appareils exécutant Windows (par exemple les ordinateurs portables et tablettes) et sur lesquels Microsoft Office 2013 est installé, vous devez définir les clés de Registre suivantes. Les clés doivent être définies sur chaque appareil pour lequel vous voulez activer l'authentification moderne :</span><span class="sxs-lookup"><span data-stu-id="f39af-p101">To enable modern authentication for any devices running Windows (for example on laptops and tablets), that have Microsoft Office 2013 installed, you need to set the following registry keys. The keys have to be set on each device that you want to enable for modern authentication:</span></span>
  
|<span data-ttu-id="f39af-109">**Clé de Registre**</span><span class="sxs-lookup"><span data-stu-id="f39af-109">**Registry key**</span></span>|<span data-ttu-id="f39af-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="f39af-110">**Type**</span></span>|<span data-ttu-id="f39af-111">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f39af-111">**Value**</span></span> |
|:-------|:------:|--------:|
|<span data-ttu-id="f39af-112">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL</span><span class="sxs-lookup"><span data-stu-id="f39af-112">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL</span></span>  |<span data-ttu-id="f39af-113">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f39af-113">REG_DWORD</span></span>  |<span data-ttu-id="f39af-114">1</span><span class="sxs-lookup"><span data-stu-id="f39af-114">1</span></span>  |
|<span data-ttu-id="f39af-115">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\Version</span><span class="sxs-lookup"><span data-stu-id="f39af-115">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\Version</span></span> |<span data-ttu-id="f39af-116">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f39af-116">REG_DWORD</span></span> |<span data-ttu-id="f39af-117">1</span><span class="sxs-lookup"><span data-stu-id="f39af-117">1</span></span> |
   
<span data-ttu-id="f39af-118">Une fois que vous avez défini les clés du registre, vous pouvez définir Office applications d’appareils 2013 pour utiliser [l’authentification multifactorielle (MFA)](set-up-multi-factor-authentication.md) avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f39af-118">Once you have set the registry keys, you can set Office 2013 devices apps to use [multifactor authentication (MFA)](set-up-multi-factor-authentication.md) with Microsoft 365.</span></span> 
  
<span data-ttu-id="f39af-p102">Si vous êtes actuellement connecté avec une application client, vous devez vous déconnecter et vous reconnecter pour que la modification prenne effet. Autrement, les paramètres MRU et d'itinérance ne seront pas disponibles tant que l'identité ADAL n'est pas établie.</span><span class="sxs-lookup"><span data-stu-id="f39af-p102">If you're currently signed-in with any of the client apps, you need to sign out and sign back in for the change to take effect. Otherwise, the MRU and roaming settings will be unavailable until the ADAL identity is established.</span></span>
  
## <a name="disable-modern-authentication-on-devices"></a><span data-ttu-id="f39af-121">Désactiver l'authentification moderne sur les appareils</span><span class="sxs-lookup"><span data-stu-id="f39af-121">Disable modern authentication on devices</span></span>

<span data-ttu-id="f39af-122">Pour désactiver l'authentification moderne sur un appareil, définissez les clés de Registre suivantes sur l'appareil :</span><span class="sxs-lookup"><span data-stu-id="f39af-122">To disable modern authentication on a device, set the following registry keys on the device:</span></span>
  
|<span data-ttu-id="f39af-123">**Clé de Registre**</span><span class="sxs-lookup"><span data-stu-id="f39af-123">**Registry key**</span></span>|<span data-ttu-id="f39af-124">**Type**</span><span class="sxs-lookup"><span data-stu-id="f39af-124">**Type**</span></span>|<span data-ttu-id="f39af-125">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="f39af-125">**Value**</span></span>|
|:-------|:------:|--------:|
|<span data-ttu-id="f39af-126">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL</span><span class="sxs-lookup"><span data-stu-id="f39af-126">HKCU\SOFTWARE\Microsoft\Office\15.0\Common\Identity\EnableADAL</span></span> |<span data-ttu-id="f39af-127">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f39af-127">REG_DWORD</span></span>|<span data-ttu-id="f39af-128">0</span><span class="sxs-lookup"><span data-stu-id="f39af-128">0</span></span>|
   
## <a name="related-content"></a><span data-ttu-id="f39af-129">Contenu connexe</span><span class="sxs-lookup"><span data-stu-id="f39af-129">Related content</span></span>

<span data-ttu-id="f39af-130">[Connectez-vous Office 2013 avec une deuxième méthode de vérification](https://support.microsoft.com/office/2b856342-170a-438e-9a4f-3c092394d3cb) (article)</span><span class="sxs-lookup"><span data-stu-id="f39af-130">[Sign in to Office 2013 with a second verification method](https://support.microsoft.com/office/2b856342-170a-438e-9a4f-3c092394d3cb) (article)</span></span>

<span data-ttu-id="f39af-131">[Outlook pour mot de passe et n’utilise pas l’authentification moderne pour se connecter à Office 365](/outlook/troubleshoot/authentication/outlook-prompt-password-modern-authentication-enabled) (article)</span><span class="sxs-lookup"><span data-stu-id="f39af-131">[Outlook prompts for password and doesn't use Modern Authentication to connect to Office 365](/outlook/troubleshoot/authentication/outlook-prompt-password-modern-authentication-enabled) (article)</span></span>

