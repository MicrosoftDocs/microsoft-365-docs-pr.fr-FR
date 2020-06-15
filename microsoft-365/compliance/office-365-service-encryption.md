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
description: 'Résumé : comprendre la résilience des données dans Microsoft Office 365.'
ms.openlocfilehash: e69d35f08070e1fe092ca8a9b4aef6d179711121
ms.sourcegitcommit: f80c6c52e5b08290f74baec1d64c4070046c32e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "44717345"
---
# <a name="service-encryption"></a><span data-ttu-id="ae9f1-103">Chiffrement de service</span><span class="sxs-lookup"><span data-stu-id="ae9f1-103">Service Encryption</span></span>

<span data-ttu-id="ae9f1-104">En plus de l’utilisation du chiffrement au niveau du volume, Exchange Online, Skype entreprise, SharePoint Online et OneDrive entreprise utilisent également le chiffrement de service pour chiffrer les données client.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-104">In addition to using volume-level encryption, Exchange Online, Skype for Business, SharePoint Online, and OneDrive for Business also use Service Encryption to encrypt customer data.</span></span> <span data-ttu-id="ae9f1-105">Le chiffrement de service autorise deux options de gestion clés :</span><span class="sxs-lookup"><span data-stu-id="ae9f1-105">Service Encryption allows for two key management options:</span></span>

## <a name="microsoft-managed-keys"></a><span data-ttu-id="ae9f1-106">Clés gérées Microsoft :</span><span class="sxs-lookup"><span data-stu-id="ae9f1-106">Microsoft managed keys:</span></span> 
<span data-ttu-id="ae9f1-107">Microsoft gère toutes les clés de chiffrement, y compris les clés racines pour le chiffrement de service.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-107">Microsoft manages all cryptographic keys including the root keys for service encryption.</span></span> <span data-ttu-id="ae9f1-108">Cette option est actuellement disponible dans SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-108">This option is currently available in SharePoint Online and OneDrive for Business.</span></span> <span data-ttu-id="ae9f1-109">Cette option est actuellement déployée pour Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-109">This option is currently being rolled out for Exchange Online.</span></span> <span data-ttu-id="ae9f1-110">Les clés gérées Microsoft fournissent le chiffrement de service par défaut, sauf si vous décidez d’utiliser la clé client.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-110">Microsoft managed keys provide default service encryption unless you decide to onboard using Customer Key.</span></span> <span data-ttu-id="ae9f1-111">Si, par la suite, vous décidez de cesser d’utiliser la clé client sans suivre le chemin de purge des données, vos données resteront chiffrées à l’aide des clés gérées Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-111">If, at a later date, you decide to stop using Customer Key without following the data purge path, then your data stays encrypted using the Microsoft managed keys.</span></span> <span data-ttu-id="ae9f1-112">Vos données sont toujours chiffrées à ce niveau par défaut au minimum.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-112">Your data is always encrypted at this default level at a minimum.</span></span> 

## <a name="customer-key"></a><span data-ttu-id="ae9f1-113">Clé client :</span><span class="sxs-lookup"><span data-stu-id="ae9f1-113">Customer Key:</span></span> 
<span data-ttu-id="ae9f1-114">Vous fournissez des clés racines utilisées avec le chiffrement de service et vous gérez ces clés à l’aide du coffre de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-114">You supply root keys used with service encryption and you manage these keys using Azure Key Vault.</span></span> <span data-ttu-id="ae9f1-115">Microsoft gère toutes les autres clés.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-115">Microsoft manages all other keys.</span></span> <span data-ttu-id="ae9f1-116">Cette option est appelée clé client et elle est actuellement disponible pour Exchange Online, SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-116">This option is called Customer Key, and it is currently available for Exchange Online, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="ae9f1-117">(Précédemment appelé chiffrement avancé avec BYOK.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-117">(Previously referred to as Advanced Encryption with BYOK.</span></span> <span data-ttu-id="ae9f1-118">Consultez la rubrique amélioration de la [transparence et du contrôle pour les clients Office 365](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) pour l’annonce d’origine.)</span><span class="sxs-lookup"><span data-stu-id="ae9f1-118">See [Enhancing transparency and control for Office 365 customers](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) for the original announcement.)</span></span>

<span data-ttu-id="ae9f1-119">Le chiffrement de service offre plusieurs avantages.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-119">Service encryption provides multiple benefits.</span></span> <span data-ttu-id="ae9f1-120">Par exemple, clé client :</span><span class="sxs-lookup"><span data-stu-id="ae9f1-120">For example, Customer Key:</span></span>

- <span data-ttu-id="ae9f1-121">Fournit des fonctionnalités de protection et de gestion des droits en plus de la protection de chiffrement élevée.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-121">Provides rights protection and management features on top of strong encryption protection.</span></span>

- <span data-ttu-id="ae9f1-122">Inclut une option de clé de client qui permet aux services mutualisés de fournir une gestion des clés par client.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-122">Includes a Customer Key option that enables multi-tenant services to provide per-tenant key management.</span></span>

- <span data-ttu-id="ae9f1-123">Permet de séparer les administrateurs du système d’exploitation Windows de l’accès aux données client stockées ou traitées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-123">Provides separation of Windows operating system administrators from access to customer data stored or processed by the operating system.</span></span>

- <span data-ttu-id="ae9f1-124">Améliore la capacité de Microsoft 365 à répondre aux exigences des clients qui ont des exigences de conformité concernant le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-124">Enhances the ability of Microsoft 365 to meet the demands of customers that have compliance requirements regarding encryption.</span></span>

<span data-ttu-id="ae9f1-125">À l’aide de la clé client, vous pouvez générer vos propres clés de chiffrement à l’aide d’un module de service matériel (HSM) local ou d’un coffre-fort de clés Azure (AKV).</span><span class="sxs-lookup"><span data-stu-id="ae9f1-125">Using Customer Key, you can generate your own cryptographic keys using either an on-premises Hardware Service Module (HSM) or Azure Key Vault (AKV).</span></span> <span data-ttu-id="ae9f1-126">Quelle que soit la façon dont vous générez la clé, vous utilisez AKV pour contrôler et gérer les clés de chiffrement utilisées par Office 365.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-126">Regardless of how you generate the key, you use AKV to control and manage the cryptographic keys used by Office 365.</span></span> <span data-ttu-id="ae9f1-127">Une fois que vos clés sont stockées dans AKV, elles peuvent être utilisées comme racine de l’une des clés qui chiffre les données ou les fichiers de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-127">Once your keys are stored in AKV, they can be used as the root of one of the keychains that encrypts your mailbox data or files.</span></span>

<span data-ttu-id="ae9f1-128">Un autre avantage de la clé client est le contrôle dont vous disposez sur la capacité de Microsoft à traiter vos données.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-128">Another benefit of Customer Key is the control you have over the ability of Microsoft to process your data.</span></span> <span data-ttu-id="ae9f1-129">Si vous souhaitez supprimer des données d’Office 365, par exemple si vous souhaitez terminer le service auprès de Microsoft ou supprimer une partie de vos données stockées dans le Cloud, vous pouvez le faire et utiliser la clé client comme un contrôle technique.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-129">If you want to remove data from Office 365, such as if you want to terminate service with Microsoft or remove a portion of your data stored in the cloud, you can do so and use Customer Key as a technical control.</span></span> <span data-ttu-id="ae9f1-130">Cela permet de s’assurer que personne, y compris Microsoft, ne peut accéder aux données ou les traiter.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-130">This ensures that no one, including Microsoft, can access or process the data.</span></span> <span data-ttu-id="ae9f1-131">La clé client est en outre et complémentaire du référentiel sécurisé du client que vous utilisez pour contrôler l’accès à vos données par le personnel de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ae9f1-131">Customer Key is in addition and complementary to Customer Lockbox that you use to control access to your data by Microsoft personnel.</span></span>

<span data-ttu-id="ae9f1-132">Pour en savoir plus sur la configuration de la clé client pour Microsoft 365 pour Exchange Online, Skype entreprise, SharePoint Online, y compris les sites d’équipe et OneDrive entreprise, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="ae9f1-132">To learn how to set up Customer Key for Microsoft 365 for Exchange Online, Skype for Business, SharePoint Online, including Team Sites, and OneDrive for Business, see these articles:</span></span>

- [<span data-ttu-id="ae9f1-133">Chiffrement de service avec clé client</span><span class="sxs-lookup"><span data-stu-id="ae9f1-133">Service encryption with Customer Key</span></span>](customer-key-overview.md)

- [<span data-ttu-id="ae9f1-134">Configurer la clé client</span><span class="sxs-lookup"><span data-stu-id="ae9f1-134">Set up Customer Key</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="ae9f1-135">Gérer la clé client</span><span class="sxs-lookup"><span data-stu-id="ae9f1-135">Manage Customer Key</span></span>](customer-key-manage.md)

- [<span data-ttu-id="ae9f1-136">Faire pivoter ou faire pivoter une clé client ou une clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="ae9f1-136">Roll or rotate a customer key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="ae9f1-137">Comprendre la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="ae9f1-137">Understand the availability key</span></span>](customer-key-availability-key-understand.md)

