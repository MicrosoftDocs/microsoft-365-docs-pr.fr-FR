---
title: Dépréciation des protocoles TLS 1,0 et 1,1 dans Office 365 GCC High et DoD
description: Explique comment Microsoft déplace la date de fin à la prise en charge de TLS 1,1 et 1,0 dans les environnements GCC High et DoD dans Office 365 et la préparation à l’utilisation de TLS 1,2.
author: simonxjx
manager: dcscontentpm
localization_priority: Normal
search.appverid:
- MET150
audience: ITPro
ms.service: O365-seccomp
ms.topic: article
ms.author: v-six
ms.reviewer: lobrion
appliesto:
- Office 365 Business
ms.openlocfilehash: f61c0a809c4666981ee0f2d67eea21474b83a675
ms.sourcegitcommit: 51a9f34796535309b8ca8b52da92da0a3621327b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2020
ms.locfileid: "45024818"
---
# <a name="deprecating-tls-10-and-11-in-office-365-gcc-high-and-dod"></a><span data-ttu-id="5f452-103">Dépréciation des protocoles TLS 1,0 et 1,1 dans Office 365 GCC High et DoD</span><span class="sxs-lookup"><span data-stu-id="5f452-103">Deprecating TLS 1.0 and 1.1 in Office 365 GCC High and DoD</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f452-104">Le monde est en pleine pandémie et, chez Microsoft, nous sommes conscients de l’impact de cette situation sur nos clients et nos partenaires.</span><span class="sxs-lookup"><span data-stu-id="5f452-104">The world is in the middle of a pandemic, and we at Microsoft are aware of the impact on our customers and partners.</span></span> <span data-ttu-id="5f452-105">Pour alléger le fardeau de nos clients commerciaux, nous avons temporairement suspendu le déclassement de TLS 1.0 et 1.1.</span><span class="sxs-lookup"><span data-stu-id="5f452-105">To lighten the burden on our commercial customers, we have temporarily halted any deprecation enforcement of TLS 1.0 and 1.1.</span></span> <span data-ttu-id="5f452-106">Une mise à jour sera envoyée selon un calendrier révisé après la stabilisation de la crise actuelle.</span><span class="sxs-lookup"><span data-stu-id="5f452-106">An update will be sent on a revised timeline after the current crisis stabilizes.</span></span> <span data-ttu-id="5f452-107">(La révision de cet article est destinée à refléter l’évolution des changements.)</span><span class="sxs-lookup"><span data-stu-id="5f452-107">(This article is revised to reflect the change.)</span></span>

## <a name="summary"></a><span data-ttu-id="5f452-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="5f452-108">Summary</span></span>

<span data-ttu-id="5f452-109">Afin de se conformer aux dernières normes de conformité du programme fédéral de gestion des autorisations et des risques (FedRAMP), nous passons aux versions 1,1 et 1,0 du protocole TLS (Transport Layer Security) dans Microsoft Office 365 pour les environnements GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="5f452-109">In order to comply with the latest compliance standards for the Federal Risk and Authorization Management Program (FedRAMP), we are moving to deprecate Transport Layer Security (TLS) versions 1.1 and 1.0 in Microsoft Office 365 for GCC High and DoD environments.</span></span> <span data-ttu-id="5f452-110">Cette modification a été précédemment annoncée via le support Microsoft dans [la préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="5f452-110">This change was previously announced through Microsoft Support in [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="5f452-111">Nous comprenons que la sécurité de vos données est importante et nous nous engageons à la transparence des modifications qui pourraient influer sur l’utilisation du service.</span><span class="sxs-lookup"><span data-stu-id="5f452-111">We understand that the security of your data is important, and we are committed to transparency about changes that could affect your use of the service.</span></span>

<span data-ttu-id="5f452-112">Bien que l' [implémentation de Microsoft TLS 1,0](https://support.microsoft.com/help/3117336) ne présente pas de failles de sécurité connues, nous nous contenterons de respecter les normes de conformité FedRAMP.</span><span class="sxs-lookup"><span data-stu-id="5f452-112">Although the [Microsoft TLS 1.0 implementation](https://support.microsoft.com/help/3117336) has no known security vulnerabilities, we remain committed to the FedRAMP compliance standards.</span></span> <span data-ttu-id="5f452-113">Par conséquent, nous allons déprécier les protocoles TLS 1,1 et 1,0 dans Office 365 dans les environnements GCC High et DoD commençant le 15 janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="5f452-113">Therefore, we will deprecate TLS 1.1 and 1.0 in Office 365 in GCC High and DoD environments starting on January 15, 2020.</span></span> <span data-ttu-id="5f452-114">Pour plus d’informations sur la suppression des dépendances TLS 1,1 et 1,0, voir le livre blanc suivant :</span><span class="sxs-lookup"><span data-stu-id="5f452-114">For information about how to remove TLS 1.1 and 1.0 dependencies, see the following white paper:</span></span>

[<span data-ttu-id="5f452-115">Résolution du problème 1,0 TLS</span><span class="sxs-lookup"><span data-stu-id="5f452-115">Solving the TLS 1.0 problem</span></span>](https://www.microsoft.com/download/details.aspx?id=55266)

<span data-ttu-id="5f452-116">Lors de la préparation de cette modification pour TLS 1,1 et 1,0, nous vous recommandons d’utiliser à la place TLS version 1,2.</span><span class="sxs-lookup"><span data-stu-id="5f452-116">In preparing for this change for TLS 1.1 and 1.0, we recommend that you use TLS version 1.2 instead.</span></span> <span data-ttu-id="5f452-117">Pour plus d’informations, consultez [la rubrique préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="5f452-117">For more information, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

## <a name="more-information"></a><span data-ttu-id="5f452-118">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="5f452-118">More information</span></span>

<span data-ttu-id="5f452-119">À partir du 15 janvier 2020, Office 365 dans les environnements GCC High et DoD déprécieront TLS 1,1 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f452-119">Starting on January 15, 2020, Office 365 in the GCC High and DoD environments will deprecate TLS 1.1 and 1.0.</span></span>

<span data-ttu-id="5f452-120">D’ici le 15 janvier 2020, toutes les combinaisons de serveurs clients et de serveurs d’exploration doivent utiliser le protocole TLS 1,2 (ou une version ultérieure) pour s’assurer que toutes les connexions peuvent être établies sans problèmes aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="5f452-120">By January 15, 2020, all combinations of client servers and browser servers should use TLS version 1.2 (or a later version) to make sure that all connections can be made without issues to Office 365 services.</span></span> <span data-ttu-id="5f452-121">Cela peut nécessiter des mises à jour de certaines combinaisons de serveurs clients et de serveurs d’exploration.</span><span class="sxs-lookup"><span data-stu-id="5f452-121">This may require updates to certain combinations of client servers and browser servers.</span></span>

<span data-ttu-id="5f452-122">Si vous ne procédez pas à la mise à jour vers la version 1,2 (ou une version ultérieure) pour le 15 janvier 2020, vous rencontrez des problèmes lorsque vous essayez de vous connecter à Office 365.</span><span class="sxs-lookup"><span data-stu-id="5f452-122">If you do not update to TLS version 1.2 (or a later version) by January 15, 2020, you will experience issues when you try to connect to Office 365.</span></span> <span data-ttu-id="5f452-123">En outre, vous devez effectuer une mise à jour vers TLS 1,2 (ou une version ultérieure) dans le cadre de la résolution.</span><span class="sxs-lookup"><span data-stu-id="5f452-123">Additionally, you will be required to update to TLS 1.2 (or a later version) as part of the resolution.</span></span>

<span data-ttu-id="5f452-124">Nous connaissons que les clients suivants ne peuvent pas utiliser TLS 1,2 :</span><span class="sxs-lookup"><span data-stu-id="5f452-124">We know that the following clients cannot use TLS 1.2:</span></span>

- <span data-ttu-id="5f452-125">Android 4.3 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5f452-125">Android 4.3 and earlier versions</span></span>
- <span data-ttu-id="5f452-126">Firefox 5.0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5f452-126">Firefox version 5.0 and earlier versions</span></span>
- <span data-ttu-id="5f452-127">Internet Explorer 8 à 10 sur Windows 7 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5f452-127">Internet Explorer 8–10 on Windows 7 and earlier versions</span></span>
- <span data-ttu-id="5f452-128">Internet Explorer 10 sur Windows Phone 8,0</span><span class="sxs-lookup"><span data-stu-id="5f452-128">Internet Explorer 10 on Windows Phone 8.0</span></span>
- <span data-ttu-id="5f452-129">Safari 6.0.4/OS X 10.8.4 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="5f452-129">Safari 6.0.4/OS X 10.8.4 and earlier versions</span></span>

<span data-ttu-id="5f452-130">Nous vous recommandons de mettre à jour vos clients afin de garantir un accès ininterrompu à Office 365 GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="5f452-130">We recommend that you update your clients to make sure that you maintain uninterrupted access to Office 365 GCC High and DoD.</span></span>

<span data-ttu-id="5f452-131">Bien que l’analyse actuelle des connexions aux services Microsoft Online indique que la plupart des services et points de terminaison voient l’utilisation de TLS 1,1 et 1,0 très peu, nous fournissons un avis de cette modification afin que vous puissiez mettre à jour les clients ou serveurs concernés, le cas échéant, avant la prise en charge de TLS 1,1 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f452-131">Although current analysis of connections to Microsoft Online services shows that most services and endpoints see very little TLS 1.1 and 1.0 usage, we are providing notice of this change so that you can update any affected clients or servers as necessary before support for TLS 1.1 and 1.0 ends.</span></span> <span data-ttu-id="5f452-132">Si vous utilisez une infrastructure locale pour des scénarios hybrides ou AD FS (Active Directory Federation Services), assurez-vous que l’infrastructure peut prendre en charge à la fois les connexions entrantes et sortantes qui utilisent TLS 1,2 (ou une version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="5f452-132">If you are using any on-premises infrastructure for hybrid scenarios or Active Directory Federation Services (AD FS), make sure that the infrastructure can support both inbound and outbound connections that use TLS 1.2 (or a later version).</span></span>

<span data-ttu-id="5f452-133">Outre les pannes que vous pouvez vous produire si vous utilisez les clients énumérés qui ne peuvent pas utiliser le protocole TLS 1,2, la suppression des protocoles TLS 1,1 et 1,0 vous empêchera d’utiliser le produit Microsoft suivant :</span><span class="sxs-lookup"><span data-stu-id="5f452-133">In addition to the outages that you might experience if you use the listed clients that cannot use TLS 1.2, removing TLS 1.1 and 1.0 will prevent you from being able to use the following Microsoft product:</span></span>

- <span data-ttu-id="5f452-134">Lync Phone</span><span class="sxs-lookup"><span data-stu-id="5f452-134">Lync phone</span></span>

## <a name="references"></a><span data-ttu-id="5f452-135">Références</span><span class="sxs-lookup"><span data-stu-id="5f452-135">References</span></span>

<span data-ttu-id="5f452-136">L’article suivant du support technique fournit des conseils et des références pour vous aider à vous assurer que vos clients utilisent TLS 1,2 :</span><span class="sxs-lookup"><span data-stu-id="5f452-136">The following support article describes guidance and references to help make sure that your clients are using TLS 1.2:</span></span>

[<span data-ttu-id="5f452-137">Préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365</span><span class="sxs-lookup"><span data-stu-id="5f452-137">Preparing for the mandatory use of TLS 1.2 in Office 365</span></span>](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)
