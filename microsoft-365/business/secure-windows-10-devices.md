---
title: Sécuriser les appareils Windows 10
ms.author: sirkkuw
author: sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: overview
f1_keywords:
- O365E_BCSSetup4WindowsConfig
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 21e5551f-fa35-4f13-9418-f80d668b6a2b
description: 'Découvrez les paramètres par défaut et autres pour sécuriser les périphériques Windows 10. '
ms.openlocfilehash: 0bdf6a56d880cb84f4a4f50550539d97c006ba49
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867397"
---
# <a name="secure-windows-10-devices"></a><span data-ttu-id="f58f7-103">Sécuriser les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="f58f7-103">Secure Windows 10 devices</span></span>

<span data-ttu-id="f58f7-p101">[] Les paramètres que vous configurez ici font partie de la stratégie d'appareil par défaut pour Windows 10. Tous les utilisateurs qui connectent un appareil Windows 10, y compris les appareils mobiles et les PC, en se connectant avec leur compte professionnel, recevront automatiquement ces paramètres. Nous vous recommandons d'accepter la stratégie par défaut lors de l'installation et d'ajouter par la suite des stratégies qui ciblent des groupes d'utilisateurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f58f7-p101">The settings that you configure here are part of the default device policy for Windows 10. All users that connect a Windows 10 device, including mobile devices and PCs, by signing in with their work account, will automatically receive these settings. We recommend that you accept the default policy during setup and add policies later that target specific groups of users.</span></span>
  
## <a name="settings-to-secure-windows-10-devices"></a><span data-ttu-id="f58f7-107">Paramètres de sécurisation des appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="f58f7-107">Settings to secure Windows 10 devices</span></span>

<span data-ttu-id="f58f7-p102">Par défaut, tous les paramètres sont **activés**. Les paramètres suivants sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="f58f7-p102">By default all settings are **On**. The following settings are available:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f58f7-110">Paramètre</span><span class="sxs-lookup"><span data-stu-id="f58f7-110">Setting</span></span>  <br/> |<span data-ttu-id="f58f7-111">Description</span><span class="sxs-lookup"><span data-stu-id="f58f7-111">Description</span></span>  <br/> |
|<span data-ttu-id="f58f7-112">Protéger les ordinateurs des virus et d'autres menaces à l'aide de l'antivirus Windows Defender</span><span class="sxs-lookup"><span data-stu-id="f58f7-112">Help protect PCs from viruses and other threats using Windows Defender Antivirus</span></span>  <br/> |<span data-ttu-id="f58f7-113">L'anti-virus Windows Defender doit être activé pour protéger les ordinateurs contre les risques liés à la connexion à internet.</span><span class="sxs-lookup"><span data-stu-id="f58f7-113">Requires that Windows Defender Antivirus is turned on to protect PCs from the dangers of being connected to the internet.</span></span>  <br/> |
|<span data-ttu-id="f58f7-114">Protéger les ordinateurs contre les menaces web dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f58f7-114">Help protect PCs from web-based threats in Microsoft Edge</span></span>  <br/> |<span data-ttu-id="f58f7-115">Active les paramètres Microsoft Edge qui protègent les utilisateurs contre les sites et téléchargements malveillants.</span><span class="sxs-lookup"><span data-stu-id="f58f7-115">Turns on settings in Edge that help protect users from malicious sites and downloads.</span></span>  <br/> |
|<span data-ttu-id="f58f7-116">Désactiver l'écran d'un appareil resté inactif pendant</span><span class="sxs-lookup"><span data-stu-id="f58f7-116">Turn off device screen when idle for this amount of time</span></span>  <br/> |<span data-ttu-id="f58f7-p103">Permet d'assurer la protection des données d'entreprise lorsqu'un utilisateur est inactif. Il est possible qu'un utilisateur travaille dans un lieu public, par exemple un café, et s'éloigne ou soit distrait pendant un instant, laissant son appareil à la vue de tous. Ce paramètre vous permet de contrôler la durée pendant laquelle l'utilisateur peut être inactif avant l'extinction de l'écran.</span><span class="sxs-lookup"><span data-stu-id="f58f7-p103">Makes sure that company data is protected if a user is idle. A user may be working in a public location, like a coffee shop, and step away or be distracted for just a moment, leaving their device vulnerable to random glances. This setting lets you control how long the user can be idle before the screen shuts off.</span></span>  <br/> |
|<span data-ttu-id="f58f7-120">Autoriser les utilisateurs à télécharger des applications à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="f58f7-120">Allow users to download apps from Microsoft Store</span></span>  <br/> |<span data-ttu-id="f58f7-p104">Permet aux utilisateurs de télécharger et d'installer des applications à partir du Microsoft Store. Il peut s'agir de jeux ou d'outils de productivité, c'est pourquoi nous laissons ce paramètre **activé**, mais vous pouvez le désactiver pour plus de sécurité.  </span><span class="sxs-lookup"><span data-stu-id="f58f7-p104">Lets users download and install apps from the Microsoft Store. Apps include everything from games to productivity tools, so we leave this setting **On**, but you can turn it off for extra security.  </span></span><br/> |
|<span data-ttu-id="f58f7-123">Autoriser les utilisateurs à accéder à Cortana</span><span class="sxs-lookup"><span data-stu-id="f58f7-123">Allow users to access Cortana</span></span>  <br/> |<span data-ttu-id="f58f7-p105">Cortana peut être très utile ! Elle peut activer ou désactiver des paramètres pour vous, vous indiquer un trajet ou veiller à ce que vous arriviez à l'heure à vos rendez-vous. C'est la raison pour laquelle ce paramètre est **activé** par défaut.  </span><span class="sxs-lookup"><span data-stu-id="f58f7-p105">Cortana can be very helpful! She can turn settings on or off for you, give directions, and make sure you're on time for appointments, so we keep this **On** by default.  </span></span><br/> |
|<span data-ttu-id="f58f7-126">Autoriser les utilisateurs à recevoir des conseils de Windows et des annonces de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f58f7-126">Allow users to receive Windows tips and advertisements from Microsoft</span></span>  <br/> |<span data-ttu-id="f58f7-127">Les conseils Windows peuvent être très pratiques et aident les utilisateurs lors du lancement de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="f58f7-127">Windows tips can be handy and help orient users when new features are released.</span></span>  <br/> |
|<span data-ttu-id="f58f7-128">Maintenir les appareils Windows 10 à jour automatiquement</span><span class="sxs-lookup"><span data-stu-id="f58f7-128">Keep Windows 10 devices up to date automatically</span></span>  <br/> |<span data-ttu-id="f58f7-129">Permet d'assurer que les appareils Windows 10 reçoivent automatiquement les dernières mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f58f7-129">Makes sure that Windows 10 devices automatically receive the latest updates.</span></span>  <br/> |
   

