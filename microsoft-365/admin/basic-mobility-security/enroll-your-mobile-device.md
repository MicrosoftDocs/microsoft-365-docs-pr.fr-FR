---
title: Inscrire votre appareil mobile à l’aide de la mobilité et de la sécurité de base
f1.keywords:
- NOCSH
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
ms.custom:
- AdminSurgePortfolio
search.appverid:
- MET150
description: Pour pouvoir utiliser les services Microsoft 365 avec votre appareil, vous devrez peut-être d’abord l’inscrire dans la sécurité et la mobilité de base pour Microsoft 365.
ms.openlocfilehash: e31054621ba44a4d5f08de9b366fa0978b738cd9
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47430165"
---
# <a name="enroll-your-mobile-device-using-basic-mobility-and-security"></a><span data-ttu-id="5b3c8-103">Inscrire votre appareil mobile à l’aide de la mobilité et de la sécurité de base</span><span class="sxs-lookup"><span data-stu-id="5b3c8-103">Enroll your mobile device using Basic Mobility and Security</span></span>

<span data-ttu-id="5b3c8-104">L’utilisation de votre téléphone, de votre tablette et d’autres appareils mobiles pour le travail est un excellent moyen de rester informé et de travailler sur des projets professionnels lorsque vous êtes en déplacement.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-104">Using your phone, tablet, and other mobile devices for work is a great way to stay informed and work on business projects while you’re away from the office.</span></span> <span data-ttu-id="5b3c8-105">Pour pouvoir utiliser les services Microsoft 365 avec votre appareil, vous devrez peut-être d’abord l’inscrire dans la sécurité et la mobilité de base pour Microsoft 365 à l’aide du portail d’entreprise Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-105">Before you can use Microsoft 365 services with your device, you might need to first enroll it in Basic Mobility and Security for Microsoft 365 using Microsoft Intune Company Portal.</span></span>

<span data-ttu-id="5b3c8-106">Les organisations choisissent la mobilité et la sécurité de base afin que les employés puissent utiliser leurs appareils mobiles pour accéder en toute sécurité aux e-mails, calendriers et documents professionnels, tandis que l’entreprise sécurise les données importantes et répond aux exigences de conformité.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-106">Organizations choose Basic Mobility and Security so that employees can use their mobile devices to securely access work email, calendars, and documents while the business secures important data and meets their compliance requirements.</span></span><span data-ttu-id="5b3c8-107">Pour plus d’informations, reportez-vous à la rubrique [Overview of Basic Mobility and Security for Microsoft 365](overview.md).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-107"> To learn more, see [Overview of Basic Mobility and Security for Microsoft 365](overview.md).</span></span> <span data-ttu-id="5b3c8-108">Pour plus d’informations, consultez la rubrique [Quelles informations mon organisation peut-il voir lorsque j’inscrit mon appareil ?](https://docs.microsoft.com/intune-user-help/what-info-can-your-company-see-when-you-enroll-your-device-in-intune).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-108">For more info, see [What information can my organization see when I enroll my device?](https://docs.microsoft.com/intune-user-help/what-info-can-your-company-see-when-you-enroll-your-device-in-intune).</span></span>

>[!IMPORTANT] 
><span data-ttu-id="5b3c8-109">Lorsque vous inscrivez votre appareil dans le cadre de la mobilité et de la sécurité de base pour Microsoft 365, il se peut que vous deviez configurer un mot de passe, ainsi que l’option permettant à votre organisation professionnelle de réinitialiser l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-109">When you enroll your device in Basic Mobility and Security for Microsoft 365, you might be required to set up a password, together with allowing the option for your work organization to wipe the device.</span></span> <span data-ttu-id="5b3c8-110">Une réinitialisation du périphérique peut être effectuée à partir du centre d’administration Microsoft 365, par exemple, pour supprimer toutes les données de l’appareil si le mot de passe n’est pas entré correctement trop souvent ou si les conditions d’utilisation sont rompues.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-110">A device wipe can be performed from the Microsoft 365 admin center, for example, to remove all data from the device if the password is entered incorrectly too many times or if usage terms are broken.</span></span>

## <a name="supported-devices"></a><span data-ttu-id="5b3c8-111">Appareils pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3c8-111">Supported devices</span></span>

<span data-ttu-id="5b3c8-112">La sécurité et la mobilité de base pour Microsoft 365 hébergées par le service Intune fonctionnent avec la plupart des appareils mobiles, mais pas tous.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-112">Basic Mobility and Security for Microsoft 365 hosted by the Intune service works with most, but not all, mobile devices.</span></span> <span data-ttu-id="5b3c8-113">Les éléments suivants sont pris en charge avec la sécurité et la mobilité de base :</span><span class="sxs-lookup"><span data-stu-id="5b3c8-113">The following are supported with Basic Mobility and Security:</span></span>

- <span data-ttu-id="5b3c8-114">iOS 10,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5b3c8-114">iOS 10.0 or later</span></span>
    
- <span data-ttu-id="5b3c8-115">Android 4,4 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5b3c8-115">Android 4.4 or later</span></span>
    
- <span data-ttu-id="5b3c8-116">Windows 8,1 et Windows 10 (téléphone et PC)</span><span class="sxs-lookup"><span data-stu-id="5b3c8-116">Windows 8.1 and Windows 10 (Phone and PC)</span></span>
    
<span data-ttu-id="5b3c8-117">Si votre appareil n’est pas mentionné ci-dessus, et que vous devez l’utiliser avec la sécurité et la mobilité de base, contactez votre administrateur professionnel ou scolaire.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-117">If your device is not listed above, and you need to use it with Basic Mobility and Security, contact your work or school administrator.</span></span>

>[!TIP] 
><span data-ttu-id="5b3c8-118">Si vous ne parvenez pas à inscrire votre appareil, consultez la rubrique [Troubleshoot Basic Mobility and Security](troubleshoot.md).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-118">If you're having trouble enrolling your device, see [Troubleshoot Basic Mobility and Security](troubleshoot.md).</span></span>

## <a name="set-up-your-mobile-device-with-intune-and-basic-mobility-and-security"></a><span data-ttu-id="5b3c8-119">Configurer votre appareil mobile avec Intune et la mobilité et la sécurité de base</span><span class="sxs-lookup"><span data-stu-id="5b3c8-119">Set up your mobile device with Intune and Basic Mobility and Security</span></span>

<span data-ttu-id="5b3c8-120">Le portail d’entreprise Intune permet à un appareil d’être géré par Microsoft 365 et la sécurité et la mobilité de base.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-120">The Intune Company Portal enables a device to be managed by Microsoft 365 and Basic Mobility and Security.</span></span>

### <a name="iphone-or-ipad"></a><span data-ttu-id="5b3c8-121">iPhone ou iPad</span><span class="sxs-lookup"><span data-stu-id="5b3c8-121">iPhone or iPad</span></span>

>[!TIP]
><span data-ttu-id="5b3c8-122">Vous ne pourrez pas envoyer et recevoir des courriers électroniques tant que vous n’aurez pas effectué cette étape.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-122">You won’t be able to send and receive email until you complete this step.</span></span>

<span data-ttu-id="5b3c8-123">Accédez à Apple App Store, puis téléchargez et installez le portail d’entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-123">Go to the Apple App Store, and download and install Intune Company Portal.</span></span>

<span data-ttu-id="5b3c8-124">Pour vous connecter et configurer votre tablette ou téléphone iOS avec le portail d’entreprise vers Office 365, consultez la rubrique [configurer l’accès des appareils iOS aux ressources de votre entreprise](https://go.microsoft.com/fwlink/?linkid=875316).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-124">To connect and configure your iOS phone or tablet with the Company portal to Office 365, see [Set up iOS device access to your company resources](https://go.microsoft.com/fwlink/?linkid=875316).</span></span>

### <a name="android-phone-or-tablet"></a><span data-ttu-id="5b3c8-125">Téléphone Android ou tablette</span><span class="sxs-lookup"><span data-stu-id="5b3c8-125">Android phone or tablet</span></span>

>[!TIP]
><span data-ttu-id="5b3c8-126">Vous ne pourrez pas envoyer et recevoir des courriers électroniques tant que vous n’aurez pas effectué cette étape.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-126">You won’t be able to send and receive email until you complete this step.</span></span>

<span data-ttu-id="5b3c8-127">Accédez à Google Play Store, puis téléchargez et installez le portail d’entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-127">Go to the Google Play store, and download and install Intune Company Portal.</span></span>

<span data-ttu-id="5b3c8-128">Pour vous connecter et configurer votre téléphone Android ou votre tablette à l’aide du portail d’entreprise vers Microsoft 365, consultez la rubrique [inscrire votre appareil avec le portail d’entreprise](https://go.microsoft.com/fwlink/?linkid=875317).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-128">To connect and configure your Android phone or tablet with the Company portal to Microsoft 365, see [Enroll your device with Company Portal](https://go.microsoft.com/fwlink/?linkid=875317).</span></span>

### <a name="windows-81-and-windows-10"></a><span data-ttu-id="5b3c8-129">Windows 8,1 et Windows 10</span><span class="sxs-lookup"><span data-stu-id="5b3c8-129">Windows 8.1 and Windows 10</span></span>

<span data-ttu-id="5b3c8-130">Accédez au Microsoft Store, puis téléchargez et installez le portail d’entreprise Intune.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-130">Go to the Microsoft Store, and download and install Intune Company Portal</span></span>

<span data-ttu-id="5b3c8-131">Pour vous connecter et configurer votre téléphone ou votre PC Windows avec le portail d’entreprise vers Microsoft 365, voir [Windows Device Apto in Intune Company Portal](https://docs.microsoft.com/intune-user-help/windows-enrollment-company-portal).</span><span class="sxs-lookup"><span data-stu-id="5b3c8-131">To connect and configure your Windows phone or PC with the Company portal to Microsoft 365, see [Windows device enrollment in Intune Company Portal](https://docs.microsoft.com/intune-user-help/windows-enrollment-company-portal).</span></span>

## <a name="whats-next"></a><span data-ttu-id="5b3c8-132">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5b3c8-132">What's next?</span></span>

<span data-ttu-id="5b3c8-133">Une fois que votre appareil est intégré à la sécurité et à la mobilité de base, vous pouvez commencer à utiliser les applications Office sur votre appareil pour utiliser la messagerie, le calendrier, les contacts et les documents.</span><span class="sxs-lookup"><span data-stu-id="5b3c8-133">After your device is enrolled in Basic Mobility and Security, you can start using Office apps on your device to work with email, calendar, contacts, and documents.</span></span>