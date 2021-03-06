---
title: Gestion des points de terminaison Office 365
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Adm_O365_Setup
- seo-marvel-apr2020
search.appverid: MOE150
ms.assetid: 99cab9d4-ef59-4207-9f2b-3728eb46bf9a
description: Découvrez comment gérer les points Office 365 afin qu’ils fonctionnent avec l’architecture réseau de votre organisation d’entreprise.
ms.openlocfilehash: fa727c5c80521b6ff67c50d202d0c11c643b021e
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925862"
---
# <a name="managing-office-365-endpoints"></a>Gestion des points de terminaison Office 365

La plupart des organisations d’entreprise disposant de plusieurs emplacements de bureau et d’une connexion WAN de connexion auront besoin de la configuration de la connectivité réseau d’Office 365. Vous pouvez optimiser votre réseau en envoyant toutes les requêtes réseau approuvées Office 365 directement via votre pare-feu, en contournant toutes les tâches d’inspection ou de traitement supplémentaires des paquets. Cela réduit ainsi la latence et les exigences relatives à la capacité du périmètre. L’identification du trafic réseau Office 365 est la première étape pour offrir des performances optimales pour vos utilisateurs. Pour plus d’informations, [Office 365 principes de connectivité réseau.](microsoft-365-network-connectivity-principles.md)

Microsoft vous recommande d’accéder aux points de terminaison Office 365 réseau et aux modifications en cours apportées à ces derniers à l’aide de l’adresse IP Office 365 et du [service Web d’URL.](microsoft-365-ip-web-service.md)

Quelle que soit la façon dont vous gérez le trafic réseau Office 365 vital, Office 365 nécessite une connectivité Internet. D’autres points de terminaison réseau pour lesquels une connectivité est requise sont répertoriés sur [Autres points de terminaison non inclus dans l’adresse IP d’Office 365 et le service Web d’URL](additional-office365-ip-addresses-and-urls.md).

La manière dont vous utilisez les points de terminaison réseau Office 365 dépendra de l’architecture réseau de votre entreprise. Cet article présente plusieurs façons d’intégrer les architectures réseau d’entreprise aux adresses IP et URL Office 365. Le moyen le plus simple de choisir les demandes réseau à faire confiance consiste à utiliser des périphériques SD-WAN qui prendre en charge la configuration Office 365 automatisée à chacun de vos bureaux.

## <a name="sd-wan-for-local-branch-egress-of-vital-office-365-network-traffic"></a>SD-WAN pour la sortie de branche locale du trafic Office 365 réseau

À chaque emplacement de succursale, vous pouvez fournir un périphérique SD-WAN configuré pour router le trafic pour la catégorie Office 365 Optimiser les points de terminaison, ou optimiser et autoriser des catégories, directement vers le réseau de Microsoft. Les autres types de trafic réseau, notamment le trafic de centre de données local, le trafic de sites Web Internet généraux et le trafic vers les points de terminaison de catégorie par défaut d’Office 365 sont envoyés à un autre emplacement dans lequel vous avez un périmètre de réseau plus important.

Microsoft travaille avec des fournisseurs SD-WAN pour activer la configuration automatisée. Pour plus d’informations, voir [Programme de partenariat réseau Office 365](microsoft-365-networking-partner-program.md).

<a name="pacfiles"> </a>
## <a name="use-a-pac-file-for-direct-routing-of-vital-office-365-traffic"></a>Utiliser un fichier PAC pour le routage direct du trafic Office 365 vital

Utilisez les fichiers PAC ou WPAD pour gérer les requêtes réseau associées à Office 365, mais qui n’ont aucune adresse IP. Les requêtes réseau classiques envoyées via un proxy ou un périphérique de périmètre augmentent la latence. Si l’arrêt et l’inspection de SSL créent la latence la plus élevée, d’autres services tels que l’authentification proxy et la recherche de réputation peuvent entraîner des performances médiocres et une expérience utilisateur incorrecte. De plus, ces périphériques réseau de périmètre ont besoin de suffisamment de ressources pour traiter toutes les requêtes de connexion réseau. Nous vous recommandons de contourner votre infrastructure de proxy ou d’inspection pour les requêtes réseau Office 365 directes.
  
[PowerShell Gallery Get-PacFile](https://www.powershellgallery.com/packages/Get-PacFile) est un script PowerShell qui lit les derniers points de terminaison réseau à partir de l’adresse IP et du service Web d’URL Office 365 et crée un exemple de fichier PAC. Vous pouvez modifier le script de sorte qu’il s’intègre à votre gestion de fichiers PAC existante.

![Connexion à Office 365 via des pare-feu et des proxys.](../media/34d402f3-f502-42a0-8156-24a7c4273fa5.png)

**Figure 1 : périmètre de réseau d’entreprise simple**

Le fichier PAC est déployé sur les navigateurs Web au point 1 de la figure 1. Lors de l’utilisation d’un fichier PAC pour la sortie directe du trafic réseau Office 365 vital, vous devez également autoriser la connectivité aux adresses IP situées derrière ces URL sur votre pare-feu de périmètre réseau. Pour ce faire, il suffit de récupérer les adresses IP des mêmes catégories de points de terminaison Office 365, comme spécifié dans le fichier PAC et de créer des listes de contrôle d’accès de pare-feu sur la base de ces adresses. Le pare-feu est le point 3 de la figure 1.

Séparément, si vous choisissez d’effectuer uniquement le routage direct pour les points de terminaison de la catégorie Optimiser, les points de terminaison de la catégorie Autoriser que vous envoyez au serveur proxy devront être répertoriés sur le serveur proxy afin de contourner le traitement. Par exemple, les points de terminaison Optimiser et Authentification de proxy sont incompatibles avec les points de terminaison Optimiser et Autoriser. Le serveur proxy est le point 2 de la figure 1.

La configuration courante consiste à autoriser sans traiter tout le trafic sortant du serveur proxy pour les adresses IP de destination du trafic réseau Office 365 qui atteint le serveur proxy. Pour plus d’informations sur les problèmes liés à l’utilisation de SSL Break et Inspect, voir [Utilisation d’appareils ou de solutions de réseau tiers sur le trafic Office 365](https://support.microsoft.com/help/2690045/using-third-party-network-devices-or-solutions-with-office-365).

Le script Get-PacFile génère deux types de fichiers PAC.

| Type | Description |
|:-----|:-----|
|**1** <br/> |Envoyez au serveur proxy Optimiser le trafic de point de terminaison direct et tout le reste. <br/> |
|**2** <br/> |Envoyez au serveur proxy Optimiser et Autoriser le trafic de point de terminaison direct et tout le reste. Ce type peut également être utilisé pour envoyer toutes les ExpressRoute prises en charge pour le trafic Office 365 vers ExpressRoute segments réseau et tout le reste vers le serveur proxy. <br/> |

Voici un exemple simple d’appel du script PowerShell :

```powershell
Get-PacFile -ClientRequestId b10c5ed1-bad1-445f-b386-b919946339a7
```

Il existe de nombreux paramètres que vous pouvez transmettre au script :

| Paramètre | Description |
|:-----|:-----|
|**ClientRequestId** <br/> |Ceci est requis et il s’agit d’un GUID transmis au service Web qui représente l’ordinateur client à l’origine de l’appel. <br/> |
|**Instance** <br/> |L Office 365 de service, qui est par défaut dans le monde entier. Il est également transmis au service web. <br/> |
|**TenantName** <br/> |Votre nom de client Office 365. Transmises au service Web et utilisées comme paramètre remplaçable dans certaines URL d’Office 365. <br/> |
|**Type** <br/> |Type du fichier PAC de proxy que vous voulez générer. <br/> |

Voici un autre exemple d’appel du script PowerShell avec d’autres paramètres :

```powershell
Get-PacFile -Type 2 -Instance Worldwide -TenantName Contoso -ClientRequestId b10c5ed1-bad1-445f-b386-b919946339a7
```

## <a name="proxy-server-bypass-processing-of-office-365-network-traffic"></a>Contournement de serveur proxy avec traitement du trafic réseau Office 365

Lorsque les fichiers PAC ne sont pas utilisés pour le trafic sortant direct, vous devez ignorer le traitement sur votre périmètre réseau en configurant votre serveur proxy. Certains fournisseurs de serveur proxy ont activé la configuration automatisée, ce qui est décrit dans le [Programme de partenariat réseau Office 365](microsoft-365-networking-partner-program.md).

Si vous le faites manuellement, vous devez obtenir les données de catégorie Optimiser et Autoriser les points de terminaison à partir du service Web URL et adresse IP Office 365 et configurer votre serveur proxy pour contourner le traitement de ces derniers. Il est important d’éviter l’arrêt et l’inspection de SSL et l’authentification proxy pour les points de terminaison Optimiser et Autoriser.
  
<a name="bkmk_changes"> </a>
## <a name="change-management-for-office-365-ip-addresses-and-urls"></a>Gestion des modifications pour Office 365 adresses IP et URL

En plus de sélectionner la configuration appropriée pour votre périmètre de réseau, il est essentiel que vous adoptiez un processus de gestion des modifications pour les points de terminaison Office 365. Ces points de terminaison changent régulièrement et si vous ne gérez pas les modifications, vous pouvez rencontrer des utilisateurs bloqués ou avec des performances médiocres suite à l’ajout d’une nouvelle adresse IP ou d’une nouvelle URL.

Les modifications apportées aux adresses IP et URL Office 365 sont généralement publiées autour du dernier jour de chaque mois. Il peut arriver qu’une modification soit publiée en dehors de cette planification en raison de besoins opérationnels, de support ou de sécurité.

Lors de la publication d’une modification nécessitant d’agir suite à l’ajout d’une adresse IP ou d’une URL, vous devriez recevoir une notification de 30 jours à partir du moment où nous publions la modification jusqu’à ce qu’un service Office 365 sur ce point de terminaison soit utilisé. Bien que nous cherchions à utiliser cette période de notification, il est possible qu’elle ne soit pas toujours possible en raison de besoins opérationnels, de support ou de sécurité. Les modifications qui n’ont pas besoin d’une action immédiate pour maintenir la connectivité, telles que les adresses IP ou URL supprimées, ou les modifications moins importantes, n’incluent pas de notification préalable. Quelle que soit la notification fournie, nous annonçons la date de mise en service attendue pour chaque changement.

### <a name="change-notification-using-the-web-service"></a>Notification des modifications à l’aide du service Web

Vous pouvez utiliser l’adresse IP Office 365 et le service Web d’URL pour obtenir la notification de modification. Nous vous recommandons d’appeler la méthode Web **/version** une fois par heure pour vérifier la version des points de terminaison que vous utilisez pour vous connecter à Office 365. Si cette version change alors qu’elle est comparée à la version que vous utilisez, vous devriez obtenir les données de point de terminaison les plus récentes à partir de la méthode Web **/Endpoints** et éventuellement obtenir les différences par rapport à la méthode Web **/changes**. Il n’est pas nécessaire d’appeler les méthodes Web **/Endpoints** ou **/changes** si aucune modification n’a été apportée à la version que vous avez trouvée.

Pour plus d’informations, voir [Service web d’URL et d’adresses IP Office 365](microsoft-365-ip-web-service.md).

### <a name="change-notification-using-rss-feeds"></a>Notification des modifications à l’aide de flux RSS

L’adresse IP et le service Web d’URL Office 365 fournissent un flux RSS auquel vous pouvez vous abonner dans Outlook. Il existe des liens vers les URL RSS sur chacune des pages spécifiques aux instances de service Office 365 pour les adresses IP et URL. Pour plus d’informations, voir [Service web d’URL et d’adresses IP Office 365](microsoft-365-ip-web-service.md).

### <a name="change-notification-and-approval-review-using-microsoft-flow"></a>Notification et révision des modifications à l’aide de Microsoft Flow

Nous savons qu’il est possible que vous deviez continuer à traiter manuellement les modifications apportées aux points de terminaison réseau par mois. Vous pouvez utiliser Microsoft Flow pour créer un flux qui vous informe par courrier électronique et exécute éventuellement un processus d’approbation pour les modifications lorsque les points de terminaison réseau Office 365 contiennent des modifications. Une fois la révision terminée, vous pouvez faire en sorte que le flux envoie par email automatiquement les modifications apportées à l’équipe de gestion de votre pare-feu et serveur proxy.

Pour plus d’informations sur un exemple de flux Microsoft et un modèle, voir [Utiliser Microsoft Flow pour recevoir un courrier électronique pour les modifications apportées aux adresses IP et URL Office 365](https://techcommunity.microsoft.com/t5/Office-365-Networking/Use-Microsoft-Flow-to-receive-an-email-for-changes-to-Office-365/td-p/240651).
  
<a name="FAQ"> </a>
## <a name="office-365-network-endpoints-faq"></a>Forum aux questions sur les points de terminaison réseau Office 365

Consultez ces questions fréquemment posées sur Office 365 connectivité réseau.
  
### <a name="how-do-i-submit-a-question"></a>Comment puis-je envoyer une question ?

Cliquez sur le lien situé au bas de la page pour indiquer si l’article vous a été utile ou non, mais également pour poser d’autres questions. Nous surveillons les commentaires et mettons à jour les questions contenues dans cet article avec celles que les clients nous posent le plus fréquemment.
  
### <a name="how-do-i-determine-the-location-of-my-tenant"></a>Comment déterminer l’emplacement de mon client ?

 **L’emplacement du client** est mieux déterminé à l’aide de notre [carte de centre de données](./o365-data-locations.md).
  
### <a name="am-i-peering-appropriately-with-microsoft"></a>Est-ce que ma relation d’homologation avec Microsoft est appropriée ?

 Les **emplacements d’homologation** sont décrits plus en détail dans l’article [Homologation avec Microsoft](https://www.microsoft.com/peering).
  
Avec plus de 2 500 relations d’homologation avec des fournisseurs de services Internet dans le monde entier et 70 points de présence, l’accès depuis votre réseau à nos réseaux devrait être transparent. En quelques minutes, vous pouvez vous assurer que la relation d’homologation de votre fournisseur de services Internet est optimale. [Voici quelques exemples](/archive/blogs/onthewire/__guidance) de bonnes et de mauvaises configurations d’homologation à notre réseau.
  
<a name="bkmk_MissingIP"> </a>
### <a name="i-see-network-requests-to-ip-addresses-not-on-the-published-list-do-i-need-to-provide-access-to-them"></a>Je vois des requêtes réseau envoyées à des adresses IP ne figurant pas sur la liste publiée. Dois-je leur octroyer l’accès ?

Nous fournissons uniquement des adresses IP pour les serveurs Office 365 sur lesquels vous devez router directement. Cette liste d’adresses IP associées aux requêtes réseau n’est pas exhaustive. Vous voyez les requêtes réseau envoyées à Microsoft et à des adresses IP non publiées appartenant à des tiers. Ces adresses IP sont gérées ou générées de manière dynamique. Il est donc impossible de fournir un préavis immédiat en cas de modification. Si votre pare-feu ne peut pas autoriser l’accès sur la base des noms de domaines complets associés à ces requêtes réseau, utilisez un fichier PAC ou WPAD pour gérer les requêtes.
  
Voir une adresse IP associée à Office 365 sur laquelle vous voulez obtenir plus d’informations.
  
1. Vérifiez si l’adresse IP est incluse dans une plage publiée plus grande à l’aide d’une calculatrice CIDR, comme celles-ci pour [IPv4](https://www.ipaddressguide.com/cidr) ou [IPv6](https://www.ipaddressguide.com/ipv6-cidr). Par exemple, 40.96.0.0/13 inclut l’adresse IP 40.103.0.1 Malgré 40.96 ne correspondant pas à 40.103.
2. Vérifiez si l’adresse IP appartient à un partenaire en utilisant une [requête whois](https://dnsquery.org/). Si elle appartient à Microsoft, il peut s’agir d’un partenaire interne. De nombreux points de terminaison réseau de partenaire sont répertoriés comme appartenant à la catégorie _par défaut_, pour laquelle les adresses IP ne sont pas publiées.
3. L’adresse IP ne fait pas partie d’Office 365 ou d’une dépendance. La publication du point de terminaison réseau Office 365 n’inclut pas tous les points de terminaison réseau Microsoft.
4. Vérifiez le certificat. Avec un navigateur, connectez-vous à l’adresse IP à l’aide de *HTTPS:// \<IP_ADDRESS\>* et vérifiez les domaines répertoriés sur le certificat pour comprendre quels domaines sont associés à l’adresse IP. S’il s’agit d’une adresse IP propriété de Microsoft et qu’elle ne figure pas dans la liste des adresses IP Office 365, il est probable que l’adresse IP soit associée à un CDN Microsoft tel que *MSOCDN.NET* ou un autre domaine Microsoft sans informations IP publiées. Si vous constatez que le domaine figurant sur le certificat est l’un de ceux dont nous déclarons répertorier l’adresse IP, faites-le nous savoir.

<a name="bkmk_cname"> </a>
### <a name="some-office-365-urls-point-to-cname-records-instead-of-a-records-in-the-dns-what-do-i-have-to-do-with-the-cname-records"></a>Certaines URL Office 365 pointent vers des enregistrements CNAME au lieu d’un enregistrement dans le DNS. Que dois-je faire des enregistrements CNAME ?

Les ordinateurs clients ont besoin d’un enregistrement DNS A ou AAAA t)hat inclut une ou plusieurs adresses IP pour se connecter à un service cloud. Certaines URL incluses dans Office 365 affichent les enregistrements CNAME au lieu des enregistrements A ou AAAA. Ces enregistrements CNAME sont intermédiaires. Il peut y en avoir plusieurs dans une chaîne. Ils sont toujours résolus en un enregistrement A ou AAAA pour une adresse IP. Par exemple, considérez la série d’enregistrements DNS suivante, qui est traduite en une adresse IP _IP_1_:

```console
serviceA.office.com -> CNAME: serviceA.domainA.com -> CNAME: serviceA.domainB.com -> A: IP_1
```

Ces redirections CNAME constituent une partie normale du DNS et sont transparentes pour l’ordinateur client et transparent pour les serveurs proxy. Elles sont utilisées pour l’équilibrage de charge, les réseaux de distribution de contenu, la haute disponibilité et l’atténuation des incidents de service. Microsoft ne publie pas les enregistrements CNAME intermédiaires, ils sont susceptibles de changer à tout moment, et vous n’avez pas besoin de les configurer comme autorisé sur votre serveur proxy.

Un serveur proxy valide l’URL initiale, qui dans l’exemple ci-dessus est serviceA.office.com, et cette URL serait incluse dans Office 365 publication. Le serveur proxy demande la résolution DNS de cette URL à une adresse IP et recevra IP_1. Il ne valide pas les enregistrements de redirection intermédiaires CNAME.

Les configurations codées en dur ou l’utilisation d’une liste d’attente basée sur des FQDN indirects Office 365 ne sont pas recommandées, ne sont pas pris en charge par Microsoft et sont connues pour provoquer des problèmes de connectivité client. Les solutions DNS qui bloquent la redirection CNAME ou qui résolvent de manière incorrecte les entrées DNS Office 365 peuvent être résolues via des redirecteurs DNS avec la récursion DNS activée ou à l’aide d’indications racine DNS. De nombreux produits de périmètre de réseau tiers intègrent en natif le point de terminaison Office 365 recommandé pour inclure une liste d’adresses ip dans leur configuration à l’aide de l’adresse IP Office 365 et du [service Web d’URL.](microsoft-365-ip-web-service.md)

<a name="bkmk_akamai"> </a>
### <a name="why-do-i-see-names-such-as-nsatcnet-or-akadnsnet-in-the-microsoft-domain-names"></a>Pourquoi des noms tels que nsatc.net ou akadns.net figurent-ils parmi les noms de domaine de Microsoft ?

Office 365 et d’autres services Microsoft utilisent des services tiers tels que MarkMonitor et Akamai pour améliorer votre expérience d’Office 365. Pour continuer de vous offrir la meilleure expérience possible, il se peut que vous changions ces services à l’avenir. Les domaines tiers peuvent héberger du contenu, tel qu’un CDN, ou héberger un service, tel qu’un service de gestion du trafic géographique. Voici quelques-uns des services actuellement utilisés :
  
[MarkMonitor](https://www.markmonitor.com/) est utilisé lorsque vous voyez des requêtes qui incluent *\* .nsatc.net*. Ce service fournit une protection de nom de domaine et une surveillance pour protéger contre des comportements malveillants.
  
[ExactTarget est](https://www.marketingcloud.com/) utilisé lorsque vous voyez des demandes à *\* .exacttarget.com*. Ce service fournit une gestion des liens de messagerie électronique et une surveillance pour protéger contre des comportements malveillants.
  
[Akamai](https://www.akamai.com/) est utilisé lorsque vous voyez des requêtes incluant l’un des noms de domaine complets (FQDN) suivants. Ce service offre des services de géo-DNS et de réseau de distribution de contenu.
  
```console
*.akadns.net
*.akam.net
*.akamai.com
*.akamai.net
*.akamaiedge.net
*.akamaihd.net
*.akamaized.net
*.edgekey.net
*.edgesuite.net
```

<a name="bkmk_thirdparty"> </a>
### <a name="i-have-to-have-the-minimum-connectivity-possible-for-office-365"></a>J’ai besoin de la connectivité minimale pour Office 365

Office 365 est une suite de services conçue pour fonctionner sur Internet. Les promesses de fiabilité et de disponibilité sont basées sur l’accès à de nombreux services Internet standard. Par exemple, des services Internet standard tels que DNS, CRL et CDN doivent être accessibles pour utiliser Office 365, tout comme ils doivent l’être pour utiliser les services Internet les plus modernes.

La suite Office 365 est divisée en zones de service majeures. Celles-ci peuvent être activées de manière sélective pour la connectivité et il existe une zone commune, qui est une dépendance pour tout et est toujours nécessaire.

| Zone de service | Description |
|:-----|:-----|
|**Exchange** <br/> |Exchange Online et Exchange Online Protection <br/> |
|**SharePoint** <br/> |Sharepoint Online et OneDrive Entreprise <br/> |
|**Skype Entreprise Online et Microsoft Teams** <br/> |Skype Entreprise et Microsoft Teams <br/> |
|**Courant** <br/> |Office 365 Pro Plus, Office dans un navigateur, Azure AD et les autres points de terminaison réseau courants <br/> |

En plus des services Internet de base, il existe des services tiers utilisés uniquement pour intégrer des fonctionnalités. Bien que ces éléments soient nécessaires pour l’intégration, ils sont marqués comme facultatifs dans l’article sur les points de terminaison Office 365, ce qui signifie que les fonctionnalités principales du service continueront de fonctionner si le point de terminaison n’est pas accessible. Tout point de terminaison réseau requis aura l’attribut requis sur true. Tout point de terminaison réseau facultatif aura l’attribut requis sur false et l’attribut notes détaillera les fonctionnalités manquantes à prévoir si la connectivité est bloquée.
  
Si vous essayez d’utiliser Office 365 et que vous trouvez que des services tiers ne sont pas accessibles, vous devez vous assurer que tous les [FQDN marqués](urls-and-ip-address-ranges.md)comme obligatoires ou facultatifs dans cet article sont autorisés via le proxy et le pare-feu.
  
<a name="bkmk_consumer"> </a>
### <a name="how-do-i-block-access-to-microsofts-consumer-services"></a>Comment bloquer l’accès aux services grand public de Microsoft ?

La limitation de l’accès aux services grand public doit être effectuée à vos risques et périls. Le seul moyen fiable de bloquer les services grand public est de restreindre l’accès aux *login.live.com* nom de domaine complet. Ce nom de domaine complet est utilisé par divers services, y compris des services non destinés au grand public tels que MSDN, TechNet, etc. Ce nom de domaine complet est également utilisé par le programme de transfert de fichiers sécurisé de support Microsoft et est nécessaire pour transférer des fichiers afin de faciliter la résolution des problèmes pour les produits Microsoft.  La limitation de l’accès à ce nom de domaine complet peut nécessiter d’inclure également les exceptions à la règle pour les requêtes réseau associées à ces services.
  
N’oubliez pas que le blocage de l’accès aux services grand public de Microsoft ne suffit pas à lui seul à empêcher un membre de votre réseau d’extraire des informations à l’aide d’un client ou d’un autre service Office 365.

<a name="bkmk_IPOnlyFirewall"> </a>
### <a name="my-firewall-requires-ip-addresses-and-cannot-process-urls-how-do-i-configure-it-for-office-365"></a>Mon pare-feu nécessite des adresses IP et ne peut pas traiter les URL. Comment puis-je le configurer pour Office 365 ?

Office 365 ne fournit aucune adresse IP de tous les points de terminaison réseau requis. Certaines sont proposées sous forme d’URL uniquement et sont classées par défaut. Les URL de la catégorie par défaut qui sont requises doivent être autorisées via un serveur proxy. Si vous n’avez pas de serveur proxy, regardez comment vous avez configuré les demandes web pour les URL que les utilisateurs tapent dans la barre d’adresses d’un navigateur web ; l’utilisateur ne fournit pas non plus d’adresse IP. Les Office 365 url de catégorie par défaut qui ne fournissent pas d’adresses IP doivent être configurées de la même manière.

## <a name="related-topics"></a>Voir aussi

[Service web d’URL et d’adresses IP Office 365](microsoft-365-ip-web-service.md)

[Plages d’adresses IP du centre de données Microsoft Azure](https://www.microsoft.com/download/details.aspx?id=41653)
  
[Espace d’adresse IP public de Microsoft](https://www.microsoft.com/download/details.aspx?id=53602)
  
[Configuration requise pour l’infrastructure réseau pour Microsoft Intune](/intune/get-started/network-infrastructure-requirements-for-microsoft-intune)
  
[ExpressRoute et Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-power-bi-expressroute/)
  
[URL et plages d’adresses IP Office 365](urls-and-ip-address-ranges.md)
  
[Gestion d’ExpressRoute pour la connectivité d’Office 365](managing-expressroute-for-connectivity.md)
  
[Principes de connectivité réseau Office 365](microsoft-365-network-connectivity-principles.md)