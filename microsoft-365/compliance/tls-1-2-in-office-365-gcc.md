---
title: Désactivation de TLS 1.0 et 1.1 dans Office 365 GCC High et DoD
description: Explique comment Microsoft désactive la prise en charge de TLS 1.1 et 1.0 dans les environnements GCC High et DoD dans Microsoft 365.
author: workshay
manager: laurawi
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.collection: M365-security-compliance
ms.service: information-protection
ms.topic: article
ms.reviewer: krowley
ms.author: shmehta
appliesto:
- Office 365 Business
ms.openlocfilehash: 006f81ee5b17baca4f42a78c5a87a59e8e90648f
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166439"
---
# <a name="disabling-tls-10-and-11-in-office-365-gcc-high-and-dod"></a><span data-ttu-id="173f4-103">Désactivation de TLS 1.0 et 1.1 dans Office 365 GCC High et DoD</span><span class="sxs-lookup"><span data-stu-id="173f4-103">Disabling TLS 1.0 and 1.1 in Office 365 GCC High and DoD</span></span>

## <a name="summary"></a><span data-ttu-id="173f4-104">Résumé</span><span class="sxs-lookup"><span data-stu-id="173f4-104">Summary</span></span>

<span data-ttu-id="173f4-105">Afin de se conformer aux dernières normes de conformité pour le Programme de gestion des risques et d’autorisations (FedRAMP), nous désactivons les versions TLS 1.1 et 1.0 dans Microsoft 365 pour les environnements GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="173f4-105">In order to comply with the latest compliance standards for the Federal Risk and Authorization Management Program (FedRAMP), we are disabling Transport Layer Security (TLS) versions 1.1 and 1.0 in Microsoft 365 for GCC High and DoD environments.</span></span> <span data-ttu-id="173f4-106">Cette modification a été précédemment annoncée via le Support Microsoft dans la préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="173f4-106">This change was previously announced through Microsoft Support in [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="173f4-107">La sécurité de vos données est importante et nous nous engageons à assurer la transparence des modifications qui pourraient affecter votre utilisation du service.</span><span class="sxs-lookup"><span data-stu-id="173f4-107">The security of your data is important, and we are committed to transparency about changes that could affect your use of the service.</span></span>

<span data-ttu-id="173f4-108">Bien que [l’implémentation de Microsoft TLS 1.0](https://support.microsoft.com/help/3117336) ne présente aucune vulnérabilité de sécurité connue, nous nous engageons à respecter les normes de conformité FedRAMP.</span><span class="sxs-lookup"><span data-stu-id="173f4-108">Although the [Microsoft TLS 1.0 implementation](https://support.microsoft.com/help/3117336) has no known security vulnerabilities, we remain committed to the FedRAMP compliance standards.</span></span> <span data-ttu-id="173f4-109">Par conséquent, nous avons désactivé TLS 1.1 et 1.0 dans Office 365 dans les environnements GCC High et DoD le 15 janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="173f4-109">Therefore, we disabled TLS 1.1 and 1.0 in Office 365 in GCC High and DoD environments on January 15, 2020.</span></span> <span data-ttu-id="173f4-110">Pour plus d’informations sur la suppression des dépendances TLS 1.1 et 1.0, consultez le livre blanc suivant :</span><span class="sxs-lookup"><span data-stu-id="173f4-110">For information about how to remove TLS 1.1 and 1.0 dependencies, see the following white paper:</span></span>

[<span data-ttu-id="173f4-111">Résolution du problème TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="173f4-111">Solving the TLS 1.0 problem</span></span>](https://www.microsoft.com/download/details.aspx?id=55266)

<span data-ttu-id="173f4-112">Vous devez utiliser TLS version 1.2 à la place.</span><span class="sxs-lookup"><span data-stu-id="173f4-112">You must use TLS version 1.2 instead.</span></span> <span data-ttu-id="173f4-113">Pour plus d’informations, voir Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="173f4-113">For more information, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="173f4-114">Pour SharePoint et OneDrive, vous devez mettre à jour et configurer .NET pour prendre en charge TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="173f4-114">For SharePoint and OneDrive, you'll need to update and configure .NET to support TLS 1.2.</span></span> <span data-ttu-id="173f4-115">Pour plus d’informations, [voir Comment activer TLS 1.2 sur les clients](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span><span class="sxs-lookup"><span data-stu-id="173f4-115">For information, see [How to enable TLS 1.2 on clients](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span></span>

## <a name="more-information"></a><span data-ttu-id="173f4-116">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="173f4-116">More information</span></span>

<span data-ttu-id="173f4-117">À compter du 15 janvier 2020, Office 365 dans les environnements GCC High et DoD sera supprimé de TLS 1.1 et 1.0.</span><span class="sxs-lookup"><span data-stu-id="173f4-117">Starting on January 15, 2020, Office 365 in the GCC High and DoD environments will deprecate TLS 1.1 and 1.0.</span></span>

<span data-ttu-id="173f4-118">D’ici le 15 janvier 2020, toutes les combinaisons de serveurs clients et de serveurs de navigateur doivent utiliser TLS version 1.2 (ou version ultérieure) pour s’assurer que toutes les connexions peuvent être réalisées sans problème avec les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="173f4-118">By January 15, 2020, all combinations of client servers and browser servers should use TLS version 1.2 (or a later version) to make sure that all connections can be made without issues to Office 365 services.</span></span> <span data-ttu-id="173f4-119">Cela peut nécessiter des mises à jour de certaines combinaisons de serveurs clients et de serveurs de navigateur.</span><span class="sxs-lookup"><span data-stu-id="173f4-119">This may require updates to certain combinations of client servers and browser servers.</span></span>

<span data-ttu-id="173f4-120">Si vous ne mettez pas à jour la version 1.2 de TLS (ou une version ultérieure) d’ici le 15 janvier 2020, vous serez face à des problèmes lorsque vous tenterez de vous connecter à Office 365.</span><span class="sxs-lookup"><span data-stu-id="173f4-120">If you do not update to TLS version 1.2 (or a later version) by January 15, 2020, you will experience issues when you try to connect to Office 365.</span></span> <span data-ttu-id="173f4-121">En outre, vous devez mettre à jour vers TLS 1.2 (ou une version ultérieure) dans le cadre de la résolution.</span><span class="sxs-lookup"><span data-stu-id="173f4-121">Additionally, you will be required to update to TLS 1.2 (or a later version) as part of the resolution.</span></span>

<span data-ttu-id="173f4-122">Nous savons que les clients suivants ne peuvent pas utiliser TLS 1.2 :</span><span class="sxs-lookup"><span data-stu-id="173f4-122">We know that the following clients cannot use TLS 1.2:</span></span>

- <span data-ttu-id="173f4-123">Android 4.3 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="173f4-123">Android 4.3 and earlier versions</span></span>
- <span data-ttu-id="173f4-124">Firefox 5.0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="173f4-124">Firefox version 5.0 and earlier versions</span></span>
- <span data-ttu-id="173f4-125">Internet Explorer 8 à 10 sur Windows 7 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="173f4-125">Internet Explorer 8–10 on Windows 7 and earlier versions</span></span>
- <span data-ttu-id="173f4-126">Internet Explorer 10 sur Windows Phone 8.0</span><span class="sxs-lookup"><span data-stu-id="173f4-126">Internet Explorer 10 on Windows Phone 8.0</span></span>
- <span data-ttu-id="173f4-127">Safari 6.0.4/OS X 10.8.4 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="173f4-127">Safari 6.0.4/OS X 10.8.4 and earlier versions</span></span>

<span data-ttu-id="173f4-128">Nous vous recommandons de mettre à jour vos clients pour vous assurer que vous conservez un accès ininterrompu à Office 365 GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="173f4-128">We recommend that you update your clients to make sure that you maintain uninterrupted access to Office 365 GCC High and DoD.</span></span>

<span data-ttu-id="173f4-129">Bien que l’analyse actuelle des connexions aux services Microsoft Online indique que la plupart des services et des points de terminaison voient très peu d’utilisation de TLS 1.1 et 1.0, nous fournissons une notification de cette modification afin que vous pouvez mettre à jour les clients ou serveurs concernés si nécessaire avant la fin de la prise en charge de TLS 1.1 et 1.0.</span><span class="sxs-lookup"><span data-stu-id="173f4-129">Although current analysis of connections to Microsoft Online services shows that most services and endpoints see very little TLS 1.1 and 1.0 usage, we are providing notice of this change so that you can update any affected clients or servers as necessary before support for TLS 1.1 and 1.0 ends.</span></span> <span data-ttu-id="173f4-130">Si vous utilisez une infrastructure locale pour des scénarios hybrides ou des services AD FS (Active Directory Federation Services), assurez-vous que l’infrastructure peut prendre en charge les connexions entrantes et sortantes qui utilisent TLS 1.2 (ou une version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="173f4-130">If you are using any on-premises infrastructure for hybrid scenarios or Active Directory Federation Services (AD FS), make sure that the infrastructure can support both inbound and outbound connections that use TLS 1.2 (or a later version).</span></span>

<span data-ttu-id="173f4-131">En plus des pannes que vous pouvez connaître si vous utilisez les clients répertoriés qui ne peuvent pas utiliser TLS 1.2, la suppression de TLS 1.1 et 1.0 vous empêchera d’utiliser le produit Microsoft suivant :</span><span class="sxs-lookup"><span data-stu-id="173f4-131">In addition to the outages that you might experience if you use the listed clients that cannot use TLS 1.2, removing TLS 1.1 and 1.0 will prevent you from being able to use the following Microsoft product:</span></span>

- <span data-ttu-id="173f4-132">Téléphone Lync</span><span class="sxs-lookup"><span data-stu-id="173f4-132">Lync phone</span></span>

## <a name="references"></a><span data-ttu-id="173f4-133">Références</span><span class="sxs-lookup"><span data-stu-id="173f4-133">References</span></span>

<span data-ttu-id="173f4-134">L’article de support suivant décrit des conseils et des références pour vous assurer que vos clients utilisent TLS 1.2 :</span><span class="sxs-lookup"><span data-stu-id="173f4-134">The following support article describes guidance and references to help make sure that your clients are using TLS 1.2:</span></span>

[<span data-ttu-id="173f4-135">Préparation de l’utilisation obligatoire de TLS 1.2 dans Office 365</span><span class="sxs-lookup"><span data-stu-id="173f4-135">Preparing for the mandatory use of TLS 1.2 in Office 365</span></span>](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)
