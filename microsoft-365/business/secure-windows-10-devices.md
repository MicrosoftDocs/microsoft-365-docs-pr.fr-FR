---
title: Sécuriser les appareils Windows 10
f1.keywords:
- CSH
ms.author: sirkkuw
author: sirkkuw
manager: scotv
audience: Admin
ms.topic: conceptual
f1_keywords:
- O365E_BCSSetup4WindowsConfig
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 21e5551f-fa35-4f13-9418-f80d668b6a2b
description: Découvrez comment configurer les paramètres de la stratégie d’appareil par défaut que tout appareil Windows 10 recevra lors de la connexion à son compte professionnel ou scolaire.
ms.openlocfilehash: 85448507835b6310ca4136849be6a40caf6bb919
ms.sourcegitcommit: abf63669daf12993ad3353e4b578f41c8910b20f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2020
ms.locfileid: "47289074"
---
# <a name="secure-windows-10-devices"></a><span data-ttu-id="2d926-103">Sécuriser les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="2d926-103">Secure Windows 10 devices</span></span>

<span data-ttu-id="2d926-104">Cet article s’applique à Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="2d926-104">This article applies to Microsoft 365 Business Premium.</span></span>

<span data-ttu-id="2d926-105">[] Les paramètres que vous configurez ici font partie de la stratégie d'appareil par défaut pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="2d926-105">The settings that you configure here are part of the default device policy for Windows 10.</span></span> <span data-ttu-id="2d926-106">Tous les utilisateurs qui connectent un appareil Windows 10, y compris les appareils mobiles et les PC, en se connectant avec leur compte professionnel reçoivent automatiquement ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="2d926-106">All users who connect a Windows 10 device, including mobile devices and PCs, by signing in with their work account will automatically receive these settings.</span></span> <span data-ttu-id="2d926-107">Nous vous recommandons d'accepter la stratégie par défaut lors de l'installation et d'ajouter par la suite des stratégies qui ciblent des groupes d'utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="2d926-107">We recommend that you accept the default policy during setup and add policies later that target specific groups of users.</span></span>
  
## <a name="settings-to-secure-windows-10-devices"></a><span data-ttu-id="2d926-108">Paramètres de sécurisation des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="2d926-108">Settings to secure Windows 10 devices</span></span>

<span data-ttu-id="2d926-p102">Par défaut, tous les paramètres sont **activés**. Les paramètres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="2d926-p102">By default all settings are **On**. The following settings are available:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2d926-111">Setting</span><span class="sxs-lookup"><span data-stu-id="2d926-111">Setting</span></span>  <br/> |<span data-ttu-id="2d926-112">Description</span><span class="sxs-lookup"><span data-stu-id="2d926-112">Description</span></span>  <br/> |
|<span data-ttu-id="2d926-113">Protéger les ordinateurs des virus et d'autres menaces à l'aide de l'antivirus Windows Defender</span><span class="sxs-lookup"><span data-stu-id="2d926-113">Help protect PCs from viruses and other threats using Windows Defender Antivirus</span></span>  <br/> |<span data-ttu-id="2d926-114">L'antivirus Windows Defender doit être activé pour protéger les ordinateurs contre les risques liés à la connexion à internet.</span><span class="sxs-lookup"><span data-stu-id="2d926-114">Requires that Windows Defender Antivirus is turned on to protect PCs from the dangers of being connected to the internet.</span></span>  <br/> |
|<span data-ttu-id="2d926-115">Protéger les ordinateurs contre les menaces web dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2d926-115">Help protect PCs from web-based threats in Microsoft Edge</span></span>  <br/> |<span data-ttu-id="2d926-116">Active les paramètres Microsoft Edge qui protègent les utilisateurs contre les sites et téléchargements malveillants.</span><span class="sxs-lookup"><span data-stu-id="2d926-116">Turns on settings in Edge that help protect users from malicious sites and downloads.</span></span>  <br/> |
|<span data-ttu-id="2d926-117">Protéger les fichiers et dossiers sur PC contre un accès non autorisé avec BitLocker</span><span class="sxs-lookup"><span data-stu-id="2d926-117">Help protect files and folders on PCs from unauthorized access with BitLocker</span></span>  <br/> |<span data-ttu-id="2d926-118">Bitlocker protège les données en chiffrant les disques durs de l'ordinateur, et protège contre l'exposition des données en cas de perte ou de vol.</span><span class="sxs-lookup"><span data-stu-id="2d926-118">Bitlocker protects data by encrypting the computer hard drives and protect against data exposure if a computer is lost or stolen.</span></span> <span data-ttu-id="2d926-119">Pour plus d’informations, consultez la rubrique [BitLocker FAQ](https://go.microsoft.com/fwlink/?linkid=871000).</span><span class="sxs-lookup"><span data-stu-id="2d926-119">For more information, see [Bitlocker FAQ](https://go.microsoft.com/fwlink/?linkid=871000).</span></span>  <br/> |
|<span data-ttu-id="2d926-120">Désactiver l'écran d'un appareil resté inactif pendant</span><span class="sxs-lookup"><span data-stu-id="2d926-120">Turn off device screen when idle for this amount of time</span></span>  <br/> |<span data-ttu-id="2d926-p104">Permet d'assurer la protection des données d'entreprise lorsqu'un utilisateur est inactif. Il est possible qu'un utilisateur travaille dans un lieu public, par exemple un café, et s'éloigne ou soit distrait pendant un instant, laissant son appareil à la vue de tous. Ce paramètre vous permet de contrôler la durée pendant laquelle l'utilisateur peut être inactif avant l'extinction de l'écran.</span><span class="sxs-lookup"><span data-stu-id="2d926-p104">Makes sure that company data is protected if a user is idle. A user may be working in a public location, like a coffee shop, and step away or be distracted for just a moment, leaving their device vulnerable to random glances. This setting lets you control how long the user can be idle before the screen shuts off.</span></span>  <br/> |
|