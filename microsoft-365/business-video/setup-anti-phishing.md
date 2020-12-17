---
title: Configuration de la protection anti-hameçonnage
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
description: Découvrez comment configurer la protection anti-hameçonnage.
ms.openlocfilehash: f3a1399c8a6a51c7b14af7ffea8fbaea39cd1541
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702234"
---
# <a name="set-up-anti-phishing"></a><span data-ttu-id="5d3ad-103">Configurer le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="5d3ad-103">Set up anti-phishing</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWvt9r?autoplay=false]

<span data-ttu-id="5d3ad-104">Le hameçonnage est une attaque malveillante dans laquelle un message électronique semble avoir été envoyé à partir d’une source familière, mais il tente de collecter vos informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-104">Phishing is a malicious attack where an email looks like it was sent from a familiar source, but it attempts to collect your personal information.</span></span> <span data-ttu-id="5d3ad-105">Par défaut, Microsoft 365 inclut une protection anti-hameçonnage, mais vous pouvez augmenter cette protection en affinant les paramètres.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-105">By default, Microsoft 365 includes some anti-phishing protection, but you can increase that protection by refining the settings.</span></span> <span data-ttu-id="5d3ad-106">Jetons un œil.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-106">Let's take a look.</span></span>

## <a name="try-it"></a><span data-ttu-id="5d3ad-107">Essayez !</span><span class="sxs-lookup"><span data-stu-id="5d3ad-107">Try it!</span></span>

1. <span data-ttu-id="5d3ad-108">Dans le centre d’administration [https://admin.microsoft.com](https://admin.microsoft.com) , sélectionnez **sécurité**, **gestion des menaces**, **stratégie**, puis **protection contre le hameçonnage (ATP**).</span><span class="sxs-lookup"><span data-stu-id="5d3ad-108">In the admin center at [https://admin.microsoft.com](https://admin.microsoft.com), select **Security**, **Threat Management**, **Policy**, then **ATP Anti-phishing**.</span></span>
1. <span data-ttu-id="5d3ad-109">Sélectionnez **stratégie par défaut** pour l’affiner.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-109">Select **Default Policy** to refine it.</span></span>
1. <span data-ttu-id="5d3ad-110">Dans la section **emprunt d’identité** , sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-110">In the **Impersonation** section, select **Edit**.</span></span>
1. <span data-ttu-id="5d3ad-111">Accédez à **Ajouter des domaines à protéger** , puis sélectionnez le bouton bascule pour inclure automatiquement les domaines que vous possédez.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-111">Go to **Add domains to protect** and select the toggle to automatically include the domains you own.</span></span>
1. <span data-ttu-id="5d3ad-112">Accédez à **actions**, ouvrez la liste déroulante **si le courrier électronique est envoyé par un utilisateur emprunté**, puis choisissez l’action souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-112">Go to **Actions**, open the drop-down **If email is sent by an impersonated user**, and choose the action you want.</span></span>

    <span data-ttu-id="5d3ad-113">Ouvrez la liste déroulante **si le courrier électronique est envoyé par un domaine emprunté** et choisissez l’action souhaitée.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-113">Open the drop-down **If email is sent by an impersonated domain** and choose the action you want.</span></span>
1. <span data-ttu-id="5d3ad-114">Sélectionnez **activer les conseils de sécurité pour l’emprunt d’identité**.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-114">Select **Turn on impersonation safety tips**.</span></span> <span data-ttu-id="5d3ad-115">Déterminez si des conseils doivent être fournis aux utilisateurs lorsque le système détecte des utilisateurs, des domaines ou des caractères inhabituels.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-115">Choose whether tips should be provided to users when the system detects impersonated users, domains, or unusual characters.</span></span> <span data-ttu-id="5d3ad-116">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-116">Select **Save**.</span></span>
1. <span data-ttu-id="5d3ad-117">Sélectionnez **intelligence des boîtes aux lettres** et vérifiez qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-117">Select **Mailbox intelligence** and verify that it's turned on.</span></span> <span data-ttu-id="5d3ad-118">Cela permet d’améliorer l’efficacité de votre courrier électronique en apprenant des modèles d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-118">This allows your email to be more efficient by learning usage patterns.</span></span>
1. <span data-ttu-id="5d3ad-119">Choisissez **Ajouter des expéditeurs et des domaines approuvés**.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-119">Choose **Add trusted senders and domains**.</span></span> <span data-ttu-id="5d3ad-120">Ici, vous pouvez ajouter des adresses de messagerie ou des domaines qui ne doivent pas être classés comme emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-120">Here you can add email addresses or domains that shouldn't be classified as an impersonation.</span></span>
1. <span data-ttu-id="5d3ad-121">Choisissez **vérifier vos paramètres**, vérifiez que tout est correct, sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-121">Choose **Review your settings**, make sure everything is correct, select **Save**, then **Close**.</span></span>

    <span data-ttu-id="5d3ad-122">Votre organisation offre désormais une meilleure protection contre les menaces de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="5d3ad-122">Your organization now has better protection from phishing threats.</span></span>