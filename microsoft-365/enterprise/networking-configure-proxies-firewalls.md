---
title: 'Étape 4 : configurer le trafic de contournement'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/31/2018
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
ms.custom: ''
description: Analysez et configurez des navigateurs web et des équipements de périmètre pour le trafic de contournement vers des emplacements Office 365 approuvés.
ms.openlocfilehash: fbc4956525e2661ce791c6ec81b449dba685d0f0
ms.sourcegitcommit: 1ca1062ccddd7a46fa0bb4af6ee5f0eb141e7280
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "36999038"
---
# <a name="step-4-configure-traffic-bypass"></a><span data-ttu-id="2c48f-103">Étape 4 : configurer le trafic de contournement</span><span class="sxs-lookup"><span data-stu-id="2c48f-103">Step 4: Configure traffic bypass</span></span>

<span data-ttu-id="2c48f-104">*Cette étape facultative s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="2c48f-104">*This step is optional and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/networking_icon-small.png)

<span data-ttu-id="2c48f-p101">Étant donné que le trafic Internet général peut être risqué, les réseaux d’organisation appliquent généralement la sécurité avec des équipements de périmètre tels que des serveurs proxy, le SSL Break and Inspect, des appareils d’inspection des paquets et des systèmes de protection contre la perte de données. Pour en savoir plus sur certains problèmes avec les périphériques d’interception réseau, reportez-vous à l’article relatif à l’utilisation de périphériques réseau tiers ou de solutions sur le trafic Office 365.</span><span class="sxs-lookup"><span data-stu-id="2c48f-p101">Because general Internet traffic can be risky, typical organization networks enforce security with edge devices such as proxy servers, SSL Break and Inspect, and packet inspection devices, and data loss prevention systems. Read about some of the issues with network interception devices at Using third-party network devices or solutions on Office 365 traffic.</span></span>

<span data-ttu-id="2c48f-p102">Toutefois, les noms de domaine DNS et les adresses IP utilisées par les services cloud Microsoft 365 sont connus. Par ailleurs, le trafic et les services eux-mêmes sont protégés avec de nombreuses fonctionnalités de sécurité. Étant donné que cette protection et cette sécurité sont déjà en place, vos équipements de périmètre n’ont pas besoin de les dupliquer. Les destinations intermédiaires et le traitement de la sécurité dupliqué pour le trafic Microsoft 365 peuvent réduire les performances de façon considérable.</span><span class="sxs-lookup"><span data-stu-id="2c48f-p102">However, the DNS domain names and IP addresses used by Microsoft 365 cloud-based services are well known. Additionally, the traffic and services themselves are protected with many security features. Because this security and protection is already in place, your edge devices don’t need to duplicate it. Intermediate destinations and duplicate security processing for Microsoft 365 traffic can dramatically decrease performance.</span></span>

<span data-ttu-id="2c48f-p103">La première chose à faire lorsque vous éliminez les destinations intermédiaires et le traitement de la sécurité dupliqué consiste à identifier le trafic Microsoft 365. Microsoft a défini les types de noms de domaine DNS et les plages d’adresses IP suivants, appelés points de terminaison :</span><span class="sxs-lookup"><span data-stu-id="2c48f-p103">The first step in eliminating intermediate destinations and duplicate security processing is to identify Microsoft 365 traffic. Microsoft has defined the following types of DNS domain names and IP address ranges, known as endpoints:</span></span>

- <span data-ttu-id="2c48f-113">**Optimiser** : obligatoires pour la connectivité à chaque service Office 365 ; représentent plus de 75 % de la bande passante, des connexions et du volume de données de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2c48f-113">**Optimize** - Required for connectivity to every Office 365 service and represent over 75% of Microsoft 365 bandwidth, connections, and volume of data.</span></span> <span data-ttu-id="2c48f-114">Ces points de terminaison représentent les scénarios de Microsoft 365 les plus sensibles aux performances, à la latence et à la disponibilité du réseau.</span><span class="sxs-lookup"><span data-stu-id="2c48f-114">These endpoints represent Microsoft 365 scenarios that are the most sensitive to network performance, latency and availability.</span></span>
- <span data-ttu-id="2c48f-115">**Autoriser** : obligatoires pour la connectivité à des services et fonctionnalités Microsoft 365 spécifiques, mais ne sont pas sensibles aux performances et à la latence du réseau comme ceux de la catégorie Optimiser.</span><span class="sxs-lookup"><span data-stu-id="2c48f-115">**Allow** - Required for connectivity to specific Microsoft 365 services and features but are not as sensitive to network performance and latency as those in the Optimize category.</span></span>
 - <span data-ttu-id="2c48f-116">**Par défaut** : représentent des services et dépendances de Microsoft 365 qui ne nécessitent pas d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="2c48f-116">**Default** - Represent Microsoft 365 services and dependencies that do not require any optimization.</span></span> <span data-ttu-id="2c48f-117">Vous pouvez considérer les points de terminaison de la catégorie Par défaut comme du trafic Internet normal.</span><span class="sxs-lookup"><span data-stu-id="2c48f-117">You can treat Default category endpoints as normal Internet traffic.</span></span>

<span data-ttu-id="2c48f-118">Vous pouvez trouver les noms de domaine DNS et les plages d’adresses IP sur la page [https://aka.ms/o365endpoints](https://aka.ms/o365endpoints).</span><span class="sxs-lookup"><span data-stu-id="2c48f-118">You can find the DNS domain names and IP address ranges at [https://aka.ms/o365endpoints](https://aka.ms/o365endpoints).</span></span>

<span data-ttu-id="2c48f-119">Microsoft vous recommande les points suivants :</span><span class="sxs-lookup"><span data-stu-id="2c48f-119">Microsoft recommends that you:</span></span>

- <span data-ttu-id="2c48f-p106">Utiliser des scripts PAC (Proxy Automatic Configuration) sur les navigateurs Internet de vos ordinateurs locaux pour contourner vos serveurs proxy pour les noms de domaine DNS des services cloud Microsoft 365. Pour le dernier script PAC de Microsoft 365, reportez-vous au [script PowerShell Get-Pacfile](https://docs.microsoft.com/office365/enterprise/managing-office-365-endpoints#use-a-pac-file-for-direct-routing-of-vital-office-365-traffic).</span><span class="sxs-lookup"><span data-stu-id="2c48f-p106">Use Proxy Automatic Configuration (PAC) scripts on the Internet browsers of your on-premises computers to bypass your proxy servers for the DNS domain names of Microsoft 365 cloud-based services. For the latest Microsoft 365 PAC script, see the Get-Pacfile PowerShell script.</span></span>
- 
- <span data-ttu-id="2c48f-p107">Analyser vos équipements de périmètre pour déterminer le traitement dupliqué, puis les configurer pour transférer le trafic vers les points de terminaison Optimiser et Autoriser sans traitement. Ceci s’appelle le trafic de contournement.</span><span class="sxs-lookup"><span data-stu-id="2c48f-p107">Analyze your edge devices to determine the duplicate processing and then configure them to forward traffic to Optimize and Allow endpoints without processing. This is known as traffic bypass.</span></span> 

<span data-ttu-id="2c48f-p108">Les équipements de périmètre incluent les pare-feux, le SSL Break and Inspect, les appareils d’inspection des paquets et les systèmes de protection contre la perte de données. Pour configurer et mettre à jour les configurations des équipements de périmètre, vous pouvez utiliser un script ou un appel REST pour consommer une liste de points de terminaison structurée à partir du service web des points de terminaison Office 365. Pour plus d’informations, reportez-vous à l’article [Service web d’URL et d’adresse IP Office 365](https://docs.microsoft.com/fr-FR/office365/enterprise/office-365-ip-web-service#exporting-a-proxy-pac-file).</span><span class="sxs-lookup"><span data-stu-id="2c48f-p108">Edge devices include firewalls, SSL Break and Inspect, and packet inspection devices, and data loss prevention systems. To configure and update the configurations of edge devices, you can use a script or a REST call to consume a structured list of endpoints from the Office 365 Endpoints web service. For more information, see [Office 365 IP Address and URL Web service](https://docs.microsoft.com/fr-FR/office365/enterprise/office-365-ip-web-service#exporting-a-proxy-pac-file).</span></span>

<span data-ttu-id="2c48f-p109">Vous ne faites que contourner le traitement de sécurité réseau et de proxy normal pour le trafic vers les points de terminaison des catégories Optimiser et Autoriser de Microsoft 365. Tout autre trafic Internet général sera en proxy et soumis au traitement de sécurité de votre réseau existant.</span><span class="sxs-lookup"><span data-stu-id="2c48f-p109">Note that you are only bypassing normal proxy and network security processing for traffic to Microsoft 365 Optimize and Allow categories endpoints. All other general Internet traffic will be proxied and be subject to your existing network security processing.</span></span>


<span data-ttu-id="2c48f-129">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](networking-exit-criteria.md#crit-networking-step4) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="2c48f-129">As an interim checkpoint, you can see the [exit criteria](networking-exit-criteria.md#crit-networking-step4) for this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="2c48f-130">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2c48f-130">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step5.png)|[<span data-ttu-id="2c48f-131">Optimiser les performances du service Office 365 et du client</span><span class="sxs-lookup"><span data-stu-id="2c48f-131">Optimize client and Office 365 service performance</span></span>](networking-optimize-tcp-performance.md) |



