---
title: Protection des ordinateurs Windows 10 et Mac non gérés
ms.author: sirkkuw
author: sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
- M365-identity-device-management
- M365-Campaigns
ms.custom:
- Adm_O365
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
description: Protégez-vous contre le hameçonnage et les autres attaques à l’aide de Microsoft 365 pour les campagnes.
ms.openlocfilehash: 2533710ccb7b173f5cc1fd19b185fcd32b7801c9
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38031289"
---
# <a name="protect-unmanaged-windows-10-pcs-and-macs"></a><span data-ttu-id="350aa-103">Protection des ordinateurs Windows 10 et Mac non gérés</span><span class="sxs-lookup"><span data-stu-id="350aa-103">Protect unmanaged Windows 10 PCs and Macs</span></span>

<span data-ttu-id="350aa-104">Vous pouvez gérer des PC Windows 10 et des Mac en les inscrivant dans Microsoft Intune, ce qui vous permet de vous assurer qu’ils sont sains et sécurisés avant d’accéder aux données de votre environnement.</span><span class="sxs-lookup"><span data-stu-id="350aa-104">You can manage Windows 10 PCs and Macs by enrolling them into Microsoft Intune, which allows you to ensure tht they are healthy and secure before accessing data in your environment.</span></span> <span data-ttu-id="350aa-105">Toutefois, de nombreuses campagnes et petites entreprises incluent des personnes qui apportent leurs propres appareils (BYOD), qui ne seront pas gérées par l’organisation.</span><span class="sxs-lookup"><span data-stu-id="350aa-105">However, many campaigns and small businesses include staff that bring their own devices (byod), which will not be managed by the organization.</span></span> <span data-ttu-id="350aa-106">Pour ces PC et Mac non gérés, utilisez cet article pour vous assurer que les fonctionnalités de sécurité minimales sont configurées.</span><span class="sxs-lookup"><span data-stu-id="350aa-106">For these unmanaged PCs and Macs, use this article to ensure that minimum security capabilities are configured.</span></span> 

<!--A Windows 10 PC is considered managed after you have completed the following two steps:

1. You (or the admin) set up device and data protection policies in the [setup  wizard](../business/set-up.md).

2. You have [connected your computer to Azure Active Directory](../business/set-up-windows-devices.md) and use your Microsoft 365 Business username and password to sign in.
3. --> 

## <a name="protect-a-computer-running-windows-10-or-a-mac"></a><span data-ttu-id="350aa-107">Protéger un ordinateur exécutant Windows 10 ou un Mac</span><span class="sxs-lookup"><span data-stu-id="350aa-107">Protect a computer running Windows 10 or a Mac</span></span>

<!--If you have a PC that is running Windows 10 that is not connected to Microsoft 365 Business, or a Mac, the Microsoft 365 Business protections do not apply to it, but here are some things you can do to keep your data secure on these devices as well:
-->
<span data-ttu-id="350aa-108">Si votre PC ou Mac Windows 10 n’est pas géré par votre organisation, veillez à configurer ces fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="350aa-108">If your Windows 10 PC or Mac is not managed by your organization, be sure to configure these security capabilities.</span></span>

## <a name="windows-10tabwindows10"></a>[<span data-ttu-id="350aa-109">Windows 10</span><span class="sxs-lookup"><span data-stu-id="350aa-109">Windows 10</span></span>](#tab/Windows10)
<span data-ttu-id="350aa-110">**Activer le chiffrement de l’appareil**</span><span class="sxs-lookup"><span data-stu-id="350aa-110">**Turn on device encryption**</span></span><p>

<span data-ttu-id="350aa-111">Le chiffrement d’appareil est disponible sur un large éventail d’appareils Windows et vous aide à protéger vos données en les chiffrant.</span><span class="sxs-lookup"><span data-stu-id="350aa-111">Device encryption is available on a wide range of Windows devices and helps protect your data by encrypting it.</span></span> <span data-ttu-id="350aa-112">Si vous activez le chiffrement de l’appareil, seules les personnes autorisées pourront accéder à votre appareil et à vos données.</span><span class="sxs-lookup"><span data-stu-id="350aa-112">If you turn on device encryption, only authorized individuals will be able to access your device and data.</span></span> <span data-ttu-id="350aa-113">Pour obtenir des instructions, voir [activer le chiffrement](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="350aa-113">See [turn on device encryption](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) for instructions.</span></span>

 <span data-ttu-id="350aa-114">Si le chiffrement de l’appareil n’est pas disponible sur votre appareil, vous pouvez activer le [chiffrement BitLocker](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) standard.</span><span class="sxs-lookup"><span data-stu-id="350aa-114">If device encryption is not available on your device, you can turn on standard [BitLocker encryption](https://support.microsoft.com/help/4028713/windows-10-turn-on-device-encryption) instead.</span></span> <span data-ttu-id="350aa-115">(BitLocker n’est pas disponible dans Windows 10 édition familiale.)</span><span class="sxs-lookup"><span data-stu-id="350aa-115">(BitLocker is not available on Windows 10 Home edition.)</span></span> 



<span data-ttu-id="350aa-116">**Protéger votre appareil avec la sécurité Windows**</span><span class="sxs-lookup"><span data-stu-id="350aa-116">**Protect your device with Windows Security**</span></span><p>
<span data-ttu-id="350aa-117">Si vous disposez de Windows 10, vous obtiendrez la dernière protection antivirus avec Windows Security.</span><span class="sxs-lookup"><span data-stu-id="350aa-117">If you have Windows 10, you’ll get the latest antivirus protection with Windows Security.</span></span> <span data-ttu-id="350aa-118">Lorsque vous démarrez Windows 10 pour la première fois, la sécurité de Windows est activée et contribue activement à protéger votre PC en recherchant les programmes malveillants (logiciels malveillants), les virus et les menaces de sécurité.</span><span class="sxs-lookup"><span data-stu-id="350aa-118">When you start up Windows 10 for the first time, Windows Security is on and actively helping to protect your PC by scanning for malware (malicious software), viruses, and security threats.</span></span> <span data-ttu-id="350aa-119">La sécurité Windows utilise la protection en temps réel pour analyser tout ce que vous téléchargez ou exécutez sur votre PC.</span><span class="sxs-lookup"><span data-stu-id="350aa-119">Windows Security uses real-time protection to scan everything you download or run on your PC.</span></span>

<span data-ttu-id="350aa-120">Windows Update télécharge automatiquement les mises à jour pour la sécurité Windows afin de protéger votre PC contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="350aa-120">Windows Update downloads updates for Windows Security automatically to help keep your PC safe and protect it from threats.</span></span>

<span data-ttu-id="350aa-121">Si vous disposez d’une version antérieure de Windows et que vous utilisez Microsoft Security Essentials, nous vous recommandons de passer à la sécurité Windows.</span><span class="sxs-lookup"><span data-stu-id="350aa-121">If you have an earlier version of Windows and are using Microsoft Security Essentials, it’s a good idea to move to Windows Security.</span></span> <span data-ttu-id="350aa-122">Pour plus d’informations, voir [protéger mon appareil avec Windows Security](https://support.microsoft.com/help/17464/windows-10-help-protect-my-device-with-windows-security) .</span><span class="sxs-lookup"><span data-stu-id="350aa-122">See [help protect my device with Windows Security](https://support.microsoft.com/help/17464/windows-10-help-protect-my-device-with-windows-security) for more information.</span></span>

<span data-ttu-id="350aa-123">**Activer le pare-feu Windows**</span><span class="sxs-lookup"><span data-stu-id="350aa-123">**Turn on Windows Firewall**</span></span><p>
<span data-ttu-id="350aa-124">Vous devez toujours exécuter le pare-feu Windows même si vous avez un autre pare-feu activé.</span><span class="sxs-lookup"><span data-stu-id="350aa-124">You should always run Windows Firewall even if you have another firewall turned on.</span></span> <span data-ttu-id="350aa-125">Désactiver le pare-feu Windows peut rendre votre appareil (et votre réseau, si vous en avez un) plus vulnérable aux accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="350aa-125">Turning off Windows Firewall might make your device (and your network, if you have one) more vulnerable to unauthorized access.</span></span> <span data-ttu-id="350aa-126">Pour obtenir des instructions, voir [activer ou désactiver le pare-feu Windows](https://support.microsoft.com/help/4028544/windows-10-turn-windows-defender-firewall-on-or-off) .</span><span class="sxs-lookup"><span data-stu-id="350aa-126">See [Turn Windows Firewall on or off](https://support.microsoft.com/help/4028544/windows-10-turn-windows-defender-firewall-on-or-off) for instructions</span></span>

## <a name="mactabmac"></a>[<span data-ttu-id="350aa-127">Mac</span><span class="sxs-lookup"><span data-stu-id="350aa-127">Mac</span></span>](#tab/Mac)
<span data-ttu-id="350aa-128">**Utiliser FileVault pour chiffrer votre disque Mac**</span><span class="sxs-lookup"><span data-stu-id="350aa-128">**Use FileVault to encrypt your Mac disk**</span></span><p>
<span data-ttu-id="350aa-129">Le chiffrement de disque protège les données en cas de perte ou de vol des appareils.</span><span class="sxs-lookup"><span data-stu-id="350aa-129">Disk encryption protects data when devices are lost or stolen.</span></span> <span data-ttu-id="350aa-130">FileVault le chiffrement de disque complet empêche l’accès non autorisé aux informations de votre disquette de démarrage.</span><span class="sxs-lookup"><span data-stu-id="350aa-130">FileVault full-disk encryption helps prevent unauthorized access to the information on your startup disk.</span></span> <span data-ttu-id="350aa-131">Pour obtenir des instructions, voir [utiliser FileVault pour chiffrer la disquette de démarrage sur votre Mac](https://support.apple.com/HT204837) .</span><span class="sxs-lookup"><span data-stu-id="350aa-131">See [use FileVault to encrypt the startup disk on your Mac](https://support.apple.com/HT204837) for instructions.</span></span>

<span data-ttu-id="350aa-132">**Protéger votre Mac contre les programmes malveillants**</span><span class="sxs-lookup"><span data-stu-id="350aa-132">**Protect your mac from malware**</span></span><p>
<span data-ttu-id="350aa-133">Microsoft vous recommande d’installer et d’utiliser un logiciel antivirus fiable sur votre Mac.</span><span class="sxs-lookup"><span data-stu-id="350aa-133">Microsoft recommends that you install and use reliable antivirus software on your Mac.</span></span> <span data-ttu-id="350aa-134">Consultez l’article suivant pour obtenir une liste de choix : [Best Mac antivirus 2019 ](https://www.macworld.co.uk/feature/mac-software/mac-antivirus-3672182/).</span><span class="sxs-lookup"><span data-stu-id="350aa-134">See the following article for a list of choices: [Best Mac antivirus 2019 ](https://www.macworld.co.uk/feature/mac-software/mac-antivirus-3672182/).</span></span>

<span data-ttu-id="350aa-135">Vous pouvez également réduire le risque de programmes malveillants à l’aide de logiciels uniquement à partir de sources fiables.</span><span class="sxs-lookup"><span data-stu-id="350aa-135">You can also reduce the risk of malware by using software only from reliable sources.</span></span> <span data-ttu-id="350aa-136">Les paramètres de sécurité & préférences de confidentialité vous permettent de spécifier les sources des logiciels installés sur votre Mac.</span><span class="sxs-lookup"><span data-stu-id="350aa-136">The settings in Security & Privacy preferences allow you to specify the sources of software installed on your Mac.</span></span> <span data-ttu-id="350aa-137">Pour plus d’informations, consultez [la rubrique Protégez votre Mac contre les programmes malveillants](https://support.apple.com/kb/PH25087) .</span><span class="sxs-lookup"><span data-stu-id="350aa-137">See [protect your Mac from malware](https://support.apple.com/kb/PH25087) for more information.</span></span>

<span data-ttu-id="350aa-138">**Activer la protection de pare-feu**</span><span class="sxs-lookup"><span data-stu-id="350aa-138">**Turn on firewall protection**</span></span><p>
<span data-ttu-id="350aa-139">Utilisez les paramètres de pare-feu pour protéger votre Mac contre les contacts indésirables initiés par d’autres ordinateurs lorsque vous êtes connecté à Internet ou à un réseau.</span><span class="sxs-lookup"><span data-stu-id="350aa-139">Use firewall settings to protect your Mac from unwanted contact initiated by other computers when you’re connected to the Internet or a network.</span></span> <span data-ttu-id="350aa-140">Sans cette protection, votre Mac peut être plus vulnérable aux accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="350aa-140">Without this protection, your Mac might be more vulnerable to unauthorized access.</span></span> <span data-ttu-id="350aa-141">Consultez [la rubrique à propos du pare-feu d’application](https://support.apple.com/HT201642) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="350aa-141">See [about the application firewall](https://support.apple.com/HT201642) for instructions.</span></span>
