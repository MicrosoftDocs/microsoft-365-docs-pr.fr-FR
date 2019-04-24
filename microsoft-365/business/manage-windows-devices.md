---
title: Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 9b4de218-f1ad-41fa-a61b-e9e8ac0cf993
description: Découvrez comment activer Microsoft 365 pour protéger les appareils locaux Windows 10.
ms.openlocfilehash: d61b3bf6be50d6b21e7b883774567bb63995e60e
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278074"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business"></a><span data-ttu-id="cb81b-103">Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cb81b-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business</span></span>

<span data-ttu-id="cb81b-104">Si votre organisation utilise Windows Server Active Directory en local, vous pouvez configurer Microsoft 365 entreprise pour protéger vos appareils Windows 10, tout en conservant l'accès aux ressources locales qui nécessitent une authentification locale.</span><span class="sxs-lookup"><span data-stu-id="cb81b-104">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication.</span></span> <span data-ttu-id="cb81b-105">Vous pouvez configurer cette configuration en commençant par synchroniser Active Directory avec Azure Active Directory, puis en enregistrant les appareils Windows 10 avec Azure AD et en les inscrivant pour la gestion des appareils mobiles par Microsoft 365 entreprise.</span><span class="sxs-lookup"><span data-stu-id="cb81b-105">You can set this up by first synchronizing your Active Directory with Azure Active Directory, followed by registering the Windows 10 devices with Azure AD and enrolling them for mobile device management by Microsoft 365 Business.</span></span>
  
## <a name="set-up-domain-joined-devices-to-be-managed-by-microsoft-365-business"></a><span data-ttu-id="cb81b-106">Configurer les appareils joints à un domaine pour qu'ils soient gérés par Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cb81b-106">Set up domain-joined devices to be managed by Microsoft 365 Business</span></span>

<span data-ttu-id="cb81b-107">Pour configurer les appareils joints à un domaine de votre organisation afin de tirer parti des fonctionnalités fournies par Azure Active Directory en plus d'Active Directory en local, vous pouvez implémenter des **appareils joints Azure ad hybrides**.</span><span class="sxs-lookup"><span data-stu-id="cb81b-107">To set up your organization's domain-joined devices to benefit from the capabilities provided by Azure Active Directory in addition to on-premises Active Directory, you can implement **Hybrid Azure AD joined devices**.</span></span> <span data-ttu-id="cb81b-108">Il s'agit des appareils qui sont joints à la fois à votre Active Directory local et à votre Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb81b-108">These are devices that are joined both to your on-premises Active Directory and your Azure Active Directory.</span></span> <span data-ttu-id="cb81b-109">Les appareils joints Azure AD hybrides peuvent être protégés et gérés par Microsoft 365 Business..</span><span class="sxs-lookup"><span data-stu-id="cb81b-109">Hybrid Azure AD joined devices can be protected and managed by Microsoft 365 Business..</span></span> 
  
<span data-ttu-id="cb81b-110">Suivez les étapes ci-dessous pour faire en sorte que les appareils Windows 10 hybrides se joignent à Azure AD et soient gérés par Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="cb81b-110">Complete the steps below to make your Windows 10 devices Hybrid Azure AD joined and managed by Microsoft 365 Business.</span></span>
  
1. <span data-ttu-id="cb81b-111">Pour synchroniser vos utilisateurs, groupes et contacts à partir d'Active Directory local avec Azure Active Directory, exécutez l'Assistant synchronisation d'annuaires et Azure Active Directory Connect comme décrit dans [set up Directory Synchronization for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span><span class="sxs-lookup"><span data-stu-id="cb81b-111">To synchronize your users, groups and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure Active Directory Connect as described in [Set up directory synchronization for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cb81b-112">Les étapes sont exactement les mêmes pour Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="cb81b-112">The steps are exactly the same for Microsoft 365 Business.</span></span> 
  
2. <span data-ttu-id="cb81b-113">Avant d'effectuer l'étape 3 pour permettre aux appareils Windows 10 d'être associés à Azure AD hybride, vous devez vous assurer que vous remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="cb81b-113">Before you complete step 3 to enable Windows 10 devices to be Hybrid Azure AD joined, you need to make sure that you meet the following prerequisites:</span></span>
    
   - <span data-ttu-id="cb81b-114">Vous exécutez la dernière version d'Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="cb81b-114">You are running the latest version of Azure AD connect.</span></span>
    
   - <span data-ttu-id="cb81b-115">Azure AD Connect a synchronisé tous les objets ordinateur des appareils que vous souhaitez associer à Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cb81b-115">Azure AD connect has synchronized all the computer objects of the devices you want to be hybrid Azure AD joined.</span></span> <span data-ttu-id="cb81b-116">Si les objets ordinateur appartiennent à des unités d'organisation (UO) spécifiques, assurez-vous également que ces unités d'organisation sont définies pour la synchronisation dans Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="cb81b-116">If the computer objects belong to specific organizational units (OU), then make sure these OUs are set for synchronization in Azure AD connect as well.</span></span>
    
3. <span data-ttu-id="cb81b-117">Enregistrez les appareils Windows 10 associés à un domaine pour qu'ils soient associés à Azure AD et inscrivez-les pour la gestion des appareils mobiles par Intune (Microsoft 365 Business):</span><span class="sxs-lookup"><span data-stu-id="cb81b-117">Register existing domain-joined Windows 10 devices to be hybrid Azure AD Joined and enroll them for mobile device management by Intune (Microsoft 365 Business):</span></span>
    
4. <span data-ttu-id="cb81b-118">Suivez les instructions pas à pas dans la [procédure de configuration des appareils joints Azure Active Directory hybrides](https://go.microsoft.com/fwlink/p/?linkid=872870).</span><span class="sxs-lookup"><span data-stu-id="cb81b-118">Follow the step by step instructions in [How to configure hybrid Azure Active Directory joined devices](https://go.microsoft.com/fwlink/p/?linkid=872870).</span></span> <span data-ttu-id="cb81b-119">Cela permettra la synchronisation de votre annuaire Active Directory sur site avec des ordinateurs Windows 10 et rendez-les en nuage prêts.</span><span class="sxs-lookup"><span data-stu-id="cb81b-119">This will enable the synchronization of your on-premises Active Directory joined Windows 10 computers and make them cloud ready.</span></span>
    
5. <span data-ttu-id="cb81b-120">Pour inscrire un appareil Windows 10 pour la gestion des appareils mobiles, reportez-vous à la rubrique [inscrire un appareil Windows 10 avec Intune à l'aide d'une stratégie de groupe](https://go.microsoft.com/fwlink/p/?linkid=872871) pour obtenir des instructions.</span><span class="sxs-lookup"><span data-stu-id="cb81b-120">In order to enroll a Windows 10 device for mobile device management, see [Enroll a Windows 10 device with Intune by using a Group Policy](https://go.microsoft.com/fwlink/p/?linkid=872871) for instructions.</span></span> <span data-ttu-id="cb81b-121">Vous pouvez définir la stratégie de groupe au niveau d'un ordinateur local ou pour des opérations en bloc, vous pouvez créer ce paramètre de stratégie de groupe sur votre serveur de contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="cb81b-121">You can set the Group Policy at a local computer level or for bulk operations, you can create this group policy setting on your domain controller server.</span></span> 
    

