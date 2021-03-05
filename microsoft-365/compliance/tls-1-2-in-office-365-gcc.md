---
title: Désactivation de TLS 1.0 et 1.1 dans Microsoft 365 GCC High et DoD
description: Explique comment Microsoft désactive la prise en charge de TLS 1.1 et 1.0 dans les environnements GCC High et DoD dans Microsoft 365.
author: kccross
manager: laurawi
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.collection: M365-security-compliance
ms.service: information-protection
ms.topic: article
ms.reviewer: krowley
ms.author: krowley
appliesto:
- Office 365 Business
ms.openlocfilehash: d4da76268791e36bd01b5d6f6140fd52c70b3b4a
ms.sourcegitcommit: 375168ee66be862cf3b00f2733c7be02e63408cf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50454193"
---
# <a name="disabling-tls-10-and-11-in-microsoft-365-gcc-high-and-dod"></a><span data-ttu-id="e94d6-103">Désactivation de TLS 1.0 et 1.1 dans Microsoft 365 GCC High et DoD</span><span class="sxs-lookup"><span data-stu-id="e94d6-103">Disabling TLS 1.0 and 1.1 in Microsoft 365 GCC High and DoD</span></span>

## <a name="summary"></a><span data-ttu-id="e94d6-104">Résumé</span><span class="sxs-lookup"><span data-stu-id="e94d6-104">Summary</span></span>

<span data-ttu-id="e94d6-105">Afin de se conformer aux dernières normes de conformité pour le programme fedramp (Federal Risk and Authorization Management Program), nous désactivons les versions 1.1 et 1.0 de Transport Layer Security (TLS) dans Microsoft 365 pour les environnements GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="e94d6-105">In order to comply with the latest compliance standards for the Federal Risk and Authorization Management Program (FedRAMP), we are disabling Transport Layer Security (TLS) versions 1.1 and 1.0 in Microsoft 365 for GCC High and DoD environments.</span></span> <span data-ttu-id="e94d6-106">Cette modification a été annoncée précédemment par le biais du Support Microsoft dans la préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="e94d6-106">This change was previously announced through Microsoft Support in [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="e94d6-107">La sécurité de vos données est importante et nous nous engageons à assurer la transparence des modifications qui pourraient affecter votre utilisation du service.</span><span class="sxs-lookup"><span data-stu-id="e94d6-107">The security of your data is important, and we are committed to transparency about changes that could affect your use of the service.</span></span>

<span data-ttu-id="e94d6-108">Bien que [l’implémentation de Microsoft TLS 1.0](https://support.microsoft.com/help/3117336) ne présente aucune vulnérabilité de sécurité connue, nous nous engageons à respecter les normes de conformité FedRAMP.</span><span class="sxs-lookup"><span data-stu-id="e94d6-108">Although the [Microsoft TLS 1.0 implementation](https://support.microsoft.com/help/3117336) has no known security vulnerabilities, we remain committed to the FedRAMP compliance standards.</span></span> <span data-ttu-id="e94d6-109">Par conséquent, nous avons désactivé TLS 1.1 et 1.0 dans Microsoft 365 dans les environnements GCC High et DoD le 15 janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="e94d6-109">Therefore, we disabled TLS 1.1 and 1.0 in Microsoft 365 in GCC High and DoD environments on January 15, 2020.</span></span> <span data-ttu-id="e94d6-110">Pour plus d’informations sur la suppression des dépendances TLS 1.1 et 1.0, voir le livre blanc suivant :</span><span class="sxs-lookup"><span data-stu-id="e94d6-110">For information about how to remove TLS 1.1 and 1.0 dependencies, see the following white paper:</span></span>

[<span data-ttu-id="e94d6-111">Résolution du problème TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="e94d6-111">Solving the TLS 1.0 problem</span></span>](https://www.microsoft.com/download/details.aspx?id=55266)

## <a name="more-information"></a><span data-ttu-id="e94d6-112">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="e94d6-112">More information</span></span>

<span data-ttu-id="e94d6-113">À compter du 15 janvier 2020, Microsoft 365 dans les environnements GCC High et DoD désactive TLS 1.1 et 1.0.</span><span class="sxs-lookup"><span data-stu-id="e94d6-113">Starting on January 15, 2020, Microsoft 365 in the GCC High and DoD environments will disable TLS 1.1 and 1.0.</span></span>

<span data-ttu-id="e94d6-114">D’ici le 15 janvier 2020, toutes les combinaisons de serveurs clients et de serveurs de navigateur doivent utiliser TLS version 1.2 (ou version ultérieure) pour s’assurer que toutes les connexions peuvent être réalisées sans problème avec Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e94d6-114">By January 15, 2020, all combinations of client servers and browser servers should use TLS version 1.2 (or a later version) to make sure that all connections can be made without issues to Microsoft 365.</span></span> <span data-ttu-id="e94d6-115">Cela peut nécessiter des mises à jour de certaines combinaisons de serveurs clients et de serveurs de navigateur.</span><span class="sxs-lookup"><span data-stu-id="e94d6-115">This may require updates to certain combinations of client servers and browser servers.</span></span>

<span data-ttu-id="e94d6-116">Pour SharePoint et OneDrive, vous devez mettre à jour et configurer .NET pour prendre en charge TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="e94d6-116">For SharePoint and OneDrive, you'll need to update and configure .NET to support TLS 1.2.</span></span> <span data-ttu-id="e94d6-117">Pour plus d’informations, [voir Comment activer TLS 1.2 sur les clients](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span><span class="sxs-lookup"><span data-stu-id="e94d6-117">For information, see [How to enable TLS 1.2 on clients](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span></span>

<span data-ttu-id="e94d6-118">Vous devez mettre à jour vos ordinateurs clients pour vous assurer que vous conservez un accès ininterrompu à Office 365 GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="e94d6-118">You must update your client computers to make sure that you maintain uninterrupted access to Office 365 GCC High and DoD.</span></span>

<span data-ttu-id="e94d6-119">Vous devez mettre à jour les applications qui appellent les API Microsoft 365 sur TLS 1.0 ou TLS 1.1 pour utiliser TLS 1.2.</span><span class="sxs-lookup"><span data-stu-id="e94d6-119">You'll need to update applications that call Microsoft 365 APIs over TLS 1.0 or TLS 1.1 to use TLS 1.2.</span></span> <span data-ttu-id="e94d6-120">Par défaut, .NET 4.5 est TLS 1.1.</span><span class="sxs-lookup"><span data-stu-id="e94d6-120">.NET 4.5 defaults to TLS 1.1.</span></span> <span data-ttu-id="e94d6-121">Pour mettre à jour votre configuration .NET, voir [Comment activer TLS (Transport Layer Security) 1.2 sur les clients.](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client)</span><span class="sxs-lookup"><span data-stu-id="e94d6-121">To update your .NET configuration, see [How to enable Transport Layer Security (TLS) 1.2 on clients](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client).</span></span> <span data-ttu-id="e94d6-122">Pour plus d’informations, voir Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="e94d6-122">For more information, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="e94d6-123">Nous savons que les applications clientes suivantes ne peuvent pas utiliser TLS 1.2 :</span><span class="sxs-lookup"><span data-stu-id="e94d6-123">We know that the following client applications cannot use TLS 1.2:</span></span>

- <span data-ttu-id="e94d6-124">Android 4.3 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e94d6-124">Android 4.3 and earlier versions</span></span>
- <span data-ttu-id="e94d6-125">Firefox 5.0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e94d6-125">Firefox version 5.0 and earlier versions</span></span>
- <span data-ttu-id="e94d6-126">Internet Explorer 8 à 10 sur Windows 7 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e94d6-126">Internet Explorer 8–10 on Windows 7 and earlier versions</span></span>
- <span data-ttu-id="e94d6-127">Internet Explorer 10 sur Windows Phone 8.0</span><span class="sxs-lookup"><span data-stu-id="e94d6-127">Internet Explorer 10 on Windows Phone 8.0</span></span>
- <span data-ttu-id="e94d6-128">Safari 6.0.4/OS X 10.8.4 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="e94d6-128">Safari 6.0.4/OS X 10.8.4 and earlier versions</span></span>

<span data-ttu-id="e94d6-129">Bien que l’analyse actuelle des connexions aux services Microsoft Online indique que la plupart des services et points de terminaison voient très peu d’utilisation de TLS 1.1 et 1.0, nous fournissons une notification de cette modification afin que vous pouvez mettre à jour les clients ou serveurs concernés si nécessaire avant la fin de la prise en charge de TLS 1.1 et 1.0.</span><span class="sxs-lookup"><span data-stu-id="e94d6-129">Although current analysis of connections to Microsoft Online services shows that most services and endpoints see very little TLS 1.1 and 1.0 usage, we're providing notice of this change so that you can update any affected clients or servers as necessary before support for TLS 1.1 and 1.0 ends.</span></span> <span data-ttu-id="e94d6-130">Si vous utilisez une infrastructure locale pour des scénarios hybrides ou des services AD FS (Active Directory Federation Services), assurez-vous que l’infrastructure peut prendre en charge les connexions entrantes et sortantes qui utilisent TLS 1.2 (ou une version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="e94d6-130">If you are using any on-premises infrastructure for hybrid scenarios or Active Directory Federation Services (AD FS), make sure that the infrastructure can support both inbound and outbound connections that use TLS 1.2 (or a later version).</span></span>

<span data-ttu-id="e94d6-131">En plus des pannes que vous pouvez connaître si vous utilisez les clients répertoriés qui ne peuvent pas utiliser TLS 1.2, la suppression de TLS 1.1 et 1.0 vous empêchera d’utiliser le produit Microsoft suivant :</span><span class="sxs-lookup"><span data-stu-id="e94d6-131">In addition to the outages that you might experience if you use the listed clients that cannot use TLS 1.2, removing TLS 1.1 and 1.0 will prevent you from being able to use the following Microsoft product:</span></span>

- <span data-ttu-id="e94d6-132">Téléphone Lync</span><span class="sxs-lookup"><span data-stu-id="e94d6-132">Lync phone</span></span>

## <a name="references"></a><span data-ttu-id="e94d6-133">Références</span><span class="sxs-lookup"><span data-stu-id="e94d6-133">References</span></span>

<span data-ttu-id="e94d6-134">Pour obtenir des conseils et des références pour vous assurer que vos clients utilisent TLS 1.2, voir Préparation de l’utilisation obligatoire de [TLS 1.2 dans Office 365.](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)</span><span class="sxs-lookup"><span data-stu-id="e94d6-134">For guidance and references to help make sure that your clients are using TLS 1.2, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>
