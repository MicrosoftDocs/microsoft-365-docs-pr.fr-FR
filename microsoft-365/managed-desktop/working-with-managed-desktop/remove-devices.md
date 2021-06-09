---
title: Supprimer des appareils
description: Supprimer des appareils de la gestion Bureau géré Microsoft gestion
ms.service: m365-md
author: jaimeo
f1.keywords:
- NOCSH
ms.author: jaimeo
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
manager: laurawi
ms.topic: article
audience: Admin
ms.openlocfilehash: fa1cb7307fddd815a2a9249c5a98739d21bd2418
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51893733"
---
# <a name="remove-devices"></a><span data-ttu-id="40d6c-103">Supprimer des appareils</span><span class="sxs-lookup"><span data-stu-id="40d6c-103">Remove devices</span></span>

<span data-ttu-id="40d6c-104">Vous pouvez supprimer des appareils de Bureau géré Microsoft gestion à l’aide du portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="40d6c-104">You can remove devices from Microsoft Managed Desktop management by using the Admin portal.</span></span> <span data-ttu-id="40d6c-105">Cette action est permanente, mais vous pouvez les inscrire à nouveau auprès Bureau géré Microsoft en suivant les étapes [d’inscription.](../get-started/register-devices-self.md)</span><span class="sxs-lookup"><span data-stu-id="40d6c-105">This action is permanent, but you can register them with Microsoft Managed Desktop again by following the [registration steps](../get-started/register-devices-self.md).</span></span>

<span data-ttu-id="40d6c-106">Lorsque vous supprimez un appareil, toutes les choses suivantes se produisent :</span><span class="sxs-lookup"><span data-stu-id="40d6c-106">When you remove a device, all of the following occur:</span></span>

- <span data-ttu-id="40d6c-107">Nous ôtons l’appareil d’Autopilot.</span><span class="sxs-lookup"><span data-stu-id="40d6c-107">We remove the device from Autopilot.</span></span>
- <span data-ttu-id="40d6c-108">Nous ôtons l’appareil de tous les groupes d’appareils « Espace de travail moderne ».</span><span class="sxs-lookup"><span data-stu-id="40d6c-108">We remove the device from  all "Modern Workplace" device groups.</span></span>
- <span data-ttu-id="40d6c-109">Nous ôtons l’appareil du panneau **Périphériques** dans le portail d’administration.</span><span class="sxs-lookup"><span data-stu-id="40d6c-109">We remove the device from the **Devices** blade in the Admin portal.</span></span>

<span data-ttu-id="40d6c-110">Lorsque vous supprimez un appareil, vous pouvez également le supprimer de Azure Active Directory (Azure AD) et de Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="40d6c-110">When you remove a device, you have the option to also remove it from Azure Active Directory (Azure AD) and Microsoft Intune.</span></span>
 
> [!CAUTION]
> <span data-ttu-id="40d6c-111">La suppression des objets liés à un appareil d’Azure AD et Microsoft Intune est permanente.</span><span class="sxs-lookup"><span data-stu-id="40d6c-111">Removing the objects related to a device from Azure AD and Microsoft Intune is permanent.</span></span> <span data-ttu-id="40d6c-112">Si vous supprimez les objets, vous ne pourrez pas afficher ou gérer les appareils à partir des portails Intune et Azure.</span><span class="sxs-lookup"><span data-stu-id="40d6c-112">If you remove the objects, you won't be able to view or manage the devices from the Intune and Azure portals.</span></span> <span data-ttu-id="40d6c-113">Les appareils ne pourront pas accéder aux ressources d’entreprise de leur entreprise.</span><span class="sxs-lookup"><span data-stu-id="40d6c-113">The devices won't be able to access their company's corporate resources.</span></span> <span data-ttu-id="40d6c-114">Les données d’entreprise peuvent être supprimées si les appareils tentent de se connecter après leur suppression.</span><span class="sxs-lookup"><span data-stu-id="40d6c-114">Company data might be deleted from them if the devices try to sign in after they're deleted.</span></span>

1. <span data-ttu-id="40d6c-115">Dans [Microsoft Endpoint Manager,](https://endpoint.microsoft.com/) **sélectionnez Appareils** dans le volet de navigation de gauche.</span><span class="sxs-lookup"><span data-stu-id="40d6c-115">In [Microsoft Endpoint Manager](https://endpoint.microsoft.com/), select **Devices** in the left navigation pane.</span></span>
2. <span data-ttu-id="40d6c-116">Recherchez la **Bureau géré Microsoft** section du menu et sélectionnez **Appareils.**</span><span class="sxs-lookup"><span data-stu-id="40d6c-116">Look for the **Microsoft Managed Desktop** section of the menu and select **Devices**.</span></span>
3. <span data-ttu-id="40d6c-117">Dans l Bureau géré Microsoft de travail Appareils, sélectionnez les appareils que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="40d6c-117">In the Microsoft Managed Desktop Devices workspace, select the devices you want to delete.</span></span>
4. <span data-ttu-id="40d6c-118">Sélectionnez **Actions** de l’appareil, puis **Supprimez l’appareil** qui ouvre un écran volant pour supprimer les appareils.</span><span class="sxs-lookup"><span data-stu-id="40d6c-118">Select **Device actions**, and then select **Delete Device** which opens a fly-in to remove the devices.</span></span>
5. <span data-ttu-id="40d6c-119">Dans le fly-in, examinez les appareils sélectionnés, puis sélectionnez **Supprimer des appareils.**</span><span class="sxs-lookup"><span data-stu-id="40d6c-119">In the fly-in, review the selected devices and then select **Remove devices**.</span></span> <span data-ttu-id="40d6c-120">Si vous souhaitez également supprimer les objets Azure AD et Intune en même temps, cochez la case.</span><span class="sxs-lookup"><span data-stu-id="40d6c-120">If you want to also remove the Azure AD and Intune objects at the same time, select the check box.</span></span> <span data-ttu-id="40d6c-121">La suppression de l’appareil peut prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="40d6c-121">Device removal can take a few minutes to complete.</span></span>

> [!NOTE]
> <span data-ttu-id="40d6c-122">Vous ne pouvez pas supprimer les appareils dont l’état d’inscription **est** en attente.</span><span class="sxs-lookup"><span data-stu-id="40d6c-122">You can't remove devices that are in a **pending** registration state.</span></span>