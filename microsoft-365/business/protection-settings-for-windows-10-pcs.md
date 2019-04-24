---
title: Définir les paramètres de protection des appareils pour les PC Windows 10
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: bd66c26c-73a4-45a8-8642-3ea4ee7cd89d
description: Découvrez les paramètres par défaut et d'autres paramètres disponibles dans Microsoft 365 Business pour sécuriser les appareils Windows 10.
ms.openlocfilehash: f9e890cde7a8290a9a8e81720d32a6a2889c312f
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285914"
---
# <a name="set-device-protection-settings-for-windows-10-pcs"></a><span data-ttu-id="5dfc8-103">Définir les paramètres de protection des appareils pour les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="5dfc8-103">Set device protection settings for Windows 10 PCs</span></span>

## <a name="secure-windows-10-devices"></a><span data-ttu-id="5dfc8-104">Sécuriser les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="5dfc8-104">Secure Windows 10 devices</span></span>

<span data-ttu-id="5dfc8-105">Visionnez une vidéo sur la sécurisation des appareils Windows 10 avec Microsoft 365 Entreprise :</span><span class="sxs-lookup"><span data-stu-id="5dfc8-105">View a video on how to secure Windows 10 devices with Microsoft 365 Business:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/a5734146-620a-4cec-8618-536b3ca37972?autoplay=false]
  
1. <span data-ttu-id="5dfc8-106">Connectez-vous au [Centre d'administration](https://go.microsoft.com/fwlink/p/?linkid=837890) avec des informations d'identification d'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-106">Sign in to [admin center](https://go.microsoft.com/fwlink/p/?linkid=837890) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="5dfc8-107">Dans le volet de navigation de gauche, choisissez **Ajout**de **stratégies** \> de **périphériques** \> .</span><span class="sxs-lookup"><span data-stu-id="5dfc8-107">On the left nav, choose **Devices** \> **Policies** \> **Add**.</span></span>
  
3. <span data-ttu-id="5dfc8-108">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-108">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="5dfc8-109">Sous **Type de stratégie**, sélectionnez **Configuration d'appareil Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-109">Under **Policy type**, choose **Windows 10 Device Configuration**.</span></span>
    
5. <span data-ttu-id="5dfc8-p101">Expand **Secure Windows 10 Devices** \> configure the settings how you would like. See [Available settings](#available-settings) for more information.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-p101">Expand **Secure Windows 10 Devices** \> configure the settings how you would like. See [Available settings](#available-settings) for more information.</span></span> 
    
    <span data-ttu-id="5dfc8-112">Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-112">You can alway use the **Reset default settings** link to return to the default setting.</span></span> 
    
    ![Add policy pane with Windows 10 Device configuration selected](media/fa9e2dc2-7eae-4c96-af34-765a1f641ecf.png)
  
6. <span data-ttu-id="5dfc8-p102">Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis recherchez le groupe qui obtiendra ces paramètres \> **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-p102">Next decide **Who will get these settings?** If you don't want to use the default **All users** security group, Choose **Change**, search for the security group who will get these settings \> **Select**.</span></span>
    
7. <span data-ttu-id="5dfc8-116">Enfin, sélectionnez **Terminé** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-116">Finally, choose **Done** to save the policy, and assign it to devices.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="5dfc8-117">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="5dfc8-117">Available settings</span></span>

<span data-ttu-id="5dfc8-p103">Par défaut, tous les paramètres sont **Activés**. Les paramètres suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-p103">By default all settings are **On**. The following settings are available.</span></span>
  
<span data-ttu-id="5dfc8-120">Pour plus d'informations, voir [Correspondance entre les fonctionnalités de protection de Microsoft 365 Business et les paramètres Intune](map-protection-features-to-intune-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5dfc8-120">See [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md) for more information.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5dfc8-121">Paramètre</span><span class="sxs-lookup"><span data-stu-id="5dfc8-121">Setting</span></span>  <br/> |<span data-ttu-id="5dfc8-122">Description</span><span class="sxs-lookup"><span data-stu-id="5dfc8-122">Description</span></span>  <br/> |
|<span data-ttu-id="5dfc8-123">Protéger les ordinateurs des virus et d'autres menaces à l'aide de l'antivirus Windows Defender</span><span class="sxs-lookup"><span data-stu-id="5dfc8-123">Help protect PCs from viruses and other threats using Windows Defender Antivirus</span></span>  <br/> |<span data-ttu-id="5dfc8-124">L'antivirus Windows Defender doit être activé pour protéger les ordinateurs contre les risques liés à la connexion à internet.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-124">Requires that Windows Defender Antivirus is turned on to protect PCs from the dangers of being connected to the internet.</span></span>  <br/> |
|<span data-ttu-id="5dfc8-125">Protéger les ordinateurs contre les menaces web dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5dfc8-125">Help protect PCs from web-based threats in Microsoft Edge</span></span>  <br/> |<span data-ttu-id="5dfc8-126">Active les paramètres Microsoft Edge qui protègent les utilisateurs contre les sites et téléchargements malveillants.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-126">Turns on settings in Edge that help protect users from malicious sites and downloads.</span></span>  <br/> |
|<span data-ttu-id="5dfc8-127">Utiliser des règles qui réduisent la surface d'attaque des appareils</span><span class="sxs-lookup"><span data-stu-id="5dfc8-127">Use rules that reduce the attack surface of devices</span></span>  <br/> |<span data-ttu-id="5dfc8-p104">Quand elle est activée, la réduction de la surface d'attaque aide à bloquer les actions et applications que les logiciels malveillants utilisent généralement pour contaminer des appareils. Ce paramètre est disponible uniquement si Antivirus Windows Defender est activé. Pour en savoir plus, voir [Réduire les surfaces d'attaque](https://go.microsoft.com/fwlink/?linkid=870417).  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p104">When turned On, attack surface reduction helps block actions and apps typically used by malware to infect devices. This setting is only available if Windows Defender Antivirus is set to On. See [Reduce attack surfaces](https://go.microsoft.com/fwlink/?linkid=870417) to learn more.  </span></span><br/> |
|<span data-ttu-id="5dfc8-131">Protéger les dossiers contre des menaces telles que des rançongiciels</span><span class="sxs-lookup"><span data-stu-id="5dfc8-131">Protect folders from threats such as ransomware</span></span>  <br/> |<span data-ttu-id="5dfc8-p105">Ce paramètre utilise l'Accès contrôlé aux dossiers pour protéger les données de l'entreprise contre l'apport de modifications par des applications suspectes ou malveillantes, telles que les rançongiciels. L'apport de modifications aux dossiers protégés par des applications de ces types est bloqué. Ce paramètre est disponible uniquement si Antivirus Windows Defender est activé. Pour en savoir plus, voir [Protéger des dossiers importants avec l'Accès contrôlé aux dossiers](https://go.microsoft.com/fwlink/?linkid=870418).  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p105">This setting uses controlled folder access to protect company data from modification by suspicious or malicious apps, such as ransomware. These types of apps are blocked from making changes in protected folders. This setting is only available if Windows Defender Antivirus is set to On. See [Protect folders with COntrolled folder access](https://go.microsoft.com/fwlink/?linkid=870418) to learn more.  </span></span><br/> |
|<span data-ttu-id="5dfc8-136">Empêcher l'accès réseau à du contenu potentiellement malveillant sur Internet</span><span class="sxs-lookup"><span data-stu-id="5dfc8-136">Prevent network access to potentially malicious content on the Internet</span></span>  <br/> |<span data-ttu-id="5dfc8-p106">Utilisez ce paramètre pour bloquer les connexions utilisateur sortantes à des sites Internet de faible réputation, susceptibles d'exposer à du hameçonnage en ligne, à des attaques ou à d'autres contenus malveillants. Ce paramètre est disponible uniquement si Antivirus Windows Defender est activé. Pour plus d'informations, voir [Protéger votre réseau](https://go.microsoft.com/fwlink/?linkid=870419).  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p106">Use this setting to block outbound user connections to low-reputation Internet locations that may host phishing scams, exploits or other malicious content. This setting is only available if Windows Defender Antivirus is set to On. See [Protect your network](https://go.microsoft.com/fwlink/?linkid=870419) for more information.  </span></span><br/> |
|<span data-ttu-id="5dfc8-140">Protéger les fichiers et dossiers sur PC contre un accès non autorisé avec BitLocker</span><span class="sxs-lookup"><span data-stu-id="5dfc8-140">Help protect files and folders on PCs from unauthorized access with BitLocker</span></span>  <br/> |<span data-ttu-id="5dfc8-p107">Bitlocker protège les données en chiffrant les disques durs de l'ordinateur, et protège contre l'exposition des données en cas de perte ou de vol. Pour plus d'informations, voir [FAQ Bitlocker](https://go.microsoft.com/fwlink/?linkid=871000).  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p107">Bitlocker protects data by encrypting the computer hard drives and protect against data exposure if a computer is lost or stolen. See [Bitlocker FAQ](https://go.microsoft.com/fwlink/?linkid=871000) for more information.  </span></span><br/> |
|<span data-ttu-id="5dfc8-143">Autoriser les utilisateurs à télécharger des applications à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5dfc8-143">Allow users to download apps from Microsoft Store</span></span>  <br/> |<span data-ttu-id="5dfc8-p108">Permet aux utilisateurs de télécharger et d'installer des applications à partir du Microsoft Store. Il peut s'agir de jeux ou d'outils de productivité, c'est pourquoi nous laissons ce paramètre **activé**, mais vous pouvez le désactiver pour plus de sécurité.  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p108">Lets users download and install apps from the Microsoft Store. Apps include everything from games to productivity tools, so we leave this setting **On**, but you can turn it off for extra security.  </span></span><br/> |
|<span data-ttu-id="5dfc8-146">Autoriser les utilisateurs à accéder à Cortana</span><span class="sxs-lookup"><span data-stu-id="5dfc8-146">Allow users to access Cortana</span></span>  <br/> |<span data-ttu-id="5dfc8-p109">Cortana peut être très utile ! Elle peut activer ou désactiver des paramètres pour vous, vous indiquer un trajet ou veiller à ce que vous arriviez à l'heure à vos rendez-vous. C'est la raison pour laquelle ce paramètre est **activé** par défaut.  </span><span class="sxs-lookup"><span data-stu-id="5dfc8-p109">Cortana can be very helpful! She can turn settings on or off for you, give directions, and make sure you're on time for appointments, so we keep this **On** by default.  </span></span><br/> |
|<span data-ttu-id="5dfc8-149">Autoriser les utilisateurs à recevoir des conseils de Windows et des annonces de Microsoft</span><span class="sxs-lookup"><span data-stu-id="5dfc8-149">Allow users to receive Windows tips and advertisements from Microsoft</span></span>  <br/> |<span data-ttu-id="5dfc8-150">Les conseils Windows peuvent être très pratiques et aident les utilisateurs lors du lancement de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-150">Windows tips can be handy and help orient users when new features are released.</span></span>  <br/> |
|<span data-ttu-id="5dfc8-151">Maintenir les appareils Windows 10 à jour automatiquement</span><span class="sxs-lookup"><span data-stu-id="5dfc8-151">Keep Windows 10 devices up to date automatically</span></span>  <br/> |<span data-ttu-id="5dfc8-152">Permet d'assurer que les appareils Windows 10 reçoivent automatiquement les dernières mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-152">Makes sure that Windows 10 devices automatically receive the latest updates.</span></span>  <br/> |
|<span data-ttu-id="5dfc8-153">Désactiver l'écran d'un appareil resté inactif pendant</span><span class="sxs-lookup"><span data-stu-id="5dfc8-153">Turn off device screen when idle for this amount of time</span></span>  <br/> |<span data-ttu-id="5dfc8-p110">Permet d'assurer la protection des données d'entreprise lorsqu'un utilisateur est inactif. Il est possible qu'un utilisateur travaille dans un lieu public, par exemple un café, et s'éloigne ou soit distrait pendant un instant, laissant son appareil à la vue de tous. Ce paramètre vous permet de contrôler la durée pendant laquelle l'utilisateur peut être inactif avant l'extinction de l'écran.</span><span class="sxs-lookup"><span data-stu-id="5dfc8-p110">Makes sure that company data is protected if a user is idle. A user may be working in a public location, like a coffee shop, and step away or be distracted for just a moment, leaving their device vulnerable to random glances. This setting lets you control how long the user can be idle before the screen shuts off.</span></span>  <br/> |
   
  

