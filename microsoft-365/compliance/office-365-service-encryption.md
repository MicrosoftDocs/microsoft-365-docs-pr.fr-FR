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
ms.date: 4/8/2020
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Résumé : comprendre le chiffrement des données au niveau de la couche de service dans Microsoft Office 365.'
ms.openlocfilehash: a8faded033ade013924eeeab269aa213840430b4
ms.sourcegitcommit: 13f28aa762e467bab8ab1e95e1917b3ac28931da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2020
ms.locfileid: "43193460"
---
# <a name="office-365-service-encryption"></a><span data-ttu-id="26863-103">Chiffrement du service Office 365</span><span class="sxs-lookup"><span data-stu-id="26863-103">Office 365 Service Encryption</span></span>

<span data-ttu-id="26863-104">En plus de l’utilisation de BitLocker pour le chiffrement au niveau du volume, Exchange Online, Skype entreprise, SharePoint Online, OneDrive entreprise et teams utilisent également le chiffrement de service pour chiffrer les données client.</span><span class="sxs-lookup"><span data-stu-id="26863-104">In addition to using BitLocker for volume-level encryption, Exchange Online, Skype for Business, SharePoint Online, OneDrive for Business, and Teams also use Service Encryption to encrypt customer data.</span></span> <span data-ttu-id="26863-105">Le chiffrement de service autorise deux options de gestion clés :</span><span class="sxs-lookup"><span data-stu-id="26863-105">Service Encryption allows for two key management options:</span></span>

- <span data-ttu-id="26863-106">Microsoft gère toutes les clés de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="26863-106">Microsoft manages all cryptographic keys.</span></span> <span data-ttu-id="26863-107">Cette option est actuellement disponible dans les conversations SharePoint Online, OneDrive entreprise, Skype entreprise et Teams.</span><span class="sxs-lookup"><span data-stu-id="26863-107">This option is currently available in SharePoint Online, OneDrive for Business, Skype for Business, and Teams chats.</span></span> <span data-ttu-id="26863-108">Vos données sont chiffrées par défaut à l’aide de clés gérées Microsoft.</span><span class="sxs-lookup"><span data-stu-id="26863-108">Your data is encrypted by default with Microsoft managed keys.</span></span>

- <span data-ttu-id="26863-109">Votre organisation fournit les clés racines.</span><span class="sxs-lookup"><span data-stu-id="26863-109">Your organization supplies the root keys.</span></span> <span data-ttu-id="26863-110">Vous gérez ces clés à l’aide du coffre de clés Azure.</span><span class="sxs-lookup"><span data-stu-id="26863-110">You manage these keys using Azure Key Vault.</span></span> <span data-ttu-id="26863-111">Cette option est appelée clé client.</span><span class="sxs-lookup"><span data-stu-id="26863-111">This option is called Customer Key.</span></span> <span data-ttu-id="26863-112">La clé client est actuellement disponible pour les fichiers Exchange Online, SharePoint Online, OneDrive entreprise, Skype entreprise et Teams.</span><span class="sxs-lookup"><span data-stu-id="26863-112">Customer Key is currently available for Exchange Online, SharePoint Online, OneDrive for Business, Skype for Business, and Teams files.</span></span> <span data-ttu-id="26863-113">Si vous utilisez la clé client, ces clés remplacent les clés gérées Microsoft pour chiffrer vos données.</span><span class="sxs-lookup"><span data-stu-id="26863-113">If you use Customer Key, these keys replace Microsoft managed keys to encrypt your data.</span></span>

<span data-ttu-id="26863-114">Quelle que soit l’option choisie, le chiffrement de service offre plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="26863-114">Regardless of the option you choose, service encryption provides multiple benefits:</span></span>

- <span data-ttu-id="26863-115">Applique l’authentification de l’utilisateur pour récupérer et déchiffrer les données demandées par un utilisateur autorisé.</span><span class="sxs-lookup"><span data-stu-id="26863-115">Enforces user authentication to retrieve and decrypt data requested by an authorized user.</span></span>

- <span data-ttu-id="26863-116">Permet de séparer les administrateurs du système d’exploitation Windows de l’accès aux données client stockées ou traitées par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="26863-116">Provides separation of Windows operating system administrators from access to customer data stored or processed by the operating system.</span></span>

- <span data-ttu-id="26863-117">Améliore la capacité d’Office 365 à répondre aux exigences des clients qui ont des exigences de conformité concernant le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="26863-117">Enhances the ability of Office 365 to meet the demands of customers that have compliance requirements regarding encryption.</span></span>

<span data-ttu-id="26863-118">Pour en savoir plus sur la configuration de la clé client pour Office 365 pour Exchange Online, Skype entreprise, SharePoint Online, OneDrive entreprise et les fichiers Teams, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="26863-118">To learn how to set up Customer Key for Office 365 for Exchange Online, Skype for Business, SharePoint Online, OneDrive for Business, and Teams files, see these articles:</span></span>

- [<span data-ttu-id="26863-119">Chiffrement de service avec clé client dans Office 365</span><span class="sxs-lookup"><span data-stu-id="26863-119">Service encryption with Customer Key in Office 365</span></span>](customer-key-overview.md)

- [<span data-ttu-id="26863-120">Configurer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="26863-120">Set up Customer Key for Office 365</span></span>](customer-key-set-up.md)

- [<span data-ttu-id="26863-121">Gérer la clé client pour Office 365</span><span class="sxs-lookup"><span data-stu-id="26863-121">Manage Customer Key for Office 365</span></span>](customer-key-manage.md)

- [<span data-ttu-id="26863-122">Faire pivoter ou faire pivoter une clé client ou une clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="26863-122">Roll or rotate a customer key or an availability key</span></span>](customer-key-availability-key-roll.md)

- [<span data-ttu-id="26863-123">Comprendre la clé de disponibilité</span><span class="sxs-lookup"><span data-stu-id="26863-123">Understand the availability key</span></span>](customer-key-availability-key-understand.md)
