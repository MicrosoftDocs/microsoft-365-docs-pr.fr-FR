---
title: Dépréciation TLS 1.0 et 1.1 pour Office 365
description: Décrit l’annulation de TLS 1.0 et 1.1 pour Office 365.
author: workshay
manager: laurawi
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.service: O365-seccomp
ms.topic: article
ms.author: shmehta
ms.reviewer: krowley
appliesto:
- Microsoft 365 Apps for enterprise
- Office 365 Business
- Office 365 Personal
- Office Online Server
- Office Web Apps
ms.openlocfilehash: 622d783011defcf9c84061087b7d05f2a117172e
ms.sourcegitcommit: 3bf4f1c0d3a8515cca651b2a520217195f89457f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "49777055"
---
# <a name="tls-10-and-11-deprecation-for-office-365"></a><span data-ttu-id="51565-103">Dépréciation TLS 1.0 et 1.1 pour Office 365</span><span class="sxs-lookup"><span data-stu-id="51565-103">TLS 1.0 and 1.1 deprecation for Office 365</span></span>
> [!IMPORTANT]
> <span data-ttu-id="51565-104">Nous avons temporairement interrompu l’application de TLS 1.0 et 1.1 pour les clients commerciaux en raison du COVID-19, mais à mesure que les chaînes d’approvisionnement se sont ajustées et que certains pays s’ouvrent, nous réinitialiserons l’application du TLS pour commencer le 15 octobre 2020 et le déploiement se poursuit au cours des semaines et des mois suivants.</span><span class="sxs-lookup"><span data-stu-id="51565-104">We temporarily halted deprecation enforcement of TLS 1.0 and 1.1 for commercial customers due to COVID-19, but as supply chains have adjusted and certain countries open back up, we are resetting the TLS enforcement to begin October 15, 2020, and rollout will continue over the following weeks and months.</span></span> 

<span data-ttu-id="51565-105">Depuis le 31 octobre 2018, les protocoles TLS 1.0 et 1.1 sont supprimés pour le service Office 365.</span><span class="sxs-lookup"><span data-stu-id="51565-105">As of October 31, 2018, the Transport Layer Security (TLS) 1.0 and 1.1 protocols are deprecated for the Office 365 service.</span></span> <span data-ttu-id="51565-106">L’effet pour les utilisateurs finaux est censé être minime.</span><span class="sxs-lookup"><span data-stu-id="51565-106">The effect for end-users is expected to be minimal.</span></span> <span data-ttu-id="51565-107">Cette modification a été annoncée pendant plus de deux ans, avec la première annonce publique en décembre 2017.</span><span class="sxs-lookup"><span data-stu-id="51565-107">This change has been publicized for over two years, with the first public announcement made in December 2017.</span></span> <span data-ttu-id="51565-108">Cet article est destiné uniquement à couvrir le client local Office 365 par rapport au service Office 365, mais peut également s’appliquer aux problèmes TLS locaux avec Office et Office Online Server/Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="51565-108">This article is only intended to cover the Office 365 local client in relation to the Office 365 service but can also apply to on-premises TLS issues with Office and Office Online Server/Office Web Apps.</span></span>

## <a name="office-and-tls-overview"></a><span data-ttu-id="51565-109">Vue d’ensemble d’Office et de TLS</span><span class="sxs-lookup"><span data-stu-id="51565-109">Office and TLS overview</span></span>

<span data-ttu-id="51565-110">Le client Office s’appuie sur le service web Windows (WINHTTP) pour envoyer et recevoir du trafic sur les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="51565-110">The Office client relies on the Windows web service (WINHTTP) to send and receive traffic over TLS protocols.</span></span> <span data-ttu-id="51565-111">Le client Office peut utiliser TLS 1.2 si le service web de l’ordinateur local peut utiliser TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="51565-111">The Office client can use TLS 1.2 if the web service of the local computer can use TLS 1.2.</span></span> <span data-ttu-id="51565-112">Tous les clients Office peuvent utiliser des protocoles TLS, car les protocoles TLS et SSL font partie du système d’exploitation et ne sont pas spécifiques au client Office.</span><span class="sxs-lookup"><span data-stu-id="51565-112">All Office clients can use TLS protocols, as TLS and SSL protocols are part of the operating system and not specific to the Office client.</span></span>

### <a name="on-windows-8-and-later-versions"></a><span data-ttu-id="51565-113">Sur Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="51565-113">On Windows 8 and later versions</span></span>

<span data-ttu-id="51565-114">Par défaut, les protocoles TLS 1.2 et 1.1 sont disponibles si aucun périphérique réseau n’est configuré pour rejeter le trafic TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="51565-114">By default, the TLS 1.2 and 1.1 protocols are available if no network devices are configured to reject TLS 1.2 traffic.</span></span>

### <a name="on-windows-7"></a><span data-ttu-id="51565-115">Sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="51565-115">On Windows 7</span></span>

<span data-ttu-id="51565-116">Les protocoles TLS 1.1 et 1.2 ne sont pas disponibles sans la mise à jour [KB 3140245.](https://support.microsoft.com/help/3140245)</span><span class="sxs-lookup"><span data-stu-id="51565-116">TLS 1.1 and 1.2 protocols are not available without the [KB 3140245](https://support.microsoft.com/help/3140245) update.</span></span> <span data-ttu-id="51565-117">La mise à jour résout ce problème et ajoute la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="51565-117">The update addresses this issue and adds the following registry sub key:</span></span>

```console
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp
```

> [!NOTE]
> <span data-ttu-id="51565-118">Les utilisateurs de Windows 7 qui n’ont pas cette mise à jour sont affectés depuis le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="51565-118">Windows 7 users who do not have this update are affected as of October 31, 2018.</span></span> <span data-ttu-id="51565-119">[La KB 3140245](https://support.microsoft.com/help/3140245) présente des détails sur la modification des paramètres WINHTTP pour activer les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="51565-119">[KB 3140245](https://support.microsoft.com/help/3140245) has details about how to change WINHTTP settings to enable TLS protocols.</span></span>

#### <a name="more-information"></a><span data-ttu-id="51565-120">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="51565-120">More information</span></span>

<span data-ttu-id="51565-121">La valeur de la clé de Registre **DefaultSecureProtocols** que l’article de la base de données décrit détermine les protocoles réseau qui peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="51565-121">The value of the **DefaultSecureProtocols** registry key that the KB article describes determines which network protocols can be used:</span></span>

|<span data-ttu-id="51565-122">Valeur DefaultSecureProtocols</span><span class="sxs-lookup"><span data-stu-id="51565-122">DefaultSecureProtocols Value</span></span>|<span data-ttu-id="51565-123">Protocole activé</span><span class="sxs-lookup"><span data-stu-id="51565-123">Protocol enabled</span></span>|
|-|-|
|<span data-ttu-id="51565-124">0x00000008</span><span class="sxs-lookup"><span data-stu-id="51565-124">0x00000008</span></span>|<span data-ttu-id="51565-125">Activer SSL 2.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="51565-125">Enable SSL 2.0 by default</span></span>|
|<span data-ttu-id="51565-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="51565-126">0x00000020</span></span>|<span data-ttu-id="51565-127">Activer SSL 3.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="51565-127">Enable SSL 3.0 by default</span></span>|
|<span data-ttu-id="51565-128">0x00000080</span><span class="sxs-lookup"><span data-stu-id="51565-128">0x00000080</span></span>|<span data-ttu-id="51565-129">Activer TLS 1.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="51565-129">Enable TLS 1.0 by default</span></span>|
|<span data-ttu-id="51565-130">0x00000200</span><span class="sxs-lookup"><span data-stu-id="51565-130">0x00000200</span></span>|<span data-ttu-id="51565-131">Activer TLS 1.1 par défaut</span><span class="sxs-lookup"><span data-stu-id="51565-131">Enable TLS 1.1 by default</span></span>|
|<span data-ttu-id="51565-132">0x00000800</span><span class="sxs-lookup"><span data-stu-id="51565-132">0x00000800</span></span>|<span data-ttu-id="51565-133">Activer TLS 1.2 par défaut</span><span class="sxs-lookup"><span data-stu-id="51565-133">Enable TLS 1.2 by default</span></span>|

## <a name="office-clients-and-tls-registry-keys"></a><span data-ttu-id="51565-134">Clients Office et clés de Registre TLS</span><span class="sxs-lookup"><span data-stu-id="51565-134">Office clients and TLS registry keys</span></span>

<span data-ttu-id="51565-135">Vous pouvez consulter la KB 4057306 Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365](https://support.microsoft.com/help/4057306).</span><span class="sxs-lookup"><span data-stu-id="51565-135">You can refer to [KB 4057306 Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306).</span></span> <span data-ttu-id="51565-136">Il s’agit d’un article général pour les administrateurs informatiques et d’une documentation officielle sur la modification de TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="51565-136">This is a general article for IT administrators, and it's official documentation about the TLS 1.2 change.</span></span>

<span data-ttu-id="51565-137">Le tableau suivant indique les valeurs de clé de Registre appropriées dans les clients Office 365 après le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="51565-137">The following table shows the appropriate registry key values in Office 365 clients after October 31, 2018.</span></span>

|<span data-ttu-id="51565-138">Protocoles activés pour le service Office 365 après le 31 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="51565-138">Enabled protocols for Office 365 service after October 31, 2018</span></span>|<span data-ttu-id="51565-139">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="51565-139">Hexadecimal value</span></span>|
|-|-|
|<span data-ttu-id="51565-140">TLS 1.0 + 1.1 + 1.2</span><span class="sxs-lookup"><span data-stu-id="51565-140">TLS 1.0 + 1.1 + 1.2</span></span>|<span data-ttu-id="51565-141">0x00000A80</span><span class="sxs-lookup"><span data-stu-id="51565-141">0x00000A80</span></span>|
|<span data-ttu-id="51565-142">TLS 1.1 + 1.2</span><span class="sxs-lookup"><span data-stu-id="51565-142">TLS 1.1 + 1.2</span></span>|<span data-ttu-id="51565-143">0x00000A00</span><span class="sxs-lookup"><span data-stu-id="51565-143">0x00000A00</span></span>|
|<span data-ttu-id="51565-144">TLS 1.0 + 1.2</span><span class="sxs-lookup"><span data-stu-id="51565-144">TLS 1.0 + 1.2</span></span>|<span data-ttu-id="51565-145">0x00000880</span><span class="sxs-lookup"><span data-stu-id="51565-145">0x00000880</span></span>|
|<span data-ttu-id="51565-146">TLS 1.2</span><span class="sxs-lookup"><span data-stu-id="51565-146">TLS 1.2</span></span>|<span data-ttu-id="51565-147">0x00000800</span><span class="sxs-lookup"><span data-stu-id="51565-147">0x00000800</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="51565-148">Nous vous déconseillons d’utiliser les protocoles SSL 2.0 et 3.0, qui peuvent également être définies à l’aide de la clé **DefaultSecureProtocols.**</span><span class="sxs-lookup"><span data-stu-id="51565-148">We don't recommend that you use the SSL 2.0 and 3.0 protocols, which can also be set by using the **DefaultSecureProtocols** key.</span></span> <span data-ttu-id="51565-149">SSL 2.0 et 3.0 sont considérés comme des protocoles dépréciés.</span><span class="sxs-lookup"><span data-stu-id="51565-149">SSL 2.0 and 3.0 are considered deprecated protocols.</span></span> <span data-ttu-id="51565-150">La meilleure pratique consiste à mettre fin à l’utilisation de SSL 2.0 et SSL 3.0, bien que la décision finale dépende de ce qui répond le mieux aux besoins de votre produit.</span><span class="sxs-lookup"><span data-stu-id="51565-150">The best practice is to end the use of SSL 2.0 and SSL 3.0, although the decision to do this ultimately depends on what best meets your product needs.</span></span> <span data-ttu-id="51565-151">Pour plus d’informations sur les vulnérabilités SSL 3.0, reportez-vous à la [KB 3009008](https://support.microsoft.com/help/3009008).</span><span class="sxs-lookup"><span data-stu-id="51565-151">For more information about SSL 3.0 vulnerabilities, refer to [KB 3009008](https://support.microsoft.com/help/3009008).</span></span>

<span data-ttu-id="51565-152">Vous pouvez utiliser la calculatrice Windows par défaut en mode programmeur pour configurer les mêmes valeurs de clé de Registre de référence.</span><span class="sxs-lookup"><span data-stu-id="51565-152">You can use the default Windows Calculator in Programmer mode to set up the same reference registry key values.</span></span> <span data-ttu-id="51565-153">Pour plus d’informations, voir la mise à jour de la [KB 3140245 pour activer TLS 1.1 et TLS 1.2](https://support.microsoft.com/help/3140245)en tant que protocoles sécurisés par défaut dans WinHTTP dans Windows.</span><span class="sxs-lookup"><span data-stu-id="51565-153">For more information, see [KB 3140245 Update to enable TLS 1.1 and TLS 1.2 as a default secure protocols in WinHTTP in Windows](https://support.microsoft.com/help/3140245).</span></span>

<span data-ttu-id="51565-154">Que la mise à jour Windows 7 ([KB 3140245](https://support.microsoft.com/help/3140245)) soit installée ou non, la sous-clé de Registre DefaultSecureProtocols n’est pas présente et doit être ajoutée manuellement ou via un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="51565-154">Regardless if the Windows 7 update ([KB 3140245](https://support.microsoft.com/help/3140245)) is installed or not, the DefaultSecureProtocols registry sub key isn't present and must be added manually or through a group policy object (GPO).</span></span> <span data-ttu-id="51565-155">Autrement dit, sauf si vous devez personnaliser les protocoles sécurisés activés ou restreints, cette clé n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="51565-155">That is, unless you have to customize what secure protocols are enabled or restricted, this key is not required.</span></span> <span data-ttu-id="51565-156">Vous avez uniquement besoin de la mise à jour de Windows 7 SP1 ([KB 3140245).](https://support.microsoft.com/help/3140245)</span><span class="sxs-lookup"><span data-stu-id="51565-156">You only need the Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)) update.</span></span>
