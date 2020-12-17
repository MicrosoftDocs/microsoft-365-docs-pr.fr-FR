---
title: Gérer les liens fiables
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
ms.collection:
- M365-subscription-management
- Adm_O365
ms.custom:
- AdminSurgePortfolio
- adminvideo
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment gérer les liens fiables afin de protéger votre entreprise contre les sites malveillants.
ms.openlocfilehash: eabb2c1f71b1183867ffcb005ba4f7e44ed6e4b7
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702066"
---
# <a name="manage-safe-links"></a><span data-ttu-id="6acf5-103">Gérer les liens fiables</span><span class="sxs-lookup"><span data-stu-id="6acf5-103">Manage Safe Links</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWvdwy?autoplay=false]

<span data-ttu-id="6acf5-104">Microsoft Defender pour Office 365, anciennement Microsoft 365 ATP, ou Advanced Threat Protection, permet de protéger votre entreprise contre les sites malveillants lorsque des personnes cliquent sur des liens dans les applications Office.</span><span class="sxs-lookup"><span data-stu-id="6acf5-104">Microsoft Defender for Office 365 , formerly called Microsoft 365 ATP, or Advanced Threat Protection, helps protect your business against malicious sites when people click links in Office apps.</span></span>

## <a name="try-it"></a><span data-ttu-id="6acf5-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="6acf5-105">Try it!</span></span>

1. <span data-ttu-id="6acf5-106">Accédez au [Centre d’administration](https://admin.microsoft.com), puis sélectionnez **configuration**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-106">Go to the [admin center](https://admin.microsoft.com), and select **Setup**.</span></span>
1. <span data-ttu-id="6acf5-107">Faites défiler vers le bas pour **augmenter la protection contre les menaces avancées**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-107">Scroll down to **Increase protection from advanced threats**.</span></span> <span data-ttu-id="6acf5-108">Sélectionnez **Afficher**, **gérer**, puis **DAV liens approuvés**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-108">Select **View**, **Manage**,and then **ATP Safe Links**.</span></span>
1. <span data-ttu-id="6acf5-109">Sous **stratégies qui s’appliquent à l’ensemble de l’organisation**, choisissez la stratégie **par défaut** , puis sélectionnez l’icône **modifier** .</span><span class="sxs-lookup"><span data-stu-id="6acf5-109">Under **Policies that apply to the entire organization**, choose the **Default** policy, and then select the **Edit** icon.</span></span>
1. <span data-ttu-id="6acf5-110">Entrez l’URL que vous souhaitez bloquer.</span><span class="sxs-lookup"><span data-stu-id="6acf5-110">Enter a URL that you want to block.</span></span>
1. <span data-ttu-id="6acf5-111">Sélectionnez **utiliser les liens fiables dans les applications Office, Office pour iOS et Android**; Sélectionnez **ne pas suivre lorsque les utilisateurs cliquent sur les liens fiables**; Sélectionnez **ne pas autoriser les utilisateurs à cliquer sur les liens fiables vers l’URL d’origine**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-111">Select **Use safe links in Office apps, Office for iOS and Android**; select **Do not track when users click safe links**; and select **Do not let users click through safe links to original URL**.</span></span> <span data-ttu-id="6acf5-112">Ces éléments peuvent déjà être sélectionnés si vous configurez la stratégie par défaut.</span><span class="sxs-lookup"><span data-stu-id="6acf5-112">These might already be selected if you set up the default policy.</span></span> <span data-ttu-id="6acf5-113">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-113">Select **Save**.</span></span>
1. <span data-ttu-id="6acf5-114">Sous **stratégies qui s’appliquent à des destinataires spécifiques**, choisissez **règle de liens approuvés recommandés**, puis sélectionnez l’icône **modifier** .</span><span class="sxs-lookup"><span data-stu-id="6acf5-114">Under **Policies that apply to specific recipients**, choose **Recommended safe links rule**, and then select the **Edit** icon.</span></span>
1. <span data-ttu-id="6acf5-115">Sélectionnez **paramètres**, faites défiler vers le bas, entrez l’URL que vous ne souhaitez pas vérifier, puis sélectionnez l’icône **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="6acf5-115">Select **settings**, scroll down, enter the URL that you do not want to be checked, and then select the **Add** icon.</span></span>
1. <span data-ttu-id="6acf5-116">Sélectionnez **appliqué à**, puis sélectionnez votre nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="6acf5-116">Select **applied to**, and then select your domain name.</span></span> <span data-ttu-id="6acf5-117">Sélectionnez les domaines supplémentaires auxquels la règle doit s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="6acf5-117">Select any additional domains that you want the rule applied to.</span></span> <span data-ttu-id="6acf5-118">Sélectionnez **Ajouter**, **OK**, puis **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="6acf5-118">Select **add**, **OK**, and then **Save**.</span></span>

<span data-ttu-id="6acf5-119">Les liens fiables ATP sont désormais configurés.</span><span class="sxs-lookup"><span data-stu-id="6acf5-119">ATP Safe Links are now configured.</span></span> <span data-ttu-id="6acf5-120">Autorisez jusqu’à 30 minutes pour que vos modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="6acf5-120">Allow up to 30 minutes for your changes to take effect.</span></span>

<span data-ttu-id="6acf5-121">Lorsqu’un utilisateur reçoit un message électronique avec des liens, les liens sont analysés.</span><span class="sxs-lookup"><span data-stu-id="6acf5-121">When a user receives an email with links, the links will be scanned.</span></span> <span data-ttu-id="6acf5-122">Si les liens sont jugés fiables, ils seront cliquables.</span><span class="sxs-lookup"><span data-stu-id="6acf5-122">If the links are deemed safe, they'll be clickable.</span></span> <span data-ttu-id="6acf5-123">Toutefois, si le lien se trouve sur la liste bloquée, les utilisateurs verront un message indiquant qu’il a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="6acf5-123">However, if the link is on the blocked list, users will see a message that it's been blocked.</span></span>