---
title: Définir les paramètres de protection des applications pour les appareils Windows 10
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
f1_keywords:
- Win10AppPolicy
- O365E_Win10AppPolicy
- BCS365_Win10AppPolicy
ms.service: o365-administration
localization_priority: Normal
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 02e74022-44af-414b-9d74-0ebf5c2197f0
description: Découvrez comment créer une stratégie de gestion d’application et de protection des fichiers de travail sur les appareils Windows 10.
ms.openlocfilehash: acf19a72d994185a35b2e425f8334a73a121ee10
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867041"
---
# <a name="set-application-protection-settings-for-windows-10-devices"></a><span data-ttu-id="50d88-103">Définir les paramètres de protection des applications pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="50d88-103">Set application protection settings for Windows 10 devices</span></span>

## <a name="create-an-app-management-policy-for-windows-10"></a><span data-ttu-id="50d88-104">Créer une stratégie de gestion des applications pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="50d88-104">Create an app management policy for Windows 10</span></span>

<span data-ttu-id="50d88-105">Si vos utilisateurs disposent d'appareils Windows 10 sur lesquels ils effectuent des tâches professionnelles, vous pouvez également protéger vos données sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="50d88-105">If your users have personal Windows 10 devices on which they perform work tasks, you can protect your data on those devices as well.</span></span>
  
1. <span data-ttu-id="50d88-p101">Connectez-vous à [Microsoft 365 Business](https://portal.office.com) avec des informations d'identification d'administrateur général. Sélectionnez la vignette **Administrateur** pour accéder au Centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="50d88-p101">Sign in to [Microsoft 365 Business](https://portal.office.com) with global admin credentials. Choose the **Admin** tile to go to the admin center.</span></span> 
    
2. <span data-ttu-id="50d88-108">Dans la carte **Stratégies d'appareil** du portail d'administration, sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="50d88-108">On the **Device policies** card of the admin portal, choose **Add policy**.</span></span>
    
    ![Device policies card in the admin center.](media/27c12b61-d112-4348-b557-4f3e46204797.png)
  
3. <span data-ttu-id="50d88-110">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="50d88-110">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="50d88-111">Sous **Type de stratégie**, sélectionnez **Gestion des applications pour Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="50d88-111">Under **Policy type**, choose **Application Management for Windows 10**.</span></span>
    
5. <span data-ttu-id="50d88-112">Sous \*\* type d’appareil \*\*, choisissez **personnel** ou **Propriétaire de la société**.</span><span class="sxs-lookup"><span data-stu-id="50d88-112">Under \*\* Device type \*\*, choose either **Personal** or **Company Owned**.</span></span>
    
6. <span data-ttu-id="50d88-113">L'option **Chiffrer les fichiers de travail** est activée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="50d88-113">The **Encrypt work files** is turned on automatically.</span></span> 
    
7. <span data-ttu-id="50d88-114">Définissez **Empêcher les utilisateurs de copier des données d'entreprise dans leurs fichiers personnels et les obliger à enregistrer les fichiers professionnels dans OneDrive Entreprise** sur **Activé** si vous ne souhaitez pas que les utilisateurs enregistrent des fichiers professionnels sur leur PC.</span><span class="sxs-lookup"><span data-stu-id="50d88-114">Set **Prevent users from copying company data to personal files and force them to save work files to OneDrive for Business** to **On** if you don't want the users to save work files on their PC.</span></span> 
    
8. <span data-ttu-id="50d88-p102">Développez **gérer comment les utilisateurs d’accès aux fichiers Office sur des appareils** \> configurer les paramètres des manière dont vous souhaitez. **Gérer les dont les utilisateurs accèdent les périphériques Office sur des appareils mobiles** est **désactivée** par défaut, mais il est recommandé que vous **allumez** et acceptez les valeurs par défaut. Pour plus d’informations, voir [paramètres disponibles](protection-settings-for-windows-10-devices.md#bkmk_settings) .</span><span class="sxs-lookup"><span data-stu-id="50d88-p102">Expand **Manage how users access Office files on devices** \> configure the settings how you would like. The **Manage how users access Office devices on mobile devices** is **Off** by default, but it is recommended that you turn it **On** and accept the default values. See [Available settings](protection-settings-for-windows-10-devices.md#bkmk_settings) for more information.</span></span> 
    
    <span data-ttu-id="50d88-118">Vous pouvez toujours utiliser le lien **Réinitialiser les paramètres par défaut** pour rétablir la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="50d88-118">You can always use the **Reset default settings** link to return to the default setting.</span></span> 
    
9. <span data-ttu-id="50d88-119">Développez **Récupérer les données sur les appareils Windows**. Nous vous recommandons d' **activer** cette option.</span><span class="sxs-lookup"><span data-stu-id="50d88-119">Expand **Recover data on Windows devices** and it is recommended that you turn it **On**.</span></span>
    
    <span data-ttu-id="50d88-p103">Avant de pouvoir accéder à l'emplacement du certificat de l'agent de récupération de données, vous devez d'abord créer un tel certificat. Pour obtenir des instructions, consultez [Créer et vérifier un certificat d'agent de récupération de données EFS (Encrypting File System)](https://go.microsoft.com/fwlink/p/?linkid=853700).</span><span class="sxs-lookup"><span data-stu-id="50d88-p103">Before you can browse to the location of the Data Recovery Agent certificate, you have to first create one. For instructions see, [Create and verify an Encrypting File System (EFS) Data Recovery Agent (DRA) certificate](https://go.microsoft.com/fwlink/p/?linkid=853700).</span></span>
    
    <span data-ttu-id="50d88-p104">Par défaut, les fichiers de travail sont chiffrés à l'aide d'une clé secrète qui est stockée sur l'appareil associé au profil de l'utilisateur. Seul l'utilisateur peut ouvrir et déchiffrer le fichier. Toutefois, si un périphérique est perdu ou si un utilisateur est supprimé, un fichier peut rester bloqué à l'état chiffré. Le certificat de l'Agent de récupération de données (DRA) peut être utilisé par un administrateur pour déchiffrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="50d88-p104">By default, work files are encrypted using a secret key that is stored on the device and associated with the user's profile. Only the user can open and decrypt the file. However, if a device is lost or a user is removed, a file can be stuck in an encrypted state. The Data Recovery Agent (DRA) certificate can be used by an admin to decrypt the file.</span></span>
    
    ![Browse to Data Recovery Agent certificate.](media/7d7d664f-b72f-4293-a3e7-d0fa7371366c.png)
  
10. <span data-ttu-id="50d88-p105">Développez **Protéger les emplacements réseau et cloud supplémentaires** pour ajouter des domaines supplémentaires ou des sites SharePoint Online afin d'assurer que les fichiers de toutes les applications répertoriées seront protégés. Si vous devez entrer plusieurs éléments pour chaque champ, utilisez un point-virgule ( ;) entre les différents éléments.</span><span class="sxs-lookup"><span data-stu-id="50d88-p105">Expand **Protect additional network and cloud locations** if you want to add additional domains or SharePoint Online locations to make sure that files in all the listed apps will be protected. If you need to enter more than one item for either field, use a semicolon (;) between the items.</span></span> 
    
    ![Expand Protect additional network and cloud locations, and enter domains or SharePoint Online sites you own.](media/7afaa0c7-ba53-456d-8c61-312c45e09625.png)
  
11. <span data-ttu-id="50d88-p106">Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis les groupes de sécurité qui recevront ces paramètres \> **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="50d88-p106">Next decide **Who will get these settings?** If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups who will get these settings \> **Select**.</span></span>
    
12. <span data-ttu-id="50d88-132">Enfin, sélectionnez **Ajouter** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="50d88-132">Finally, choose **Add** to save the policy, and assign it to devices.</span></span> 
    
## <a name="available-settings"></a><span data-ttu-id="50d88-133">Paramètres disponibles</span><span class="sxs-lookup"><span data-stu-id="50d88-133">Available settings</span></span>

<span data-ttu-id="50d88-134">Les paramètres suivants sont disponibles pour gérer la manière dont les utilisateurs accèdent aux fichiers professionnels Office.</span><span class="sxs-lookup"><span data-stu-id="50d88-134">The following settings are available to manage how users access Office work files.</span></span>
  
<span data-ttu-id="50d88-135">Pour plus d'informations, voir [Correspondance entre les fonctionnalités de protection de Microsoft 365 Business et les paramètres Intune](map-protection-features-to-intune-settings.md).</span><span class="sxs-lookup"><span data-stu-id="50d88-135">For more information, see [How do protection features in Microsoft 365 Business map to Intune settings](map-protection-features-to-intune-settings.md).</span></span>
  
|<span data-ttu-id="50d88-136">**Paramètre**</span><span class="sxs-lookup"><span data-stu-id="50d88-136">**Setting**</span></span>|<span data-ttu-id="50d88-137">**Description**</span><span class="sxs-lookup"><span data-stu-id="50d88-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="50d88-138">Exiger un code confidentiel ou une empreinte pour accéder aux applications Office</span><span class="sxs-lookup"><span data-stu-id="50d88-138">Require a PIN or fingerprint to access Office apps</span></span>  <br/> |<span data-ttu-id="50d88-139">Si ce paramètre est **activé**, les utilisateurs doivent fournir une autre forme d'authentification, en plus de leur nom d'utilisateur et de leur mot de passe, pour pouvoir utiliser les applications Office sur leur appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="50d88-139">If this settings is **On** users have to provide another form of authentication, in addition to their username and password, before they can use Office apps on their mobile device.</span></span>  <br/> |
|<span data-ttu-id="50d88-140">Réinitialiser le code confidentiel en cas d'échecs successifs de la connexion</span><span class="sxs-lookup"><span data-stu-id="50d88-140">Reset PIN when login fails this many times</span></span>  <br/> |<span data-ttu-id="50d88-141">Afin d'empêcher un utilisateur non autorisé de deviner un code confidentiel de façon aléatoire, le code confidentiel est réinitialisé après le nombre d'entrées incorrectes que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="50d88-141">To prevent an unauthorized user from randomly guessing a PIN, the PIN will reset after the number of wrong entries that you specify.</span></span>  <br/> |
|<span data-ttu-id="50d88-142">Demander aux utilisateurs de se reconnecter à l'issue d'une période d'inactivité des applications Office</span><span class="sxs-lookup"><span data-stu-id="50d88-142">Require users to sign in again after Office apps have been idle for</span></span>  <br/> |<span data-ttu-id="50d88-143">Ce paramètre détermine combien de temps un utilisateur peut être inactif avant d'être invité à se connecter à nouveau.</span><span class="sxs-lookup"><span data-stu-id="50d88-143">This setting determines how long a user can be idle before they are prompted to sign in again.</span></span>  <br/> |
   

