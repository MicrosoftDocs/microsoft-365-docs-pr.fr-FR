---
title: 'Étape 5 : effacer et bloquer l’appareil mobile d’un ancien employé'
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
- SPO_Content
ms.custom:
- MSStore_Link
- TRN_M365B
- OKR_SMB_Videos
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
description: Suivez ces étapes pour bloquer l’accès à l’appareil mobile d’un ancien employé.
ms.openlocfilehash: 1ce12b06b6a0a74615ff8ac43b8f333456a469bb
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52244241"
---
# <a name="step-5---wipe-and-block-a-former-employees-mobile-device"></a><span data-ttu-id="04800-103">Étape 5 : effacer et bloquer l’appareil mobile d’un ancien employé</span><span class="sxs-lookup"><span data-stu-id="04800-103">Step 5 - Wipe and block a former employee's mobile device</span></span>

<span data-ttu-id="04800-104">Si votre ancien employé avait un téléphone d’organisation, vous pouvez utiliser le Centre d’administration Exchange pour effacer et bloquer cet appareil afin que toutes les données de l’organisation sont supprimées de l’appareil et qu’il ne puisse plus se connecter à Office 365.</span><span class="sxs-lookup"><span data-stu-id="04800-104">If your former employee had an organization phone, you can use the Exchange admin center to wipe and block that device so that all organization data is removed from the device and it can no longer connect to Office 365.</span></span> <span data-ttu-id="04800-105">Si votre organisation utilise Basic Mobility and Security pour gérer les appareils mobiles, vous pouvez effacer et bloquer ces appareils à l’aide de Basic Mobility and Security.</span><span class="sxs-lookup"><span data-stu-id="04800-105">If your organization uses Basic Mobility and Security to manage mobile devices, you can wipe and block those devices using Basic Mobility and Security.</span></span>

## <a name="wipe-mobile-device-using-the-exchange-admin-center"></a><span data-ttu-id="04800-106">Effacer l’appareil mobile à l’aide Exchange d’administration</span><span class="sxs-lookup"><span data-stu-id="04800-106">Wipe mobile device using the Exchange admin center</span></span>

1. <span data-ttu-id="04800-107">Accédez au <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Centre d’administration Exchange</a>.</span><span class="sxs-lookup"><span data-stu-id="04800-107">Go to the <a href="https://go.microsoft.com/fwlink/p/?linkid=2059104" target="_blank">Exchange admin center</a>.</span></span>
2. <span data-ttu-id="04800-108">Dans le Centre d'administration Exchange, accédez à **Destinataires** \> **Boîtes aux lettres**.</span><span class="sxs-lookup"><span data-stu-id="04800-108">In the Exchange admin center, navigate to **Recipients** \> **Mailboxes**.</span></span>
3. <span data-ttu-id="04800-109">Sélectionnez l’utilisateur, puis sous **Appareils mobiles,** **sélectionnez Afficher les détails.**</span><span class="sxs-lookup"><span data-stu-id="04800-109">Select the user, and under **Mobile Devices**, select **View details**.</span></span>
4. <span data-ttu-id="04800-110">Dans la page **Détails de** l’appareil mobile, sous **Appareils** mobiles, sélectionnez l’appareil mobile, sélectionnez Effacer le périphérique de effacement des données, puis ![ ](../../media/1c113a36-53cb-4974-884f-3ecd9535506e.png) sélectionnez **Bloquer**.</span><span class="sxs-lookup"><span data-stu-id="04800-110">On the **Mobile Device Details** page, under **Mobile devices**, select the mobile device, select **Wipe Data**![Wipe Device](../../media/1c113a36-53cb-4974-884f-3ecd9535506e.png), and then select **Block**.</span></span>
5. <span data-ttu-id="04800-111">Cliquez sur **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="04800-111">Select **Save**.</span></span>
   > [!TIP]
   > <span data-ttu-id="04800-112">Assurez-vous de supprimer ou de désactiver l’utilisateur de votre service Blackberry Enterprise local.</span><span class="sxs-lookup"><span data-stu-id="04800-112">Be sure you remove or disable the user from your on-premises Blackberry Enterprise Service.</span></span> <span data-ttu-id="04800-113">Vous devez également désactiver les appareils Blackberry de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04800-113">You should also disable any Blackberry devices for the user.</span></span> <span data-ttu-id="04800-114">Reportez-vous au guide d'administration des services Blackberry Business Cloud Services pour consulter les étapes spécifiques relatives à la désactivation de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04800-114">Refer to the Blackberry Business Cloud Services Administration Guide if you need specific steps on how to disable the user.</span></span>
