---
title: Configurer la protection anti-hameçonnage
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
- okr_smb
monikerRange: o365-worldwide
search.appverid:
- BCS160
- MET150
- MOE150
description: Découvrez comment configurer la protection anti-hameçonnage.
ms.openlocfilehash: bcb6b8bac316b4b74c505656cb9a93e7a87e0830
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49927873"
---
# <a name="set-up-anti-phishing"></a><span data-ttu-id="259b9-103">Configurer les stratégies d’anti-hameçonnage et d’anti-hameçonnage</span><span class="sxs-lookup"><span data-stu-id="259b9-103">Set up anti-phishing</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWvt9r?autoplay=false]

<span data-ttu-id="259b9-104">Le hameçonnage est une attaque malveillante dans laquelle un e-mail semble avoir été envoyé à partir d’une source familière, mais il tente de collecter vos informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="259b9-104">Phishing is a malicious attack where an email looks like it was sent from a familiar source, but it attempts to collect your personal information.</span></span> <span data-ttu-id="259b9-105">Par défaut, Microsoft 365 inclut une protection anti-hameçonnage, mais vous pouvez augmenter cette protection en affinant les paramètres.</span><span class="sxs-lookup"><span data-stu-id="259b9-105">By default, Microsoft 365 includes some anti-phishing protection, but you can increase that protection by refining the settings.</span></span> <span data-ttu-id="259b9-106">Examinons ce qui se fait.</span><span class="sxs-lookup"><span data-stu-id="259b9-106">Let's take a look.</span></span>

## <a name="try-it"></a><span data-ttu-id="259b9-107">Essayez !</span><span class="sxs-lookup"><span data-stu-id="259b9-107">Try it!</span></span>

1. <span data-ttu-id="259b9-108">Dans le centre d’administration, [https://admin.microsoft.com](https://admin.microsoft.com) sélectionnez **Sécurité,** **Gestion** des **menaces, Stratégie,** puis **Anti-hameçonnage ATP**.</span><span class="sxs-lookup"><span data-stu-id="259b9-108">In the admin center at [https://admin.microsoft.com](https://admin.microsoft.com), select **Security**, **Threat Management**, **Policy**, then **ATP Anti-phishing**.</span></span>
1. <span data-ttu-id="259b9-109">Sélectionnez **Stratégie par défaut** pour l’affiner.</span><span class="sxs-lookup"><span data-stu-id="259b9-109">Select **Default Policy** to refine it.</span></span>
1. <span data-ttu-id="259b9-110">Dans la section **Emprunt d’identité,** sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="259b9-110">In the **Impersonation** section, select **Edit**.</span></span>
1. <span data-ttu-id="259b9-111">Go to **Add domains to protect** and select the toggle to automatically include the domains you own.</span><span class="sxs-lookup"><span data-stu-id="259b9-111">Go to **Add domains to protect** and select the toggle to automatically include the domains you own.</span></span>
1. <span data-ttu-id="259b9-112">Go to **Actions**, open the drop-down **If email is sent by an impersonated user**, and choose the action you want.</span><span class="sxs-lookup"><span data-stu-id="259b9-112">Go to **Actions**, open the drop-down **If email is sent by an impersonated user**, and choose the action you want.</span></span>

    <span data-ttu-id="259b9-113">Ouvrez la liste liste si **le courrier électronique** est envoyé par un domaine dont l’identité a été usurpée et choisissez l’action de votre choix.</span><span class="sxs-lookup"><span data-stu-id="259b9-113">Open the drop-down **If email is sent by an impersonated domain** and choose the action you want.</span></span>
1. <span data-ttu-id="259b9-114">Sélectionnez **Activer les conseils de sécurité pour l’emprunt d’identité.**</span><span class="sxs-lookup"><span data-stu-id="259b9-114">Select **Turn on impersonation safety tips**.</span></span> <span data-ttu-id="259b9-115">Choisissez si des conseils doivent être fournis aux utilisateurs lorsque le système détecte des utilisateurs usurpés d’identité, des domaines ou des caractères inhabituels.</span><span class="sxs-lookup"><span data-stu-id="259b9-115">Choose whether tips should be provided to users when the system detects impersonated users, domains, or unusual characters.</span></span> <span data-ttu-id="259b9-116">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="259b9-116">Select **Save**.</span></span>
1. <span data-ttu-id="259b9-117">Sélectionnez **l’intelligence de** boîte aux lettres et vérifiez qu’elle est allumée.</span><span class="sxs-lookup"><span data-stu-id="259b9-117">Select **Mailbox intelligence** and verify that it's turned on.</span></span> <span data-ttu-id="259b9-118">Cela permet à votre courrier électronique d’être plus efficace en apprendant les modèles d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="259b9-118">This allows your email to be more efficient by learning usage patterns.</span></span>
1. <span data-ttu-id="259b9-119">Choose **Add trusted senders and domains**.</span><span class="sxs-lookup"><span data-stu-id="259b9-119">Choose **Add trusted senders and domains**.</span></span> <span data-ttu-id="259b9-120">Ici, vous pouvez ajouter des adresses e-mail ou des domaines qui ne doivent pas être classés comme emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="259b9-120">Here you can add email addresses or domains that shouldn't be classified as an impersonation.</span></span>
1. <span data-ttu-id="259b9-121">Sélectionnez **Passer en revue vos paramètres,** assurez-vous que tout est correct, **sélectionnez Enregistrer,** puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="259b9-121">Choose **Review your settings**, make sure everything is correct, select **Save**, then **Close**.</span></span>

    <span data-ttu-id="259b9-122">Votre organisation dispose désormais d’une meilleure protection contre les menaces de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="259b9-122">Your organization now has better protection from phishing threats.</span></span>