---
title: Déployer une authentification fédérée haute disponibilité pour Microsoft 365 dans Azure
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 11/25/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150s
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
f1.keywords:
- CSH
ms.custom:
- Ent_Solutions
ms.assetid: 34b1ab9c-814c-434d-8fd0-e5a82cd9bff6
description: 'Résumé : Configurez l’authentification fédérée haute disponibilité pour Microsoft 365 abonnement dans Microsoft Azure.'
ms.openlocfilehash: 3989ebb06b4ac5dfa1cded5e07c086c4778f94e7
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50919151"
---
# <a name="deploy-high-availability-federated-authentication-for-microsoft-365-in-azure"></a><span data-ttu-id="a09c3-103">Déployer une authentification fédérée haute disponibilité pour Microsoft 365 dans Azure</span><span class="sxs-lookup"><span data-stu-id="a09c3-103">Deploy high availability federated authentication for Microsoft 365 in Azure</span></span>

<span data-ttu-id="a09c3-104">Cet article propose des liens vers les instructions pas à pas pour déployer l’authentification fédérée haute disponibilité pour Microsoft Microsoft 365 dans les services d’infrastructure Azure avec ces machines virtuelles :</span><span class="sxs-lookup"><span data-stu-id="a09c3-104">This article has links to the step-by-step instructions for deploying high availability federated authentication for Microsoft Microsoft 365 in Azure infrastructure services with these virtual machines:</span></span>
  
- <span data-ttu-id="a09c3-105">Deux serveurs proxy d’application web</span><span class="sxs-lookup"><span data-stu-id="a09c3-105">Two web application proxy servers</span></span>
    
- <span data-ttu-id="a09c3-106">Deux serveurs de services ADFS (Active Directory Federation Services)</span><span class="sxs-lookup"><span data-stu-id="a09c3-106">Two Active Directory Federation Services (AD FS) servers</span></span>
    
- <span data-ttu-id="a09c3-107">Deux contrôleurs de domaine répliqués</span><span class="sxs-lookup"><span data-stu-id="a09c3-107">Two replica domain controllers</span></span>
    
- <span data-ttu-id="a09c3-108">Un serveur de synchronisation d’annuaire exécutant Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="a09c3-108">One directory synchronization server running Azure AD Connect</span></span>
    
<span data-ttu-id="a09c3-109">Voici la configuration, avec les noms d’espace réservé pour chaque serveur.</span><span class="sxs-lookup"><span data-stu-id="a09c3-109">Here is the configuration, with placeholder names for each server.</span></span>
  
<span data-ttu-id="a09c3-110">**Une authentification fédérée haute disponibilité pour Microsoft 365'infrastructure dans Azure**</span><span class="sxs-lookup"><span data-stu-id="a09c3-110">**A high availability federated authentication for Microsoft 365 infrastructure in Azure**</span></span>

![Configuration finale de l’infrastructure d’authentification fédérée Microsoft 365 haute disponibilité dans Azure](../media/c5da470a-f2aa-489a-a050-df09b4d641df.png)
  
<span data-ttu-id="a09c3-112">Toutes les machines virtuelles sont dans un réseau virtuel intersites unique Azure.</span><span class="sxs-lookup"><span data-stu-id="a09c3-112">All of the virtual machines are in a single cross-premises Azure virtual network (VNet).</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a09c3-p101">L'authentification fédérée d'utilisateurs individuels n'utilise aucune ressource locale. Toutefois, si la connexion entre différents locaux devient indisponible, les contrôleurs de domaine du réseau virtuel ne reçoivent plus les mises à jour des comptes d'utilisateurs et des groupes apportées dans l'instance Active Directory Domain Services locale. Pour l’éviter, vous pouvez configurer une haute disponibilité pour votre connexion entre différents locaux. Pour plus d'informations, consultez [Configuration haute disponibilité pour la connectivité entre les réseaux locaux et la connectivité entre deux réseaux virtuels](/azure/vpn-gateway/vpn-gateway-highlyavailable)</span><span class="sxs-lookup"><span data-stu-id="a09c3-p101">Federated authentication of individual users does not rely on any on-premises resources. However, if the cross-premises connection becomes unavailable, the domain controllers in the VNet will not receive updates to user accounts and groups made in the on-premises Active Directory Domain Services (AD DS). To ensure this does not happen, you can configure high availability for your cross-premises connection. For more information, see [Highly Available Cross-Premises and VNet-to-VNet Connectivity](/azure/vpn-gateway/vpn-gateway-highlyavailable)</span></span>
  
<span data-ttu-id="a09c3-117">Chaque paire de machines virtuelles utilisée pour un rôle spécifique est dans son propre sous-réseau et son propre groupe à haute disponibilité.</span><span class="sxs-lookup"><span data-stu-id="a09c3-117">Each pair of virtual machines for a specific role is in its own subnet and availability set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a09c3-p102">Étant donné que ce réseau virtuel est connecté au réseau local, cette configuration n'inclut pas de machines virtuelles jumpbox ou de machines virtuelles de surveillance sur un sous-réseau de gestion. Pour plus d'informations, voir l'article relatif à l'[exécution de machines virtuelles Windows pour une architecture n-tiers](/azure/guidance/guidance-compute-n-tier-vm).</span><span class="sxs-lookup"><span data-stu-id="a09c3-p102">Because this VNet is connected to the on-premises network, this configuration does not include jumpbox or monitoring virtual machines on a management subnet. For more information, see [Running Windows VMs for an N-tier architecture](/azure/guidance/guidance-compute-n-tier-vm).</span></span> 
  
<span data-ttu-id="a09c3-120">Le résultat de cette configuration est que vous aurez une authentification fédérée pour tous vos utilisateurs Microsoft 365, dans lesquels ils peuvent utiliser leurs informations d’identification AD DS pour se connecter au lieu de leur compte Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a09c3-120">The result of this configuration is that you will have federated authentication for all of your Microsoft 365 users, in which they can use their AD DS credentials to sign in rather than their Microsoft 365 account.</span></span> <span data-ttu-id="a09c3-121">L’infrastructure d’authentification fédérés utilise un ensemble redondant de serveurs qui sont plus faciles à déployer dans les services d’infrastructure Azure que dans votre réseau de périmètre en local.</span><span class="sxs-lookup"><span data-stu-id="a09c3-121">The federated authentication infrastructure uses a redundant set of servers that are more easily deployed in Azure infrastructure services, rather than in your on-premises edge network.</span></span>
  
## <a name="bill-of-materials"></a><span data-ttu-id="a09c3-122">Nomenclature</span><span class="sxs-lookup"><span data-stu-id="a09c3-122">Bill of materials</span></span>

<span data-ttu-id="a09c3-123">Cette configuration de base requiert l’ensemble de composants et services Azure suivant :</span><span class="sxs-lookup"><span data-stu-id="a09c3-123">This baseline configuration requires the following set of Azure services and components:</span></span>
  
- <span data-ttu-id="a09c3-124">Sept machines virtuelles</span><span class="sxs-lookup"><span data-stu-id="a09c3-124">Seven virtual machines</span></span>
    
- <span data-ttu-id="a09c3-125">Un réseau virtuel intersites avec quatre sous-réseaux.</span><span class="sxs-lookup"><span data-stu-id="a09c3-125">One cross-premises virtual network with four subnets</span></span>
    
- <span data-ttu-id="a09c3-126">Quatre groupes de ressources</span><span class="sxs-lookup"><span data-stu-id="a09c3-126">Four resource groups</span></span>
    
- <span data-ttu-id="a09c3-127">Trois groupes à haute disponibilité</span><span class="sxs-lookup"><span data-stu-id="a09c3-127">Three availability sets</span></span>
    
- <span data-ttu-id="a09c3-128">Un abonnement Azure</span><span class="sxs-lookup"><span data-stu-id="a09c3-128">One Azure subscription</span></span>
    
<span data-ttu-id="a09c3-129">Voici les machines virtuelles et leurs tailles par défaut pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="a09c3-129">Here are the virtual machines and their default sizes for this configuration.</span></span>
  
|<span data-ttu-id="a09c3-130">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a09c3-130">**Item**</span></span>|<span data-ttu-id="a09c3-131">**Description de la machine virtuelle**</span><span class="sxs-lookup"><span data-stu-id="a09c3-131">**Virtual machine description**</span></span>|<span data-ttu-id="a09c3-132">**Image de la galerie Azure**</span><span class="sxs-lookup"><span data-stu-id="a09c3-132">**Azure gallery image**</span></span>|<span data-ttu-id="a09c3-133">**Taille par défaut**</span><span class="sxs-lookup"><span data-stu-id="a09c3-133">**Default size**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a09c3-134">1.</span><span class="sxs-lookup"><span data-stu-id="a09c3-134">1.</span></span>  <br/> |<span data-ttu-id="a09c3-135">Premier contrôleur de domaine</span><span class="sxs-lookup"><span data-stu-id="a09c3-135">First domain controller</span></span>  <br/> |<span data-ttu-id="a09c3-136">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-136">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-137">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-137">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-138">2.</span><span class="sxs-lookup"><span data-stu-id="a09c3-138">2.</span></span>  <br/> |<span data-ttu-id="a09c3-139">Deuxième contrôleur de domaine</span><span class="sxs-lookup"><span data-stu-id="a09c3-139">Second domain controller</span></span>  <br/> |<span data-ttu-id="a09c3-140">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-140">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-141">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-141">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-142">3.</span><span class="sxs-lookup"><span data-stu-id="a09c3-142">3.</span></span>  <br/> |<span data-ttu-id="a09c3-143">Serveur Azure AD Connect</span><span class="sxs-lookup"><span data-stu-id="a09c3-143">Azure AD Connect server</span></span>  <br/> |<span data-ttu-id="a09c3-144">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-144">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-145">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-145">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-146">4.</span><span class="sxs-lookup"><span data-stu-id="a09c3-146">4.</span></span>  <br/> |<span data-ttu-id="a09c3-147">Premier serveur AD FS</span><span class="sxs-lookup"><span data-stu-id="a09c3-147">First AD FS server</span></span>  <br/> |<span data-ttu-id="a09c3-148">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-148">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-149">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-149">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-150">5.</span><span class="sxs-lookup"><span data-stu-id="a09c3-150">5.</span></span>  <br/> |<span data-ttu-id="a09c3-151">Deuxième serveur AD FS</span><span class="sxs-lookup"><span data-stu-id="a09c3-151">Second AD FS server</span></span>  <br/> |<span data-ttu-id="a09c3-152">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-152">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-153">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-153">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-154">6.</span><span class="sxs-lookup"><span data-stu-id="a09c3-154">6.</span></span>  <br/> |<span data-ttu-id="a09c3-155">Premier serveur proxy d’application web</span><span class="sxs-lookup"><span data-stu-id="a09c3-155">First web application proxy server</span></span>  <br/> |<span data-ttu-id="a09c3-156">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-156">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-157">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-157">D2</span></span>  <br/> |
|<span data-ttu-id="a09c3-158">7.</span><span class="sxs-lookup"><span data-stu-id="a09c3-158">7.</span></span>  <br/> |<span data-ttu-id="a09c3-159">Deuxième serveur proxy d’application web</span><span class="sxs-lookup"><span data-stu-id="a09c3-159">Second web application proxy server</span></span>  <br/> |<span data-ttu-id="a09c3-160">Windows Server 2016 Datacenter</span><span class="sxs-lookup"><span data-stu-id="a09c3-160">Windows Server 2016 Datacenter</span></span>  <br/> |<span data-ttu-id="a09c3-161">D2</span><span class="sxs-lookup"><span data-stu-id="a09c3-161">D2</span></span>  <br/> |
   
<span data-ttu-id="a09c3-162">Pour calculer les coûts estimés pour cette configuration, utilisez la [calculatrice de prix Azure](https://azure.microsoft.com/pricing/calculator/)</span><span class="sxs-lookup"><span data-stu-id="a09c3-162">To compute the estimated costs for this configuration, see the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/)</span></span>
  
## <a name="phases-of-deployment"></a><span data-ttu-id="a09c3-163">Phases de déploiement</span><span class="sxs-lookup"><span data-stu-id="a09c3-163">Phases of deployment</span></span>

<span data-ttu-id="a09c3-164">Vous déployez cette charge de travail au cours des phases suivantes :</span><span class="sxs-lookup"><span data-stu-id="a09c3-164">You deploy this workload in the following phases:</span></span>
  
- <span data-ttu-id="a09c3-p104">[Phase 1 : Configuration Azure](high-availability-federated-authentication-phase-1-configure-azure.md). Créez des groupes de ressources, des comptes de stockage, des groupes à haute disponibilité et un réseau virtuel intersites.</span><span class="sxs-lookup"><span data-stu-id="a09c3-p104">[Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md). Create resource groups, storage accounts, availability sets, and a cross-premises virtual network.</span></span>
    
- <span data-ttu-id="a09c3-167">[Étape 2 : configurer les contrôleurs de domaine](high-availability-federated-authentication-phase-2-configure-domain-controllers.md).</span><span class="sxs-lookup"><span data-stu-id="a09c3-167">[Phase 2: Configure domain controllers](high-availability-federated-authentication-phase-2-configure-domain-controllers.md).</span></span> <span data-ttu-id="a09c3-168">Créer et configurer les contrôleurs de domaine réplica Azure AD et le serveur de synchronisation d’annuaires.</span><span class="sxs-lookup"><span data-stu-id="a09c3-168">Create and configure replica AD DS domain controllers and the directory synchronization server.</span></span>
    
- <span data-ttu-id="a09c3-p106">[Phase 3 : Configuration des serveurs AD FS](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md). Créez et configurez les deux serveurs AD FS.</span><span class="sxs-lookup"><span data-stu-id="a09c3-p106">[Phase 3: Configure AD FS servers](high-availability-federated-authentication-phase-3-configure-ad-fs-servers.md). Create and configure the two AD FS servers.</span></span>
    
- <span data-ttu-id="a09c3-p107">[Phase 4 : Configuration des proxys d’application web](high-availability-federated-authentication-phase-4-configure-web-application-pro.md). Créez et configurez les deux serveurs proxy d’application web.</span><span class="sxs-lookup"><span data-stu-id="a09c3-p107">[Phase 4: Configure web application proxies](high-availability-federated-authentication-phase-4-configure-web-application-pro.md). Create and configure the two web application proxy servers.</span></span>
    
- <span data-ttu-id="a09c3-173">[Phase 5 : Configurer l’authentification fédérée pour Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md).</span><span class="sxs-lookup"><span data-stu-id="a09c3-173">[Phase 5: Configure federated authentication for Microsoft 365](high-availability-federated-authentication-phase-5-configure-federated-authentic.md).</span></span> <span data-ttu-id="a09c3-174">Configurez l’authentification fédérée pour Microsoft 365 abonnement.</span><span class="sxs-lookup"><span data-stu-id="a09c3-174">Configure federated authentication for your Microsoft 365 subscription.</span></span>
    
<span data-ttu-id="a09c3-175">Ces articles fournissent un guide normatif, phase par phase, pour une architecture prédéfini afin de créer une authentification fédérée haute disponibilité fonctionnelle pour les Microsoft 365 services d’infrastructure Azure.</span><span class="sxs-lookup"><span data-stu-id="a09c3-175">These articles provide a prescriptive, phase-by-phase guide for a predefined architecture to create a functional, high availability federated authentication for Microsoft 365 in Azure infrastructure services.</span></span> <span data-ttu-id="a09c3-176">Gardez les éléments suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="a09c3-176">Keep the following in mind:</span></span>
  
- <span data-ttu-id="a09c3-177">Si vous êtes un implémenteur d’AD FS expérimenté, n’hésitez pas à adapter les instructions des étapes 3 à 4 et à créer l’ensemble de serveurs qui correspond le mieux à vos besoins. </span><span class="sxs-lookup"><span data-stu-id="a09c3-177">If you are an experienced AD FS implementer, feel free to adapt the instructions in phases 3 and 4 and build the set of servers that best suits your needs.</span></span>
    
- <span data-ttu-id="a09c3-178">Si vous disposez déjà d’un déploiement de cloud hybride Azure avec un réseau virtuel entre différents locaux, n’hésitez pas à adapter ou à ignorer les instructions des phases 1 et 2 et placez les serveurs proxy AD FS et d’application web dans les sous-réseaux appropriés.</span><span class="sxs-lookup"><span data-stu-id="a09c3-178">If you already have an existing Azure hybrid cloud deployment with an existing cross-premises virtual network, feel free to adapt or skip the instructions in phases 1 and 2 and place the AD FS and web application proxy servers on the appropriate subnets.</span></span>
    
<span data-ttu-id="a09c3-179">Pour créer un environnement de développement/test ou une preuve de concept de cette configuration, voir Identité fédérée pour votre environnement de [développement/test Microsoft 365 de développement/test.](federated-identity-for-your-microsoft-365-dev-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="a09c3-179">To build a dev/test environment or a proof-of-concept of this configuration, see [Federated identity for your Microsoft 365 dev/test environment](federated-identity-for-your-microsoft-365-dev-test-environment.md).</span></span>
  
## <a name="next-step"></a><span data-ttu-id="a09c3-180">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="a09c3-180">Next step</span></span>

<span data-ttu-id="a09c3-181">Démarrer la configuration de la charge de travail avec [Phase 1 : configurer Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span><span class="sxs-lookup"><span data-stu-id="a09c3-181">Start the configuration of this workload with [Phase 1: Configure Azure](high-availability-federated-authentication-phase-1-configure-azure.md).</span></span> 
