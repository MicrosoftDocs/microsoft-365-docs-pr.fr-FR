---
title: Sécuriser les applications Office sur iOS
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
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
description: Découvrez comment sécuriser les applications Office sur iOS avec Microsoft 365 Business Premium.
ms.openlocfilehash: 197041a4eb9ada65f4b6046d93f2a856cbdfb40d
ms.sourcegitcommit: 355bd51ab6a79d5c36a4e4f57df74ae6873eba19
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "50422110"
---
# <a name="secure-office-apps-on-ios"></a><span data-ttu-id="1011e-103">Sécuriser les applications Office sur iOS</span><span class="sxs-lookup"><span data-stu-id="1011e-103">Secure Office apps on iOS</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FLvZ?autoplay=false]

<span data-ttu-id="1011e-104">Vous pouvez configurer une stratégie d’accès utilisateur qui oblige les utilisateurs mobiles à entrer un code confidentiel ou une empreinte digitale pour se connecter, et chiffre également les fichiers de travail stockés sur leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="1011e-104">You can set up a user access policy that requires mobile users to enter a PIN or fingerprint to sign in, and also encrypts work files stored on their devices.</span></span>

## <a name="try-it"></a><span data-ttu-id="1011e-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="1011e-105">Try it!</span></span>

1. <span data-ttu-id="1011e-106">Connectez-vous au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1011e-106">Sign in to the Microsoft 365 admin center.</span></span>
1. <span data-ttu-id="1011e-107">Sous **Stratégies,** choisissez **Ajouter une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="1011e-107">Under **Policies**, choose **Add policy**.</span></span>
1. <span data-ttu-id="1011e-108">Dans le **volet Ajouter une** stratégie, entrez un nom sous nom de stratégie, puis choisissez le type de stratégie que vous souhaitez sous Type de **stratégie.** </span><span class="sxs-lookup"><span data-stu-id="1011e-108">In the **Add policy** pane, enter a name under **Policy name**, and choose the policy type that you want under **Policy type**.</span></span>
1. <span data-ttu-id="1011e-109">Activer la **gestion de la façon dont les utilisateurs** accèdent aux fichiers Office sur les appareils mobiles, puis assurez-vous que les trois paramètres suivants sont actifs :</span><span class="sxs-lookup"><span data-stu-id="1011e-109">Turn on **Manage how users access Office files on mobile devices**, and then make sure the following three settings are turned on:</span></span>
    - <span data-ttu-id="1011e-110">**Exiger un code confidentiel ou une empreinte pour accéder aux applications Office**</span><span class="sxs-lookup"><span data-stu-id="1011e-110">**Require a PIN or fingerprint to access Office apps**</span></span>
    - <span data-ttu-id="1011e-111">**Protéger les fichiers de travail en cas de perte ou de vol d’appareils**</span><span class="sxs-lookup"><span data-stu-id="1011e-111">**Protect work files when devices are lost or stolen**</span></span>
    - <span data-ttu-id="1011e-112">**Chiffrer les fichiers de travail**</span><span class="sxs-lookup"><span data-stu-id="1011e-112">**Encrypt work files**</span></span>

1. <span data-ttu-id="1011e-113">Sous **Les fichiers de ces applications seront protégés,** sélectionnez les applications Office que vous souhaitez protéger sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1011e-113">Under **Files in these apps will be protected**, select the Office apps you want to protect on mobile devices.</span></span>
1. <span data-ttu-id="1011e-114">Sous **Qui obtenira ces paramètres ?**, tous les utilisateurs sont sélectionnés par défaut, mais vous pouvez choisir Modifier pour sélectionner les groupes de sécurité que vous avez créés. </span><span class="sxs-lookup"><span data-stu-id="1011e-114">Under **Who will get these settings?**, all users are selected by default, but you can choose **Change** to select any security groups you've created.</span></span>
1. <span data-ttu-id="1011e-115">Pour terminer la création de la stratégie, choisissez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="1011e-115">To finish creating the policy, choose **Add**.</span></span>
1. <span data-ttu-id="1011e-116">Dans la page **Ajouter une stratégie,** choisissez **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="1011e-116">On the **Add policy** page, choose **Close**.</span></span>
1. <span data-ttu-id="1011e-117">Dans la page d’accueil du Centre d’administration,  confirmez que votre nouvelle stratégie a été ajoutée en choisissant Stratégies et en l’avisant sur la page **Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="1011e-117">On the admin center home page, confirm that your new policy was added by choosing **Policies** and reviewing your policy on the **Policies** page.</span></span>