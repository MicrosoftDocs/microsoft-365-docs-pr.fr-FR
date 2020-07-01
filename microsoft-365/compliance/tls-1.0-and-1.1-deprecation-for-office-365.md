---
title: TLS 1,0 et 1,1 désapprobation pour Office 365
description: Décrit les protocoles TLS 1,0 et 1,1 obsolètes pour Office 365.
author: simonxjx
manager: dcscontentpm
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.service: O365-seccomp
ms.topic: article
ms.author: v-six
appliesto:
- Microsoft 365 Apps for enterprise
- Office 365 Business
- Office 365 Personal
- Office Online Server
- Office Web Apps
ms.openlocfilehash: 611b6970c3ecb95f4cdf046b96a5e3aa9155391d
ms.sourcegitcommit: c43ebb915fa0eb7eb720b21b62c0d1e58e7cde3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2020
ms.locfileid: "44937329"
---
# <a name="tls-10-and-11-deprecation-for-office-365"></a><span data-ttu-id="6d6ff-103">TLS 1,0 et 1,1 désapprobation pour Office 365</span><span class="sxs-lookup"><span data-stu-id="6d6ff-103">TLS 1.0 and 1.1 deprecation for Office 365</span></span>

<span data-ttu-id="6d6ff-104">À partir du 31 octobre 2018, les protocoles TLS (Transport Layer Security) 1,0 et 1,1 sont déconseillés pour le service Office 365.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-104">As of October 31, 2018, the Transport Layer Security (TLS) 1.0 and 1.1 protocols are deprecated for the Office 365 service.</span></span> <span data-ttu-id="6d6ff-105">L’effet pour les utilisateurs finaux est supposé minimal.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-105">The effect for end-users is expected to be minimal.</span></span> <span data-ttu-id="6d6ff-106">Cette modification a été publique depuis près de deux ans, avec la première annonce publique effectuée en décembre 2017.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-106">This change was publicized for almost two years, with the first public announcement made in December 2017.</span></span> <span data-ttu-id="6d6ff-107">Cet article est destiné uniquement à traiter le client local Office 365 en relation avec le service Office 365, mais peut également s’appliquer aux problèmes TLS sur site avec Office et Office Online Server/Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-107">This article is only intended to cover the Office 365 local client in relation to the Office 365 service but can also apply to on-premises TLS issues with Office and Office Online Server/Office Web Apps.</span></span>

## <a name="office-and-tls-overview"></a><span data-ttu-id="6d6ff-108">Vue d’ensemble d’Office et de TLS</span><span class="sxs-lookup"><span data-stu-id="6d6ff-108">Office and TLS overview</span></span>

<span data-ttu-id="6d6ff-109">Le client Office s’appuie sur le service Web Windows (WINHTTP) pour envoyer et recevoir le trafic sur les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-109">The Office client relies on the Windows web service (WINHTTP) to send and receive traffic over TLS protocols.</span></span> <span data-ttu-id="6d6ff-110">Le client Office peut utiliser TLS 1,2 si le service Web de l’ordinateur local peut utiliser TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-110">The Office client can use TLS 1.2 if the web service of the local computer can use TLS 1.2.</span></span> <span data-ttu-id="6d6ff-111">Tous les clients Office peuvent utiliser les protocoles TLS, car les protocoles TLS et SSL font partie du système d’exploitation et ne sont pas spécifiques du client Office.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-111">All Office clients can use TLS protocols, as TLS and SSL protocols are part of the operating system and not specific to the Office client.</span></span>

### <a name="on-windows-8-and-later-versions"></a><span data-ttu-id="6d6ff-112">Sur Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="6d6ff-112">On Windows 8 and later versions</span></span>

<span data-ttu-id="6d6ff-113">Par défaut, les protocoles TLS 1,2 et 1,1 sont disponibles si aucun périphérique réseau n’est configuré pour rejeter le trafic TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-113">By default, the TLS 1.2 and 1.1 protocols are available if no network devices are configured to reject TLS 1.2 traffic.</span></span>

### <a name="on-windows-7"></a><span data-ttu-id="6d6ff-114">Sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d6ff-114">On Windows 7</span></span>

<span data-ttu-id="6d6ff-115">Les protocoles TLS 1,1 et 1,2 ne sont pas disponibles sans la mise à jour [KB 3140245](https://support.microsoft.com/help/3140245) .</span><span class="sxs-lookup"><span data-stu-id="6d6ff-115">TLS 1.1 and 1.2 protocols are not available without the [KB 3140245](https://support.microsoft.com/help/3140245) update.</span></span> <span data-ttu-id="6d6ff-116">La mise à jour corrige ce problème et ajoute la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="6d6ff-116">The update addresses this issue and adds the following registry sub key:</span></span>

```console
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp
```

> [!NOTE]
> <span data-ttu-id="6d6ff-117">Les utilisateurs de Windows 7 qui n’ont pas cette mise à jour sont affectés le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-117">Windows 7 users who do not have this update are affected as of October 31, 2018.</span></span> <span data-ttu-id="6d6ff-118">[KB 3140245](https://support.microsoft.com/help/3140245) explique comment modifier les paramètres WinHTTP pour activer les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-118">[KB 3140245](https://support.microsoft.com/help/3140245) has details about how to change WINHTTP settings to enable TLS protocols.</span></span>

#### <a name="more-information"></a><span data-ttu-id="6d6ff-119">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="6d6ff-119">More information</span></span>

<span data-ttu-id="6d6ff-120">La valeur de la clé de Registre **DefaultSecureProtocols** décrite dans l’article de la base de connaissances détermine les protocoles réseau qui peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="6d6ff-120">The value of the **DefaultSecureProtocols** registry key that the KB article describes determines which network protocols can be used:</span></span>

|<span data-ttu-id="6d6ff-121">Valeur DefaultSecureProtocols</span><span class="sxs-lookup"><span data-stu-id="6d6ff-121">DefaultSecureProtocols Value</span></span>|<span data-ttu-id="6d6ff-122">Protocole activé</span><span class="sxs-lookup"><span data-stu-id="6d6ff-122">Protocol enabled</span></span>|
|-|-|
|<span data-ttu-id="6d6ff-123">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6d6ff-123">0x00000008</span></span>|<span data-ttu-id="6d6ff-124">Activer SSL 2.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="6d6ff-124">Enable SSL 2.0 by default</span></span>|
|<span data-ttu-id="6d6ff-125">0x00000020</span><span class="sxs-lookup"><span data-stu-id="6d6ff-125">0x00000020</span></span>|<span data-ttu-id="6d6ff-126">Activer SSL 3.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="6d6ff-126">Enable SSL 3.0 by default</span></span>|
|<span data-ttu-id="6d6ff-127">0x00000080</span><span class="sxs-lookup"><span data-stu-id="6d6ff-127">0x00000080</span></span>|<span data-ttu-id="6d6ff-128">Activer TLS 1.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="6d6ff-128">Enable TLS 1.0 by default</span></span>|
|<span data-ttu-id="6d6ff-129">0x00000200</span><span class="sxs-lookup"><span data-stu-id="6d6ff-129">0x00000200</span></span>|<span data-ttu-id="6d6ff-130">Activer TLS 1.1 par défaut</span><span class="sxs-lookup"><span data-stu-id="6d6ff-130">Enable TLS 1.1 by default</span></span>|
|<span data-ttu-id="6d6ff-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="6d6ff-131">0x00000800</span></span>|<span data-ttu-id="6d6ff-132">Activer TLS 1.2 par défaut</span><span class="sxs-lookup"><span data-stu-id="6d6ff-132">Enable TLS 1.2 by default</span></span>|

## <a name="office-clients-and-tls-registry-keys"></a><span data-ttu-id="6d6ff-133">Clients Office et clés de Registre TLS</span><span class="sxs-lookup"><span data-stu-id="6d6ff-133">Office clients and TLS registry keys</span></span>

<span data-ttu-id="6d6ff-134">Vous pouvez vous reporter à [la 4057306 de la préparation à l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306).</span><span class="sxs-lookup"><span data-stu-id="6d6ff-134">You can refer to [KB 4057306 Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306).</span></span> <span data-ttu-id="6d6ff-135">Il s’agit d’un article général pour les administrateurs informatiques, et de la documentation officielle sur la modification TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-135">This is a general article for IT administrators, and it's official documentation about the TLS 1.2 change.</span></span>

<span data-ttu-id="6d6ff-136">Le tableau suivant indique les valeurs de clés de Registre appropriées dans les clients Office 365 après le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-136">The following table shows the appropriate registry key values in Office 365 clients after October 31, 2018.</span></span>

|<span data-ttu-id="6d6ff-137">Protocoles activés pour le service Office 365 après le 31 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="6d6ff-137">Enabled protocols for Office 365 service after October 31, 2018</span></span>|<span data-ttu-id="6d6ff-138">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="6d6ff-138">Hexadecimal value</span></span>|
|-|-|
|<span data-ttu-id="6d6ff-139">TLS 1,0 + 1,1 + 1,2</span><span class="sxs-lookup"><span data-stu-id="6d6ff-139">TLS 1.0 + 1.1 + 1.2</span></span>|<span data-ttu-id="6d6ff-140">0x00000A80</span><span class="sxs-lookup"><span data-stu-id="6d6ff-140">0x00000A80</span></span>|
|<span data-ttu-id="6d6ff-141">TLS 1,1 + 1,2</span><span class="sxs-lookup"><span data-stu-id="6d6ff-141">TLS 1.1 + 1.2</span></span>|<span data-ttu-id="6d6ff-142">0x00000A00</span><span class="sxs-lookup"><span data-stu-id="6d6ff-142">0x00000A00</span></span>|
|<span data-ttu-id="6d6ff-143">TLS 1,0 + 1,2</span><span class="sxs-lookup"><span data-stu-id="6d6ff-143">TLS 1.0 + 1.2</span></span>|<span data-ttu-id="6d6ff-144">0x00000880</span><span class="sxs-lookup"><span data-stu-id="6d6ff-144">0x00000880</span></span>|
|<span data-ttu-id="6d6ff-145">TLS 1.2</span><span class="sxs-lookup"><span data-stu-id="6d6ff-145">TLS 1.2</span></span>|<span data-ttu-id="6d6ff-146">0x00000800</span><span class="sxs-lookup"><span data-stu-id="6d6ff-146">0x00000800</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="6d6ff-147">Il n’est pas recommandé d’utiliser les protocoles SSL 2,0 et 3,0, qui peuvent également être définis à l’aide de la clé **DefaultSecureProtocols** .</span><span class="sxs-lookup"><span data-stu-id="6d6ff-147">We don't recommend that you use the SSL 2.0 and 3.0 protocols, which can also be set by using the **DefaultSecureProtocols** key.</span></span> <span data-ttu-id="6d6ff-148">Les protocoles SSL 2,0 et 3,0 sont considérés comme des protocoles déconseillés.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-148">SSL 2.0 and 3.0 are considered deprecated protocols.</span></span> <span data-ttu-id="6d6ff-149">La meilleure pratique consiste à mettre fin à l’utilisation des protocoles SSL 2,0 et SSL 3,0, bien que la décision de le faire dépende de ce qui est le mieux adapté à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-149">The best practice is to end the use of SSL 2.0 and SSL 3.0, although the decision to do this ultimately depends on what best meets your product needs.</span></span> <span data-ttu-id="6d6ff-150">Pour plus d’informations sur les vulnérabilités SSL 3,0, reportez-vous à [KB 3009008](https://support.microsoft.com/help/3009008).</span><span class="sxs-lookup"><span data-stu-id="6d6ff-150">For more information about SSL 3.0 vulnerabilities, refer to [KB 3009008](https://support.microsoft.com/help/3009008).</span></span>

<span data-ttu-id="6d6ff-151">Vous pouvez utiliser la calculatrice Windows par défaut en mode programmeur pour configurer les mêmes valeurs de clés de registre de référence.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-151">You can use the default Windows Calculator in Programmer mode to set up the same reference registry key values.</span></span> <span data-ttu-id="6d6ff-152">Pour plus d’informations, reportez-vous à [la mise à jour KB 3140245 pour activer tls 1,1 et tls 1,2 comme protocoles de sécurité par défaut dans WinHTTP dans Windows](https://support.microsoft.com/help/3140245).</span><span class="sxs-lookup"><span data-stu-id="6d6ff-152">For more information, see [KB 3140245 Update to enable TLS 1.1 and TLS 1.2 as a default secure protocols in WinHTTP in Windows](https://support.microsoft.com/help/3140245).</span></span>

<span data-ttu-id="6d6ff-153">Quelle que soit la mise à jour de Windows 7 ([KB 3140245](https://support.microsoft.com/help/3140245)) installée ou non, la sous-clé de Registre DefaultSecureProtocols n’est pas présente et doit être ajoutée manuellement ou par le biais d’un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="6d6ff-153">Regardless if the Windows 7 update ([KB 3140245](https://support.microsoft.com/help/3140245)) is installed or not, the DefaultSecureProtocols registry sub key isn't present and must be added manually or through a group policy object (GPO).</span></span> <span data-ttu-id="6d6ff-154">Autrement dit, sauf si vous devez personnaliser les protocoles sécurisés qui sont activés ou restreints, cette clé n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="6d6ff-154">That is, unless you have to customize what secure protocols are enabled or restricted, this key is not required.</span></span> <span data-ttu-id="6d6ff-155">Vous n’avez besoin que de la mise à jour de Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)).</span><span class="sxs-lookup"><span data-stu-id="6d6ff-155">You only need the Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)) update.</span></span>
