---
title: Créer un groupe Microsoft 365 avec un PDL spécifique
ms.reviewer: adwood
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: o365-solutions
f1.keywords:
- NOCSH
ms.collection: Strat_SP_gtc
localization_priority: Normal
description: Découvrez comment créer un groupe Microsoft 365 avec un emplacement de données par défaut spécifié dans un environnement multi-géo.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 5af32827d11289f7a966311080d2c15197786799
ms.sourcegitcommit: 27daadad9ca0f02a833ff3cff8a574551b9581da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2020
ms.locfileid: "47547733"
---
# <a name="create-a-microsoft-365-group-with-a-specific-pdl"></a><span data-ttu-id="8454c-103">Créer un groupe Microsoft 365 avec un PDL spécifique</span><span class="sxs-lookup"><span data-stu-id="8454c-103">Create a Microsoft 365 Group with a specific PDL</span></span>

<span data-ttu-id="8454c-104">Lorsque les utilisateurs dans un environnement multi-géo créent un groupe Microsoft 365, l’emplacement des données par défaut du groupe est automatiquement défini sur celui de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8454c-104">When users in a multi-geo environment create a Microsoft 365 Group, the group preferred data location is automatically set to that of the user.</span></span> <span data-ttu-id="8454c-105">Les administrateurs Exchange, SharePoint et généraux peuvent créer des groupes dans n’importe quelle région sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="8454c-105">Global, SharePoint, and Exchange Administrators can create groups in any region they select.</span></span> 

<span data-ttu-id="8454c-106">Si vous devez créer un groupe avec un emplacement par défaut des données spécifique, vous le faire à l’aide de l’applet de commande Microsoft PowerShell New-UnifiedGroup d’Exchange Online ou à partir du Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8454c-106">If you need to create a group with a specific PDL, you can do that using from the SharePoint admin center or through the Exchange Online New-UnifiedGroup Microsoft PowerShell cmdlet.</span></span> <span data-ttu-id="8454c-107">Lorsque vous procédez de la sorte, la boîte aux lettres de groupe et le site SharePoint associé à celui-ci sont configurés dans l’emplacement par défaut des données spécifié.</span><span class="sxs-lookup"><span data-stu-id="8454c-107">When you do this, both the group mailbox and SharePoint site associated with the group will be provisioned in the specified PDL.</span></span>

<span data-ttu-id="8454c-108">Pour créer un groupe Microsoft 365 avec le langage PDL que vous spécifiez, accédez au centre d’administration SharePoint à l’emplacement géographique dans lequel vous souhaitez créer le site de groupe.</span><span class="sxs-lookup"><span data-stu-id="8454c-108">To create a Microsoft 365 Group with the PDL that you specify, go to the SharePoint admin center in the geo location where you want to create the group site.</span></span>

<span data-ttu-id="8454c-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8454c-109">For example:</span></span>

<span data-ttu-id="8454c-110">Si vous souhaitez créer un site de groupe à partir de votre emplacement en Australie, vous pouvez aller à https://ContosoAUS-admin.sharepoint.com/_layouts/15/online/AdminHome.aspx#/siteManagement</span><span class="sxs-lookup"><span data-stu-id="8454c-110">If you want to create a group site in your Australia location, you can go to https://ContosoAUS-admin.sharepoint.com/_layouts/15/online/AdminHome.aspx#/siteManagement</span></span>

1. <span data-ttu-id="8454c-111">Sélectionnez **+ Créer**.</span><span class="sxs-lookup"><span data-stu-id="8454c-111">Select **+ Create**.</span></span>
2. <span data-ttu-id="8454c-112">Suivez le processus pour créer un site de groupe.</span><span class="sxs-lookup"><span data-stu-id="8454c-112">Follow the process to create a group site.</span></span>

<span data-ttu-id="8454c-113">Votre site de groupe est configuré dans l’emplacement géographique correspondant au Centre d’administration SharePoint à partir duquel vous avez initié la demande de création de site.</span><span class="sxs-lookup"><span data-stu-id="8454c-113">Your group site will be provisioned in the geo location corresponding to the SharePoint admin center from which you initiated the site creation request.</span></span> 

<span data-ttu-id="8454c-114">Utilisation d’Exchange PowerShell</span><span class="sxs-lookup"><span data-stu-id="8454c-114">Using Exchange PowerShell</span></span> 

<span data-ttu-id="8454c-115">Connectez-vous à Exchange Online PowerShell en transmettant le paramètre *-MailBoxRegion* avec le code d’emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="8454c-115">Connect to Exchange Online PowerShell and pass the parameter *-MailBoxRegion* with the geo location code.</span></span>

<span data-ttu-id="8454c-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="8454c-116">For example:</span></span> 

```PowerShell
New-UnifiedGroup -DisplayName MultiGeoEUR -Alias "MultiGeoEUR" -AccessType Public -MailboxRegion EUR 
```

![Capture d’écran de la cmdlet PowerShell New-UnifiedGroup avec la syntaxe](../media/multi-geo-new-group-with-pdl-powershell.png)

<span data-ttu-id="8454c-118">Notez que l’approvisionnement du site du groupe SharePoint est à la demande.</span><span class="sxs-lookup"><span data-stu-id="8454c-118">Note that SharePoint group site provisioning is on-demand.</span></span> <span data-ttu-id="8454c-119">Le site est approvisionné la première fois qu’un propriétaire ou un membre du groupe tente d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="8454c-119">The site will be provisioned the first time a group owner or member attempts to access it.</span></span>

## <a name="geo-location-codes"></a><span data-ttu-id="8454c-120">Codes d’emplacement géographique</span><span class="sxs-lookup"><span data-stu-id="8454c-120">Geo location codes</span></span>

[!INCLUDE [Microsoft 365 Multi-Geo locations](../includes/microsoft-365-multi-geo-locations.md)]

## <a name="related-topics"></a><span data-ttu-id="8454c-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8454c-121">Related topics</span></span>

[<span data-ttu-id="8454c-122">Connexion à Exchange Online PowerShell</span><span class="sxs-lookup"><span data-stu-id="8454c-122">Connect to Exchange Online PowerShell</span></span>](https://docs.microsoft.com/powershell/exchange/connect-to-exchange-online-powershell)
