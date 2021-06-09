---
title: Suppression ou désactivation de l’authentification moderne hybride à partir de Skype Entreprise et Exchange
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 11/3/2017
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5a91b9e3-1508-475b-93e0-710fa5d5cd2d
ms.collection:
- M365-security-compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
description: Cet article explique comment supprimer ou désactiver l’authentification moderne hybride de Skype Entreprise et Exchange.
ms.openlocfilehash: 9442ef3e19d0835bfd59f27ec425e36fd7dfcf7a
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50927287"
---
# <a name="removing-or-disabling-hybrid-modern-authentication-from-skype-for-business-and-exchange"></a><span data-ttu-id="a4bab-103">Suppression ou désactivation de l’authentification moderne hybride à partir de Skype Entreprise et Exchange</span><span class="sxs-lookup"><span data-stu-id="a4bab-103">Removing or disabling Hybrid Modern Authentication from Skype for Business and Exchange</span></span>

<span data-ttu-id="a4bab-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="a4bab-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="a4bab-105">Si vous avez activé l’authentification moderne hybride (HMA) uniquement pour trouver qu’elle ne convient pas à votre environnement actuel, vous pouvez désactiver HMA.</span><span class="sxs-lookup"><span data-stu-id="a4bab-105">If you've enabled Hybrid Modern Authentication (HMA) only to find it's unsuitable for your current environment, you can disable HMA.</span></span> <span data-ttu-id="a4bab-106">Cet article explique comment.</span><span class="sxs-lookup"><span data-stu-id="a4bab-106">This article explains how.</span></span>
  
## <a name="who-is-this-article-for"></a><span data-ttu-id="a4bab-107">Qui cet article est-il pour ?</span><span class="sxs-lookup"><span data-stu-id="a4bab-107">Who is this article for?</span></span>

<span data-ttu-id="a4bab-108">Si vous avez activé l’authentification moderne dans Skype Entreprise Online ou en local, et/ou Exchange Online ou en local et que vous avez trouvé que vous devez désactiver HMA, ces étapes sont à votre place.</span><span class="sxs-lookup"><span data-stu-id="a4bab-108">If you've enabled Modern Authentication in Skype for Business Online or On-premises, and/or Exchange Online or On-premises and found you need to disable HMA, these steps are for you.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4bab-109">Consultez l’article «[topologies](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported)Skype Entreprise pris en charge avec l’authentification moderne » si vous êtes dans Skype Entreprise Online ou en local, que vous avez un HMA de topologie mixte et que vous devez examiner les topologies pris en charge avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="a4bab-109">See the '[Skype for Business topologies supported with Modern Authentication](/skypeforbusiness/plan-your-deployment/modern-authentication/topologies-supported)' article if you're in Skype for Business Online or On-premises, have a mixed-topology HMA, and need to look at supported topologies before you begin.</span></span>
  
## <a name="how-to-disable-hybrid-modern-authentication-exchange"></a><span data-ttu-id="a4bab-110">Comment désactiver l’authentification moderne hybride (Exchange)</span><span class="sxs-lookup"><span data-stu-id="a4bab-110">How to disable Hybrid Modern Authentication (Exchange)</span></span>

1. <span data-ttu-id="a4bab-111">**Exchange local**: ouvrez l’Exchange Management Shell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4bab-111">**Exchange On-premises**: Open the Exchange Management Shell and run the following commands:</span></span> 

```powershell
Set-OrganizationConfig -OAuth2ClientProfileEnabled $false
Set-AuthServer -Identity evoSTS -IsDefaultAuthorizationEndpoint $false
```

2. <span data-ttu-id="a4bab-112">**Exchange Online**: [Connecter à Exchange Online](/powershell/exchange/connect-to-exchange-online-powershell) avec Remote PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4bab-112">**Exchange Online**: [Connect to Exchange Online](/powershell/exchange/connect-to-exchange-online-powershell) with Remote PowerShell.</span></span> <span data-ttu-id="a4bab-113">Exécutez la commande suivante pour transformer votre  *indicateur OAuth2ClientProfileEnabled*  en « false » :</span><span class="sxs-lookup"><span data-stu-id="a4bab-113">Run the following command to turn your  *OAuth2ClientProfileEnabled*  flag to 'false':</span></span>

```powershell    
Set-OrganizationConfig -OAuth2ClientProfileEnabled:$false
```
    
## <a name="how-to-disable-hybrid-modern-authentication-skype-for-business"></a><span data-ttu-id="a4bab-114">Comment désactiver l’authentification moderne hybride (Skype Entreprise)</span><span class="sxs-lookup"><span data-stu-id="a4bab-114">How to disable Hybrid Modern Authentication (Skype for Business)</span></span>

1. <span data-ttu-id="a4bab-115">**Skype Entreprise local**: exécutez les commandes suivantes dans Skype Entreprise Management Shell :</span><span class="sxs-lookup"><span data-stu-id="a4bab-115">**Skype for Business On-premises**: Run the following commands in Skype for Business Management Shell:</span></span>

```powershell
Set-CsOAuthConfiguration -ClientAuthorizationOAuthServerIdentity ""
```

2. <span data-ttu-id="a4bab-116">**Skype Entreprise Online :** [Connecter à Skype Entreprise Online avec](manage-skype-for-business-online-with-microsoft-365-powershell.md) Remote PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a4bab-116">**Skype for Business Online**: [Connect to Skype for Business Online](manage-skype-for-business-online-with-microsoft-365-powershell.md) with Remote PowerShell.</span></span> <span data-ttu-id="a4bab-117">Exécutez la commande suivante pour désactiver l’authentification moderne :</span><span class="sxs-lookup"><span data-stu-id="a4bab-117">Run the following command to disable Modern Authentication:</span></span>

```powershell    
Set-CsOAuthConfiguration -ClientAdalAuthOverride Disallowed
```

<span data-ttu-id="a4bab-118">[Revenir à la vue d’ensemble de l’authentification moderne.](hybrid-modern-auth-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a4bab-118">[Link back to the Modern Authentication overview](hybrid-modern-auth-overview.md) .</span></span> 
