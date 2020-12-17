---
title: Gérer les stratégies d’appareil Windows 10 professionnel avec Microsoft 365 Business Premium
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
description: Découvrez comment gérer les stratégies d’appareils Windows 10 professionnel avec Microsoft 365 Business Premium.
ms.openlocfilehash: 9052859f03035a76bf69b7c8c23c75ae00353846
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49702384"
---
# <a name="manage-windows-10-pro-device-policies"></a><span data-ttu-id="ba0fd-103">Gérer les stratégies d’appareil Windows 10 professionnel</span><span class="sxs-lookup"><span data-stu-id="ba0fd-103">Manage Windows 10 Pro device policies</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE1FYSL?autoplay=false]

<span data-ttu-id="ba0fd-104">Vous pouvez utiliser Microsoft 365 entreprise pour vous assurer que l’antivirus Windows Defender est activé sur les appareils Windows 10 et que les mises à jour Microsoft sont automatiquement téléchargées sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-104">You can use Microsoft 365 Business to ensure that Windows Defender Antivirus is activated on Windows 10 devices and Microsoft updates are automatically downloaded to users' devices.</span></span>

## <a name="try-it"></a><span data-ttu-id="ba0fd-105">Essayez !</span><span class="sxs-lookup"><span data-stu-id="ba0fd-105">Try it!</span></span>

1. <span data-ttu-id="ba0fd-106">Connectez-vous au Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-106">Sign in to the Microsoft 365 admin center.</span></span>
1. <span data-ttu-id="ba0fd-107">Sous **stratégies**, choisissez Ajouter une stratégie.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-107">Under **Policies**, choose Add policy.</span></span>
1. <span data-ttu-id="ba0fd-108">Dans le **volet ajouter une stratégie** , entrez un nom sous nom de la **stratégie**, puis sélectionnez Configuration de l' **appareil Windows 10** sous **type de stratégie**.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-108">In the **Add policy** pane, enter a name under **Policy name**, and then select **Windows 10 Device Configuration** under **Policy type**.</span></span>
1. <span data-ttu-id="ba0fd-109">Choisissez **sécuriser les appareils Windows 10** pour afficher les sous-paramètres.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-109">Choose **Secure Windows 10 devices** to see the sub-settings.</span></span>
1. <span data-ttu-id="ba0fd-110">Assurez-vous que la **protection des PC contre les virus et les autres menaces à l’aide de l’antivirus Windows Defender** et que **les appareils Windows 10 à jour** sont activés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-110">Make sure that **Help protect PCs from viruses and other threats using Windows Defender Antivirus** and **Keep Windows 10 devices up to date automatically** are turned on.</span></span>
1. <span data-ttu-id="ba0fd-111">Sous **qui va obtenir ces paramètres ?**, tous les utilisateurs sont sélectionnés par défaut, mais vous pouvez choisir **modifier** pour sélectionner les groupes de sécurité que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-111">Under **Who will get these settings?**, all users are selected by default, but you can choose **Change** to select any security groups you've created.</span></span>
1. <span data-ttu-id="ba0fd-112">Pour terminer la création de la stratégie, sélectionnez **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-112">To finish creating the policy, choose **Add**.</span></span>
1. <span data-ttu-id="ba0fd-113">Sur la page **Ajouter une stratégie** , cliquez sur **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-113">On the **Add policy** page, choose **Close**.</span></span>
1. <span data-ttu-id="ba0fd-114">Sur la page d’accueil du centre d’administration, vérifiez que votre nouvelle stratégie a été ajoutée en sélectionnant **stratégies** et en examinant votre stratégie sur la page **stratégies** .</span><span class="sxs-lookup"><span data-stu-id="ba0fd-114">On the admin center home page, confirm that your new policy was added by choosing **Policies** and reviewing your policy on the **Policies** page.</span></span>
1. <span data-ttu-id="ba0fd-115">Pour vérifier que la stratégie a pris effet, sur le périphérique Windows 10 d’un utilisateur, accédez à Windows Update, choisissez **Options avancées**, puis vérifiez que les paramètres sont grisés.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-115">To verify that the policy has taken effect, on a user's Windows 10 device, go to Windows Update, choose **Advanced options**, and confirm that settings are grayed out.</span></span>

    <span data-ttu-id="ba0fd-116">Ensuite, cliquez sur **choisir comment les mises à jour sont livrées** et vérifiez que les paramètres sont grisés et que le message suivant s’affiche : **certains paramètres sont masqués ou gérés par votre organisation**.</span><span class="sxs-lookup"><span data-stu-id="ba0fd-116">Then, click **Choose how updates are delivered**, and confirm that settings are grayed out and the following message appears: **Some settings are hidden or managed by your organization**.</span></span>

