---
title: Planifier les certificats SSL tiers pour Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.date: 05/15/2019
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- M365-subscription-management
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- MET150
- MOE150
- BCS160
ms.assetid: b48cdf63-07e0-4cda-8c12-4871590f59ce
description: 'Résumé : décrit les certificats SSL nécessaires pour Exchange sur site et hybride, l’authentification unique à l’aide d’AD FS, d’Exchange Online Services et des services Web Exchange.'
ms.openlocfilehash: 1738e4c316772d928138adc654372bd0b9efae65
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46689866"
---
# <a name="plan-for-third-party-ssl-certificates-for-microsoft-365"></a><span data-ttu-id="b0571-103">Planifier les certificats SSL tiers pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0571-103">Plan for third-party SSL certificates for Microsoft 365</span></span>

<span data-ttu-id="b0571-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="b0571-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="b0571-105">Pour chiffrer les communications entre vos clients et l’environnement Microsoft 365, les certificats SSL (Secure Socket Layer) tiers doivent être installés sur vos serveurs d’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="b0571-105">To encrypt communications between your clients and the Microsoft 365 environment, third-party Secure Socket Layer (SSL) certificates must be installed on your infrastructure servers.</span></span>

<span data-ttu-id="b0571-106">Cet article fait partie de la [planification réseau et du réglage des performances pour Microsoft 365](https://aka.ms/tune).</span><span class="sxs-lookup"><span data-stu-id="b0571-106">This article is part of [Network planning and performance tuning for Microsoft 365](https://aka.ms/tune).</span></span>
   
<span data-ttu-id="b0571-107">Les certificats sont requis pour les composants Microsoft 365 suivants :</span><span class="sxs-lookup"><span data-stu-id="b0571-107">Certificates are required for the following Microsoft 365 components:</span></span>
  
- <span data-ttu-id="b0571-108">Exchange local</span><span class="sxs-lookup"><span data-stu-id="b0571-108">Exchange on-premises</span></span>
    
- <span data-ttu-id="b0571-109">Authentification unique (SSO) (pour les serveurs de fédération AD FS (Active Directory Federation Services) et les proxys de serveur de fédération AD FS)</span><span class="sxs-lookup"><span data-stu-id="b0571-109">Single sign-on (SSO) (for both the Active Directory Federation Services (AD FS) federation servers and AD FS federation server proxies)</span></span>
    
- <span data-ttu-id="b0571-110">Services Exchange Online, tels que la découverte automatique, Outlook Anywhere et les services Web Exchange</span><span class="sxs-lookup"><span data-stu-id="b0571-110">Exchange Online services, such as Autodiscover, Outlook Anywhere, and Exchange Web Services</span></span>
    
- <span data-ttu-id="b0571-111">Serveur Exchange hybride</span><span class="sxs-lookup"><span data-stu-id="b0571-111">Exchange hybrid server</span></span>
    
## <a name="certificates-for-exchange-on-premises"></a><span data-ttu-id="b0571-112">Certificats pour Exchange local</span><span class="sxs-lookup"><span data-stu-id="b0571-112">Certificates for Exchange On-Premises</span></span>

<span data-ttu-id="b0571-113">Pour obtenir une vue d’ensemble de l’utilisation des certificats numériques pour établir la communication entre l’organisation Exchange locale et Exchange Online sécurisé, voir l’article TechNet [Understanding Certificate Requirements](https://go.microsoft.com/fwlink/p/?LinkID=243657).</span><span class="sxs-lookup"><span data-stu-id="b0571-113">For an overview about how to use digital certificates to make the communication between the on-premises Exchange organization and Exchange Online secure, see the TechNet article [Understanding Certificate Requirements](https://go.microsoft.com/fwlink/p/?LinkID=243657).</span></span>
  
## <a name="certificates-for-single-sign-on"></a><span data-ttu-id="b0571-114">Certificats pour l’authentification unique</span><span class="sxs-lookup"><span data-stu-id="b0571-114">Certificates for Single Sign-On</span></span>

<span data-ttu-id="b0571-115">Pour fournir à vos utilisateurs une expérience d’authentification unique simplifiée qui inclut une sécurité fiable, les certificats indiqués dans le tableau suivant sont requis sur les serveurs de Fédération ou sur les serveurs proxy de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b0571-115">To provide your users with a simplified single sign-on experience that includes robust security, the certificates shown in the following table are required on either the federation servers or the federation server proxies.</span></span> <span data-ttu-id="b0571-116">Le tableau suivant se concentre sur les services ADFS (Active Directory Federation Services), d’autres informations sur [l’utilisation des fournisseurs d’identité tiers](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-compatibility).</span><span class="sxs-lookup"><span data-stu-id="b0571-116">The table below focuses on Active Directory Federation Services (AD FS), we also have more information on [using third-party identity providers](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-fed-compatibility).</span></span>
  
| <span data-ttu-id="b0571-117">Type de certificat</span><span class="sxs-lookup"><span data-stu-id="b0571-117">Certificate Type</span></span> | <span data-ttu-id="b0571-118">Description</span><span class="sxs-lookup"><span data-stu-id="b0571-118">Description</span></span> | <span data-ttu-id="b0571-119">Ce que vous devez savoir avant de procéder au déploiement</span><span class="sxs-lookup"><span data-stu-id="b0571-119">What you need to know before you deploy</span></span> |
|:-----|:-----|:-----|
|<span data-ttu-id="b0571-120">**Certificat SSL (également appelé certificat d’authentification de serveur)**</span><span class="sxs-lookup"><span data-stu-id="b0571-120">**SSL certificate (also called a server authentication certificate)**</span></span> <br/> |<span data-ttu-id="b0571-121">Il s’agit d’un certificat SSL standard utilisé pour sécuriser les communications entre les serveurs de Fédération, les clients et les serveurs proxy de Fédération.</span><span class="sxs-lookup"><span data-stu-id="b0571-121">This is a standard SSL certificate that is used to make communications between federation servers, clients, and federation server proxy computers secure.</span></span>  <br/> |<span data-ttu-id="b0571-122">AD FS nécessite un certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="b0571-122">AD FS requires an SSL certificate.</span></span> <span data-ttu-id="b0571-123">Par défaut, AD FS utilise le certificat SSL configuré pour le site Web par défaut dans Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="b0571-123">By default, AD FS uses the SSL certificate that is configured for the default website in Internet Information Services (IIS).</span></span>  <br/> <span data-ttu-id="b0571-124">Le nom de sujet de ce certificat SSL est utilisé pour déterminer le nom du service FS (Federation Service) pour chaque instance des services ADFS (Active Directory Federation Services) que vous déployez.</span><span class="sxs-lookup"><span data-stu-id="b0571-124">The subject name of this SSL certificate is used to determine the Federation Service (FS) name for each instance of AD FS that you deploy.</span></span> <span data-ttu-id="b0571-125">Vous pouvez choisir un nom de sujet pour les nouveaux certificats émis par une autorité de certification qui représente le mieux le nom de votre société ou organisation à Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b0571-125">Consider choosing a subject name for any new certification authority (CA)-issued certificates that best represents the name of your company or organization to Microsoft 365.</span></span> <span data-ttu-id="b0571-126">Ce nom doit être routable par Internet.</span><span class="sxs-lookup"><span data-stu-id="b0571-126">This name must be Internet-routable.</span></span>  <br/><span data-ttu-id="b0571-127">**Attention :** AD FS nécessite que ce certificat SSL n’ait pas de nom d’objet sans point (nom abrégé).</span><span class="sxs-lookup"><span data-stu-id="b0571-127">**Caution:** AD FS requires that this SSL certificate have no dotless (short-name) subject name.</span></span>          <br/> <span data-ttu-id="b0571-128">**Recommandation :** Étant donné que ce certificat doit être approuvé par les clients AD FS, nous vous recommandons d’utiliser un certificat SSL émis par une autorité de certification publique (tierce) ou par une autorité de certification qui est subordonnée à une racine de confiance publique ; par exemple, VeriSign ou Thawte.</span><span class="sxs-lookup"><span data-stu-id="b0571-128">**Recommendation:** Because this certificate must be trusted by clients of AD FS, we recommend that you use an SSL certificate issued by a public (third-party) CA or by a CA that is subordinate to a publicly trusted root; for example, VeriSign or Thawte.</span></span>  <br/> |
|<span data-ttu-id="b0571-129">**Certificat de signature de jetons**</span><span class="sxs-lookup"><span data-stu-id="b0571-129">**Token-signing certificate**</span></span> <br/> |<span data-ttu-id="b0571-130">Il s’agit d’un certificat X. 509 standard qui est utilisé pour signer de manière sécurisée tous les jetons que le serveur de Fédération émet et que Microsoft 365 accepte et valide.</span><span class="sxs-lookup"><span data-stu-id="b0571-130">This is a standard X.509 certificate that's used for securely signing all tokens that the federation server issues and that Microsoft 365 accepts and validates.</span></span>  <br/> |<span data-ttu-id="b0571-131">Le certificat de signature de jetons doit contenir une clé privée qui est chaînée à une racine de confiance dans les FS.</span><span class="sxs-lookup"><span data-stu-id="b0571-131">The token-signing certificate must contain a private key that chains to a trusted root in the FS.</span></span> <span data-ttu-id="b0571-132">Par défaut, AD FS crée un certificat auto-signé.</span><span class="sxs-lookup"><span data-stu-id="b0571-132">By default, AD FS creates a self-signed certificate.</span></span> <span data-ttu-id="b0571-133">Toutefois, en fonction des besoins de votre organisation, vous pouvez modifier ce certificat en un certificat émis par l’autorité de certification à l’aide du composant logiciel enfichable Gestion AD FS.</span><span class="sxs-lookup"><span data-stu-id="b0571-133">However, depending on the needs of your organization, you can change this certificate to a CA-issued certificate by using the AD FS management snap-in.</span></span>  <br/><span data-ttu-id="b0571-134">**Attention :** Le certificat de signature de jetons est essentiel à la stabilité des FS.</span><span class="sxs-lookup"><span data-stu-id="b0571-134">**Caution:** The token-signing certificate is critical to the stability of the FS.</span></span> <span data-ttu-id="b0571-135">Si le certificat est modifié, Microsoft 365 doit être informé de la modification.</span><span class="sxs-lookup"><span data-stu-id="b0571-135">If the certificate is changed, Microsoft 365 must be notified of the change.</span></span> <span data-ttu-id="b0571-136">Si la notification n’est pas fournie, les utilisateurs ne peuvent pas se connecter à leurs offres de service Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b0571-136">If notification is not provided, users can't sign in to their Microsoft 365 service offerings.</span></span><br/><span data-ttu-id="b0571-137">**Recommandation :** Nous vous recommandons d’utiliser le certificat de signature de jetons auto-signé qui est généré par les services ADFS (Active Directory Federation Services).</span><span class="sxs-lookup"><span data-stu-id="b0571-137">**Recommendation:** We recommend that you use the self-signed token-signing certificate that is generated by AD FS.</span></span> <span data-ttu-id="b0571-138">En procédant ainsi, il gère ce certificat par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0571-138">By doing so, it manages this certificate for you by default.</span></span> <span data-ttu-id="b0571-139">Par exemple, lorsque ce certificat est sur le paragraphe expire, AD FS génère un nouveau certificat auto-signé.</span><span class="sxs-lookup"><span data-stu-id="b0571-139">For example, when this certificate is about to expire, AD FS will generate a new self-signed certificate.</span></span>  <br/> |
   
<span data-ttu-id="b0571-140">Les proxies de serveur de Fédération nécessitent le certificat décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b0571-140">Federation server proxies require the certificate that is described in the following table.</span></span>
  
| <span data-ttu-id="b0571-141">Type de certificat</span><span class="sxs-lookup"><span data-stu-id="b0571-141">Certificate Type</span></span> | <span data-ttu-id="b0571-142">Description</span><span class="sxs-lookup"><span data-stu-id="b0571-142">Description</span></span> | <span data-ttu-id="b0571-143">Ce que vous devez savoir avant de procéder au déploiement</span><span class="sxs-lookup"><span data-stu-id="b0571-143">What you need to know before you deploy</span></span> |
|:-----|:-----|:-----|
|<span data-ttu-id="b0571-144">certificat SSL</span><span class="sxs-lookup"><span data-stu-id="b0571-144">SSL certificate</span></span>  <br/> |<span data-ttu-id="b0571-145">Il s’agit d’un certificat SSL standard utilisé pour sécuriser les communications entre un serveur de Fédération, un serveur proxy de Fédération et des ordinateurs clients Internet.</span><span class="sxs-lookup"><span data-stu-id="b0571-145">This is a standard SSL certificate that is used for securing communications between a federation server, a federation server proxy, and Internet client computers.</span></span>  <br/> |<span data-ttu-id="b0571-146">Ce certificat SSL doit être lié au site Web par défaut dans IIS avant de pouvoir exécuter l’Assistant Configuration du serveur proxy de fédération AD FS.</span><span class="sxs-lookup"><span data-stu-id="b0571-146">This SSL certificate must be bound to the default website in IIS before you can successfully run the AD FS Federation Server Proxy Configuration wizard.</span></span>  <br/> <span data-ttu-id="b0571-147">Ce certificat doit avoir le même nom de sujet que le certificat SSL configuré sur le serveur de Fédération dans le réseau d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="b0571-147">This certificate must have the same subject name as the SSL certificate that was configured on the federation server in the corporate network.</span></span>  <br/> <span data-ttu-id="b0571-148">**Recommandation :** Nous vous recommandons d’utiliser le même certificat d’authentification de serveur que celui configuré sur le serveur de Fédération auquel ce serveur proxy de Fédération se connecte.</span><span class="sxs-lookup"><span data-stu-id="b0571-148">**Recommendation:** We recommend that you use the same server authentication certificate that is configured on the federation server that this federation server proxy connects to.</span></span>  <br/> |
   
## <a name="certificates-for-autodiscover-outlook-anywhere-and-active-directory-synchronization"></a><span data-ttu-id="b0571-149">Certificats pour la synchronisation Autodiscover, Outlook Anywhere et Active Directory</span><span class="sxs-lookup"><span data-stu-id="b0571-149">Certificates for Autodiscover, Outlook Anywhere, and Active Directory Synchronization</span></span>

<span data-ttu-id="b0571-150">Vos serveurs d’accès au client Exchange 2013, Exchange 2010, Exchange 2007 et Exchange 2003 (CASs) externes requièrent un certificat SSL tiers pour les connexions sécurisées pour la découverte automatique, Outlook Anywhere et les services de synchronisation Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0571-150">Your external-facing Exchange 2013, Exchange 2010, Exchange 2007, and Exchange 2003 Client Access servers (CASs) require a third-party SSL certificate for secure connections for Autodiscover, Outlook Anywhere, and Active Directory synchronization services.</span></span> <span data-ttu-id="b0571-151">Ce certificat est peut-être déjà installé dans votre environnement local.</span><span class="sxs-lookup"><span data-stu-id="b0571-151">You may already have this certificate installed in your on-premises environment.</span></span>
  
## <a name="certificate-for-an-exchange-hybrid-server"></a><span data-ttu-id="b0571-152">Certificat pour un serveur hybride Exchange</span><span class="sxs-lookup"><span data-stu-id="b0571-152">Certificate for an Exchange Hybrid Server</span></span>

<span data-ttu-id="b0571-153">Votre ou vos serveurs Exchange hybrides externes nécessitent un certificat SSL tiers pour la connectivité sécurisée avec le service Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="b0571-153">Your external-facing Exchange hybrid server or servers require a third-party SSL certificate for secure connectivity with the Exchange Online service.</span></span> <span data-ttu-id="b0571-154">Vous devez obtenir ce certificat auprès de votre fournisseur SSL tiers.</span><span class="sxs-lookup"><span data-stu-id="b0571-154">You need to get this certificate from your third-party SSL provider.</span></span>
  
## <a name="microsoft-365-certificate-chains"></a><span data-ttu-id="b0571-155">Chaînes de certificats Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0571-155">Microsoft 365 Certificate Chains</span></span>

<span data-ttu-id="b0571-156">Cet article décrit les certificats que vous devrez peut-être installer sur votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="b0571-156">This article describes the certificates you may need to install on your infrastructure.</span></span> <span data-ttu-id="b0571-157">Pour plus d’informations sur les certificats installés sur nos serveurs Microsoft 365, consultez la rubrique [microsoft 365 Certificate Chains](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb).</span><span class="sxs-lookup"><span data-stu-id="b0571-157">For more information on the certificates installed on our Microsoft 365 servers, see [Microsoft 365 Certificate Chains](https://support.office.com/article/0c03e6b3-e73f-4316-9e2b-bf4091ae96bb).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0571-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0571-158">See also</span></span>

[<span data-ttu-id="b0571-159">Vue d’ensemble de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="b0571-159">Microsoft 365 Enterprise overview</span></span>](microsoft-365-overview.md)