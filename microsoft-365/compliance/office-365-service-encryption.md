---
title: Chiffrement de service
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.date: 10/3/2019
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : Comprendre la résilience des données dans Microsoft Office 365.'
ms.openlocfilehash: 89f3fbcc90cee0ad822156014ee4ac9e04fe3371
ms.sourcegitcommit: 50f10d83fa21db8572adab90784146e5231e3321
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2021
ms.locfileid: "50058547"
---
# <a name="service-encryption"></a><span data-ttu-id="7d21f-103">Chiffrement de service</span><span class="sxs-lookup"><span data-stu-id="7d21f-103">Service Encryption</span></span>

<span data-ttu-id="7d21f-104">En plus d’utiliser le chiffrement au niveau du volume, Exchange Online, Microsoft Teams, SharePoint Online et OneDrive Entreprise utilisent également le chiffrement de service pour chiffrer les données client.</span><span class="sxs-lookup"><span data-stu-id="7d21f-104">In addition to using volume-level encryption, Exchange Online, Microsoft Teams, SharePoint Online, and OneDrive for Business also use Service Encryption to encrypt customer data.</span></span> <span data-ttu-id="7d21f-105">Le chiffrement de service offre deux options de gestion des clés :</span><span class="sxs-lookup"><span data-stu-id="7d21f-105">Service Encryption allows for two key management options:</span></span>

## <a name="microsoft-managed-keys"></a><span data-ttu-id="7d21f-106">Clés gérées par Microsoft</span><span class="sxs-lookup"><span data-stu-id="7d21f-106">Microsoft-managed keys</span></span>
<span data-ttu-id="7d21f-107">Microsoft gère toutes les clés de chiffrement, y compris les clés racines pour le chiffrement de service.</span><span class="sxs-lookup"><span data-stu-id="7d21f-107">Microsoft manages all cryptographic keys including the root keys for service encryption.</span></span> <span data-ttu-id="7d21f-108">Cette option est actuellement activée par défaut pour Exchange Online, SharePoint Online, OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="7d21f-108">This option is currently enabled by default for Exchange Online, SharePoint Online, OneDrive for Business.</span></span> <span data-ttu-id="7d21f-109">Les clés gérées par Microsoft fournissent le chiffrement de service par défaut, sauf si vous décidez d’intégrer à l’aide de la clé client.</span><span class="sxs-lookup"><span data-stu-id="7d21f-109">Microsoft-managed keys provide default service encryption unless you decide to onboard using Customer Key.</span></span> <span data-ttu-id="7d21f-110">Si, à une date ultérieure, vous décidez d’arrêter d’utiliser la clé client sans suivre le chemin de purge des données, vos données restent chiffrées à l’aide des clés gérées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d21f-110">If, at a later date, you decide to stop using Customer Key without following the data purge path, then your data stays encrypted using the Microsoft-managed keys.</span></span> <span data-ttu-id="7d21f-111">Vos données sont toujours chiffrées à ce niveau par défaut au minimum.</span><span class="sxs-lookup"><span data-stu-id="7d21f-111">Your data is always encrypted at this default level at a minimum.</span></span> 

## <a name="customer-key"></a><span data-ttu-id="7d21f-112">Clé client</span><span class="sxs-lookup"><span data-stu-id="7d21f-112">Customer Key</span></span>
<span data-ttu-id="7d21f-113">Vous fournissez les clés racine utilisées avec le chiffrement de service et vous les gérez à l’aide d’Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7d21f-113">You supply root keys used with service encryption and you manage these keys using Azure Key Vault.</span></span> <span data-ttu-id="7d21f-114">Microsoft gère toutes les autres clés.</span><span class="sxs-lookup"><span data-stu-id="7d21f-114">Microsoft manages all other keys.</span></span> <span data-ttu-id="7d21f-115">Cette option, appelée clé client, est actuellement disponible pour Exchange Online, SharePoint Online et OneDrive Entreprise.</span><span class="sxs-lookup"><span data-stu-id="7d21f-115">This option is called Customer Key, and it is currently available for Exchange Online, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="7d21f-116">(Précédemment appelé chiffrement avancé avec BYOK.</span><span class="sxs-lookup"><span data-stu-id="7d21f-116">(Previously referred to as Advanced Encryption with BYOK.</span></span> <span data-ttu-id="7d21f-117">Voir Amélioration de la transparence et du contrôle pour les clients [Office 365](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) pour l’annonce d’origine.)</span><span class="sxs-lookup"><span data-stu-id="7d21f-117">See [Enhancing transparency and control for Office 365 customers](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) for the original announcement.)</span></span>

<span data-ttu-id="7d21f-118">Le chiffrement de service offre plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="7d21f-118">Service encryption provides multiple benefits:</span></span>

- <span data-ttu-id="7d21f-119">Fournit une couche de protection supplémentaire sur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7d21f-119">Provides an added layer of protection on top of BitLocker.</span></span>

- <span data-ttu-id="7d21f-120">Permet de séparer les administrateurs du système d’exploitation Windows de l’accès aux données d’application stockées ou traitées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7d21f-120">Provides separation of Windows operating system administrators from access to application data stored or processed by the operating system.</span></span>

- <span data-ttu-id="7d21f-121">Inclut une option de clé client qui permet aux services multi-clients de fournir une gestion des clés par client.</span><span class="sxs-lookup"><span data-stu-id="7d21f-121">Includes a Customer Key option that enables multi-tenant services to provide per-tenant key management.</span></span>

- <span data-ttu-id="7d21f-122">Améliore la capacité de Microsoft 365 à répondre aux demandes des clients qui ont des exigences de conformité spécifiques en matière de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="7d21f-122">Enhances the ability of Microsoft 365 to meet the demands of customers that have specific compliance requirements regarding encryption.</span></span>

<span data-ttu-id="7d21f-123">À l’aide de la clé client, vous pouvez générer vos propres clés de chiffrement à l’aide d’un module de service matériel (HSM) local ou d’Azure Key Vault (AKV).</span><span class="sxs-lookup"><span data-stu-id="7d21f-123">Using Customer Key, you can generate your own cryptographic keys using either an on-premises Hardware Service Module (HSM) or Azure Key Vault (AKV).</span></span> <span data-ttu-id="7d21f-124">Quelle que soit la façon dont vous générez la clé, vous utilisez AKV pour contrôler et gérer les clés de chiffrement utilisées par Office 365.</span><span class="sxs-lookup"><span data-stu-id="7d21f-124">Regardless of how you generate the key, you use AKV to control and manage the cryptographic keys used by Office 365.</span></span> <span data-ttu-id="7d21f-125">Une fois que vos clés sont stockées dans AKV, elles peuvent être utilisées comme racine de l’un des chaînes de clés qui chiffre les données ou fichiers de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7d21f-125">Once your keys are stored in AKV, they can be used as the root of one of the keychains that encrypts your mailbox data or files.</span></span>

<span data-ttu-id="7d21f-126">Un autre avantage de la clé client est le contrôle que vous avez sur la capacité de Microsoft à traiter vos données.</span><span class="sxs-lookup"><span data-stu-id="7d21f-126">Another benefit of Customer Key is the control you have over the ability of Microsoft to process your data.</span></span> <span data-ttu-id="7d21f-127">Si vous souhaitez supprimer des données d’Office 365, par exemple si vous souhaitez mettre fin au service avec Microsoft ou supprimer une partie de vos données stockées dans le cloud, vous pouvez le faire et utiliser la clé client comme contrôle technique.</span><span class="sxs-lookup"><span data-stu-id="7d21f-127">If you want to remove data from Office 365, such as if you want to terminate service with Microsoft or remove a portion of your data stored in the cloud, you can do so and use Customer Key as a technical control.</span></span> <span data-ttu-id="7d21f-128">La suppression de données garantit que personne, y compris Microsoft, ne peut accéder aux données ni les traiter.</span><span class="sxs-lookup"><span data-stu-id="7d21f-128">Removing data ensures that no one, including Microsoft, can access or process the data.</span></span> <span data-ttu-id="7d21f-129">La clé client est en plus et complète du Customer Lockbox que vous utilisez pour contrôler l’accès à vos données par le personnel Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7d21f-129">Customer Key is in addition and complementary to Customer Lockbox that you use to control access to your data by Microsoft personnel.</span></span>

<span data-ttu-id="7d21f-130">Pour découvrir comment configurer la clé client pour Microsoft 365 pour Exchange Online, Microsoft Teams, SharePoint Online, y compris les sites d’équipe et OneDrive Entreprise, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="7d21f-130">To learn how to set up Customer Key for Microsoft 365 for Exchange Online, Microsoft Teams, SharePoint Online, including Team Sites, and OneDrive for Business, see these articles:</span></span>

- [<span data-ttu-id="7d21f-131">Chiffrement du service avec la clé client</span><span class="sxs-lookup"><span data-stu-id="7d21f-131">Service encryption with Customer Key</span></span>](customer-key-overview.md)

- [<span data-ttu-id="7d21f-132">Configurer la clé client</span><span class="sxs-lookup"><span data-stu-id="7d21f-132">Set up Customer Key</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="7d21f-133">Gérer la clé client</span><span class="sxs-lookup"><span data-stu-id="7d21f-133">Manage Customer Key</span></span>](customer-key-manage.md)

- [<span data-ttu-id="7d21f-134">Faire pivoter ou faire pivoter une clé client ou une clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="7d21f-134">Roll or rotate a customer key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="7d21f-135">Comprendre la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="7d21f-135">Understand the availability key</span></span>](customer-key-availability-key-understand.md)
