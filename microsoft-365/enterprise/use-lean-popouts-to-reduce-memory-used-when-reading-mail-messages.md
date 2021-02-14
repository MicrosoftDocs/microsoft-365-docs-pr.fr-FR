---
title: Utiliser des fenêtres publicitaires légères pour réduire la mémoire utilisée lors de la lecture des messages électroniques
ms.author: kvice
author: kelleyvice-msft
manager: laurawi
ms.date: 12/3/2019
audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a6d6ba01-2562-4c3d-a8f1-78748dd506cf
f1.keywords:
- NOCSH
description: Cet article contient des informations sur l’utilisation de fenêtres popout légères pour améliorer les performances de téléchargement des messages dans Outlook sur le web.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 7bf53464ac6b2783fbbfc335fd4ff73dbe4435fb
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690106"
---
# <a name="use-lean-popouts-to-reduce-memory-used-when-reading-mail-messages"></a><span data-ttu-id="c4293-103">Utiliser des fenêtres publicitaires légères pour réduire la mémoire utilisée lors de la lecture des messages électroniques</span><span class="sxs-lookup"><span data-stu-id="c4293-103">Use lean popouts to reduce memory used when reading mail messages</span></span>

<span data-ttu-id="c4293-104">Cet article contient des informations pour améliorer les performances de téléchargement des messages dans Outlook sur le web.</span><span class="sxs-lookup"><span data-stu-id="c4293-104">This article contains information for improving message download performance in Outlook on the web.</span></span> <span data-ttu-id="c4293-105">Cet article fait partie de la planification réseau et de l’optimisation des performances pour le projet [Office 365.](https://aka.ms/tune)</span><span class="sxs-lookup"><span data-stu-id="c4293-105">This article is part of the [Network planning and performance tuning for Office 365](https://aka.ms/tune) project.</span></span>
  
<span data-ttu-id="c4293-106">En tant qu’administrateur général Office 365, vous pouvez configurer Outlook sur le web pour fournir des fenêtres _publicitaires légères,_ une version plus petite et moins intensive de la mémoire de certains messages électroniques dans Microsoft Edge ou Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c4293-106">As an Office 365 global administrator, you can configure Outlook on the web to deliver _lean popouts_, a smaller, less memory-intensive version of certain email messages in Microsoft Edge or Internet Explorer.</span></span> <span data-ttu-id="c4293-107">Lorsque des fenêtres popout légères sont configurées pour Outlook sur le web, les composants restituer côté serveur sont chargés pour optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="c4293-107">When lean popouts are configured for Outlook on the web, server-side rendered components are loaded that optimize performance.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c4293-108">Depuis mars 2018, les fenêtres publicitaires légères ne sont pas disponibles pour les messages qui spécifient des restrictions de droits d’utilisation, telles que la Gestion des droits d’information (IRM).</span><span class="sxs-lookup"><span data-stu-id="c4293-108">As of March 2018, lean popouts are not available for messages that specify usage rights restrictions, such as Information Rights Management (IRM).</span></span>
  
<span data-ttu-id="c4293-109">Ces fonctionnalités continueront de fonctionner dans la fenêtre principale, mais ne sont pas disponibles dans les fenêtres popout légères :</span><span class="sxs-lookup"><span data-stu-id="c4293-109">These features will continue to work in the main window but are not available in lean popouts:</span></span>
  
- <span data-ttu-id="c4293-110">Compléments Outlook</span><span class="sxs-lookup"><span data-stu-id="c4293-110">Outlook add-ins</span></span>
  
- <span data-ttu-id="c4293-111">Présence de Skype Entreprise</span><span class="sxs-lookup"><span data-stu-id="c4293-111">Skype for Business presence</span></span>
  
## <a name="to-configure-lean-popouts-for-all-users-within-your-office-365-organization"></a><span data-ttu-id="c4293-112">Pour configurer des fenêtres pop-out allégées pour tous les utilisateurs de votre organisation Office 365</span><span class="sxs-lookup"><span data-stu-id="c4293-112">To configure lean popouts for all users within your Office 365 organization</span></span>
  
1. <span data-ttu-id="c4293-113">[Connectez-vous à Exchange Online à l’aide de Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx ).</span><span class="sxs-lookup"><span data-stu-id="c4293-113">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx ).</span></span>
  
2. <span data-ttu-id="c4293-114">Exécutez la cmdlet [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443%28v=exchg.160%29.aspx) avec le paramètre LeanPopoutEnabled comme suit :</span><span class="sxs-lookup"><span data-stu-id="c4293-114">Run the [Set-OrganizationConfig](https://technet.microsoft.com/library/aa997443%28v=exchg.160%29.aspx) cmdlet with the LeanPopoutEnabled parameter as follows:</span></span>

  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled <$true |$false >
  ```

  <span data-ttu-id="c4293-115">Par exemple, pour activer les fenêtres pop-out allégées pour tous les utilisateurs de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c4293-115">For example, to enable lean popouts for all users in your organization:</span></span>
  
  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled $true
  ```

  <span data-ttu-id="c4293-116">Pour désactiver les fenêtres pop-out allégées pour tous les utilisateurs de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c4293-116">To disable lean popouts for all users in your organization:</span></span>

  ```powershell
  Set-OrganizationConfig -LeanPopoutEnabled $false
  ```
