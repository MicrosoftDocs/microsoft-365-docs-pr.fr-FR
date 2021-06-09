---
title: Résoudre les problèmes de mobilité et de sécurité de base
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
description: Suivez ces étapes pour suivre les problèmes de mobilité et de sécurité de base
ms.openlocfilehash: b8df8c17f3a2fc5b7b6cce21769ca20742dbd397
ms.sourcegitcommit: 8849dd6f80217c29f427c7f008d918f30c792240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2021
ms.locfileid: "49876851"
---
# <a name="troubleshoot-basic-mobility-and-security"></a><span data-ttu-id="68da9-103">Résoudre les problèmes de mobilité et de sécurité de base</span><span class="sxs-lookup"><span data-stu-id="68da9-103">Troubleshoot Basic Mobility and Security</span></span>

<span data-ttu-id="68da9-104">Si vous êtes face à des problèmes lorsque vous essayez d’inscrire un appareil dans Basic Mobility and Security, suivez les étapes ci-après pour suivre le problème.</span><span class="sxs-lookup"><span data-stu-id="68da9-104">If you're running into issues when you try to enroll a device in Basic Mobility and Security, try the steps here to track down the problem.</span></span> <span data-ttu-id="68da9-105">Si les étapes générales ne corrigent pas le problème, consultez l’une des sections suivantes avec des étapes spécifiques pour votre type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="68da9-105">If the general steps don't fix the issue, see one of the later sections with specific steps for your device type.</span></span>

## <a name="steps-to-try-first"></a><span data-ttu-id="68da9-106">Étapes à suivre pour essayer en premier</span><span class="sxs-lookup"><span data-stu-id="68da9-106">Steps to try first</span></span>

<span data-ttu-id="68da9-107">Pour commencer, vérifiez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="68da9-107">To start, check the following:</span></span>

- <span data-ttu-id="68da9-108">Assurez-vous que l’appareil n’est pas déjà inscrit auprès d’un autre fournisseur de gestion des appareils mobiles, tel qu’Intune.</span><span class="sxs-lookup"><span data-stu-id="68da9-108">Make sure that the device is not already enrolled with another mobile device management provider, such as Intune.</span></span>

- <span data-ttu-id="68da9-109">Assurez-vous que la date et l’heure de l’appareil sont correctes.</span><span class="sxs-lookup"><span data-stu-id="68da9-109">Make sure that the device is set to the correct date and time.</span></span>

- <span data-ttu-id="68da9-110">Basculez vers un autre réseau WIFI ou cellulaire sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="68da9-110">Switch to a different WIFI or cellular network on the device.</span></span>

- <span data-ttu-id="68da9-111">Pour les appareils Android ou iOS, désinstallez et réinstallez l’Portail d’entreprise Intune sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="68da9-111">For Android or iOS devices, uninstall and reinstall the Intune Company Portal app on the device.</span></span> 

## <a name="ios-phone-or-tablet"></a><span data-ttu-id="68da9-112">Téléphone ou tablette iOS</span><span class="sxs-lookup"><span data-stu-id="68da9-112">iOS phone or tablet</span></span>

- <span data-ttu-id="68da9-113">Assurez-vous que vous avez bien installé un certificat APNs.</span><span class="sxs-lookup"><span data-stu-id="68da9-113">Make sure that you've set up an APNs certificate.</span></span> <span data-ttu-id="68da9-114">Pour plus d’informations, voir [Créer un certificat APNs pour les appareils iOS.](create-an-apns-certificate-for-ios-devices.md)</span><span class="sxs-lookup"><span data-stu-id="68da9-114">For more info, see [Create an APNs Certificate for iOS devices](create-an-apns-certificate-for-ios-devices.md).</span></span>

- <span data-ttu-id="68da9-115">Dans **Paramètres** profil général (ou gestion des appareils), assurez-vous qu’un profil de   >  \*\*\*\*   >  \*\*\*\* gestion n’est pas déjà installé.</span><span class="sxs-lookup"><span data-stu-id="68da9-115">In **Settings** > **General** > **Profile (or Device Management)**, make sure that a Management Profile is not already installed.</span></span> <span data-ttu-id="68da9-116">Si c’est le cas, supprimez-le.</span><span class="sxs-lookup"><span data-stu-id="68da9-116">If it is, remove it.</span></span>

- <span data-ttu-id="68da9-117">Si le message d’erreur « L’appareil n’a pas pu s’inscrire », connectez-vous à Microsoft 365 et assurez-vous qu’une licence incluant Exchange Online a été attribuée à l’utilisateur connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="68da9-117">If you see the error message, "Device failed to enroll," sign in to Microsoft 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>

- <span data-ttu-id="68da9-118">Si vous voyez le message d’erreur « Échec de l’installation du profil », essayez l’une des procédures suivantes :</span><span class="sxs-lookup"><span data-stu-id="68da9-118">If you see the error message, "Profile failed to install," try one of the following:</span></span>

    - <span data-ttu-id="68da9-119">Assurez-vous que Safari est le navigateur par défaut sur l’appareil et que les cookies ne sont pas désactivés.</span><span class="sxs-lookup"><span data-stu-id="68da9-119">Make sure that Safari is the default browser on the device, and that cookies are not disabled.</span></span>

    - <span data-ttu-id="68da9-120">Redémarrez l’appareil, puis accédez à portal.manage.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="68da9-120">Reboot the device, and then navigate to portal.manage.microsoft.com.</span></span> <span data-ttu-id="68da9-121">Connectez-vous avec votre Microsoft 365'utilisateur et votre mot de passe, puis essayez d’installer le profil manuellement.</span><span class="sxs-lookup"><span data-stu-id="68da9-121">Sign in with your Microsoft 365 user ID and password, and attempt to install the profile manually.</span></span>

## <a name="windows-rt"></a><span data-ttu-id="68da9-122">Windows RT</span><span class="sxs-lookup"><span data-stu-id="68da9-122">Windows RT</span></span>

- <span data-ttu-id="68da9-123">Assurez-vous que votre domaine est Microsoft 365 pour fonctionner avec basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="68da9-123">Make sure that your domain is set up in Microsoft 365 to work with Basic Mobility and Security.</span></span> <span data-ttu-id="68da9-124">Pour plus d’informations, voir [Configurer la mobilité et la sécurité de base.](set-up.md)</span><span class="sxs-lookup"><span data-stu-id="68da9-124">For more info, see [Set up Basic Mobility and Security](set-up.md).</span></span>
    
- <span data-ttu-id="68da9-125">Assurez-vous que l’utilisateur **choisit** Activer   plutôt que de participer. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="68da9-125">Make sure that the user is choosing **Turn On** rather than choosing **Join**.</span></span>

## <a name="windows-10-pc"></a><span data-ttu-id="68da9-126">Windows 10 PC</span><span class="sxs-lookup"><span data-stu-id="68da9-126">Windows 10 PC</span></span>

- <span data-ttu-id="68da9-127">Assurez-vous que votre domaine est Microsoft 365 pour fonctionner avec basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="68da9-127">Make sure that your domain is set up in Microsoft 365 to work with Basic Mobility and Security.</span></span> <span data-ttu-id="68da9-128">Pour plus d’informations, voir [Configurer la mobilité et la sécurité de base.](set-up.md)</span><span class="sxs-lookup"><span data-stu-id="68da9-128">For more info, see [Set up Basic Mobility and Security](set-up.md).</span></span>
    
- <span data-ttu-id="68da9-129">Sauf si vous avez Azure Active Directory Premium, assurez-vous que \*\*\*\* l’utilisateur choisit l’inscription à la gestion des appareils uniquement au lieu de   choisir **Connecter**.</span><span class="sxs-lookup"><span data-stu-id="68da9-129">Unless you have Azure Active Directory Premium, make sure that the user is choosing **Enroll in Device Management only** rather than choosing **Connect**.</span></span>

## <a name="android-phone-or-tablet"></a><span data-ttu-id="68da9-130">Téléphone ou tablette Android</span><span class="sxs-lookup"><span data-stu-id="68da9-130">Android phone or tablet</span></span>

- <span data-ttu-id="68da9-131">Assurez-vous que l’appareil exécute Android 4.4 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="68da9-131">Make sure the device is running Android 4.4 or later.</span></span>

- <span data-ttu-id="68da9-132">Assurez-vous que Chrome est à jour et qu’il est le navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="68da9-132">Make sure that Chrome is up to date and is set as the default browser.</span></span>

- <span data-ttu-id="68da9-133">Si le message d’erreur « Nous n’avons pas pu inscrire cet appareil » s’affiche, connectez-vous à Microsoft 365 et assurez-vous qu’une licence incluant Exchange Online a été attribuée à l’utilisateur qui est connecté à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="68da9-133">If you see the error message, "We couldn't enroll this device," sign in to Microsoft 365 and make sure that a license that includes Exchange Online has been assigned to the user who is signed in to the device.</span></span>

- <span data-ttu-id="68da9-134">Vérifiez la zone de notification sur l’appareil pour voir si des actions de l’utilisateur final requises sont en attente et, si c’est le cas, effectuer les actions.</span><span class="sxs-lookup"><span data-stu-id="68da9-134">Check the Notification Area on the device to see if any required end-user actions are pending, and if they are, complete the actions.</span></span>