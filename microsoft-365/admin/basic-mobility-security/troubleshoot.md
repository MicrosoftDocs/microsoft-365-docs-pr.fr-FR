---
title: Résoudre les problèmes de sécurité et de mobilité de base
f1.keywords: NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom: AdminSurgePortfolio
description: Suivez ces étapes pour suivre les problèmes de sécurité et de mobilité de base
ms.openlocfilehash: 43e7533e598f769dd5f2bcae28c4252f96a9be76
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47430155"
---
# <a name="troubleshoot-basic-mobility-and-security"></a><span data-ttu-id="f20e4-103">Résoudre les problèmes de sécurité et de mobilité de base</span><span class="sxs-lookup"><span data-stu-id="f20e4-103">Troubleshoot Basic Mobility and Security</span></span>

<span data-ttu-id="f20e4-104">Si vous rencontrez des problèmes lorsque vous essayez d’inscrire un appareil dans le cadre de la sécurité et de la mobilité de base, essayez les étapes suivantes pour suivre le problème.</span><span class="sxs-lookup"><span data-stu-id="f20e4-104">If you're running into issues when you try to enroll a device in Basic Mobility and Security, try the steps here to track down the problem.</span></span> <span data-ttu-id="f20e4-105">Si la procédure générale ne résout pas le problème, reportez-vous à l’une des sections suivantes avec des étapes spécifiques pour votre type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="f20e4-105">If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>

## <a name="steps-to-try-first"></a><span data-ttu-id="f20e4-106">Étapes à essayer en premier lieu</span><span class="sxs-lookup"><span data-stu-id="f20e4-106">Steps to try first</span></span>

<span data-ttu-id="f20e4-107">Pour commencer, vérifiez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="f20e4-107">To start, check the following:</span></span>

- <span data-ttu-id="f20e4-108">Assurez-vous que l’appareil n’est pas déjà associé à un autre fournisseur de gestion des appareils mobiles, comme Intune.</span><span class="sxs-lookup"><span data-stu-id="f20e4-108">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>
    
- <span data-ttu-id="f20e4-109">Assurez-vous que l’appareil est défini sur la date et l’heure correctes.</span><span class="sxs-lookup"><span data-stu-id="f20e4-109">Make sure that the device is set to the correct date and time.</span></span>
    
- <span data-ttu-id="f20e4-110">Basculez vers un autre réseau Wi-Fi ou cellulaire sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f20e4-110">Switch to a different WIFI or cellular network on the device.</span></span>
    
- <span data-ttu-id="f20e4-111">Pour les appareils Android ou iOS, désinstallez et réinstallez l’application portail d’entreprise Intune sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f20e4-111">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span> 

## <a name="ios-phone-or-tablet"></a><span data-ttu-id="f20e4-112">téléphone ou tablette iOS</span><span class="sxs-lookup"><span data-stu-id="f20e4-112">iOS phone or tablet</span></span>

- <span data-ttu-id="f20e4-113">Assurez-vous que vous avez configuré un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="f20e4-113">Make sure that you've set up an APNs certificate.</span></span> <span data-ttu-id="f20e4-114">Pour plus d’informations, consultez la rubrique [créer un certificat APNs pour les appareils iOS](create-an-apns-certificate-for-ios-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f20e4-114">For more info, see [Create an APNs Certificate for iOS devices](create-an-apns-certificate-for-ios-devices.md).</span></span>
    
- <span data-ttu-id="f20e4-115">Dans **paramètres**   >  **généraux**   >  **profil (ou gestion des appareils)**, assurez-vous qu’aucun profil de gestion n’est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="f20e4-115">In **Settings** > **General** > **Profile (or Device Management)**, make sure that a Management Profile is not already installed.</span></span> <span data-ttu-id="f20e4-116">Si c’est le cas, supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="f20e4-116">If it is, remove it.</span></span>
    
- <span data-ttu-id="f20e4-117">Si vous voyez le message d’erreur « Échec de l’inscription de l’appareil », connectez-vous à Microsoft 365 et assurez-vous qu’une licence qui inclut Exchange Online a été affectée à l’utilisateur connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f20e4-117">If you see the error message, "Device failed to enroll," sign in to Microsoft 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="f20e4-118">Si vous voyez le message d’erreur « Échec de l’installation du profil », effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f20e4-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>
    
    - <span data-ttu-id="f20e4-119">Assurez-vous que Safari est le navigateur par défaut sur l’appareil et que les cookies ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="f20e4-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>
    
    - <span data-ttu-id="f20e4-120">Redémarrez l’appareil, puis accédez à portal.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="f20e4-120">Reboot the device, and then navigate to portal.manage.microsoft.com.</span></span> <span data-ttu-id="f20e4-121">Connectez-vous avec votre ID d’utilisateur et votre mot de passe Microsoft 365, puis essayez d’installer le profil manuellement.</span><span class="sxs-lookup"><span data-stu-id="f20e4-121">Sign in with your Microsoft 365 user ID and password, and attempt to install the profile manually.</span></span>    

## <a name="windows-rt"></a><span data-ttu-id="f20e4-122">Windows RT</span><span class="sxs-lookup"><span data-stu-id="f20e4-122">Windows RT</span></span>

- <span data-ttu-id="f20e4-123">Assurez-vous que votre domaine est configuré dans Microsoft 365 pour fonctionner avec la sécurité et la mobilité de base.</span><span class="sxs-lookup"><span data-stu-id="f20e4-123">Make sure that your domain is set up in Microsoft 365 to work with Basic Mobility and Security.</span></span> <span data-ttu-id="f20e4-124">Pour plus d’informations, consultez la rubrique [Set Up Basic Mobility and Security](set-up.md).</span><span class="sxs-lookup"><span data-stu-id="f20e4-124">For more info, see [Set up Basic Mobility and Security](set-up.md).</span></span>
    
- <span data-ttu-id="f20e4-125">Assurez-vous que l’utilisateur choisit **activer**   plutôt que de **joindre**.</span><span class="sxs-lookup"><span data-stu-id="f20e4-125">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>    

## <a name="windows-10-pc"></a><span data-ttu-id="f20e4-126">PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="f20e4-126">Windows 10 PC</span></span>

- <span data-ttu-id="f20e4-127">Assurez-vous que votre domaine est configuré dans Microsoft 365 pour fonctionner avec la sécurité et la mobilité de base.</span><span class="sxs-lookup"><span data-stu-id="f20e4-127">Make sure that your domain is set up in Microsoft 365 to work with Basic Mobility and Security.</span></span> <span data-ttu-id="f20e4-128">Pour plus d’informations, consultez la rubrique [Set Up Basic Mobility and Security](set-up.md).</span><span class="sxs-lookup"><span data-stu-id="f20e4-128">For more info, see [Set up Basic Mobility and Security](set-up.md).</span></span>
    
- <span data-ttu-id="f20e4-129">À moins d’avoir Azure Active Directory Premium, assurez-vous que l’utilisateur choisit **inscrire dans la gestion des appareils uniquement**   plutôt que de choisir **connecter**.</span><span class="sxs-lookup"><span data-stu-id="f20e4-129">Unless you have Azure Active Directory Premium, make sure that the user is choosing **Enroll in Device Management only** rather than choosing **Connect**.</span></span>

## <a name="android-phone-or-tablet"></a><span data-ttu-id="f20e4-130">Téléphone Android ou tablette</span><span class="sxs-lookup"><span data-stu-id="f20e4-130">Android phone or tablet</span></span>

- <span data-ttu-id="f20e4-131">Assurez-vous que l’appareil exécute Android 4,4 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f20e4-131">Make sure the device is running Android 4.4 or later.</span></span>
    
- <span data-ttu-id="f20e4-132">Assurez-vous que Chrome est à jour et qu’il est défini en tant que navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f20e4-132">Make sure that Chrome is up to date and is set as the default browser.</span></span>
    
- <span data-ttu-id="f20e4-133">Si vous voyez le message d’erreur « nous n’avons pas pu inscrire ce périphérique », connectez-vous à Microsoft 365 et assurez-vous qu’une licence qui inclut Exchange Online a été affectée à l’utilisateur connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f20e4-133">If you see the error message, "We couldn't enroll this device," sign in to Microsoft 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>
    
- <span data-ttu-id="f20e4-134">Vérifiez la zone de notification sur l’appareil pour voir si des actions de l’utilisateur final requises sont en attente et, le cas échéant, effectuez les actions.</span><span class="sxs-lookup"><span data-stu-id="f20e4-134">Check the Notification Area on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span>