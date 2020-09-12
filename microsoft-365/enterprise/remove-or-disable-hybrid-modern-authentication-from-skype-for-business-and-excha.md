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
description: Cet article explique comment supprimer ou désactiver l’authentification moderne hybride de Skype entreprise et d’Exchange.
ms.openlocfilehash: 70f62b9b2165464837aa1dea0e12854df116efe0
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47547095"
---
# <a name="removing-or-disabling-hybrid-modern-authentication-from-skype-for-business-and-exchange"></a><span data-ttu-id="157fe-103">Suppression ou désactivation de l’authentification moderne hybride à partir de Skype Entreprise et Exchange</span><span class="sxs-lookup"><span data-stu-id="157fe-103">Removing or disabling Hybrid Modern Authentication from Skype for Business and Exchange</span></span>

<span data-ttu-id="157fe-104">*Cet article est valable pour Microsoft 365 Entreprise et Office 365 Entreprise.*</span><span class="sxs-lookup"><span data-stu-id="157fe-104">*This article applies to both Microsoft 365 Enterprise and Office 365 Enterprise.*</span></span>

<span data-ttu-id="157fe-105">Si vous avez activé uniquement l’authentification moderne hybride (HMA) pour qu’elle ne soit pas appropriée pour votre environnement actuel, vous pouvez désactiver la HMA.</span><span class="sxs-lookup"><span data-stu-id="157fe-105">If you've enabled Hybrid Modern Authentication (HMA) only to find it's unsuitable for your current environment, you can disable HMA.</span></span> <span data-ttu-id="157fe-106">Cet article explique comment procéder.</span><span class="sxs-lookup"><span data-stu-id="157fe-106">This article explains how.</span></span>
  
## <a name="who-is-this-article-for"></a><span data-ttu-id="157fe-107">À qui est destiné cet article ?</span><span class="sxs-lookup"><span data-stu-id="157fe-107">Who is this article for?</span></span>

<span data-ttu-id="157fe-108">Si vous avez activé l’authentification moderne dans Skype entreprise Online ou en local, et/ou Exchange Online ou en local et que vous avez besoin de désactiver la haute disponibilité, ces étapes sont pour vous.</span><span class="sxs-lookup"><span data-stu-id="157fe-108">If you've enabled Modern Authentication in Skype for Business Online or On-premises, and/or Exchange Online or On-premises and found you need to disable HMA, these steps are for you.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="157fe-109">Reportez-vous à l’article «[topologies Skype entreprise prises en charge avec l’authentification moderne](https://technet.microsoft.com/library/mt803262.aspx)» si vous êtes dans Skype entreprise Online ou en local, que vous disposez d’une mémoire HMA mixte et que vous devez consulter les topologies prises en charge avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="157fe-109">See the '[Skype for Business topologies supported with Modern Authentication](https://technet.microsoft.com/library/mt803262.aspx)' article if you're in Skype for Business Online or On-premises, have a mixed-topology HMA, and need to look at supported topologies before you begin.</span></span>
  
## <a name="how-to-disable-hybrid-modern-authentication-exchange"></a><span data-ttu-id="157fe-110">Désactivation de l’authentification moderne hybride (Exchange)</span><span class="sxs-lookup"><span data-stu-id="157fe-110">How to disable Hybrid Modern Authentication (Exchange)</span></span>

1. <span data-ttu-id="157fe-111">**Exchange local**: Ouvrez l’environnement de commande Exchange Management Shell et exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="157fe-111">**Exchange On-premises**: Open the Exchange Management Shell and run the following commands:</span></span> 

```powershell
Set-OrganizationConfig -OAuth2ClientProfileEnabled $false
Set-AuthServer -Identity evoSTS -IsDefaultAuthorizationEndpoint $false
```

2. <span data-ttu-id="157fe-112">**Exchange Online**: [Connectez-vous à Exchange Online](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) à l’aide de PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="157fe-112">**Exchange Online**: [Connect to Exchange Online](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell) with Remote PowerShell.</span></span> <span data-ttu-id="157fe-113">Exécutez la commande suivante pour transformer votre indicateur  *OAuth2ClientProfileEnabled*  en « false » :</span><span class="sxs-lookup"><span data-stu-id="157fe-113">Run the following command to turn your  *OAuth2ClientProfileEnabled*  flag to 'false':</span></span>

```powershell    
Set-OrganizationConfig -OAuth2ClientProfileEnabled:$false
```
    
## <a name="how-to-disable-hybrid-modern-authentication-skype-for-business"></a><span data-ttu-id="157fe-114">Procédure de désactivation de l’authentification moderne hybride (Skype entreprise)</span><span class="sxs-lookup"><span data-stu-id="157fe-114">How to disable Hybrid Modern Authentication (Skype for Business)</span></span>

1. <span data-ttu-id="157fe-115">**Skype entreprise en local**: exécutez les commandes suivantes dans Skype entreprise Management Shell :</span><span class="sxs-lookup"><span data-stu-id="157fe-115">**Skype for Business On-premises**: Run the following commands in Skype for Business Management Shell:</span></span>

```powershell
Set-CsOAuthConfiguration -ClientAuthorizationOAuthServerIdentity ""
```

2. <span data-ttu-id="157fe-116">**Skype entreprise Online**: [Connectez-vous à Skype entreprise Online](manage-skype-for-business-online-with-microsoft-365-powershell.md) avec PowerShell à distance.</span><span class="sxs-lookup"><span data-stu-id="157fe-116">**Skype for Business Online**: [Connect to Skype for Business Online](manage-skype-for-business-online-with-microsoft-365-powershell.md) with Remote PowerShell.</span></span> <span data-ttu-id="157fe-117">Exécutez la commande suivante pour désactiver l’authentification moderne :</span><span class="sxs-lookup"><span data-stu-id="157fe-117">Run the following command to disable Modern Authentication:</span></span>

```powershell    
Set-CsOAuthConfiguration -ClientAdalAuthOverride Disallowed
```

<span data-ttu-id="157fe-118">[Revenez à la vue d’ensemble de l’authentification moderne](hybrid-modern-auth-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="157fe-118">[Link back to the Modern Authentication overview](hybrid-modern-auth-overview.md) .</span></span> 
  

