---
title: Désactiver la création de rapports de courrier indésirable dans Outlook sur le web
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8d57fe9e-57b8-4884-9317-80b380804b4a
ms.collection:
- M365-security-compliance
description: En tant qu’administrateur Office 365, vous pouvez désactiver la possibilité pour les utilisateurs de signaler le courrier indésirable.
ms.openlocfilehash: de0e5d1aa51ececafc0d344b9907f6751a613370
ms.sourcegitcommit: cbf117a4cd92a907115c9f10752f3c557361e586
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2019
ms.locfileid: "37441171"
---
# <a name="turn-off-junk-email-reporting-in-outlook-on-the-web"></a><span data-ttu-id="24b6b-103">Désactiver la création de rapports de courrier indésirable dans Outlook sur le web</span><span class="sxs-lookup"><span data-stu-id="24b6b-103">Turn off junk email reporting in Outlook on the web</span></span>

<span data-ttu-id="24b6b-104">Vous pouvez envoyer des messages indésirables, de hameçonnage et non de courrier indésirable à Microsoft à des fins d’analyse à l’aide des options de création de rapports de courrier indésirable Outlook sur le Web (anciennement appelé Outlook Web App), comme décrit dans le rapport de courrier [indésirable et les escroqueries par hameçonnage dans Outlook sur le Web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md).</span><span class="sxs-lookup"><span data-stu-id="24b6b-104">You can send junk, phishing, and not junk messages to Microsoft for analysis using the Outlook on the web (formerly known as Outlook Web App) junk email reporting options, as described in [Report junk email and phishing scams in Outlook on the web](report-junk-email-and-phishing-scams-in-outlook-on-the-web-eop.md).</span></span> <span data-ttu-id="24b6b-105">Si vous ne souhaitez pas utiliser ces options, les administrateurs peuvent les désactiver via la cmdlet [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) .</span><span class="sxs-lookup"><span data-stu-id="24b6b-105">If you don't want to use these options,admins can turn them off via the [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx) cmdlet.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="24b6b-106">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="24b6b-106">What do you need to know before you begin?</span></span>
<span data-ttu-id="24b6b-107"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="24b6b-107"></span></span>

- <span data-ttu-id="24b6b-108">Durée d'exécution estimée : 5 minutes</span><span class="sxs-lookup"><span data-stu-id="24b6b-108">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="24b6b-109">Des autorisations doivent vous être attribuées avant de pouvoir exécuter cette procédure.</span><span class="sxs-lookup"><span data-stu-id="24b6b-109">You need to be assigned permissions before you can perform this procedure or procedures.</span></span> <span data-ttu-id="24b6b-110">Pour voir les autorisations qui vous sont nécessaires, consultez entrée « stratégies de boîte aux lettres Outlook sur le Web » dans la rubrique [autorisations Outlook sur le Web](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) .</span><span class="sxs-lookup"><span data-stu-id="24b6b-110">To see what permissions you need, see the "Outlook on the web mailbox policies" entry in the [Outlook on the web permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx#OutlookWebApp) topic.</span></span> 

- <span data-ttu-id="24b6b-111">Pour vous connecter à Exchange Online PowerShell, voir [Connexion à Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="24b6b-111">To connect to Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

## <a name="turn-off-junk-phishing-and-not-junk-reporting-to-microsoft"></a><span data-ttu-id="24b6b-112">Désactiver le courrier indésirable, le hameçonnage et les notifications de courrier indésirable à Microsoft</span><span class="sxs-lookup"><span data-stu-id="24b6b-112">Turn off junk, phishing, and not junk reporting to Microsoft</span></span>
<span data-ttu-id="24b6b-113"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="24b6b-113"></span></span>

<span data-ttu-id="24b6b-114">Tout d’abord, exécutez la commande suivante pour obtenir les noms de vos stratégies de boîte aux lettres Outlook sur le Web disponibles :</span><span class="sxs-lookup"><span data-stu-id="24b6b-114">First, run the following command to get the names of your available Outlook on the web mailbox policies:</span></span>
  
```
Get-OwaMailboxPolicy | Format-Table Name
```

<span data-ttu-id="24b6b-115">Ensuite, utilisez la syntaxe suivante pour activer ou désactiver le signalement de courrier indésirable à Microsoft dans Outlook sur le Web :</span><span class="sxs-lookup"><span data-stu-id="24b6b-115">Next, use the following syntax to enable or disable junk and not junk reporting to Microsoft in Outlook on the web:</span></span>
  
```
Set-OwaMailboxPolicy -Identity "<OWAMailboxPolicyName>" -ReportJunkEmailEnabled <$true | $false>
```

<span data-ttu-id="24b6b-116">Cet exemple montre comment désactiver la création de rapports dans la stratégie de boîte aux lettres Outlook Web App par défaut :</span><span class="sxs-lookup"><span data-stu-id="24b6b-116">This example turns off reporting in the default Outlook web app mailbox policy:</span></span>
  
```
Set-OwaMailboxPolicy -Identity "OwaMailboxPolicy-Default" -ReportJunkEmailEnabled $false
```

<span data-ttu-id="24b6b-117">Pour obtenir des informations détaillées sur la syntaxe et les paramètres, voir [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) et [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).</span><span class="sxs-lookup"><span data-stu-id="24b6b-117">For detailed syntax and parameter information, see [Get-OwaMailboxPolicy](http://technet.microsoft.com/library/bdd580d3-8812-4b4a-93e8-c6401b0d2f0f.aspx) and [Set-OwaMailboxPolicy](http://technet.microsoft.com/library/530166f7-ab42-4609-ba73-9b5a39b567be.aspx).</span></span>

## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="24b6b-118">Comment savoir si cela a fonctionné ?</span><span class="sxs-lookup"><span data-stu-id="24b6b-118">How do you know this worked?</span></span>
<span data-ttu-id="24b6b-119"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="24b6b-119"></span></span>

<span data-ttu-id="24b6b-120">Exécutez **Get-OwaMailboxPolicy** pour vérifier les valeurs des paramètres, puis ouvrez Outlook sur le Web pour un utilisateur affecté (auquel la stratégie de boîte aux lettres Outlook sur le Web est appliquée) et vérifiez que les options de signalement de courrier indésirable, de hameçonnage et non de courrier indésirable ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="24b6b-120">Run **Get-OWAMailboxPolicy** to check the parameter values, and then open Outlook on the web for an affected user (who has the Outlook on the web mailbox policy applied to them) and verify that the options to report junk, phishing, and not junk are not available.</span></span> <span data-ttu-id="24b6b-121">Vous serez toujours en mesure de marquer les messages comme courriers indésirables, de hameçonnage et non comme courriers indésirables, mais vous ne pourrez pas les signaler.</span><span class="sxs-lookup"><span data-stu-id="24b6b-121">You'll still be able to mark messages as junk, phishing, and not junk, but you won't be able to report them.</span></span> 
