---
title: Protéger les PC Windows 10 et les Mac non gérés
f1.keywords:
- NOCSH
ms.author: sharik
author: SKjerland
manager: scotv
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
- M365-Campaigns
- m365solution-smb
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Protégez les appareils BYOD (ByOD) non utilisés ou apportez-les à l’Microsoft 365.
ms.openlocfilehash: 430f5446f86c26cb1f0fd1c7f34613cddec473b2
ms.sourcegitcommit: c5d1528559953c6db7dca1d5cb453e0aa3215f02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/27/2021
ms.locfileid: "51398252"
---
# <a name="protect-unmanaged-windows-10-pcs-and-macs"></a><span data-ttu-id="15b28-103">Protéger les PC Windows 10 et les Mac non gérés</span><span class="sxs-lookup"><span data-stu-id="15b28-103">Protect unmanaged Windows 10 PCs and Macs</span></span>

<span data-ttu-id="15b28-104">Vous pouvez gérer Windows 10 PC et Mac en les inscrivant dans Microsoft Intune, ce qui vous permet de vous assurer qu’ils sont sains et sécurisés avant d’accéder aux données de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="15b28-104">You can manage Windows 10 PCs and Macs by enrolling them in Microsoft Intune, which allows you to ensure they're healthy and secure before accessing data in your environment.</span></span> <span data-ttu-id="15b28-105">Toutefois, de nombreuses campagnes et petites entreprises incluent des employés qui apportent leurs propres appareils (BYOD), qui ne seront pas gérés par l’organisation.</span><span class="sxs-lookup"><span data-stu-id="15b28-105">However, many campaigns and small businesses include staff who bring their own devices (BYOD), which will not be managed by the organization.</span></span> <span data-ttu-id="15b28-106">Pour ces PC et Mac non utilisés, utilisez cet article pour vous assurer que les fonctionnalités de sécurité minimales sont configurées.</span><span class="sxs-lookup"><span data-stu-id="15b28-106">For these unmanaged PCs and Macs, use this article to ensure that minimum security capabilities are configured.</span></span>

<!--A Windows 10 PC is considered managed after you have completed the following two steps:

1. You (or the admin) set up device and data protection policies in the [setup  wizard](../business/set-up.md).

2. You have [connected your computer to Azure Active Directory](../business/set-up-windows-devices.md) and use your Microsoft 365 username and password to sign in.
3. --> 

## <a name="protect-a-computer-running-windows-10-or-a-mac"></a><span data-ttu-id="15b28-107">Protéger un ordinateur exécutant Windows 10 mac</span><span class="sxs-lookup"><span data-stu-id="15b28-107">Protect a computer running Windows 10 or a Mac</span></span>

<!--If you have a PC that is running Windows 10 that is not connected to Microsoft 365, or a Mac, the Microsoft 365 protections do not apply to it, but here are some things you can do to keep your data secure on these devices as well:
-->
<span data-ttu-id="15b28-108">Si votre pc Windows 10 mac n’est pas géré par votre organisation, assurez-vous de configurer ces fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="15b28-108">If your Windows 10 PC or Mac is not managed by your organization, be sure to configure these security capabilities.</span></span>

## <a name="windows-10"></a>[<span data-ttu-id="15b28-109">Windows 10</span><span class="sxs-lookup"><span data-stu-id="15b28-109">Windows 10</span></span>](#tab/Windows10)

<span data-ttu-id="15b28-110">**Activer le chiffrement de l’appareil**</span><span class="sxs-lookup"><span data-stu-id="15b28-110">**Turn on device encryption**</span></span><p>

<span data-ttu-id="15b28-111">Le chiffrement de l’appareil est disponible sur un large éventail Windows et permet de protéger vos données en les chiffrant.</span><span class="sxs-lookup"><span data-stu-id="15b28-111">Device encryption is available on a wide range of Windows devices and helps protect your data by encrypting it.</span></span> <span data-ttu-id="15b28-112">Si vous allumez le chiffrement de l’appareil, seules les personnes autorisées pourront accéder à votre appareil et à vos données.</span><span class="sxs-lookup"><span data-stu-id="15b28-112">If you turn on device encryption, only authorized individuals will be able to access your device and data.</span></span> <span data-ttu-id="15b28-113">Pour obtenir [des instructions, voir](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) activer le chiffrement de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="15b28-113">See [turn on device encryption](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) for instructions.</span></span>

 <span data-ttu-id="15b28-114">Si le chiffrement de l’appareil n’est pas disponible sur votre appareil, vous pouvez activer le chiffrement [BitLocker standard](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) à la place.</span><span class="sxs-lookup"><span data-stu-id="15b28-114">If device encryption isn't available on your device, you can turn on standard [BitLocker encryption](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) instead.</span></span> <span data-ttu-id="15b28-115">(BitLocker n’est pas disponible sur Windows 10 Famille édition.)</span><span class="sxs-lookup"><span data-stu-id="15b28-115">(BitLocker isn't available on Windows 10 Home edition.)</span></span> 

<span data-ttu-id="15b28-116">**Protégez votre appareil à l’Sécurité Windows**</span><span class="sxs-lookup"><span data-stu-id="15b28-116">**Protect your device with Windows Security**</span></span><p>
<span data-ttu-id="15b28-117">Si vous avez Windows 10, vous obtenez la dernière protection antivirus avec Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="15b28-117">If you have Windows 10, you'll get the latest antivirus protection with Windows Security.</span></span> <span data-ttu-id="15b28-118">Lorsque vous démarrez Windows 10 pour la première fois, Sécurité Windows est active et contribue activement à protéger votre PC en analysant les programmes malveillants (logiciels malveillants), les virus et les menaces de sécurité.</span><span class="sxs-lookup"><span data-stu-id="15b28-118">When you start up Windows 10 for the first time, Windows Security is on and actively helping to protect your PC by scanning for malware (malicious software), viruses, and security threats.</span></span> <span data-ttu-id="15b28-119">Sécurité Windows la protection en temps réel pour analyser tout ce que vous téléchargez ou exécutez sur votre PC.</span><span class="sxs-lookup"><span data-stu-id="15b28-119">Windows Security uses real-time protection to scan everything you download or run on your PC.</span></span>

<span data-ttu-id="15b28-120">Windows Update télécharge automatiquement les mises à jour de sécurité Windows pour assurer la sécurité de votre PC et le protéger contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="15b28-120">Windows Update downloads updates for Windows Security automatically to help keep your PC safe and protect it from threats.</span></span>

<span data-ttu-id="15b28-121">Si vous avez une version antérieure de Windows et que vous utilisez Microsoft Security Essentials, il est bon de passer à Sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="15b28-121">If you have an earlier version of Windows and are using Microsoft Security Essentials, it's a good idea to move to Windows Security.</span></span> <span data-ttu-id="15b28-122">Pour plus d’informations, [voir l’aide pour protéger mon appareil avec Sécurité Windows](https://support.microsoft.com/help/17464/windows-10-help-protect-my-device-with-windows-security).</span><span class="sxs-lookup"><span data-stu-id="15b28-122">For more information, see [help protect my device with Windows Security](https://support.microsoft.com/help/17464/windows-10-help-protect-my-device-with-windows-security).</span></span>

<span data-ttu-id="15b28-123">**Activer le pare-feu Windows de sécurité**</span><span class="sxs-lookup"><span data-stu-id="15b28-123">**Turn on Windows Firewall**</span></span><p>
<span data-ttu-id="15b28-124">Vous devez toujours exécuter Windows pare-feu même si un autre pare-feu est allumé.</span><span class="sxs-lookup"><span data-stu-id="15b28-124">You should always run Windows Firewall even if you have another firewall turned on.</span></span> <span data-ttu-id="15b28-125">La dés Windows pare-feu peut rendre votre appareil (et votre réseau, si vous en avez un) plus vulnérable aux accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="15b28-125">Turning off Windows Firewall might make your device (and your network, if you have one) more vulnerable to unauthorized access.</span></span> <span data-ttu-id="15b28-126">Pour [plus d’Windows, voir](https://support.microsoft.com/help/4028544/windows-10-turn-windows-defender-firewall-on-or-off) Activer ou désactiver le pare-feu.</span><span class="sxs-lookup"><span data-stu-id="15b28-126">See [Turn Windows Firewall on or off](https://support.microsoft.com/help/4028544/windows-10-turn-windows-defender-firewall-on-or-off) for instructions.</span></span>

## <a name="mac"></a>[<span data-ttu-id="15b28-127">Mac</span><span class="sxs-lookup"><span data-stu-id="15b28-127">Mac</span></span>](#tab/Mac)

<span data-ttu-id="15b28-128">**Utiliser FileVault pour chiffrer votre disque Mac**</span><span class="sxs-lookup"><span data-stu-id="15b28-128">**Use FileVault to encrypt your Mac disk**</span></span><p>
<span data-ttu-id="15b28-129">Le chiffrement de disque protège les données en cas de perte ou de vol d’appareils.</span><span class="sxs-lookup"><span data-stu-id="15b28-129">Disk encryption protects data when devices are lost or stolen.</span></span> <span data-ttu-id="15b28-130">Le chiffrement de disque intégral FileVault permet d’empêcher l’accès non autorisé aux informations sur votre disque de démarrage.</span><span class="sxs-lookup"><span data-stu-id="15b28-130">FileVault full-disk encryption helps prevent unauthorized access to the information on your startup disk.</span></span> <span data-ttu-id="15b28-131">Voir [utiliser FileVault pour chiffrer le disque de démarrage sur votre Mac pour](https://support.apple.com/HT204837) obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="15b28-131">See [use FileVault to encrypt the startup disk on your Mac](https://support.apple.com/HT204837) for instructions.</span></span>

<span data-ttu-id="15b28-132">**Protéger votre mac contre les programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="15b28-132">**Protect your mac from malware**</span></span><p>
<span data-ttu-id="15b28-133">Microsoft vous recommande d’installer et d’utiliser des logiciels antivirus fiables sur votre Mac.</span><span class="sxs-lookup"><span data-stu-id="15b28-133">Microsoft recommends that you install and use reliable antivirus software on your Mac.</span></span> <span data-ttu-id="15b28-134">Consultez l’article suivant pour obtenir la liste des choix : [Best Mac antivirus 2019 ](https://www.macworld.co.uk/feature/mac-software/mac-antivirus-3672182/).</span><span class="sxs-lookup"><span data-stu-id="15b28-134">See the following article for a list of choices: [Best Mac antivirus 2019 ](https://www.macworld.co.uk/feature/mac-software/mac-antivirus-3672182/).</span></span>

<span data-ttu-id="15b28-135">Vous pouvez également réduire le risque de programmes malveillants en utilisant des logiciels uniquement à partir de sources fiables.</span><span class="sxs-lookup"><span data-stu-id="15b28-135">You can also reduce the risk of malware by using software only from reliable sources.</span></span> <span data-ttu-id="15b28-136">Les paramètres des préférences de confidentialité & sécurité vous permettent de spécifier les sources de logiciels installées sur votre Mac.</span><span class="sxs-lookup"><span data-stu-id="15b28-136">The settings in Security & Privacy preferences allow you to specify the sources of software installed on your Mac.</span></span> <span data-ttu-id="15b28-137">Pour plus d’informations, [voir protéger votre Mac contre les programmes malveillants.](https://support.apple.com/kb/PH25087)</span><span class="sxs-lookup"><span data-stu-id="15b28-137">For more information, see [protect your Mac from malware](https://support.apple.com/kb/PH25087).</span></span>

<span data-ttu-id="15b28-138">**Activer la protection contre le pare-feu**</span><span class="sxs-lookup"><span data-stu-id="15b28-138">**Turn on firewall protection**</span></span><p>
<span data-ttu-id="15b28-139">Utilisez les paramètres de pare-feu pour protéger votre Mac contre les contacts indésirables initiés par d’autres ordinateurs lorsque vous êtes connecté à Internet ou à un réseau.</span><span class="sxs-lookup"><span data-stu-id="15b28-139">Use firewall settings to protect your Mac from unwanted contact initiated by other computers when you're connected to the Internet or a network.</span></span> <span data-ttu-id="15b28-140">Sans cette protection, votre Mac peut être plus vulnérable aux accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="15b28-140">Without this protection, your Mac might be more vulnerable to unauthorized access.</span></span> <span data-ttu-id="15b28-141">Pour obtenir des instructions, voir le [pare-feu](https://support.apple.com/HT201642) de l’application.</span><span class="sxs-lookup"><span data-stu-id="15b28-141">See [about the application firewall](https://support.apple.com/HT201642) for instructions.</span></span>
