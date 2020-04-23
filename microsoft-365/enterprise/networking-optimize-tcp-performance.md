---
title: 'Étape 5 : Optimiser les performances du service Microsoft 365 et du client'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Configurez les paramètres TCP et les services Microsoft 365 pour de meilleures performances.
ms.openlocfilehash: 2db35f67ff19998b8a70742ec8fa24cb8d517c5d
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631464"
---
# <a name="step-5-optimize-client-and-microsoft-365-service-performance"></a><span data-ttu-id="3ab81-103">Étape 5 : Optimiser les performances du service Microsoft 365 et du client</span><span class="sxs-lookup"><span data-stu-id="3ab81-103">Step 5: Optimize client and Microsoft 365 service performance</span></span>

<span data-ttu-id="3ab81-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="3ab81-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 1 : Réseau](../media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="3ab81-106">Vous pouvez accroître les performances en ajustant la façon dont le protocole TCP fonctionne entre les appareils clients et les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3ab81-106">You can increase performance by fine tuning the way that the Transmission Control Protocol (TCP) works between client devices and Microsoft 365 services.</span></span>

<span data-ttu-id="3ab81-107">Pour les appareils clients, vous pouvez modifier les paramètres TCP suivants sur des appareils clients afin d’optimiser les performances TCP :</span><span class="sxs-lookup"><span data-stu-id="3ab81-107">For client devices, you can change the following TCP settings on client devices to optimize TCP performance:</span></span>

- <span data-ttu-id="3ab81-108">[Mise à l’échelle des fenêtres TCP](https://blogs.technet.microsoft.com/onthewire/2014/03/28/ensuring-your-office-365-network-connection-isnt-throttled-by-your-proxy/), pour que votre appareil client puisse envoyer plus de données avant d’exiger un accusé de réception</span><span class="sxs-lookup"><span data-stu-id="3ab81-108">[TCP window scaling](https://blogs.technet.microsoft.com/onthewire/2014/03/28/ensuring-your-office-365-network-connection-isnt-throttled-by-your-proxy/), so your client device can send more data before requiring an acknowledgement</span></span>
- <span data-ttu-id="3ab81-109">[Durée d’inactivité TCP](https://blogs.technet.microsoft.com/onthewire/2014/03/04/network-perimeters-tcp-idle-session-settings-for-outlook-on-office-365/), pour que votre appareil client puisse gérer les connexions ouvertes plus efficacement</span><span class="sxs-lookup"><span data-stu-id="3ab81-109">[TCP idle time](https://blogs.technet.microsoft.com/onthewire/2014/03/04/network-perimeters-tcp-idle-session-settings-for-outlook-on-office-365/), so your client device can handle open connections more efficiently</span></span>
- <span data-ttu-id="3ab81-110">[Taille maximale de segment TCP](https://blogs.technet.microsoft.com/onthewire/2014/06/27/checking-your-tcp-packets-are-pulling-their-weight-tcp-max-segment-size-or-mss/), pour que votre appareil client puisse envoyer les blocs de données les plus volumineux dans un paquet</span><span class="sxs-lookup"><span data-stu-id="3ab81-110">[TCP maximum segment size](https://blogs.technet.microsoft.com/onthewire/2014/06/27/checking-your-tcp-packets-are-pulling-their-weight-tcp-max-segment-size-or-mss/), so your client device can send the largest blocks of data in a packet</span></span>
- <span data-ttu-id="3ab81-111">[Accusés de réception sélectifs TCP](https://blogs.technet.microsoft.com/onthewire/2014/06/27/ensuring-your-tcp-stack-isnt-throwing-data-away/), pour que votre appareil client puisse accuser reçu des données plus efficacement</span><span class="sxs-lookup"><span data-stu-id="3ab81-111">[TCP selective acknowledgements](https://blogs.technet.microsoft.com/onthewire/2014/06/27/ensuring-your-tcp-stack-isnt-throwing-data-away/), so your client device can acknowledge received data more efficiently</span></span>

<span data-ttu-id="3ab81-112">Pour les services Microsoft 365, consultez ces ressources supplémentaires pour optimiser les performances :</span><span class="sxs-lookup"><span data-stu-id="3ab81-112">For Microsoft 365 services, see these additional resources to optimize performance:</span></span>

- [<span data-ttu-id="3ab81-113">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3ab81-113">Exchange Online</span></span>](https://docs.microsoft.com/office365/enterprise/tune-exchange-online-performance)
- [<span data-ttu-id="3ab81-114">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="3ab81-114">Skype for Business Online</span></span>](https://docs.microsoft.com/office365/enterprise/tune-skype-for-business-online-performance)
- [<span data-ttu-id="3ab81-115">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="3ab81-115">SharePoint Online</span></span>](https://docs.microsoft.com/office365/enterprise/tune-sharepoint-online-performance)
- [<span data-ttu-id="3ab81-116">Project Web App dans Project Online</span><span class="sxs-lookup"><span data-stu-id="3ab81-116">Project Web App in Project Online</span></span>](https://docs.microsoft.com/ProjectOnline/tune-project-online-performance)

<span data-ttu-id="3ab81-117">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step5) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="3ab81-117">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step5) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="3ab81-118">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3ab81-118">Next step</span></span>

[<span data-ttu-id="3ab81-119">Critères de sortie de l’infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="3ab81-119">Networking infrastructure exit criteria</span></span>](networking-exit-criteria.md)
