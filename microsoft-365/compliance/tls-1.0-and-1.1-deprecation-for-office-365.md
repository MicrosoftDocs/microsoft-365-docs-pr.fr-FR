---
title: Désactivation de TLS 1.0 et 1.1 pour Microsoft 365
description: Décrit l’annulation et la désactivation de TLS 1.0 et 1.1 pour Microsoft 365.
author: workshay
manager: laurawi
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.service: O365-seccomp
ms.topic: article
ms.author: fasqiu
ms.reviewer: krowley
appliesto:
- Microsoft 365 Apps for enterprise
- Office 365 Business
- Office 365 Personal
- Office Online Server
- Office Web Apps
ms.openlocfilehash: 3d44e178d351942b4a178ddc1954ddd839665639
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919300"
---
# <a name="disabling-tls-10-and-11-for-microsoft-365"></a><span data-ttu-id="0f29e-103">Désactivation de TLS 1.0 et 1.1 pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="0f29e-103">Disabling TLS 1.0 and 1.1 for Microsoft 365</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f29e-104">Nous avons temporairement interrompu la désactivation de TLS 1.0 et 1.1 pour les clients commerciaux en raison du COVID-19.</span><span class="sxs-lookup"><span data-stu-id="0f29e-104">We temporarily halted disablement of TLS 1.0 and 1.1 for commercial customers due to COVID-19.</span></span> <span data-ttu-id="0f29e-105">À mesure que les chaînes d’approvisionnement ont été ajustées et que certains pays s’ouvrent à nouveau, nous avons redémarré le déploiement de l’application de TLS 1.2 le 15 octobre 2020.</span><span class="sxs-lookup"><span data-stu-id="0f29e-105">As supply chains have adjusted and certain countries open back up, we restarted the TLS 1.2 enforcement rollout on October 15, 2020.</span></span> <span data-ttu-id="0f29e-106">Le déploiement se poursuit au cours des semaines et des mois suivants.</span><span class="sxs-lookup"><span data-stu-id="0f29e-106">Rollout will continue over the following weeks and months.</span></span>

<span data-ttu-id="0f29e-107">Depuis le 31 octobre 2018, les protocoles TLS 1.0 et 1.1 sont supprimés pour le service Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f29e-107">As of October 31, 2018, the Transport Layer Security (TLS) 1.0 and 1.1 protocols are deprecated for the Microsoft 365 service.</span></span> <span data-ttu-id="0f29e-108">L’effet est minime pour les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="0f29e-108">The effect for end-users is minimal.</span></span> <span data-ttu-id="0f29e-109">Cette modification a été rendue publique pendant plus de deux ans, avec la première annonce publique en décembre 2017.</span><span class="sxs-lookup"><span data-stu-id="0f29e-109">This change has been publicized for over two years, with the first public announcement made in December 2017.</span></span> <span data-ttu-id="0f29e-110">Cet article est destiné uniquement à couvrir le client local Office 365 par rapport au service Office 365, mais peut également s’appliquer aux problèmes TLS locaux avec Office et Office Online Server/Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="0f29e-110">This article is only intended to cover the Office 365 local client in relation to the Office 365 service but can also apply to on-premises TLS issues with Office and Office Online Server/Office Web Apps.</span></span>

<span data-ttu-id="0f29e-111">Pour SharePoint et OneDrive, vous devez mettre à jour et configurer .NET pour prendre en charge TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-111">For SharePoint and OneDrive, you'll need to update and configure .NET to support TLS 1.2.</span></span> <span data-ttu-id="0f29e-112">Pour plus d’informations, [voir Comment activer TLS 1.2 sur les clients](/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span><span class="sxs-lookup"><span data-stu-id="0f29e-112">For information, see [How to enable TLS 1.2 on clients](/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span></span>

## <a name="office-365-and-tls-overview"></a><span data-ttu-id="0f29e-113">Vue d’ensemble d’Office 365 et de TLS</span><span class="sxs-lookup"><span data-stu-id="0f29e-113">Office 365 and TLS overview</span></span>

<span data-ttu-id="0f29e-114">Le client Office s’appuie sur le service web Windows (WINHTTP) pour envoyer et recevoir du trafic sur les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="0f29e-114">The Office client relies on the Windows web service (WINHTTP) to send and receive traffic over TLS protocols.</span></span> <span data-ttu-id="0f29e-115">Le client Office peut utiliser TLS 1.2 si le service web de l’ordinateur local peut utiliser TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-115">The Office client can use TLS 1.2 if the web service of the local computer can use TLS 1.2.</span></span> <span data-ttu-id="0f29e-116">Tous les clients Office peuvent utiliser des protocoles TLS, car les protocoles TLS et SSL font partie du système d’exploitation et ne sont pas spécifiques au client Office.</span><span class="sxs-lookup"><span data-stu-id="0f29e-116">All Office clients can use TLS protocols, as TLS and SSL protocols are part of the operating system and not specific to the Office client.</span></span>

### <a name="on-windows-8-and-later-versions"></a><span data-ttu-id="0f29e-117">Sur Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="0f29e-117">On Windows 8 and later versions</span></span>

<span data-ttu-id="0f29e-118">Par défaut, les protocoles TLS 1.2 et 1.1 sont disponibles si aucun périphérique réseau n’est configuré pour rejeter le trafic TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-118">By default, the TLS 1.2 and 1.1 protocols are available if no network devices are configured to reject TLS 1.2 traffic.</span></span>

### <a name="on-windows-7"></a><span data-ttu-id="0f29e-119">Sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f29e-119">On Windows 7</span></span>

<span data-ttu-id="0f29e-120">Les protocoles TLS 1.1 et 1.2 ne sont pas disponibles sans la mise à jour de la [KB 3140245.](https://support.microsoft.com/help/3140245)</span><span class="sxs-lookup"><span data-stu-id="0f29e-120">TLS 1.1 and 1.2 protocols are not available without the [KB 3140245](https://support.microsoft.com/help/3140245) update.</span></span> <span data-ttu-id="0f29e-121">La mise à jour résout ce problème et ajoute la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="0f29e-121">The update addresses this issue and adds the following registry sub key:</span></span>

```console
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp
```

> [!NOTE]
> <span data-ttu-id="0f29e-122">Les utilisateurs de Windows 7 qui n’ont pas cette mise à jour sont affectés depuis le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="0f29e-122">Windows 7 users who do not have this update are affected as of October 31, 2018.</span></span> <span data-ttu-id="0f29e-123">[La KB 3140245](https://support.microsoft.com/help/3140245) présente des détails sur la modification des paramètres WINHTTP pour activer les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="0f29e-123">[KB 3140245](https://support.microsoft.com/help/3140245) has details about how to change WINHTTP settings to enable TLS protocols.</span></span>

#### <a name="more-information"></a><span data-ttu-id="0f29e-124">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0f29e-124">More information</span></span>

<span data-ttu-id="0f29e-125">La valeur de la clé de Registre **DefaultSecureProtocols** que l’article de la base de données décrit détermine les protocoles réseau qui peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="0f29e-125">The value of the **DefaultSecureProtocols** registry key that the KB article describes determines which network protocols can be used:</span></span>

|<span data-ttu-id="0f29e-126">Valeur DefaultSecureProtocols</span><span class="sxs-lookup"><span data-stu-id="0f29e-126">DefaultSecureProtocols Value</span></span>|<span data-ttu-id="0f29e-127">Protocole activé</span><span class="sxs-lookup"><span data-stu-id="0f29e-127">Protocol enabled</span></span>|
|-|-|
|<span data-ttu-id="0f29e-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="0f29e-128">0x00000008</span></span>|<span data-ttu-id="0f29e-129">Activer SSL 2.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="0f29e-129">Enable SSL 2.0 by default</span></span>|
|<span data-ttu-id="0f29e-130">0x00000020</span><span class="sxs-lookup"><span data-stu-id="0f29e-130">0x00000020</span></span>|<span data-ttu-id="0f29e-131">Activer SSL 3.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="0f29e-131">Enable SSL 3.0 by default</span></span>|
|<span data-ttu-id="0f29e-132">0x00000080</span><span class="sxs-lookup"><span data-stu-id="0f29e-132">0x00000080</span></span>|<span data-ttu-id="0f29e-133">Activer TLS 1.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="0f29e-133">Enable TLS 1.0 by default</span></span>|
|<span data-ttu-id="0f29e-134">0x00000200</span><span class="sxs-lookup"><span data-stu-id="0f29e-134">0x00000200</span></span>|<span data-ttu-id="0f29e-135">Activer TLS 1.1 par défaut</span><span class="sxs-lookup"><span data-stu-id="0f29e-135">Enable TLS 1.1 by default</span></span>|
|<span data-ttu-id="0f29e-136">0x00000800</span><span class="sxs-lookup"><span data-stu-id="0f29e-136">0x00000800</span></span>|<span data-ttu-id="0f29e-137">Activer TLS 1.2 par défaut</span><span class="sxs-lookup"><span data-stu-id="0f29e-137">Enable TLS 1.2 by default</span></span>|

## <a name="office-clients-and-tls-registry-keys"></a><span data-ttu-id="0f29e-138">Clients Office et clés de Registre TLS</span><span class="sxs-lookup"><span data-stu-id="0f29e-138">Office clients and TLS registry keys</span></span>

<span data-ttu-id="0f29e-139">Vous pouvez consulter la KB 4057306 Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306)</span><span class="sxs-lookup"><span data-stu-id="0f29e-139">You can refer to [KB 4057306 Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306).</span></span> <span data-ttu-id="0f29e-140">Il s’agit d’un article général pour les administrateurs informatiques et d’une documentation officielle sur la modification de TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-140">This is a general article for IT administrators, and it's official documentation about the TLS 1.2 change.</span></span>

<span data-ttu-id="0f29e-141">Le tableau suivant indique les valeurs de clé de Registre appropriées dans les clients Office 365 après le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="0f29e-141">The following table shows the appropriate registry key values in Office 365 clients after October 31, 2018.</span></span>

|<span data-ttu-id="0f29e-142">Protocoles activés pour le service Office 365 après le 31 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="0f29e-142">Enabled protocols for Office 365 service after October 31, 2018</span></span>|<span data-ttu-id="0f29e-143">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="0f29e-143">Hexadecimal value</span></span>|
|-|-|
|<span data-ttu-id="0f29e-144">TLS 1.0 + 1.1 + 1.2</span><span class="sxs-lookup"><span data-stu-id="0f29e-144">TLS 1.0 + 1.1 + 1.2</span></span>|<span data-ttu-id="0f29e-145">0x00000A80</span><span class="sxs-lookup"><span data-stu-id="0f29e-145">0x00000A80</span></span>|
|<span data-ttu-id="0f29e-146">TLS 1.1 + 1.2</span><span class="sxs-lookup"><span data-stu-id="0f29e-146">TLS 1.1 + 1.2</span></span>|<span data-ttu-id="0f29e-147">0x00000A00</span><span class="sxs-lookup"><span data-stu-id="0f29e-147">0x00000A00</span></span>|
|<span data-ttu-id="0f29e-148">TLS 1.0 + 1.2</span><span class="sxs-lookup"><span data-stu-id="0f29e-148">TLS 1.0 + 1.2</span></span>|<span data-ttu-id="0f29e-149">0x00000880</span><span class="sxs-lookup"><span data-stu-id="0f29e-149">0x00000880</span></span>|
|<span data-ttu-id="0f29e-150">TLS 1.2</span><span class="sxs-lookup"><span data-stu-id="0f29e-150">TLS 1.2</span></span>|<span data-ttu-id="0f29e-151">0x00000800</span><span class="sxs-lookup"><span data-stu-id="0f29e-151">0x00000800</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="0f29e-152">N’utilisez pas les protocoles SSL 2.0 et 3.0, qui peuvent également être définies à l’aide de la clé **DefaultSecureProtocols.**</span><span class="sxs-lookup"><span data-stu-id="0f29e-152">Don't use the SSL 2.0 and 3.0 protocols, which can also be set by using the **DefaultSecureProtocols** key.</span></span> <span data-ttu-id="0f29e-153">SSL 2.0 et 3.0 sont considérés comme des protocoles obsolètes et non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="0f29e-153">SSL 2.0 and 3.0 are considered outdated and insecure protocols.</span></span> <span data-ttu-id="0f29e-154">La meilleure pratique consiste à mettre fin à l’utilisation de SSL 2.0 et SSL 3.0, bien que la décision finale dépende de ce qui répond le mieux aux besoins de votre produit.</span><span class="sxs-lookup"><span data-stu-id="0f29e-154">The best practice is to end the use of SSL 2.0 and SSL 3.0, although the decision to do this ultimately depends on what best meets your product needs.</span></span> <span data-ttu-id="0f29e-155">Pour plus d’informations sur les vulnérabilités SSL 3.0, reportez-vous à la [KB 3009008](https://support.microsoft.com/help/3009008).</span><span class="sxs-lookup"><span data-stu-id="0f29e-155">For more information about SSL 3.0 vulnerabilities, refer to [KB 3009008](https://support.microsoft.com/help/3009008).</span></span>

<span data-ttu-id="0f29e-156">Vous pouvez utiliser la calculatrice Windows par défaut en mode programmeur pour configurer les mêmes valeurs de clé de Registre de référence.</span><span class="sxs-lookup"><span data-stu-id="0f29e-156">You can use the default Windows Calculator in Programmer mode to set up the same reference registry key values.</span></span> <span data-ttu-id="0f29e-157">Pour plus d’informations, voir la mise à jour de la [KB 3140245 pour activer TLS 1.1 et TLS 1.2](https://support.microsoft.com/help/3140245)en tant que protocoles sécurisés par défaut dans WinHTTP dans Windows.</span><span class="sxs-lookup"><span data-stu-id="0f29e-157">For more information, see [KB 3140245 Update to enable TLS 1.1 and TLS 1.2 as a default secure protocols in WinHTTP in Windows](https://support.microsoft.com/help/3140245).</span></span>

<span data-ttu-id="0f29e-158">Que la mise à jour Windows 7 ([KB 3140245](https://support.microsoft.com/help/3140245)) soit installée ou non, la sous-clé de Registre DefaultSecureProtocols n’est pas présente et doit être ajoutée manuellement ou via un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="0f29e-158">Regardless if the Windows 7 update ([KB 3140245](https://support.microsoft.com/help/3140245)) is installed or not, the DefaultSecureProtocols registry sub key isn't present and must be added manually or through a group policy object (GPO).</span></span> <span data-ttu-id="0f29e-159">Autrement dit, sauf si vous devez personnaliser les protocoles sécurisés activés ou restreints, cette clé n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="0f29e-159">That is, unless you have to customize what secure protocols are enabled or restricted, this key is not required.</span></span> <span data-ttu-id="0f29e-160">Vous avez uniquement besoin de la mise à jour de Windows 7 SP1 ([KB 3140245).](https://support.microsoft.com/help/3140245)</span><span class="sxs-lookup"><span data-stu-id="0f29e-160">You only need the Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)) update.</span></span>

## <a name="update-and-configure-the-net-framework-to-support-tls-12"></a><span data-ttu-id="0f29e-161">Mettre à jour et configurer le .NET Framework pour prendre en charge TLS 1.2</span><span class="sxs-lookup"><span data-stu-id="0f29e-161">Update and configure the .NET Framework to support TLS 1.2</span></span>

<span data-ttu-id="0f29e-162">Vous devez mettre à jour les applications qui appellent les API Microsoft 365 sur TLS 1.0 ou TLS 1.1 pour utiliser TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="0f29e-162">You'll need to update applications that call Microsoft 365 APIs over TLS 1.0 or TLS 1.1 to use TLS 1.2.</span></span> <span data-ttu-id="0f29e-163">Par défaut, .NET 4.5 est TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="0f29e-163">.NET 4.5 defaults to TLS 1.1.</span></span> <span data-ttu-id="0f29e-164">Pour mettre à jour votre configuration .NET, voir [Comment activer TLS (Transport Layer Security) 1.2 sur les clients.](/mem/configmgr/core/plan-design/security/enable-tls-1-2-client)</span><span class="sxs-lookup"><span data-stu-id="0f29e-164">To update your .NET configuration, see [How to enable Transport Layer Security (TLS) 1.2 on clients](/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span></span>

## <a name="more-information"></a><span data-ttu-id="0f29e-165">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0f29e-165">More information</span></span>

<span data-ttu-id="0f29e-166">Pour plus d’informations, voir Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="0f29e-166">For more information, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>