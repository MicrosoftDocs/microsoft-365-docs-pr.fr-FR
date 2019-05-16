---
title: Valider les paramètres de protection des applications sur les PC Windows 10
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
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
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Découvrez comment valider les paramètres de protection des applications professionnelles Microsoft 365 dans les appareils Windows 10.
ms.openlocfilehash: 15c2d54c6281369875d15985c9d4ed16f0114176
ms.sourcegitcommit: 66bb5af851947078872a4d31d3246e69f7dd42bb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2019
ms.locfileid: "34072227"
---
# <a name="validate-device-protection-settings-on-windows-10-pcs"></a><span data-ttu-id="54f00-103">Valider les paramètres de protection des appareils sur des PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="54f00-103">Validate device protection settings on Windows 10 PCs</span></span>

## <a name="verify-that-windows-10-device-policies-are-set"></a><span data-ttu-id="54f00-104">Vérifier que les stratégies d’appareil Windows 10 sont définies</span><span class="sxs-lookup"><span data-stu-id="54f00-104">Verify that Windows 10 device policies are set</span></span>

<span data-ttu-id="54f00-105">Une fois que vous avez [configuré les stratégies de périphériques](protection-settings-for-windows-10-pcs.md), la stratégie peut prendre plusieurs heures et prendre effet sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54f00-105">After you [set up devices policies](protection-settings-for-windows-10-pcs.md), it may take up to a few hours for the policy to take effect on users' devices.</span></span> <span data-ttu-id="54f00-106">Vous pouvez vérifier que les stratégies ont pris effet en consultant les différents écrans de paramètres Windows sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="54f00-106">You can confirm that the policies took effect by looking at various Windows Settings screens on the users' devices.</span></span> <span data-ttu-id="54f00-107">Étant donné que les utilisateurs ne peuvent pas modifier les paramètres de l’antivirus Windows Update et Windows Defender sur leurs appareils Windows 10, un grand nombre de ces options seront grisées.</span><span class="sxs-lookup"><span data-stu-id="54f00-107">Because the users won't be able to modify the Windows Update and Windows Defender Antivirus settings on their Windows 10 devices, a lot of those options will be greyed out.</span></span>
  
1. <span data-ttu-id="54f00-108">Accédez aux **paramètres** \> **mettre &amp; à jour** les **options** de redémarrage de la sécurité \> **Windows Update** \> et vérifiez que tous les paramètres sont grisés.</span><span class="sxs-lookup"><span data-stu-id="54f00-108">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Restart options** and confirm that all settings are greyed out.</span></span> 
    
    ![Toutes les options de redémarrage sont grisées.](media/31308da9-18b0-47c5-bbf6-d5fa6747c376.png)
  
2. <span data-ttu-id="54f00-110">Accédez à **paramètres** \> **mettre &amp; à jour** les **Options avancées** de sécurité \> **Windows Update** \> et vérifiez que tous les paramètres sont grisés.</span><span class="sxs-lookup"><span data-stu-id="54f00-110">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** and confirm that all settings are greyed out.</span></span> 
    
    ![Les options de mises à jour avancées de Windows sont toutes grisées.](media/049cf281-d503-4be9-898b-c0a3286c7fc2.png)
  
3. <span data-ttu-id="54f00-112">Accéder aux **paramètres** \> **mettre &amp; à jour la sécurité** \> **Windows Update** \> **Advanced options** \> **sélectionnez le mode de remise des mises à jour**.</span><span class="sxs-lookup"><span data-stu-id="54f00-112">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** \> **Choose how updates are delivered**.</span></span>
    
    <span data-ttu-id="54f00-113">Vérifiez que vous pouvez voir le message (en rouge) que certains paramètres sont masqués ou gérés par votre organisation, et que toutes les options sont grisées.</span><span class="sxs-lookup"><span data-stu-id="54f00-113">Confirm that you can see the message (in red) that some settings are hidden or managed by your organization, and all the options are greyed out.</span></span>
    
    ![Page choisir le mode de remise des mises à jour: indique que les paramètres sont masqués ou gérés par votre organisation.](media/6b3e37c5-da41-4afd-9983-b4f406216b59.png)
  
4. <span data-ttu-id="54f00-115">Pour ouvrir le centre de sécurité Windows Defender, accédez à **paramètres** \> **mise &amp; à jour sécurité** \> **Windows Defender** \> , cliquez sur Ouvrir le thread de \> virus \*\*\*\* \*\* &amp; du centre de sécurité Windows Defender protection\*\* \> **des &amp; paramètres de protection contre les menaces antivirus**.</span><span class="sxs-lookup"><span data-stu-id="54f00-115">To open the Windows Defender Security Center, go to **Settings** \> **Update &amp; security** \> **Windows Defender** \> click **Open Windows Defender Security Center** \> **Virus &amp; thread protection** \> **Virus &amp; threat protection settings**.</span></span> 
    
5. <span data-ttu-id="54f00-116">Vérifiez que toutes les options sont grisées.</span><span class="sxs-lookup"><span data-stu-id="54f00-116">Verify that all options are greyed out.</span></span> 
    
    ![Les paramètres de protection contre les virus et les menaces sont grisés.](media/9ca68d40-a5d9-49d7-92a4-c581688b5926.png)
  
## <a name="related-topics"></a><span data-ttu-id="54f00-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54f00-118">Related Topics</span></span>

[<span data-ttu-id="54f00-119">Documentation et ressources pour Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="54f00-119">Microsoft 365 Business documentation and resources</span></span>](https://go.microsoft.com/fwlink/p/?linkid=853701)
  
[<span data-ttu-id="54f00-120">Prise en main de Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="54f00-120">Get started with Microsoft 365 Business</span></span>](microsoft-365-business-overview.md)
  
[<span data-ttu-id="54f00-121">Gérer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="54f00-121">Manage Microsoft 365 Business</span></span>](manage.md)
  
[<span data-ttu-id="54f00-122">Définir des configurations d'application pour les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="54f00-122">Set device configurations for Windows 10 PCs</span></span>](protection-settings-for-windows-10-pcs.md)
  

