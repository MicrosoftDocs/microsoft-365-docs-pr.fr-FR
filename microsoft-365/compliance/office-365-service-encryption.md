---
title: Chiffrement du service Office 365
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
ms.openlocfilehash: ec7f794a62a910fadaece890cf73451644d44109
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42071111"
---
# <a name="office-365-service-encryption"></a><span data-ttu-id="13695-103">Chiffrement du service Office 365</span><span class="sxs-lookup"><span data-stu-id="13695-103">Office 365 Service Encryption</span></span>

<span data-ttu-id="13695-104">En plus de l’utilisation du chiffrement au niveau du volume, Exchange Online, Skype entreprise, SharePoint Online et OneDrive entreprise utilisent également le chiffrement de service pour chiffrer les données client.</span><span class="sxs-lookup"><span data-stu-id="13695-104">In addition to using volume-level encryption, Exchange Online, Skype for Business, SharePoint Online, and OneDrive for Business also use Service Encryption to encrypt customer data.</span></span> <span data-ttu-id="13695-105">Le chiffrement de service autorise deux options de gestion clés :</span><span class="sxs-lookup"><span data-stu-id="13695-105">Service Encryption allows for two key management options:</span></span>

- <span data-ttu-id="13695-106">Microsoft gère toutes les clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="13695-106">Microsoft manages all cryptographic keys.</span></span> <span data-ttu-id="13695-107">(Cette option est actuellement disponible dans SharePoint Online, OneDrive entreprise et Skype entreprise.)</span><span class="sxs-lookup"><span data-stu-id="13695-107">(This option is currently available in SharePoint Online, OneDrive for Business, and Skype for Business.)</span></span>

- <span data-ttu-id="13695-108">Le client fournit des clés racines utilisées avec le chiffrement de service et le client gère ces clés à l’aide d’Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="13695-108">The customer supplies root keys used with service encryption and the customer manages these keys using Azure Key Vault.</span></span> <span data-ttu-id="13695-109">Microsoft gère toutes les autres clés.</span><span class="sxs-lookup"><span data-stu-id="13695-109">Microsoft manages all other keys.</span></span> <span data-ttu-id="13695-110">Cette option est appelée clé client et elle est actuellement disponible pour Exchange Online, SharePoint Online et OneDrive entreprise.</span><span class="sxs-lookup"><span data-stu-id="13695-110">This option is called Customer Key, and it is currently available for Exchange Online, SharePoint Online, and OneDrive for Business.</span></span> <span data-ttu-id="13695-111">(Précédemment appelé chiffrement avancé avec BYOK.</span><span class="sxs-lookup"><span data-stu-id="13695-111">(Previously referred to as Advanced Encryption with BYOK.</span></span> <span data-ttu-id="13695-112">Consultez la rubrique amélioration de la [transparence et du contrôle pour les clients Office 365](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) pour l’annonce d’origine.)</span><span class="sxs-lookup"><span data-stu-id="13695-112">See [Enhancing transparency and control for Office 365 customers](https://blogs.office.com/2015/04/21/enhancing-transparency-and-control-for-office-365-customers/) for the original announcement.)</span></span>

<span data-ttu-id="13695-113">Le chiffrement de service offre plusieurs avantages.</span><span class="sxs-lookup"><span data-stu-id="13695-113">Service encryption provides multiple benefits.</span></span> <span data-ttu-id="13695-114">Par exemple, clé client :</span><span class="sxs-lookup"><span data-stu-id="13695-114">For example, Customer Key:</span></span>

- <span data-ttu-id="13695-115">Fournit des fonctionnalités de protection et de gestion des droits en plus de la protection de chiffrement élevée.</span><span class="sxs-lookup"><span data-stu-id="13695-115">Provides rights protection and management features on top of strong encryption protection.</span></span>

- <span data-ttu-id="13695-116">Inclut une option de clé de client qui permet aux services mutualisés de fournir une gestion des clés par client.</span><span class="sxs-lookup"><span data-stu-id="13695-116">Includes a Customer Key option that enables multi-tenant services to provide per-tenant key management.</span></span>

- <span data-ttu-id="13695-117">Permet de séparer les administrateurs du système d’exploitation Windows de l’accès aux données client stockées ou traitées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="13695-117">Provides separation of Windows operating system administrators from access to customer data stored or processed by the operating system.</span></span>

- <span data-ttu-id="13695-118">Améliore la capacité d’Office 365 à répondre aux exigences des clients qui ont des exigences de conformité concernant le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="13695-118">Enhances the ability of Office 365 to meet the demands of customers that have compliance requirements regarding encryption.</span></span>

## <a name="customer-key"></a><span data-ttu-id="13695-119">Clé client</span><span class="sxs-lookup"><span data-stu-id="13695-119">Customer Key</span></span>

<span data-ttu-id="13695-120">À l’aide de la clé client, vous pouvez générer vos propres clés de chiffrement à l’aide d’un module de service matériel (HSM) local ou d’un coffre-fort de clés Azure (AKV).</span><span class="sxs-lookup"><span data-stu-id="13695-120">Using Customer Key, you can generate your own cryptographic keys using either an on-premises Hardware Service Module (HSM) or Azure Key Vault (AKV).</span></span> <span data-ttu-id="13695-121">Quelle que soit la façon dont vous générez la clé, vous utilisez AKV pour contrôler et gérer les clés de chiffrement utilisées par Office 365.</span><span class="sxs-lookup"><span data-stu-id="13695-121">Regardless of how you generate the key, you use AKV to control and manage the cryptographic keys used by Office 365.</span></span> <span data-ttu-id="13695-122">Une fois que vos clés sont stockées dans AKV, elles peuvent être utilisées comme racine de l’une des clés qui chiffre les données ou les fichiers de votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="13695-122">Once your keys are stored in AKV, they can be used as the root of one of the keychains that encrypts your mailbox data or files.</span></span>

<span data-ttu-id="13695-123">Un autre avantage de la clé client est le contrôle dont vous disposez sur la capacité de Microsoft à traiter vos données.</span><span class="sxs-lookup"><span data-stu-id="13695-123">Another benefit of Customer Key is the control you have over the ability of Microsoft to process your data.</span></span> <span data-ttu-id="13695-124">Si vous souhaitez supprimer des données d’Office 365, par exemple si vous souhaitez terminer le service auprès de Microsoft ou supprimer une partie de vos données stockées dans le Cloud, vous pouvez le faire et utiliser la clé client comme un contrôle technique.</span><span class="sxs-lookup"><span data-stu-id="13695-124">If you want to remove data from Office 365, such as if you want to terminate service with Microsoft or remove a portion of your data stored in the cloud, you can do so and use Customer Key as a technical control.</span></span> <span data-ttu-id="13695-125">Cela permet de s’assurer que personne, y compris Microsoft, ne peut accéder aux données ou les traiter.</span><span class="sxs-lookup"><span data-stu-id="13695-125">This ensures that no one, including Microsoft, can access or process the data.</span></span> <span data-ttu-id="13695-126">La clé client est en outre et complémentaire du référentiel sécurisé du client que vous utilisez pour contrôler l’accès à vos données par le personnel de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13695-126">Customer Key is in addition and complementary to Customer Lockbox that you use to control access to your data by Microsoft personnel.</span></span>

<span data-ttu-id="13695-127">Pour en savoir plus sur la configuration de la clé client pour Office 365 pour Exchange Online, Skype entreprise, SharePoint Online, y compris les sites d’équipe et OneDrive entreprise, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="13695-127">To learn how to set up Customer Key for Office 365 for Exchange Online, Skype for Business, SharePoint Online, including Team Sites, and OneDrive for Business, see these articles:</span></span>

- [<span data-ttu-id="13695-128">Chiffrement de service avec clé client dans Office 365</span><span class="sxs-lookup"><span data-stu-id="13695-128">Service encryption with Customer Key in Office 365</span></span>](customer-key-overview.md)

- [<span data-ttu-id="13695-129">Configurer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="13695-129">Set up Customer Key for Office 365</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="13695-130">Gérer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="13695-130">Manage Customer Key for Office 365</span></span>](customer-key-manage.md)

- [<span data-ttu-id="13695-131">Faire pivoter ou faire pivoter une clé client ou une clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="13695-131">Roll or rotate a customer key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="13695-132">Comprendre la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="13695-132">Understand the availability key</span></span>](customer-key-availability-key-understand.md)
 
