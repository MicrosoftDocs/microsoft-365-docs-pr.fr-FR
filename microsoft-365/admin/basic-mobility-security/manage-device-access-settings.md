---
title: Gérer les paramètres d’accès aux appareils dans la sécurité et la mobilité de base
f1.keywords:
- NOCSH
ms.author: kwekua
author: kwekua
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Adm_O365
- Adm_TOC
ms.custom:
- AdminSurgePortfolio
search.appverid:
- MET150
description: La sécurité et la mobilité de base peuvent vous aider à sécuriser et gérer les appareils mobiles.
ms.openlocfilehash: e66465d312c4268aca82677fa4e517aaeb822ce3
ms.sourcegitcommit: aeb94601a81db3ead8610c2f36cff30eb9fe10e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "47430152"
---
# <a name="manage-device-access-settings-in-basic-mobility-and-security"></a><span data-ttu-id="75b03-103">Gérer les paramètres d’accès aux appareils dans la sécurité et la mobilité de base</span><span class="sxs-lookup"><span data-stu-id="75b03-103">Manage device access settings in Basic Mobility and Security</span></span>

<span data-ttu-id="75b03-104">Si vous utilisez la mobilité et la sécurité de base, il est possible que vous ne puissiez pas gérer les appareils avec la sécurité et la mobilité de base.</span><span class="sxs-lookup"><span data-stu-id="75b03-104">If you're using Basic Mobility and Security, there might be devices that you can't manage with Basic Mobility and Security.</span></span> <span data-ttu-id="75b03-105">Si c’est le cas, vous devez bloquer l’accès de l’application Exchange ActiveSync aux courriers électroniques Microsoft 365 pour les appareils mobiles qui ne sont pas pris en charge par la sécurité et la mobilité de base.</span><span class="sxs-lookup"><span data-stu-id="75b03-105">If so, you should block Exchange ActiveSync app access to Microsoft 365 email for mobile devices that aren't supported by Basic Mobility and Security.</span></span> <span data-ttu-id="75b03-106">Cela permet de sécuriser les informations de votre organisation sur plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="75b03-106">This helps secure your organization information across more devices.</span></span>

<span data-ttu-id="75b03-107">Procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="75b03-107">Use these steps:</span></span>

1. <span data-ttu-id="75b03-108">Connectez-vous à Microsoft 365 avec votre compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="75b03-108">Sign in to  Microsoft 365 with your global admin account.</span></span>
    
2. <span data-ttu-id="75b03-109">Dans votre navigateur, tapez :  [https://protection.office.com](https://protection.office.com/) .</span><span class="sxs-lookup"><span data-stu-id="75b03-109">In your browser, type: [https://protection.office.com](https://protection.office.com/).</span></span>    

    >[!IMPORTANT]
    ><span data-ttu-id="75b03-110">S’il s’agit de la première fois que vous utilisez MDM pour Microsoft 365 Business standard, activez-la ici : [activer la gestion des appareils mobiles](https://admin.microsoft.com/EAdmin/Device/IntuneInventory.aspx).</span><span class="sxs-lookup"><span data-stu-id="75b03-110">If this is the first time you're using MDM for Microsoft 365 Business Standard, activate it here: [Activate Mobile Device Management](https://admin.microsoft.com/EAdmin/Device/IntuneInventory.aspx).</span></span> <span data-ttu-id="75b03-111">Une fois que vous l’avez activé, gérez vos appareils avec [Office 365 Security & Compliance](https://protection.office.com/).</span><span class="sxs-lookup"><span data-stu-id="75b03-111">After you've activated it, manage your devices with [Office 365 Security & Compliance](https://protection.office.com/).</span></span>

3. <span data-ttu-id="75b03-112">Accédez à protection contre la perte de données >stratégies d’appareil de  **gestion des appareils**   >  **Device policies**et sélectionnez **gérer les paramètres d’accès aux appareils à l’échelle de l’organisation**.</span><span class="sxs-lookup"><span data-stu-id="75b03-112">Go to Data loss prevention > **Device management** > **Device policies**, and select **Manage organization-wide device access settings**.</span></span>
    
4. <span data-ttu-id="75b03-113">Sélectionnez **bloquer**.</span><span class="sxs-lookup"><span data-stu-id="75b03-113">Select **Block**.</span></span>

    :::image type="content" source="../../media/basic-mobility-security/bms-5-block-access.png" alt-text="Case à cocher accès aux blocs de sécurité et de mobilité de base":::

5. <span data-ttu-id="75b03-115">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="75b03-115">Select **Save**.</span></span> 

<span data-ttu-id="75b03-116">Pour connaître les appareils pris en charge par la mobilité et la sécurité de base, reportez-vous à la rubrique [fonctionnalités de base et de sécurité](capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="75b03-116">To learn what devices Basic Mobility and Security supports, see [Capabilities of Basic Mobility and Security](capabilities.md).</span></span>