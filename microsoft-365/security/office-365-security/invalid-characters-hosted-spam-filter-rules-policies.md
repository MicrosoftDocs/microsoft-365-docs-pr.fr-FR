---
title: Éviter les caractères non valides dans vos règles de filtrage et dans la stratégie de filtrage de courrier indésirable
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 09/24/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Fournit de l’aide aux administrateurs qui ont des caractères non valides dans leur configuration de blocage du courrier indésirable et &amp; génèrent des problèmes lors de la tentative d’utilisation du centre de sécurité conformité.
ms.openlocfilehash: f1841eb86583a48acecde0770f030b626323fa8e
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599111"
---
# <a name="avoid-invalid-characters-in-your-spam-filter-rules-and-spam-filter-policy"></a><span data-ttu-id="485d7-103">Éviter les caractères non valides dans vos règles de filtrage du courrier indésirable et votre stratégie de filtrage</span><span class="sxs-lookup"><span data-stu-id="485d7-103">Avoid invalid characters in your spam filter rules and spam filter policy</span></span> 

<span data-ttu-id="485d7-104">Auparavant, les administrateurs Office 365 configurent et configurent les règles de filtrage du courrier indésirable et la stratégie de filtrage du courrier indésirable à l’aide du centre d’administration Exchange.</span><span class="sxs-lookup"><span data-stu-id="485d7-104">Previously, Office 365 administrators set up and configured spam filter rules and the spam filter policy by using the Exchange admin center (EAC).</span></span> <span data-ttu-id="485d7-105">À présent, vous utilisez le &amp; Centre de sécurité conformité pour gérer la configuration de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="485d7-105">Now, you use the Security &amp; Compliance Center to manage the your anti-spam configuration.</span></span> <span data-ttu-id="485d7-106">Les caractères suivants étaient pris en charge dans le centre d’administration Exchange mais ne sont pas &amp; pris en charge dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="485d7-106">The following characters were supported in the EAC but are not supported for use in the Security &amp; Compliance Center.</span></span>  

<span data-ttu-id="485d7-107">**Caractères non valides :**</span><span class="sxs-lookup"><span data-stu-id="485d7-107">**Invalid characters:**</span></span>
  
```\ % & * + / = ? { } | < > ( ) ; : , [ ] "```

<span data-ttu-id="485d7-108">Si vos règles de filtrage du courrier indésirable ou votre stratégie de filtrage du courrier indésirable contient l’un des caractères non valides, vous pouvez rencontrer un ou plusieurs des problèmes suivants :</span><span class="sxs-lookup"><span data-stu-id="485d7-108">If your spam filter rules or your spam filter policy contains any of the invalid characters, you might encounter any or all of these issues:</span></span>
- <span data-ttu-id="485d7-109">Il se peut que vous ne puissiez pas trouver la stratégie ou les &amp; règles dans le centre de sécurité conformité.</span><span class="sxs-lookup"><span data-stu-id="485d7-109">You might be unable to find the policy or rules in the Security &amp; Compliance Center.</span></span>
- <span data-ttu-id="485d7-110">Vous pouvez recevoir des erreurs lors de la tentative d’obtention des règles ou de la stratégie à l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="485d7-110">You might receive errors when trying to get the rules or policy by using Windows PowerShell.</span></span>
- <span data-ttu-id="485d7-111">Vous pouvez constater que la stratégie ou les paramètres ne s’exécutent pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="485d7-111">You might find that the policy or settings do not run or perform as expected.</span></span>

## <a name="remove-the-invalid-characters-from-the-spam-filter-policy-and-rules"></a><span data-ttu-id="485d7-112">Supprimer les caractères non valides de la stratégie et des règles de filtrage du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="485d7-112">Remove the invalid characters from the spam filter policy and rules</span></span>

<span data-ttu-id="485d7-113">Une fois que vous avez identifié la stratégie et les règles qui contiennent des caractères non valides, vous pouvez modifier les noms à l’aide des applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="485d7-113">Once you have identified the policy and rules that contain invalid characters, you can change the names by using the Windows PowerShell cmdlets.</span></span> 

1. <span data-ttu-id="485d7-114">[Connectez-vous à Exchange Online à l’aide de Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="485d7-114">[Connect to Exchange Online Using Remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>
    
2. <span data-ttu-id="485d7-115">Pour modifier le nom de la stratégie de filtrage du courrier indésirable, exécutez la cmdlet Set-HostedContentFilterPolicy comme suit :</span><span class="sxs-lookup"><span data-stu-id="485d7-115">To change the name of the spam filter policy, run the Set-HostedContentFilterPolicy cmdlet as follows:</span></span>
    
    ```powershell
    Set-HostedContentFilterPolicy -Identity "Old policy name" -Name "New policy name"
    ```  

3. <span data-ttu-id="485d7-116">Pour modifier le nom d’une règle de filtrage du courrier indésirable, exécutez la cmdlet Set-Hostedcontentfilterrule permet comme suit :</span><span class="sxs-lookup"><span data-stu-id="485d7-116">To change the name of a spam filter rule, run the Set-HostedContentFilterRule cmdlet as follows:</span></span>
    
    ```powershell
    Set-HostedContentFilterRule -Identity "Old rule name" -Name "New rule name"
    ```  

  
 ## <a name="for-more-information"></a><span data-ttu-id="485d7-117">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="485d7-117">For more information</span></span>

[<span data-ttu-id="485d7-118">Gestion des menaces dans le &amp; Centre de sécurité conformité</span><span class="sxs-lookup"><span data-stu-id="485d7-118">Threat management in the Security &amp; Compliance Center</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="485d7-119">Set-HostedContentFilterPolicy</span><span class="sxs-lookup"><span data-stu-id="485d7-119">Set-HostedContentFilterPolicy</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterpolicy)

[<span data-ttu-id="485d7-120">Set-Hostedcontentfilterrule permet</span><span class="sxs-lookup"><span data-stu-id="485d7-120">Set-HostedContentFilterRule</span></span>](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedcontentfilterrule)
