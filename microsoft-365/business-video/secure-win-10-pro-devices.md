---
title: Gérer les stratégies d’appareil Windows 10 Professionnel avec Microsoft 365 Business Premium
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
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
description: Découvrez comment gérer les stratégies d’appareil Windows 10 Professionnel avec Microsoft 365 Business Premium.
ms.openlocfilehash: 0f7cfff227e1ab4ea992414b513e341adbd9ef22
ms.sourcegitcommit: 53acc851abf68e2272e75df0856c0e16b0c7e48d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "51578686"
---
# <a name="manage-windows-10-pro-device-policies"></a><span data-ttu-id="4261e-103">Gérer les stratégies d’appareil Windows 10 Professionnel</span><span class="sxs-lookup"><span data-stu-id="4261e-103">Manage Windows 10 Pro device policies</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FYSL?autoplay=false]

<span data-ttu-id="4261e-104">Vous pouvez utiliser Microsoft 365 Business pour vous assurer que l’antivirus Windows Defender est activé sur les appareils Windows 10 et que les mises à jour Microsoft sont automatiquement téléchargées sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4261e-104">You can use Microsoft 365 Business to ensure that Windows Defender Antivirus is activated on Windows 10 devices and Microsoft updates are automatically downloaded to users' devices.</span></span>

## <a name="try-it"></a><span data-ttu-id="4261e-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="4261e-105">Try it!</span></span>

1. <span data-ttu-id="4261e-106">Connectez-vous au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="4261e-106">Sign in to the Microsoft 365 admin center.</span></span>
1. <span data-ttu-id="4261e-107">Sous **Stratégies,** choisissez Ajouter une stratégie.</span><span class="sxs-lookup"><span data-stu-id="4261e-107">Under **Policies**, choose Add policy.</span></span>
1. <span data-ttu-id="4261e-108">Dans le volet Ajouter **une** stratégie, entrez un nom sous nom de **stratégie,** puis sélectionnez Configuration de l’appareil **Windows 10** sous **Type de stratégie.**</span><span class="sxs-lookup"><span data-stu-id="4261e-108">In the **Add policy** pane, enter a name under **Policy name**, and then select **Windows 10 Device Configuration** under **Policy type**.</span></span>
1. <span data-ttu-id="4261e-109">Sélectionnez **Sécuriser les appareils Windows 10** pour voir les sous-paramètres.</span><span class="sxs-lookup"><span data-stu-id="4261e-109">Choose **Secure Windows 10 devices** to see the sub-settings.</span></span>
1. <span data-ttu-id="4261e-110">Veillez à protéger les PC contre les virus et autres menaces à l’aide de **l’antivirus Windows Defender** et que les appareils **Windows 10** sont automatiquement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="4261e-110">Make sure that **Help protect PCs from viruses and other threats using Windows Defender Antivirus** and **Keep Windows 10 devices up to date automatically** are turned on.</span></span>
1. <span data-ttu-id="4261e-111">Sous **Qui obtenira ces paramètres ?**, tous les utilisateurs sont sélectionnés par défaut, mais vous pouvez choisir Modifier pour sélectionner les groupes de sécurité que vous avez créés. </span><span class="sxs-lookup"><span data-stu-id="4261e-111">Under **Who will get these settings?**, all users are selected by default, but you can choose **Change** to select any security groups you've created.</span></span>
1. <span data-ttu-id="4261e-112">Pour terminer la création de la stratégie, choisissez **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="4261e-112">To finish creating the policy, choose **Add**.</span></span>
1. <span data-ttu-id="4261e-113">Dans la page **Ajouter une stratégie,** choisissez **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="4261e-113">On the **Add policy** page, choose **Close**.</span></span>
1. <span data-ttu-id="4261e-114">Dans la page d’accueil du Centre d’administration,  confirmez que votre nouvelle stratégie a été ajoutée en choisissant Stratégies et en l’avisant sur la page **Stratégies.**</span><span class="sxs-lookup"><span data-stu-id="4261e-114">On the admin center home page, confirm that your new policy was added by choosing **Policies** and reviewing your policy on the **Policies** page.</span></span>
1. <span data-ttu-id="4261e-115">Pour vérifier que la stratégie a pris effet, sur l’appareil Windows 10 d’un utilisateur, sélectionnez Windows Update, choisissez **Options** avancées et vérifiez que les paramètres sont grisés.</span><span class="sxs-lookup"><span data-stu-id="4261e-115">To verify that the policy has taken effect, on a user's Windows 10 device, go to Windows Update, choose **Advanced options**, and confirm that settings are grayed out.</span></span>

    <span data-ttu-id="4261e-116">Ensuite, cliquez sur Choisir la manière dont les mises à jour sont **livrées** et confirmez que les paramètres sont grisés et que le message suivant s’affiche : Certains paramètres sont masqués ou gérés par **votre organisation.**</span><span class="sxs-lookup"><span data-stu-id="4261e-116">Then, click **Choose how updates are delivered**, and confirm that settings are grayed out and the following message appears: **Some settings are hidden or managed by your organization**.</span></span>

