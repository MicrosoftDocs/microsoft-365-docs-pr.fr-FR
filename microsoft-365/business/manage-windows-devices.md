---
title: Permettre à un domaine aux périphériques Windows 10 devant être gérés par Microsoft 365 entreprise
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 9b4de218-f1ad-41fa-a61b-e9e8ac0cf993
description: Découvrez comment activer Microsoft 365 protéger AD local joints périphériques Windows 10.
ms.openlocfilehash: 6e66a2c5417c9037232c1ada654d4cac3c520607
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866988"
---
# <a name="enable-domain-joined-windows-10-devices-to-be-managed-by-microsoft-365-business"></a><span data-ttu-id="db0a6-103">Permettre à un domaine aux périphériques Windows 10 devant être gérés par Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="db0a6-103">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business</span></span>

<span data-ttu-id="db0a6-p101">Si votre organisation utilise Windows Server Active Directory sur site, vous pouvez configurer Microsoft 365 Business pour protéger vos périphériques Windows 10, tout en conservant l’accès aux ressources locales qui nécessitent une authentification locale. Vous pouvez configurer ce paramètre en première synchronisation Active Directory avec Azure Active Directory, suivi d’inscription les périphériques Windows 10 avec Azure AD et leur inscription pour la gestion des appareils mobiles par Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="db0a6-p101">If your organization uses Windows Server Active Directory on-premises, you can set up Microsoft 365 Business to protect your Windows 10 devices, while still maintaining access to on-premises resources that require local authentication. You can set this up by first synchronizing your Active Directory with Azure Active Directory, followed by registering the Windows 10 devices with Azure AD and enrolling them for mobile device management by Microsoft 365 Business.</span></span>
  
## <a name="set-up-domain-joined-devices-to-be-managed-by-microsoft-365-business"></a><span data-ttu-id="db0a6-106">Configurer les périphériques liés à un domaine devant être gérés par Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="db0a6-106">Set up domain-joined devices to be managed by Microsoft 365 Business</span></span>

<span data-ttu-id="db0a6-p102">Pour configurer les périphériques liés à un domaine de votre organisation afin de bénéficier des fonctionnalités fournies par Azure Active Directory en plus des locaux Active Directory, vous pouvez implémenter **hybride Azure AD participé à des périphériques**. Il s’agit de périphériques qui sont joints à la fois sur site Active Directory et Azure Active Directory. Hybride Azure AD joint périphériques peuvent être protégés et gérées par Microsoft 365 Business...</span><span class="sxs-lookup"><span data-stu-id="db0a6-p102">To set up your organization's domain-joined devices to benefit from the capabilities provided by Azure Active Directory in addition to on-premises Active Directory, you can implement **Hybrid Azure AD joined devices**. These are devices that are joined both to your on-premises Active Directory and your Azure Active Directory. Hybrid Azure AD joined devices can be protected and managed by Microsoft 365 Business..</span></span> 
  
<span data-ttu-id="db0a6-110">Effectuez les étapes ci-dessous pour rendre vos périphériques Windows 10 hybride Azure AD joint et gérées par Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="db0a6-110">Complete the steps below to make your Windows 10 devices Hybrid Azure AD joined and managed by Microsoft 365 Business.</span></span>
  
1. <span data-ttu-id="db0a6-111">Pour synchroniser vos utilisateurs, groupes et des contacts à partir d’Active Directory local dans Azure Active Directory, exécutez l’Assistant synchronisation d’annuaires et Azure Active Directory se connecter comme décrit dans [configurer la synchronisation d’annuaires pour Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span><span class="sxs-lookup"><span data-stu-id="db0a6-111">To synchronize your users, groups and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure Active Directory Connect as described in [Set up directory synchronization for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="db0a6-112">Les étapes sont exactement les mêmes pour Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="db0a6-112">The steps are exactly the same for Microsoft 365 Business.</span></span> 
  
2. <span data-ttu-id="db0a6-113">Avant d’effectuer l’étape 3 pour permettre aux périphériques Windows 10 être hybride Azure AD lié, vous devez respecter les conditions préalables suivantes :</span><span class="sxs-lookup"><span data-stu-id="db0a6-113">Before you complete step 3 to enable Windows 10 devices to be Hybrid Azure AD joined, you need to make sure that you meet the following prerequisites:</span></span>
    
   - <span data-ttu-id="db0a6-114">Vous exécutez la dernière version d’Azure AD se connecter.</span><span class="sxs-lookup"><span data-stu-id="db0a6-114">You are running the latest version of Azure AD connect.</span></span>
    
   - <span data-ttu-id="db0a6-p103">Se connecter Azure AD a synchronisé tous les objets ordinateur des périphériques devant être hybride joints Azure AD. Se connecter également si les objets ordinateur appartenant à des unités d’organisation (UO), assurez-vous que ces unités d’organisation sont définies pour la synchronisation dans Azure AD.</span><span class="sxs-lookup"><span data-stu-id="db0a6-p103">Azure AD connect has synchronized all the computer objects of the devices you want to be hybrid Azure AD joined. If the computer objects belong to specific organizational units (OU), then make sure these OUs are set for synchronization in Azure AD connect as well.</span></span>
    
3. <span data-ttu-id="db0a6-117">Inscrivez à un domaine Windows 10 les périphériques existants pour être hybride Azure AD joint et les inscrire pour la gestion des appareils mobiles par Intune (365 Microsoft Business) :</span><span class="sxs-lookup"><span data-stu-id="db0a6-117">Register existing domain-joined Windows 10 devices to be hybrid Azure AD Joined and enroll them for mobile device management by Intune (Microsoft 365 Business):</span></span>
    
4. <span data-ttu-id="db0a6-p104">Suivez les instructions étape par étape comment [configurer les périphériques d’Azure Active Directory joint hybride](https://go.microsoft.com/fwlink/p/?linkid=872870). Cela permettra la synchronisation d’Active Directory local joint des ordinateurs Windows 10 et rendre prêt en nuage.</span><span class="sxs-lookup"><span data-stu-id="db0a6-p104">Follow the step by step instructions in [How to configure hybrid Azure Active Directory joined devices](https://go.microsoft.com/fwlink/p/?linkid=872870). This will enable the synchronization of your on-premises Active Directory joined Windows 10 computers and make them cloud ready.</span></span>
    
5. <span data-ttu-id="db0a6-p105">Pour inscrire un appareil Windows 10 pour la gestion des appareils mobiles, voir [inscrire un appareil Windows 10 avec Intune à l’aide d’une stratégie de groupe](https://go.microsoft.com/fwlink/p/?linkid=872871) pour obtenir des instructions. Vous pouvez définir la stratégie de groupe sur un ordinateur local au niveau ou pour les opérations en bloc, vous pouvez créer ce paramètre de stratégie de groupe sur votre serveur de contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="db0a6-p105">In order to enroll a Windows 10 device for mobile device management, see [Enroll a Windows 10 device with Intune by using a Group Policy](https://go.microsoft.com/fwlink/p/?linkid=872871) for instructions. You can set the Group Policy at a local computer level or for bulk operations, you can create this group policy setting on your domain controller server.</span></span> 
    

