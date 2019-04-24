---
title: Automatiquement installer ou désinstaller Office sur les appareils Windows 10
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: cbc6bfe5-565a-4fb8-95f0-b06e7b74ac46
description: "Installez ou désinstallez Office sur des appareils Windows 10 à partir du centre d'administration de Microsoft 365 Business. "
ms.openlocfilehash: fef4a543aed489202bf05dfb1e8cafbb784ca819
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32277272"
---
# <a name="automatically-install-or-uninstall-office-on-windows-10-devices"></a><span data-ttu-id="ec0c1-103">Automatiquement installer ou désinstaller Office sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="ec0c1-103">Automatically install or uninstall Office on Windows 10 devices</span></span>

<span data-ttu-id="ec0c1-104">[] Vous pouvez rapidement et facilement installer Office sur les ordinateurs Windows 10 à partir du centre d'administration Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-104">You can quickly and easily install Office to Windows 10 PCs from the Microsoft 365 Business admin center.</span></span>
  
<span data-ttu-id="ec0c1-105">Pour mieux comprendre comment cela fonctionne avec les applications Office déjà installées, lisez [Se préparer à l'installation du client Office](prepare-for-office-client-deployment.md) avant de commencer.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-105">To understand how this works with previously installed Office apps, read [Prepare for Office client installation](prepare-for-office-client-deployment.md) before you get started.</span></span> 
  
## <a name="manage-office-deployments"></a><span data-ttu-id="ec0c1-106">Gérer les déploiements d'Office</span><span class="sxs-lookup"><span data-stu-id="ec0c1-106">Manage Office deployments</span></span>

1. <span data-ttu-id="ec0c1-107">Connectez-vous au [centre d'administration](https://aka.ms/bcsportal) avec les informations d'identification de l'administrateur général.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-107">Sign in to the [admin center](https://aka.ms/bcsportal) with global admin credentials.</span></span> 
    
2. <span data-ttu-id="ec0c1-108">Dans la carte **Appareils**, sélectionnez **Gérer le déploiement d'Office**.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-108">On the **Devices** card, choose **Manage Office Deployment**.</span></span>
      <span data-ttu-id="ec0c1-109">Si vous ne voyez pas la carte actions de l' **appareil** , dans la page d' **Accueil** du centre d'administration, cliquez sur **Ajouter** (+) pour l'ajouter à votre domicile d'administration.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-109">If you do not see the **Device actions** card, in the admin center **Home** page, click **Add** (+) to add it to your admin home.</span></span>
    
    ![Screenshot of the Devices card in the admin center](media/9982e784-dbf9-4a76-a159-bb3e2e5aa23f.png)
  
3. <span data-ttu-id="ec0c1-111">Dans le volet **Gérer le déploiement d'Office** qui s'affiche, sélectionnez **Ajouter un groupe**, puis sélectionnez les groupes que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-111">On the **Manage Office deployment** pane that opens, choose **Add a group**, then select the groups you want use.</span></span>
    
4. <span data-ttu-id="ec0c1-112">Une fois le ou les groupes à utiliser ajoutés, dans la liste déroulante **Action de déploiement**, sélectionnez **Installer Office dès que possible** ou **Désinstaller Office**.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-112">After you have added the group or groups you want to use, from the **Deployment Action** drop-down, select either **Install Office as soon as possible** or **Uninstall Office**.</span></span>
    
    ![In the Manage Office deployment pane, choose either Install Office as soon as possible, or Uninstall Office.](media/00f24a61-1848-40c0-b037-78d726c7d757.png)
  
5. <span data-ttu-id="ec0c1-114">Choose **Next** \> review the settings and then choose **Confirm**.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-114">Choose **Next** \> review the settings and then choose **Confirm**.</span></span>
    
<span data-ttu-id="ec0c1-115">Une version 32 bits d'Office est installée automatiquement ou désinstallée sur les appareils appartenant à des utilisateurs spécifiés par le groupe ou les groupes que vous avez utilisés.</span><span class="sxs-lookup"><span data-stu-id="ec0c1-115">A 32-bit Office will be automatically installed, or uninstalled in the devices owned by users specified by the group or groups you used.</span></span>
  
<span data-ttu-id="ec0c1-116">À des fins de vérification, vous pouvez ouvrir le Gestionnaire des tâches sur un ordinateur qui a été sélectionné pour une installation d'Office, puis rechercher le processus Microsoft Office « Démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="ec0c1-116">To verify you can open the Task Manager on a computer that was selected for an Office install and look for Microsoft Office Click-to-Run process.</span></span>
  


