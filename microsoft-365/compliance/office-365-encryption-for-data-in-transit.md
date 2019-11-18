---
title: Chiffrement Office 365 pour les données en transit
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
ms.openlocfilehash: 571a0e28386539058a9998f703d7b4537e1a155a
ms.sourcegitcommit: 93cef4906c5495ae293450ceb52d6cc336f52b53
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/08/2019
ms.locfileid: "38690409"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="8e358-103">Chiffrement Office 365 pour les données en transit</span><span class="sxs-lookup"><span data-stu-id="8e358-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="8e358-104">En plus de protéger les données client au repos, Microsoft utilise des technologies de chiffrement pour protéger les données client Office 365 en transit.</span><span class="sxs-lookup"><span data-stu-id="8e358-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="8e358-105">Les données sont en transit :</span><span class="sxs-lookup"><span data-stu-id="8e358-105">Data is in transit:</span></span>

- <span data-ttu-id="8e358-106">Lorsqu’un ordinateur client communique avec un serveur Office 365 ;</span><span class="sxs-lookup"><span data-stu-id="8e358-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="8e358-107">Lorsqu’un serveur Office 365 communique avec un autre serveur Office 365 ; les</span><span class="sxs-lookup"><span data-stu-id="8e358-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="8e358-108">Lorsqu’un serveur Office 365 communique avec un serveur 365 non Office (par exemple, Exchange Online de remise de courrier électronique à un serveur de messagerie étranger).</span><span class="sxs-lookup"><span data-stu-id="8e358-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="8e358-109">Les communications entre les centres de contenu entre les serveurs Office 365 s’effectuent via TLS ou IPsec, et tous les serveurs de client négocient une session sécurisée à l’aide de TLS avec des machines client (par exemple, Exchange Online utilise TLS 1,2 avec une force de chiffrement de 256 bits est utilisée (FIPS). 140-2 niveau 2 validé).</span><span class="sxs-lookup"><span data-stu-id="8e358-109">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="8e358-110">(Consultez les [Détails de référence technique sur le chiffrement dans office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) pour obtenir une liste des suites de chiffrement TLS prises en charge par Office 365.) Cela s’applique aux protocoles utilisés par des clients tels qu’Outlook, Skype entreprise et Outlook sur le Web (par exemple, HTTP, POP3, etc.).</span><span class="sxs-lookup"><span data-stu-id="8e358-110">(See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="8e358-111">Les certificats publics sont émis par Microsoft IT SSL à l’aide de SSLAdmin, un outil Microsoft interne permettant de protéger la confidentialité des informations transmises.</span><span class="sxs-lookup"><span data-stu-id="8e358-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="8e358-112">Tous les certificats émis par le service informatique de Microsoft ont une longueur minimale de 2048 bits et la conformité WebTrust nécessite SSLAdmin pour s’assurer que les certificats sont émis uniquement vers des adresses IP publiques appartenant à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8e358-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="8e358-113">Toutes les adresses IP qui ne satisfont pas à ce critère sont routées via un processus d’exception.</span><span class="sxs-lookup"><span data-stu-id="8e358-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="8e358-114">Tous les détails de l’implémentation, tels que la version de TLS utilisée, si le protocole FS (Forward Secrecy) est activé, l’ordre des suites de chiffrement, etc., sont disponibles publiquement.</span><span class="sxs-lookup"><span data-stu-id="8e358-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="8e358-115">Pour voir ces informations, vous pouvez utiliser un site Web tiers, tel que les [ateliers de Qualys SSL](https://www.ssllabs.com).</span><span class="sxs-lookup"><span data-stu-id="8e358-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="8e358-116">Vous trouverez ci-dessous les liens vers les pages de test automatisées de Qualys qui affichent des informations sur les services suivants :</span><span class="sxs-lookup"><span data-stu-id="8e358-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="8e358-117">Portail Office 365</span><span class="sxs-lookup"><span data-stu-id="8e358-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="8e358-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="8e358-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="8e358-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="8e358-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="8e358-120">Skype entreprise (SIP)</span><span class="sxs-lookup"><span data-stu-id="8e358-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="8e358-121">Skype entreprise (Web)</span><span class="sxs-lookup"><span data-stu-id="8e358-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="8e358-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="8e358-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="8e358-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8e358-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="8e358-124">Pour Exchange Online Protection, les URL varient en fonction des noms de client ; Toutefois, tous les clients peuvent tester Office 365 à l’aide de **Microsoft-com.mail.protection.Outlook.com**.</span><span class="sxs-lookup"><span data-stu-id="8e358-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
