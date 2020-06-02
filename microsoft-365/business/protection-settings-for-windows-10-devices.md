---
title: Définir les paramètres de protection des applications pour les appareils Windows 10
f1.keywords:
- NOCSH
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
f1_keywords:
- Win10AppPolicy
- O365E_Win10AppPolicy
- BCS365_Win10AppPolicy
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- M365-subscription-management
- M365-identity-device-management
ms.custom:
- Core_O365Admin_Migration
- MiniMaven
- MSB365
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 02e74022-44af-414b-9d74-0ebf5c2197f0
description: Découvrez comment créer une stratégie de gestion des applications et protéger les fichiers de travail sur les appareils Windows 10 personnels de vos utilisateurs.
ms.openlocfilehash: df10470c6bd7aad2f35700a267c4d24d949f569c
ms.sourcegitcommit: 2d664a95b9875f0775f0da44aca73b16a816e1c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2020
ms.locfileid: "44470864"
---
# <a name="set-application-protection-settings-for-windows-10-devices"></a><span data-ttu-id="7a676-103">Définir les paramètres de protection des applications pour les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a676-103">Set application protection settings for Windows 10 devices</span></span>

<span data-ttu-id="7a676-104">Cet article s’applique à Microsoft 365 Business Premium.</span><span class="sxs-lookup"><span data-stu-id="7a676-104">This article applies to Microsoft 365 Business Premium.</span></span>

## <a name="create-an-app-management-policy-for-windows-10"></a><span data-ttu-id="7a676-105">Créer une stratégie de gestion des applications pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a676-105">Create an app management policy for Windows 10</span></span>

<span data-ttu-id="7a676-106">Si vos utilisateurs disposent d'appareils Windows 10 sur lesquels ils effectuent des tâches professionnelles, vous pouvez également protéger vos données sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="7a676-106">If your users have personal Windows 10 devices on which they perform work tasks, you can protect your data on those devices as well.</span></span>
  
1. <span data-ttu-id="7a676-107">Accédez au Centre d’administration à l’adresse <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span><span class="sxs-lookup"><span data-stu-id="7a676-107">Go to the admin center at <a href="https://go.microsoft.com/fwlink/p/?linkid=837890" target="_blank">https://admin.microsoft.com</a>.</span></span> 
    
2. <span data-ttu-id="7a676-108">Dans le volet de navigation de gauche, choisissez ajout de stratégies de **périphériques** \> **Policies** \> **Add**.</span><span class="sxs-lookup"><span data-stu-id="7a676-108">On the left nav, choose **Devices** \> **Policies** \> **Add**.</span></span>

3. <span data-ttu-id="7a676-109">Dans le volet **Ajouter une stratégie**, entrez un nom unique pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="7a676-109">On the **Add policy** pane, enter a unique name for this policy.</span></span> 
    
4. <span data-ttu-id="7a676-110">Sous **Type de stratégie**, sélectionnez **Gestion des applications pour Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="7a676-110">Under **Policy type**, choose **Application Management for Windows 10**.</span></span>
    
5. <span data-ttu-id="7a676-111">Sous **type d’appareil**, choisissez **personnel** ou **société appartenant**.</span><span class="sxs-lookup"><span data-stu-id="7a676-111">Under **Device type**, choose either **Personal** or **Company Owned**.</span></span>
    
6. <span data-ttu-id="7a676-112">L'option **Chiffrer les fichiers de travail** est activée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7a676-112">The **Encrypt work files** is turned on automatically.</span></span> 
    
7. <span data-ttu-id="7a676-113">Définissez **Empêcher les utilisateurs de copier des données d'entreprise dans leurs fichiers personnels et les obliger à enregistrer les fichiers professionnels dans OneDrive Entreprise** sur **Activé** si vous ne souhaitez pas que les utilisateurs enregistrent des fichiers professionnels sur leur PC.</span><span class="sxs-lookup"><span data-stu-id="7a676-113">Set **Prevent users from copying company data to personal files and force them to save work files to OneDrive for Business** to **On** if you don't want the users to save work files on their PC.</span></span> 
    
9. <span data-ttu-id="7a676-114">Développez **récupération de données sur les appareils Windows**.</span><span class="sxs-lookup"><span data-stu-id="7a676-114">Expand **Recover data on Windows devices**.</span></span> <span data-ttu-id="7a676-115">Nous vous recommandons **de**l’activer.</span><span class="sxs-lookup"><span data-stu-id="7a676-115">We recommend that you turn it **On**.</span></span>
    
    <span data-ttu-id="7a676-116">Avant de pouvoir accéder à l'emplacement du certificat de l'agent de récupération de données, vous devez d'abord créer un tel certificat.</span><span class="sxs-lookup"><span data-stu-id="7a676-116">Before you can browse to the location of the Data Recovery Agent certificate, you have to first create one.</span></span> <span data-ttu-id="7a676-117">Pour obtenir des instructions, consultez la rubrique [créer et vérifier un certificat d’agent de récupération de données (DRA) EFS (Encrypting File System)](https://go.microsoft.com/fwlink/p/?linkid=853700).</span><span class="sxs-lookup"><span data-stu-id="7a676-117">For instructions, see [Create and verify an Encrypting File System (EFS) Data Recovery Agent (DRA) certificate](https://go.microsoft.com/fwlink/p/?linkid=853700).</span></span>
    
    <span data-ttu-id="7a676-118">Par défaut, les fichiers de travail sont chiffrés à l'aide d'une clé secrète qui est stockée sur l'appareil associé au profil de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a676-118">By default, work files are encrypted using a secret key that is stored on the device and associated with the user's profile.</span></span> <span data-ttu-id="7a676-119">Seul l'utilisateur peut ouvrir et déchiffrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="7a676-119">Only the user can open and decrypt the file.</span></span> <span data-ttu-id="7a676-120">Toutefois, si un périphérique est perdu ou si un utilisateur est supprimé, un fichier peut rester bloqué à l'état chiffré.</span><span class="sxs-lookup"><span data-stu-id="7a676-120">However, if a device is lost or a user is removed, a file can be stuck in an encrypted state.</span></span> <span data-ttu-id="7a676-121">Un administrateur peut utiliser le certificat de l’agent de récupération de données (DRA) pour déchiffrer le fichier.</span><span class="sxs-lookup"><span data-stu-id="7a676-121">An admin can use the Data Recovery Agent (DRA) certificate to decrypt the file.</span></span>
    
    ![Browse to Data Recovery Agent certificate.](../media/7d7d664f-b72f-4293-a3e7-d0fa7371366c.png)
  
10. <span data-ttu-id="7a676-123">Développez **protéger d’autres emplacements réseau et Cloud** si vous souhaitez ajouter des domaines ou des emplacements SharePoint Online supplémentaires pour vous assurer que les fichiers de toutes les applications répertoriées sont protégés.</span><span class="sxs-lookup"><span data-stu-id="7a676-123">Expand **Protect additional network and cloud locations** if you want to add additional domains or SharePoint Online locations to make sure that files in all the listed apps are protected.</span></span> <span data-ttu-id="7a676-124">Si vous devez entrer plusieurs éléments pour chaque champ, utilisez un point-virgule ( ;) entre les différents éléments.</span><span class="sxs-lookup"><span data-stu-id="7a676-124">If you need to enter more than one item for either field, use a semicolon (;) between the items.</span></span>
    
    ![Expand Protect additional network and cloud locations, and enter domains or SharePoint Online sites you own.](../media/7afaa0c7-ba53-456d-8c61-312c45e09625.png)
  
11. <span data-ttu-id="7a676-p105">Maintenant, définissez **Qui recevra ces paramètres ?** Si vous ne voulez pas utiliser le groupe de sécurité par défaut **Tous les utilisateurs**, sélectionnez **Modifier**, puis les groupes de sécurité qui recevront ces paramètres \> **Sélectionner**.</span><span class="sxs-lookup"><span data-stu-id="7a676-p105">Next decide **Who will get these settings?** If you don't want to use the default **All Users** security group, choose **Change**, choose the security groups who will get these settings \> **Select**.</span></span>
    
12. <span data-ttu-id="7a676-128">Enfin, sélectionnez **Ajouter** pour enregistrer la stratégie et l'affecter à des appareils.</span><span class="sxs-lookup"><span data-stu-id="7a676-128">Finally, choose **Add** to save the policy, and assign it to devices.</span></span> 
