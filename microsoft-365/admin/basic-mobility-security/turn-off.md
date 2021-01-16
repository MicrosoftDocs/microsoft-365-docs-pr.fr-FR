---
title: Désactiver la mobilité et la sécurité de base
f1.keywords: NOCSH
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
ms.custom: AdminSurgePortfolio
description: Supprimez des groupes ou des stratégies pour désactiver la mobilité et la sécurité de base.
ms.openlocfilehash: 0786ac8ebd190b9af3211c211cc6db2ea9e0ea48
ms.sourcegitcommit: 8849dd6f80217c29f427c7f008d918f30c792240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/15/2021
ms.locfileid: "49876839"
---
# <a name="turn-off-basic-mobility-and-security"></a><span data-ttu-id="49bd3-103">Désactiver la mobilité et la sécurité de base</span><span class="sxs-lookup"><span data-stu-id="49bd3-103">Turn off Basic Mobility and Security</span></span>

<span data-ttu-id="49bd3-104">Pour désactiver efficacement la mobilité et la sécurité de base, vous supprimez des groupes de personnes définis par des groupes de sécurité des stratégies de gestion des appareils ou vous supprimez les stratégies elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="49bd3-104">To effectively turn off Basic Mobility and Security, you remove groups of people defined by security groups from the device management policies, or remove the policies themselves.</span></span>

- <span data-ttu-id="49bd3-105">Supprimez des groupes d’utilisateurs en supprimant des groupes de sécurité d’utilisateurs des stratégies d’appareil que vous avez créées.</span><span class="sxs-lookup"><span data-stu-id="49bd3-105">Remove groups of users by removing user security groups from the device policies you've created.</span></span>

- <span data-ttu-id="49bd3-106">Désactivez la mobilité et la sécurité de base pour tout le monde en supprimant toutes les stratégies d’appareil de mobilité et de sécurité de base.</span><span class="sxs-lookup"><span data-stu-id="49bd3-106">Disable Basic Mobility and Security for everyone by removing all Basic Mobility and Security device policies.</span></span>

<span data-ttu-id="49bd3-107">Ces options suppriment l’application de la mobilité et de la sécurité de base pour les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="49bd3-107">These options remove Basic Mobility and Security enforcement for devices in your organization.</span></span> <span data-ttu-id="49bd3-108">Malheureusement, vous ne pouvez pas simplement « mettre en service » Basic Mobility and Security après l’avoir installé.</span><span class="sxs-lookup"><span data-stu-id="49bd3-108">Unfortunately, you can't simply "unprovision" Basic Mobility and Security after you've set it up.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="49bd3-109">N’ignorez pas l’impact sur les appareils des utilisateurs lorsque vous supprimez des groupes de sécurité d’utilisateurs des stratégies ou supprimez les stratégies elles-mêmes.</span><span class="sxs-lookup"><span data-stu-id="49bd3-109">Be aware of the impact on users' devices when you remove user security groups from policies or remove the policies themselves.</span></span> <span data-ttu-id="49bd3-110">Par exemple, les profils de messagerie et les e-mails mis en cache peuvent être supprimés, en fonction de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="49bd3-110">For example, email profiles and cached emails might be removed, depending on the device.</span></span> <span data-ttu-id="49bd3-111">Pour plus d’informations,  [que se passe-t-il lorsque](https://support.microsoft.com/office/create-device-security-policies-in-basic-mobility-and-security-d310f556-8bfb-497b-9bd7-fe3c36ea2fd6#bkmk_changeimpact) vous supprimez une stratégie ou supprimez un utilisateur de la stratégie ?</span><span class="sxs-lookup"><span data-stu-id="49bd3-111">For more info, see  [What happens when you delete a policy or remove a user from the policy?](https://support.microsoft.com/office/create-device-security-policies-in-basic-mobility-and-security-d310f556-8bfb-497b-9bd7-fe3c36ea2fd6#bkmk_changeimpact)</span></span>

## <a name="remove-user-security-groups-from-basic-mobility-and-security-device-policies"></a><span data-ttu-id="49bd3-112">Supprimer des groupes de sécurité utilisateur des stratégies d’appareil de mobilité et de sécurité de base</span><span class="sxs-lookup"><span data-stu-id="49bd3-112">Remove user security groups from Basic Mobility and Security device policies</span></span>

1. <span data-ttu-id="49bd3-113">Dans votre type de navigateur :  [https://protection.office.com/devicev2](https://protection.office.com/devicev2) .</span><span class="sxs-lookup"><span data-stu-id="49bd3-113">In your browser type: [https://protection.office.com/devicev2](https://protection.office.com/devicev2).</span></span>

2. <span data-ttu-id="49bd3-114">Sélectionnez une stratégie d’appareil, puis **sélectionnez Modifier la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="49bd3-114">Select a device policy, and select **Edit policy**.</span></span> 

3. <span data-ttu-id="49bd3-115">Dans la page  **Déploiement,**   sélectionnez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="49bd3-115">On the  **Deployment**  page, select **Remove**.</span></span>

4. <span data-ttu-id="49bd3-116">Sous  **Groupes,** sélectionnez un groupe de sécurité.</span><span class="sxs-lookup"><span data-stu-id="49bd3-116">Under  **Groups**, select a security group.</span></span>

5. <span data-ttu-id="49bd3-117">Sélectionnez  **Supprimer,** puis **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="49bd3-117">Select  **Remove**, and select **Save**.</span></span>

## <a name="remove-basic-mobility-and-security-device-policies"></a><span data-ttu-id="49bd3-118">Supprimer des stratégies d’appareil de mobilité et de sécurité de base</span><span class="sxs-lookup"><span data-stu-id="49bd3-118">Remove Basic Mobility and Security device policies</span></span>

1.  <span data-ttu-id="49bd3-119">Dans votre type de navigateur :  [https://protection.office.com/devicev2](https://protection.office.com/devicev2) .</span><span class="sxs-lookup"><span data-stu-id="49bd3-119">In your browser type: [https://protection.office.com/devicev2](https://protection.office.com/devicev2).</span></span> 

2.  <span data-ttu-id="49bd3-120">Sélectionnez une stratégie d’appareil, puis  **sélectionnez Supprimer la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="49bd3-120">Select a device policy, and then select  **Delete policy**.</span></span>
    
3.  <span data-ttu-id="49bd3-121">Dans la boîte de dialogue Avertissement, sélectionnez **Oui.**</span><span class="sxs-lookup"><span data-stu-id="49bd3-121">In the Warning dialog box, select **Yes**.</span></span>

>[!NOTE]
><span data-ttu-id="49bd3-122">Pour plus d’informations sur la procédure de déblocage des appareils si les appareils de votre organisation sont toujours dans un état bloqué, consultez le billet de blog sur la suppression du contrôle d’accès de la gestion des appareils mobiles pour [Office 365.](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/Removing-Access-Control-from-Mobile-Device-Management-for-Office/ba-p/279934)</span><span class="sxs-lookup"><span data-stu-id="49bd3-122">For more steps to unblock devices if your organization devices are still in a blocked state,  see the blog post [Removing Access Control from Mobile Device Management for Office 365](https://techcommunity.microsoft.com/t5/Intune-Customer-Success/Removing-Access-Control-from-Mobile-Device-Management-for-Office/ba-p/279934).</span></span>
