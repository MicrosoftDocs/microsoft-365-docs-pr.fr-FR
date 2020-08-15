---
title: Afficher les erreurs de synchronisation d’annuaires dans Microsoft 365
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
f1.keywords:
- CSH
ms.custom:
- Adm_O365
- seo-marvel-apr2020
ms.collection:
- Ent_O365
- M365-identity-device-management
search.appverid:
- MET150
- MOE150
- MED150
- MBS150
- GPA150
ms.assetid: b4fc07a5-97ea-4ca6-9692-108acab74067
description: Découvrez comment afficher les erreurs de synchronisation d’annuaires et les correctifs possibles dans le centre d’administration Microsoft 365.
ms.openlocfilehash: 5103b1f8a8f0514ca30fd71b94dee2530f0b082f
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46690089"
---
# <a name="view-directory-synchronization-errors-in-microsoft-365"></a><span data-ttu-id="2b990-103">Afficher les erreurs de synchronisation d’annuaires dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b990-103">View directory synchronization errors in Microsoft 365</span></span>

<span data-ttu-id="2b990-104">Vous pouvez afficher les erreurs de synchronisation d’annuaires dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2b990-104">You can view directory synchronization errors in the Microsoft 365 admin center.</span></span> <span data-ttu-id="2b990-105">Seules les erreurs d’objet utilisateur sont affichées.</span><span class="sxs-lookup"><span data-stu-id="2b990-105">Only the User object errors are displayed.</span></span> <span data-ttu-id="2b990-106">Pour afficher les erreurs avec PowerShell, consultez la rubrique [identifier les objets avec DirSyncProvisioningErrors](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency).</span><span class="sxs-lookup"><span data-stu-id="2b990-106">To view errors with PowerShell, see [Identify objects with DirSyncProvisioningErrors](https://docs.microsoft.com/azure/active-directory/hybrid/how-to-connect-syncservice-duplicate-attribute-resiliency).</span></span>

## <a name="view-directory-synchronization-errors-in-the-microsoft-365-admin-center"></a><span data-ttu-id="2b990-107">Afficher les erreurs de synchronisation d’annuaires dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="2b990-107">View directory synchronization errors in the Microsoft 365 admin center</span></span>

<span data-ttu-id="2b990-108">Pour afficher les erreurs dans le centre d’administration Microsoft 365 :</span><span class="sxs-lookup"><span data-stu-id="2b990-108">To view any errors in the Microsoft 365 admin center:</span></span>
  
1. <span data-ttu-id="2b990-109">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) avec un compte d’administrateur général.</span><span class="sxs-lookup"><span data-stu-id="2b990-109">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) with a global administrator account.</span></span> 
    
2. <span data-ttu-id="2b990-110">Sur la page d' **Accueil** , vous verrez la carte de **gestion des utilisateurs** .</span><span class="sxs-lookup"><span data-stu-id="2b990-110">On the **Home** page, you'll see the **User management** card.</span></span> 
    
    ![Carte de gestion des utilisateurs dans le centre d’administration Microsoft 365](../media/060006e9-de61-49d5-8979-e77cda198e71.png)
  
3. <span data-ttu-id="2b990-112">Sur la carte, sélectionnez **synchroniser les erreurs** sous **Azure ad Connect** pour afficher les erreurs sur la page **Erreurs de synchronisation d’annuaires** .</span><span class="sxs-lookup"><span data-stu-id="2b990-112">On the card, choose **Sync errors** under **Azure AD Connect** to see the errors on the **Directory sync errors** page.</span></span>   
    
    ![Exemple de page d’erreurs de synchronisation d’annuaires](../media/882094a3-80d3-4aae-b90b-78b27047974c.png)

4. <span data-ttu-id="2b990-114">Choisissez l’une des erreurs pour afficher le volet d’informations avec des informations sur l’erreur et des conseils sur la façon de résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="2b990-114">Choose any of the errors to display the details pane with information about the error and tips on how to fix it.</span></span>

   ![Exemple de détails d’une erreur de synchronisation d’annuaires](../media/a6e302d4-6be7-4e3a-b4b5-81c5a2c02952.png)
  
<span data-ttu-id="2b990-116">Après l’affichage, consultez la rubrique [résolution des problèmes liés à la synchronisation d’annuaires pour Microsoft 365](fix-problems-with-directory-synchronization.md) pour corriger les problèmes identifiés.</span><span class="sxs-lookup"><span data-stu-id="2b990-116">After viewing, see [fixing problems with directory synchronization for Microsoft 365](fix-problems-with-directory-synchronization.md) to correct any identified issues.</span></span>

