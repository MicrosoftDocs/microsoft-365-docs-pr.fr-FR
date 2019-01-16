---
title: Accès aux ressources à partir d’un périphérique joint à AD Azure dans Microsoft 365 Business sur site
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: b0f4d010-9fd1-44d0-9d20-fabad2cdbab5
description: Découvrez comment accéder aux ressources locales telles que les applications métier, des partages de fichiers et des imprimantes à partir d’Azure Active Directory joint périphérique Windows 10.
ms.openlocfilehash: 0a5d4b0828888fcb99676223000c446479f84ddc
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26866866"
---
# <a name="access-on-premises-resources-from-an-azure-ad-joined-device-in-microsoft-365-business"></a><span data-ttu-id="c164f-103">Accès aux ressources à partir d’un périphérique joint à AD Azure dans Microsoft 365 Business sur site</span><span class="sxs-lookup"><span data-stu-id="c164f-103">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business</span></span>

<span data-ttu-id="c164f-p101">Tout périphérique 10 Windows Azure Active Directory joint auront accès à toutes les ressources en nuage tels que vos applications Office 365 et peut être protégé par Microsoft 365 Business. Pour également autoriser l’accès aux ressources locales telles que des applications, des partages de fichiers et des imprimantes ligne de métier (LOB), vous devez synchroniser Active Directory local avec Azure Active Directory à l’aide [d’Azure AD se connecter](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect). Voir [Introduction à la gestion des périphériques dans Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction) pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="c164f-p101">Any Windows 10 device that is Azure Active Directory joined will have access to all cloud-based resources such as your Office 365 apps and can be protected by Microsoft 365 Business. To also allow access to on-premises resources like Line Of Business (LOB) apps, file shares, and printers, you must synchronize your on-premises Active Directory with Azure Active Directory by using [Azure AD Connect](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnect). See [Introduction to device management in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction) to learn more.</span></span> 
  
## <a name="run-azure-ad-connect"></a><span data-ttu-id="c164f-107">Exécuter Azure AD</span><span class="sxs-lookup"><span data-stu-id="c164f-107">Run Azure AD Connect</span></span>

<span data-ttu-id="c164f-108">Effectuez les étapes suivantes pour permettre aux appareils Azure AD joint de votre organisation d’accéder aux ressources locales.</span><span class="sxs-lookup"><span data-stu-id="c164f-108">Complete the following steps to enable your organization's Azure AD joined devices to access on-premises resources.</span></span>
  
1. <span data-ttu-id="c164f-109">Pour synchroniser vos utilisateurs, groupes et des contacts à partir d’Active Directory local dans Azure Active Directory, exécutez l’Assistant synchronisation d’annuaires et Azure AD se connecter en tant que décrit dans [configurer la synchronisation d’annuaires pour Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span><span class="sxs-lookup"><span data-stu-id="c164f-109">To synchronize your users, groups and contacts from local Active Directory into Azure Active Directory, run the Directory synchronization wizard and Azure AD Connect as described in [Set up directory synchronization for Office 365](https://support.office.com/article/1b3b5318-6977-42ed-b5c7-96fa74b08846).</span></span>
    
2. <span data-ttu-id="c164f-p102">À l’issue de la synchronisation d’annuaires, assurez-vous que les périphériques Windows 10 de votre organisation sont Azure AD lié. Cette étape est effectuée individuellement sur chaque périphérique Windows 10. Pour plus d’informations, voir [configurer les périphériques de Windows pour les utilisateurs professionnels 365 de Microsoft](set-up-windows-devices.md) .</span><span class="sxs-lookup"><span data-stu-id="c164f-p102">After the directory synchronization has completed, make sure your organization's Windows 10 devices are Azure AD joined. This step is done individually on each Windows 10 device. See [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md) for details.</span></span> 
    
3. <span data-ttu-id="c164f-p103">Une fois les périphériques 10 Windows Azure AD lié, chaque utilisateur doit redémarrer leurs périphériques et la connexion avec leurs informations d’identification Microsoft 365 Business. Tous les périphériques maintenant auront accès à ainsi que les ressources locales.</span><span class="sxs-lookup"><span data-stu-id="c164f-p103">Once the Windows 10 devices are Azure AD joined, each user should reboot their devices and login with their Microsoft 365 Business credentials. All devices will now have access to on-premises resources as well.</span></span>
    
<span data-ttu-id="c164f-p104">Des étapes supplémentaires sont nécessaires pour accéder aux ressources pour Azure AD joint périphériques sur site. Il s’agit des fonctionnalités intégrées dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c164f-p104">No additional steps are required to get access to on-premise resources for Azure AD joined devices. This is built-in functionality available in Windows 10.</span></span> 
  
<span data-ttu-id="c164f-117">Si votre organisation n’est pas prête à déployer dans la Azure AD joints périphérique Configuration décrite ci-dessus, pensez à configurer [configuration hybride Azure AD joint du périphérique](manage-windows-devices.md).</span><span class="sxs-lookup"><span data-stu-id="c164f-117">If your organization is not ready to deploy in the Azure AD Joined Device Configuration described above, consider setting up [Hybrid Azure AD Joined device configuration](manage-windows-devices.md).</span></span>
  
### <a name="considerations-when-joining-your-windows-devices-to-azure-ad"></a><span data-ttu-id="c164f-118">Considérations relatives à la participation à vos périphériques Windows pour Azure AD</span><span class="sxs-lookup"><span data-stu-id="c164f-118">Considerations when joining your Windows devices to Azure AD</span></span>

<span data-ttu-id="c164f-119">Si vous êtes Azure AD joindre un appareil Windows qui a été précédemment à un domaine ou un groupe de travail, vous devez prendre en compte les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c164f-119">If you are Azure AD joining a Windows device that has previously been domain-joined or in a workgroup, you need to consider the following limitations:</span></span>
  
- <span data-ttu-id="c164f-p105">Lorsqu’un périphérique Azure AD joint, il crée un nouvel utilisateur sans faire référence à un profil existant. Pour résoudre ce problème, les profils doivent être migrées manuellement. Un profil utilisateur contient des informations telles que des Favoris, les fichiers locaux, les paramètres du navigateur, les paramètres du menu Démarrer, etc.. Une meilleure approche consiste à trouver un outil tiers pour mapper les fichiers et paramètres existants dans le nouveau profil</span><span class="sxs-lookup"><span data-stu-id="c164f-p105">When a device Azure AD joins, it creates a new user without referencing an existing profile. To fix this, profiles need to be manually migrated. A user profile contains information like favorites, local files, browser settings, Start menu settings, etc. A best approach is to find a third-party tool to map existing files and settings to the new profile</span></span>
    
- <span data-ttu-id="c164f-p106">Si le périphérique est à l’aide des objets de stratégie de groupe (GPO), certains objets de stratégie de groupe peut-être pas un comparables de [Fournisseur de services de Configuration](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) Intune. Exécutez l' [outil MMAT](https://www.microsoft.com/download/details.aspx?id=45520) pour rechercher les fournisseurs comparables pour les objets GPO existants.</span><span class="sxs-lookup"><span data-stu-id="c164f-p106">If the device is using Group Policy Objects (GPO), some GPOs may not have a comparable [Configuration Service Provider](https://docs.microsoft.com/windows/configuration/provisioning-packages/how-it-pros-can-use-configuration-service-providers) (CSP) in Intune. Run the [MMAT tool](https://www.microsoft.com/download/details.aspx?id=45520) to find comparable CSPs for existing GPOs.</span></span> 
    
- <span data-ttu-id="c164f-p107">Les utilisateurs ne pourront pas s’authentifier sur les applications qui dépendent de l’authentification Active Directory. Pour traiter cette évaluation de l’utilisation d’une application héritée et prendre en compte la mise à jour vers une application qui utilise une authentification moderne si possible.</span><span class="sxs-lookup"><span data-stu-id="c164f-p107">Users will not be able to authenticate to applications that depend on Active Directory authentication. To deal with this evaluate using a legacy app and consider updating to an app that uses modern Auth if possible.</span></span>
    
- <span data-ttu-id="c164f-p108">Recherche d’imprimante Active Directory ne fonctionne pas. Pour résoudre ce problème, fournir des chemins d’accès de l’imprimante directe pour tous les utilisateurs ou tirer parti [d’Impression de nuage hybride](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span><span class="sxs-lookup"><span data-stu-id="c164f-p108">Active Directory printer discovery will not work. To fix this, provide direct printer paths for all users or leverage [Hybrid Cloud Print](https://docs.microsoft.com/windows-server/administration/hybrid-cloud-print/hybrid-cloud-print-deploy).</span></span>
    

