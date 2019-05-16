---
title: 'Étape 5 : Optimiser les performances du service Office 365 et du client'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/13/2018
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Configurez les paramètres TCP et les services Office 365 pour de meilleures performances.
ms.openlocfilehash: 9e786b36d7a2afccc3b9112b815cd42a40317c15
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34073184"
---
# <a name="step-5-optimize-client-and-office-365-service-performance"></a><span data-ttu-id="2f0ad-103">Étape 5 : Optimiser les performances du service Office 365 et du client</span><span class="sxs-lookup"><span data-stu-id="2f0ad-103">Step 5: Optimize client and Office 365 service performance</span></span>

<span data-ttu-id="2f0ad-104">*Cette étape est facultative et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="2f0ad-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="2f0ad-105">Vous pouvez accroître les performances en ajustant la façon dont le protocole TCP fonctionne entre les appareils clients et les services Office 365.</span><span class="sxs-lookup"><span data-stu-id="2f0ad-105">You can increase performance by fine tuning the way that the Transmission Control Protocol (TCP) works between client devices and Office 365 services.</span></span>

<span data-ttu-id="2f0ad-106">Pour les appareils clients, vous pouvez modifier les paramètres TCP suivants sur des appareils clients afin d’optimiser les performances TCP :</span><span class="sxs-lookup"><span data-stu-id="2f0ad-106">For client devices, you can change the following TCP settings on client devices to optimize TCP performance:</span></span>

- <span data-ttu-id="2f0ad-107">[Mise à l’échelle des fenêtres TCP](https://blogs.technet.microsoft.com/onthewire/2014/03/28/ensuring-your-office-365-network-connection-isnt-throttled-by-your-proxy/), pour que votre appareil client puisse envoyer plus de données avant d’exiger un accusé de réception</span><span class="sxs-lookup"><span data-stu-id="2f0ad-107">[TCP window scaling](https://blogs.technet.microsoft.com/onthewire/2014/03/28/ensuring-your-office-365-network-connection-isnt-throttled-by-your-proxy/), so your client device can send more data before requiring an acknowledgement</span></span>
- <span data-ttu-id="2f0ad-108">[Durée d’inactivité TCP](https://blogs.technet.microsoft.com/onthewire/2014/03/04/network-perimeters-tcp-idle-session-settings-for-outlook-on-office-365/), pour que votre appareil client puisse gérer les connexions ouvertes plus efficacement</span><span class="sxs-lookup"><span data-stu-id="2f0ad-108">[TCP idle time](https://blogs.technet.microsoft.com/onthewire/2014/03/04/network-perimeters-tcp-idle-session-settings-for-outlook-on-office-365/), so your client device can handle open connections more efficiently</span></span>
- <span data-ttu-id="2f0ad-109">[Taille maximale de segment TCP](https://blogs.technet.microsoft.com/onthewire/2014/06/27/checking-your-tcp-packets-are-pulling-their-weight-tcp-max-segment-size-or-mss/), pour que votre appareil client puisse envoyer les blocs de données les plus volumineux dans un paquet</span><span class="sxs-lookup"><span data-stu-id="2f0ad-109">[TCP maximum segment size](https://blogs.technet.microsoft.com/onthewire/2014/06/27/checking-your-tcp-packets-are-pulling-their-weight-tcp-max-segment-size-or-mss/), so your client device can send the largest blocks of data in a packet</span></span>
- <span data-ttu-id="2f0ad-110">[Accusés de réception sélectifs TCP](https://blogs.technet.microsoft.com/onthewire/2014/06/27/ensuring-your-tcp-stack-isnt-throwing-data-away/), pour que votre appareil client puisse accuser reçu des données plus efficacement</span><span class="sxs-lookup"><span data-stu-id="2f0ad-110">[TCP selective acknowledgements](https://blogs.technet.microsoft.com/onthewire/2014/06/27/ensuring-your-tcp-stack-isnt-throwing-data-away/), so your client device can acknowledge received data more efficiently</span></span>

<span data-ttu-id="2f0ad-111">Pour les services Office 365, consultez ces ressources supplémentaires pour optimiser les performances :</span><span class="sxs-lookup"><span data-stu-id="2f0ad-111">For Office 365 services, see these additional resources to optimize performance:</span></span>

- [<span data-ttu-id="2f0ad-112">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="2f0ad-112">Exchange Online</span></span>](https://support.office.com/article/Tune-Exchange-Online-performance-026e83cb-a945-4543-97b0-a8af6e80ac61)
- [<span data-ttu-id="2f0ad-113">Skype Entreprise Online</span><span class="sxs-lookup"><span data-stu-id="2f0ad-113">Skype for Business Online</span></span>](https://support.office.com/article/Tune-Skype-for-Business-Online-performance-beec23c2-c5d6-4e84-a8af-e82aefca7802)
- [<span data-ttu-id="2f0ad-114">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="2f0ad-114">SharePoint Online</span></span>](https://support.office.com/article/Tune-SharePoint-Online-performance-f0522d4a-fbf4-41f9-854e-c9b59555091d)
- [<span data-ttu-id="2f0ad-115">Project Online</span><span class="sxs-lookup"><span data-stu-id="2f0ad-115">Project Online</span></span>](https://support.office.com/article/Tune-Project-Online-performance-12ba0ebd-c616-42e5-b9b6-cad570e8409c)

<span data-ttu-id="2f0ad-116">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step5) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="2f0ad-116">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step5) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="2f0ad-117">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2f0ad-117">Next step</span></span>

[<span data-ttu-id="2f0ad-118">Critères de sortie de l’infrastructure réseau</span><span class="sxs-lookup"><span data-stu-id="2f0ad-118">Networking infrastructure exit criteria</span></span>](networking-exit-criteria.md)
