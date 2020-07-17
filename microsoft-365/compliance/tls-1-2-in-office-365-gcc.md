---
title: Dépréciation des protocoles TLS 1,0 et 1,1 dans Office 365 GCC High et DoD
description: Explique comment Microsoft déplace la date de fin à la prise en charge de TLS 1,1 et 1,0 dans les environnements GCC High et DoD dans Office 365 et la préparation à l’utilisation de TLS 1,2.
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
ms.openlocfilehash: 76e9b203e58ba7fa23942ea42810456e3bee377d
ms.sourcegitcommit: 42b618231e9f608f3ae7226a313b0366601d0ea2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45158879"
---
# <a name="deprecating-tls-10-and-11-in-office-365-gcc-high-and-dod"></a><span data-ttu-id="6053c-103">Dépréciation des protocoles TLS 1,0 et 1,1 dans Office 365 GCC High et DoD</span><span class="sxs-lookup"><span data-stu-id="6053c-103">Deprecating TLS 1.0 and 1.1 in Office 365 GCC High and DoD</span></span>

## <a name="summary"></a><span data-ttu-id="6053c-104">Résumé</span><span class="sxs-lookup"><span data-stu-id="6053c-104">Summary</span></span>

<span data-ttu-id="6053c-105">Afin de se conformer aux dernières normes de conformité pour le programme fédéral de gestion des risques et d’autorisations (FedRAMP), nous déprécions les versions 1,1 et 1,0 de Transport Layer Security (TLS) dans Microsoft Office 365 pour les environnements GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="6053c-105">In order to comply with the latest compliance standards for the Federal Risk and Authorization Management Program (FedRAMP), we are deprecating Transport Layer Security (TLS) versions 1.1 and 1.0 in Microsoft Office 365 for GCC High and DoD environments.</span></span> <span data-ttu-id="6053c-106">Cette modification a été précédemment annoncée via le support Microsoft dans [la préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="6053c-106">This change was previously announced through Microsoft Support in [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

<span data-ttu-id="6053c-107">La sécurité de vos données est importante et nous nous engageons à la transparence des modifications susceptibles d’affecter l’utilisation du service.</span><span class="sxs-lookup"><span data-stu-id="6053c-107">The security of your data is important, and we are committed to transparency about changes that could affect your use of the service.</span></span>

<span data-ttu-id="6053c-108">Bien que l' [implémentation de Microsoft TLS 1,0](https://support.microsoft.com/help/3117336) ne présente pas de failles de sécurité connues, nous nous contenterons de respecter les normes de conformité FedRAMP.</span><span class="sxs-lookup"><span data-stu-id="6053c-108">Although the [Microsoft TLS 1.0 implementation](https://support.microsoft.com/help/3117336) has no known security vulnerabilities, we remain committed to the FedRAMP compliance standards.</span></span> <span data-ttu-id="6053c-109">Par conséquent, nous allons déprécier les protocoles TLS 1,1 et 1,0 dans Office 365 dans les environnements GCC High et DoD commençant le 15 janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="6053c-109">Therefore, we will deprecate TLS 1.1 and 1.0 in Office 365 in GCC High and DoD environments starting on January 15, 2020.</span></span> <span data-ttu-id="6053c-110">Pour plus d’informations sur la suppression des dépendances TLS 1,1 et 1,0, voir le livre blanc suivant :</span><span class="sxs-lookup"><span data-stu-id="6053c-110">For information about how to remove TLS 1.1 and 1.0 dependencies, see the following white paper:</span></span>

[<span data-ttu-id="6053c-111">Résolution du problème 1,0 TLS</span><span class="sxs-lookup"><span data-stu-id="6053c-111">Solving the TLS 1.0 problem</span></span>](https://www.microsoft.com/download/details.aspx?id=55266)

<span data-ttu-id="6053c-112">Lors de la préparation de cette modification pour TLS 1,1 et 1,0, nous vous recommandons d’utiliser à la place TLS version 1,2.</span><span class="sxs-lookup"><span data-stu-id="6053c-112">In preparing for this change for TLS 1.1 and 1.0, we recommend that you use TLS version 1.2 instead.</span></span> <span data-ttu-id="6053c-113">Pour plus d’informations, consultez [la rubrique préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span><span class="sxs-lookup"><span data-stu-id="6053c-113">For more information, see [Preparing for the mandatory use of TLS 1.2 in Office 365](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365).</span></span>

## <a name="more-information"></a><span data-ttu-id="6053c-114">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="6053c-114">More information</span></span>

<span data-ttu-id="6053c-115">À partir du 15 janvier 2020, Office 365 dans les environnements GCC High et DoD déprécieront TLS 1,1 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6053c-115">Starting on January 15, 2020, Office 365 in the GCC High and DoD environments will deprecate TLS 1.1 and 1.0.</span></span>

<span data-ttu-id="6053c-116">D’ici le 15 janvier 2020, toutes les combinaisons de serveurs clients et de serveurs d’exploration doivent utiliser le protocole TLS 1,2 (ou une version ultérieure) pour s’assurer que toutes les connexions peuvent être établies sans problèmes aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="6053c-116">By January 15, 2020, all combinations of client servers and browser servers should use TLS version 1.2 (or a later version) to make sure that all connections can be made without issues to Office 365 services.</span></span> <span data-ttu-id="6053c-117">Cela peut nécessiter des mises à jour de certaines combinaisons de serveurs clients et de serveurs d’exploration.</span><span class="sxs-lookup"><span data-stu-id="6053c-117">This may require updates to certain combinations of client servers and browser servers.</span></span>

<span data-ttu-id="6053c-118">Si vous ne procédez pas à la mise à jour vers la version 1,2 (ou une version ultérieure) pour le 15 janvier 2020, vous rencontrez des problèmes lorsque vous essayez de vous connecter à Office 365.</span><span class="sxs-lookup"><span data-stu-id="6053c-118">If you do not update to TLS version 1.2 (or a later version) by January 15, 2020, you will experience issues when you try to connect to Office 365.</span></span> <span data-ttu-id="6053c-119">En outre, vous devez effectuer une mise à jour vers TLS 1,2 (ou une version ultérieure) dans le cadre de la résolution.</span><span class="sxs-lookup"><span data-stu-id="6053c-119">Additionally, you will be required to update to TLS 1.2 (or a later version) as part of the resolution.</span></span>

<span data-ttu-id="6053c-120">Nous connaissons que les clients suivants ne peuvent pas utiliser TLS 1,2 :</span><span class="sxs-lookup"><span data-stu-id="6053c-120">We know that the following clients cannot use TLS 1.2:</span></span>

- <span data-ttu-id="6053c-121">Android 4.3 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6053c-121">Android 4.3 and earlier versions</span></span>
- <span data-ttu-id="6053c-122">Firefox 5.0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6053c-122">Firefox version 5.0 and earlier versions</span></span>
- <span data-ttu-id="6053c-123">Internet Explorer 8 à 10 sur Windows 7 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6053c-123">Internet Explorer 8–10 on Windows 7 and earlier versions</span></span>
- <span data-ttu-id="6053c-124">Internet Explorer 10 sur Windows Phone 8,0</span><span class="sxs-lookup"><span data-stu-id="6053c-124">Internet Explorer 10 on Windows Phone 8.0</span></span>
- <span data-ttu-id="6053c-125">Safari 6.0.4/OS X 10.8.4 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="6053c-125">Safari 6.0.4/OS X 10.8.4 and earlier versions</span></span>

<span data-ttu-id="6053c-126">Nous vous recommandons de mettre à jour vos clients afin de garantir un accès ininterrompu à Office 365 GCC High et DoD.</span><span class="sxs-lookup"><span data-stu-id="6053c-126">We recommend that you update your clients to make sure that you maintain uninterrupted access to Office 365 GCC High and DoD.</span></span>

<span data-ttu-id="6053c-127">Bien que l’analyse actuelle des connexions aux services Microsoft Online indique que la plupart des services et points de terminaison voient l’utilisation de TLS 1,1 et 1,0 très peu, nous fournissons un avis de cette modification afin que vous puissiez mettre à jour les clients ou serveurs concernés, le cas échéant, avant la prise en charge de TLS 1,1 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="6053c-127">Although current analysis of connections to Microsoft Online services shows that most services and endpoints see very little TLS 1.1 and 1.0 usage, we are providing notice of this change so that you can update any affected clients or servers as necessary before support for TLS 1.1 and 1.0 ends.</span></span> <span data-ttu-id="6053c-128">Si vous utilisez une infrastructure locale pour des scénarios hybrides ou AD FS (Active Directory Federation Services), assurez-vous que l’infrastructure peut prendre en charge à la fois les connexions entrantes et sortantes qui utilisent TLS 1,2 (ou une version ultérieure).</span><span class="sxs-lookup"><span data-stu-id="6053c-128">If you are using any on-premises infrastructure for hybrid scenarios or Active Directory Federation Services (AD FS), make sure that the infrastructure can support both inbound and outbound connections that use TLS 1.2 (or a later version).</span></span>

<span data-ttu-id="6053c-129">Outre les pannes que vous pouvez vous produire si vous utilisez les clients énumérés qui ne peuvent pas utiliser le protocole TLS 1,2, la suppression des protocoles TLS 1,1 et 1,0 vous empêchera d’utiliser le produit Microsoft suivant :</span><span class="sxs-lookup"><span data-stu-id="6053c-129">In addition to the outages that you might experience if you use the listed clients that cannot use TLS 1.2, removing TLS 1.1 and 1.0 will prevent you from being able to use the following Microsoft product:</span></span>

- <span data-ttu-id="6053c-130">Lync Phone</span><span class="sxs-lookup"><span data-stu-id="6053c-130">Lync phone</span></span>

## <a name="references"></a><span data-ttu-id="6053c-131">Références</span><span class="sxs-lookup"><span data-stu-id="6053c-131">References</span></span>

<span data-ttu-id="6053c-132">L’article suivant du support technique fournit des conseils et des références pour vous aider à vous assurer que vos clients utilisent TLS 1,2 :</span><span class="sxs-lookup"><span data-stu-id="6053c-132">The following support article describes guidance and references to help make sure that your clients are using TLS 1.2:</span></span>

[<span data-ttu-id="6053c-133">Préparation de l’utilisation obligatoire de TLS 1,2 dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6053c-133">Preparing for the mandatory use of TLS 1.2 in Office 365</span></span>](https://support.microsoft.com/help/4057306/preparing-for-tls-1-2-in-office-365)
