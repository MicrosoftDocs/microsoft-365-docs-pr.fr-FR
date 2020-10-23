---
title: Dépréciation TLS 1.0 et 1.1 pour Office 365
description: Décrit les protocoles TLS 1,0 et 1,1 obsolètes pour Office 365.
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
ms.openlocfilehash: ab3685883ac08522ab9ea1ee0cf194ba263d9166
ms.sourcegitcommit: 554755bc9ce40228ce6e34bde6fc6e226869b6a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48681688"
---
# <a name="tls-10-and-11-deprecation-for-office-365"></a><span data-ttu-id="2330e-103">Dépréciation TLS 1.0 et 1.1 pour Office 365</span><span class="sxs-lookup"><span data-stu-id="2330e-103">TLS 1.0 and 1.1 deprecation for Office 365</span></span>
> [!IMPORTANT]
> <span data-ttu-id="2330e-104">Nous avons interrompu temporairement l’application de la désapprobation de TLS 1,0 et 1,1 pour les clients commerciaux en raison du COVID-19, mais, étant donné que les chaînes d’approvisionnement ont été ajustées et que certains pays sont ouverts, nous redéfinissons la mise en œuvre TLS pour commencer le 15 octobre, 2020 et le lancement se poursuivra au cours des semaines et mois suivants.</span><span class="sxs-lookup"><span data-stu-id="2330e-104">We temporarily halted deprecation enforcement of TLS 1.0 and 1.1 for commercial customers due to covid-19, but as supply chains have adjusted and certain countries open back up, we are resetting the TLS enforcement to begin Oct 15, 2020 and rollout will continue over the following weeks and months.</span></span> 

<span data-ttu-id="2330e-105">À partir du 31 octobre 2018, les protocoles TLS (Transport Layer Security) 1,0 et 1,1 sont déconseillés pour le service Office 365.</span><span class="sxs-lookup"><span data-stu-id="2330e-105">As of October 31, 2018, the Transport Layer Security (TLS) 1.0 and 1.1 protocols are deprecated for the Office 365 service.</span></span> <span data-ttu-id="2330e-106">L’effet pour les utilisateurs finaux est supposé minimal.</span><span class="sxs-lookup"><span data-stu-id="2330e-106">The effect for end-users is expected to be minimal.</span></span> <span data-ttu-id="2330e-107">Cette modification a été publique depuis plus de deux ans, avec la première annonce publique effectuée en décembre 2017.</span><span class="sxs-lookup"><span data-stu-id="2330e-107">This change has been publicized for over two years, with the first public announcement made in December 2017.</span></span> <span data-ttu-id="2330e-108">Cet article est destiné uniquement à traiter le client local Office 365 en relation avec le service Office 365, mais peut également s’appliquer aux problèmes TLS sur site avec Office et Office Online Server/Office Web Apps.</span><span class="sxs-lookup"><span data-stu-id="2330e-108">This article is only intended to cover the Office 365 local client in relation to the Office 365 service but can also apply to on-premises TLS issues with Office and Office Online Server/Office Web Apps.</span></span>

## <a name="office-and-tls-overview"></a><span data-ttu-id="2330e-109">Vue d’ensemble d’Office et de TLS</span><span class="sxs-lookup"><span data-stu-id="2330e-109">Office and TLS overview</span></span>

<span data-ttu-id="2330e-110">Le client Office s’appuie sur le service Web Windows (WINHTTP) pour envoyer et recevoir le trafic sur les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="2330e-110">The Office client relies on the Windows web service (WINHTTP) to send and receive traffic over TLS protocols.</span></span> <span data-ttu-id="2330e-111">Le client Office peut utiliser TLS 1,2 si le service Web de l’ordinateur local peut utiliser TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="2330e-111">The Office client can use TLS 1.2 if the web service of the local computer can use TLS 1.2.</span></span> <span data-ttu-id="2330e-112">Tous les clients Office peuvent utiliser les protocoles TLS, car les protocoles TLS et SSL font partie du système d’exploitation et ne sont pas spécifiques du client Office.</span><span class="sxs-lookup"><span data-stu-id="2330e-112">All Office clients can use TLS protocols, as TLS and SSL protocols are part of the operating system and not specific to the Office client.</span></span>

### <a name="on-windows-8-and-later-versions"></a><span data-ttu-id="2330e-113">Sur Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="2330e-113">On Windows 8 and later versions</span></span>

<span data-ttu-id="2330e-114">Par défaut, les protocoles TLS 1,2 et 1,1 sont disponibles si aucun périphérique réseau n’est configuré pour rejeter le trafic TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="2330e-114">By default, the TLS 1.2 and 1.1 protocols are available if no network devices are configured to reject TLS 1.2 traffic.</span></span>

### <a name="on-windows-7"></a><span data-ttu-id="2330e-115">Sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="2330e-115">On Windows 7</span></span>

<span data-ttu-id="2330e-116">Les protocoles TLS 1,1 et 1,2 ne sont pas disponibles sans la mise à jour [KB 3140245](https://support.microsoft.com/help/3140245) .</span><span class="sxs-lookup"><span data-stu-id="2330e-116">TLS 1.1 and 1.2 protocols are not available without the [KB 3140245](https://support.microsoft.com/help/3140245) update.</span></span> <span data-ttu-id="2330e-117">La mise à jour corrige ce problème et ajoute la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="2330e-117">The update addresses this issue and adds the following registry sub key:</span></span>

```console
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Internet Settings\WinHttp
```

> [!NOTE]
> <span data-ttu-id="2330e-118">Les utilisateurs de Windows 7 qui n’ont pas cette mise à jour sont affectés le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="2330e-118">Windows 7 users who do not have this update are affected as of October 31, 2018.</span></span> <span data-ttu-id="2330e-119">[KB 3140245](https://support.microsoft.com/help/3140245) explique comment modifier les paramètres WinHTTP pour activer les protocoles TLS.</span><span class="sxs-lookup"><span data-stu-id="2330e-119">[KB 3140245](https://support.microsoft.com/help/3140245) has details about how to change WINHTTP settings to enable TLS protocols.</span></span>

#### <a name="more-information"></a><span data-ttu-id="2330e-120">Informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2330e-120">More information</span></span>

<span data-ttu-id="2330e-121">La valeur de la clé de Registre **DefaultSecureProtocols** décrite dans l’article de la base de connaissances détermine les protocoles réseau qui peuvent être utilisés :</span><span class="sxs-lookup"><span data-stu-id="2330e-121">The value of the **DefaultSecureProtocols** registry key that the KB article describes determines which network protocols can be used:</span></span>

|<span data-ttu-id="2330e-122">Valeur DefaultSecureProtocols</span><span class="sxs-lookup"><span data-stu-id="2330e-122">DefaultSecureProtocols Value</span></span>|<span data-ttu-id="2330e-123">Protocole activé</span><span class="sxs-lookup"><span data-stu-id="2330e-123">Protocol enabled</span></span>|
|-|-|
|<span data-ttu-id="2330e-124">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2330e-124">0x00000008</span></span>|<span data-ttu-id="2330e-125">Activer SSL 2.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="2330e-125">Enable SSL 2.0 by default</span></span>|
|<span data-ttu-id="2330e-126">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2330e-126">0x00000020</span></span>|<span data-ttu-id="2330e-127">Activer SSL 3.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="2330e-127">Enable SSL 3.0 by default</span></span>|
|<span data-ttu-id="2330e-128">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2330e-128">0x00000080</span></span>|<span data-ttu-id="2330e-129">Activer TLS 1.0 par défaut</span><span class="sxs-lookup"><span data-stu-id="2330e-129">Enable TLS 1.0 by default</span></span>|
|<span data-ttu-id="2330e-130">0x00000200</span><span class="sxs-lookup"><span data-stu-id="2330e-130">0x00000200</span></span>|<span data-ttu-id="2330e-131">Activer TLS 1.1 par défaut</span><span class="sxs-lookup"><span data-stu-id="2330e-131">Enable TLS 1.1 by default</span></span>|
|<span data-ttu-id="2330e-132">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2330e-132">0x00000800</span></span>|<span data-ttu-id="2330e-133">Activer TLS 1.2 par défaut</span><span class="sxs-lookup"><span data-stu-id="2330e-133">Enable TLS 1.2 by default</span></span>|

## <a name="office-clients-and-tls-registry-keys"></a><span data-ttu-id="2330e-134">Clients Office et clés de Registre TLS</span><span class="sxs-lookup"><span data-stu-id="2330e-134">Office clients and TLS registry keys</span></span>

<span data-ttu-id="2330e-135">Vous pouvez vous reporter à [la 4057306 de la préparation à l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306).</span><span class="sxs-lookup"><span data-stu-id="2330e-135">You can refer to [KB 4057306 Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306).</span></span> <span data-ttu-id="2330e-136">Il s’agit d’un article général pour les administrateurs informatiques, et de la documentation officielle sur la modification TLS 1,2.</span><span class="sxs-lookup"><span data-stu-id="2330e-136">This is a general article for IT administrators, and it's official documentation about the TLS 1.2 change.</span></span>

<span data-ttu-id="2330e-137">Le tableau suivant indique les valeurs de clés de Registre appropriées dans les clients Office 365 après le 31 octobre 2018.</span><span class="sxs-lookup"><span data-stu-id="2330e-137">The following table shows the appropriate registry key values in Office 365 clients after October 31, 2018.</span></span>

|<span data-ttu-id="2330e-138">Protocoles activés pour le service Office 365 après le 31 octobre 2018</span><span class="sxs-lookup"><span data-stu-id="2330e-138">Enabled protocols for Office 365 service after October 31, 2018</span></span>|<span data-ttu-id="2330e-139">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="2330e-139">Hexadecimal value</span></span>|
|-|-|
|<span data-ttu-id="2330e-140">TLS 1,0 + 1,1 + 1,2</span><span class="sxs-lookup"><span data-stu-id="2330e-140">TLS 1.0 + 1.1 + 1.2</span></span>|<span data-ttu-id="2330e-141">0x00000A80</span><span class="sxs-lookup"><span data-stu-id="2330e-141">0x00000A80</span></span>|
|<span data-ttu-id="2330e-142">TLS 1,1 + 1,2</span><span class="sxs-lookup"><span data-stu-id="2330e-142">TLS 1.1 + 1.2</span></span>|<span data-ttu-id="2330e-143">0x00000A00</span><span class="sxs-lookup"><span data-stu-id="2330e-143">0x00000A00</span></span>|
|<span data-ttu-id="2330e-144">TLS 1,0 + 1,2</span><span class="sxs-lookup"><span data-stu-id="2330e-144">TLS 1.0 + 1.2</span></span>|<span data-ttu-id="2330e-145">0x00000880</span><span class="sxs-lookup"><span data-stu-id="2330e-145">0x00000880</span></span>|
|<span data-ttu-id="2330e-146">TLS 1.2</span><span class="sxs-lookup"><span data-stu-id="2330e-146">TLS 1.2</span></span>|<span data-ttu-id="2330e-147">0x00000800</span><span class="sxs-lookup"><span data-stu-id="2330e-147">0x00000800</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="2330e-148">Il n’est pas recommandé d’utiliser les protocoles SSL 2,0 et 3,0, qui peuvent également être définis à l’aide de la clé **DefaultSecureProtocols** .</span><span class="sxs-lookup"><span data-stu-id="2330e-148">We don't recommend that you use the SSL 2.0 and 3.0 protocols, which can also be set by using the **DefaultSecureProtocols** key.</span></span> <span data-ttu-id="2330e-149">Les protocoles SSL 2,0 et 3,0 sont considérés comme des protocoles déconseillés.</span><span class="sxs-lookup"><span data-stu-id="2330e-149">SSL 2.0 and 3.0 are considered deprecated protocols.</span></span> <span data-ttu-id="2330e-150">La meilleure pratique consiste à mettre fin à l’utilisation des protocoles SSL 2,0 et SSL 3,0, bien que la décision de le faire dépende de ce qui est le mieux adapté à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="2330e-150">The best practice is to end the use of SSL 2.0 and SSL 3.0, although the decision to do this ultimately depends on what best meets your product needs.</span></span> <span data-ttu-id="2330e-151">Pour plus d’informations sur les vulnérabilités SSL 3,0, reportez-vous à [KB 3009008](https://support.microsoft.com/help/3009008).</span><span class="sxs-lookup"><span data-stu-id="2330e-151">For more information about SSL 3.0 vulnerabilities, refer to [KB 3009008](https://support.microsoft.com/help/3009008).</span></span>

<span data-ttu-id="2330e-152">Vous pouvez utiliser la calculatrice Windows par défaut en mode programmeur pour configurer les mêmes valeurs de clés de registre de référence.</span><span class="sxs-lookup"><span data-stu-id="2330e-152">You can use the default Windows Calculator in Programmer mode to set up the same reference registry key values.</span></span> <span data-ttu-id="2330e-153">Pour plus d’informations, reportez-vous à [la mise à jour KB 3140245 pour activer tls 1,1 et tls 1,2 comme protocoles de sécurité par défaut dans WinHTTP dans Windows](https://support.microsoft.com/help/3140245).</span><span class="sxs-lookup"><span data-stu-id="2330e-153">For more information, see [KB 3140245 Update to enable TLS 1.1 and TLS 1.2 as a default secure protocols in WinHTTP in Windows](https://support.microsoft.com/help/3140245).</span></span>

<span data-ttu-id="2330e-154">Quelle que soit la mise à jour de Windows 7 ([KB 3140245](https://support.microsoft.com/help/3140245)) installée ou non, la sous-clé de Registre DefaultSecureProtocols n’est pas présente et doit être ajoutée manuellement ou par le biais d’un objet de stratégie de groupe (GPO).</span><span class="sxs-lookup"><span data-stu-id="2330e-154">Regardless if the Windows 7 update ([KB 3140245](https://support.microsoft.com/help/3140245)) is installed or not, the DefaultSecureProtocols registry sub key isn't present and must be added manually or through a group policy object (GPO).</span></span> <span data-ttu-id="2330e-155">Autrement dit, sauf si vous devez personnaliser les protocoles sécurisés qui sont activés ou restreints, cette clé n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="2330e-155">That is, unless you have to customize what secure protocols are enabled or restricted, this key is not required.</span></span> <span data-ttu-id="2330e-156">Vous n’avez besoin que de la mise à jour de Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)).</span><span class="sxs-lookup"><span data-stu-id="2330e-156">You only need the Windows 7 SP1 ([KB 3140245](https://support.microsoft.com/help/3140245)) update.</span></span>
