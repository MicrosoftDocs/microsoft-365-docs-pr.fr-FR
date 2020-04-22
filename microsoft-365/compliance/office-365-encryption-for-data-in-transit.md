---
title: Chiffrement des données en transit
f1.keywords:
- NOCSH
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Résumé : explique brièvement comment Microsoft chiffre les données en transit.'
ms.openlocfilehash: 0775d28a96f271a24406fd68c2ccb9fe4954e66d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43637330"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="a5a9f-103">Chiffrement des données en transit</span><span class="sxs-lookup"><span data-stu-id="a5a9f-103">Encryption for data in transit</span></span>

<span data-ttu-id="a5a9f-104">En plus de protéger les données client au repos, Microsoft utilise des technologies de chiffrement pour protéger les données client en transit.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> 

<span data-ttu-id="a5a9f-105">Les données sont en transit :</span><span class="sxs-lookup"><span data-stu-id="a5a9f-105">Data is in transit:</span></span>

- <span data-ttu-id="a5a9f-106">Lorsqu’un ordinateur client communique avec un serveur Microsoft ;</span><span class="sxs-lookup"><span data-stu-id="a5a9f-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="a5a9f-107">Lorsqu’un serveur Microsoft communique avec un autre serveur Microsoft ; les</span><span class="sxs-lookup"><span data-stu-id="a5a9f-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="a5a9f-108">Lorsqu’un serveur Microsoft communique avec un serveur non-Microsoft (par exemple, Exchange Online de remise de courrier électronique à un serveur de messagerie étranger).</span><span class="sxs-lookup"><span data-stu-id="a5a9f-108">when a Microsoft server communicates with a non-Microsoft server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="a5a9f-109">Les communications entre les centres de contenu entre les serveurs Microsoft sont effectuées via TLS ou IPsec, et tous les serveurs de client négocient une session sécurisée à l’aide de TLS avec des machines client (par exemple, Exchange Online utilise TLS 1,2 avec la force de chiffrement 256 bits est utilisée (FIPS 140-2 niveau 2-validé).</span><span class="sxs-lookup"><span data-stu-id="a5a9f-109">Inter-datacenter communications between Microsoft servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="a5a9f-110">(Consultez les [Détails de référence technique sur le chiffrement dans office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) pour obtenir une liste des suites de chiffrement TLS prises en charge par Office 365.) Cela s’applique aux protocoles utilisés par des clients tels qu’Outlook, Skype entreprise et Outlook sur le Web (par exemple, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="a5a9f-110">(See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="a5a9f-111">Les certificats publics sont émis par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne permettant de protéger la confidentialité des informations transmises.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="a5a9f-112">Tous les certificats émis par le service informatique de Microsoft ont une longueur minimale de 2048 bits et la conformité WebTrust nécessite SSLAdmin pour s’assurer que les certificats sont émis uniquement vers des adresses IP publiques appartenant à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="a5a9f-113">Toutes les adresses IP qui ne satisfont pas à ce critère sont routées via un processus d’exception.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="a5a9f-114">Tous les détails de l’implémentation, tels que la version de TLS utilisée, si le protocole FS (Forward Secrecy) est activé, l’ordre des suites de chiffrement, etc., sont disponibles publiquement.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="a5a9f-115">Pour voir ces informations, vous pouvez utiliser un site Web tiers, tel que les [ateliers de Qualys SSL](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="a5a9f-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="a5a9f-116">Vous trouverez ci-dessous les liens vers les pages de test automatisées de Qualys qui affichent des informations sur les services suivants :</span><span class="sxs-lookup"><span data-stu-id="a5a9f-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="a5a9f-117">Portail Office 365</span><span class="sxs-lookup"><span data-stu-id="a5a9f-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="a5a9f-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="a5a9f-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="a5a9f-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="a5a9f-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="a5a9f-120">Skype entreprise (SIP)</span><span class="sxs-lookup"><span data-stu-id="a5a9f-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="a5a9f-121">Skype entreprise (Web)</span><span class="sxs-lookup"><span data-stu-id="a5a9f-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="a5a9f-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="a5a9f-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="a5a9f-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a5a9f-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="a5a9f-124">Pour Exchange Online Protection, les URL varient en fonction des noms de client ; Toutefois, tous les clients peuvent tester Microsoft 365 à l’aide de **Microsoft-com.mail.protection.Outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="a5a9f-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
