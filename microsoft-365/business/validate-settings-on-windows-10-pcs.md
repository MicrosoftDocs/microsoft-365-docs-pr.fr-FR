---
title: Valider les paramètres de protection des applications sur les PC Windows 10
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Adm_O365
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MiniMaven
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Découvrez comment valider les paramètres de protection Microsoft 365 Business application pour les appareils Windows 10.
ms.openlocfilehash: db05c86bd75cc30e22e025034a3dab478d0f5365
ms.sourcegitcommit: e491c4713115610cbe13d2fbd0d65e1a41c34d62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/16/2019
ms.locfileid: "26867006"
---
# <a name="validate-device-protection-settings-on-windows-10-pcs"></a><span data-ttu-id="834c2-103">Valider les paramètres de protection de périphériques sur Windows 10 PC</span><span class="sxs-lookup"><span data-stu-id="834c2-103">Validate device protection settings on Windows 10 PCs</span></span>

## <a name="verify-that-windows-10-device-policies-are-set"></a><span data-ttu-id="834c2-104">Vérifiez que les stratégies d’appareil Windows 10 sont définies</span><span class="sxs-lookup"><span data-stu-id="834c2-104">Verify that Windows 10 device policies are set</span></span>

<span data-ttu-id="834c2-p101">Après vous [configurez des stratégies de périphériques](protection-settings-for-windows-10-pcs.md), elle peut prendre quelques heures pour la stratégie prennent effet sur les périphériques des utilisateurs. Vous pouvez vérifier que les stratégies en vigueur en examinant les écrans différents paramètres Windows sur les périphériques de l’utilisateur. Étant donné que les utilisateurs ne seront pas en mesure de modifier les paramètres de mise à jour de Windows et Windows Defender Antivirus sur leurs appareils Windows 10, un grand nombre de ces options est grisé.</span><span class="sxs-lookup"><span data-stu-id="834c2-p101">After you [set up devices policies](protection-settings-for-windows-10-pcs.md), it may take up to a few hours for the policy to take effect on users' devices. You can confirm that the policies took effect by looking at various Windows Settings screens on the users' devices. Because the users won't be able to modify the Windows Update and Windows Defender Antivirus settings on their Windows 10 devices, a lot of those options will be greyed out.</span></span>
  
1. <span data-ttu-id="834c2-108">Accédez à **paramètres** \> **mise à jour &amp; sécurité** \> **Mise à jour Windows** \> **les options de redémarrage** et vérifiez que tous les paramètres sont estompées.</span><span class="sxs-lookup"><span data-stu-id="834c2-108">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Restart options** and confirm that all settings are greyed out.</span></span> 
    
    ![Toutes les options de redémarrage sont estompées.](media/31308da9-18b0-47c5-bbf6-d5fa6747c376.png)
  
2. <span data-ttu-id="834c2-110">Accédez à **paramètres** \> **mise à jour &amp; sécurité** \> **Mise à jour Windows** \> **options avancées** et vérifiez que tous les paramètres sont estompées.</span><span class="sxs-lookup"><span data-stu-id="834c2-110">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** and confirm that all settings are greyed out.</span></span> 
    
    ![Options avancées de Windows de mises à jour sont toutes estompées.](media/049cf281-d503-4be9-898b-c0a3286c7fc2.png)
  
3. <span data-ttu-id="834c2-112">Accédez à **paramètres** \> **mise à jour &amp; sécurité** \> **Mise à jour Windows** \> **options avancées** \> **Choisir comment les mises à jour sont remis**.</span><span class="sxs-lookup"><span data-stu-id="834c2-112">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** \> **Choose how updates are delivered**.</span></span>
    
    <span data-ttu-id="834c2-113">Vérifiez que vous pouvez voir le message (en rouge) certains paramètres sont masqués ou gérés par votre organisation, et toutes les options sont estompées.</span><span class="sxs-lookup"><span data-stu-id="834c2-113">Confirm that you can see the message (in red) that some settings are hidden or managed by your organization, and all the options are greyed out.</span></span>
    
    ![Choisir la façon dont les mises à jour sont remis page indique les paramètres sont masqués ou gérés par votre organisation.](media/6b3e37c5-da41-4afd-9983-b4f406216b59.png)
  
4. <span data-ttu-id="834c2-115">Pour ouvrir le centre de sécurité Windows Defender, accédez à **paramètres** \> **mise à jour &amp; sécurité** \> **Windows Defender** \> cliquez sur **Ouvrir le centre de sécurité Windows Defender** \> **Virus &amp; thread protection** \> **Virus &amp; paramètres de protection contre les menaces**.</span><span class="sxs-lookup"><span data-stu-id="834c2-115">To open the Windows Defender Security Center, go to **Settings** \> **Update &amp; security** \> **Windows Defender** \> click **Open Windows Defender Security Center** \> **Virus &amp; thread protection** \> **Virus &amp; threat protection settings**.</span></span> 
    
5. <span data-ttu-id="834c2-116">Vérifiez que toutes les options sont estompées.</span><span class="sxs-lookup"><span data-stu-id="834c2-116">Verify that all options are greyed out.</span></span> 
    
    ![Les paramètres de protection contre les Virus et les menaces sont estompées.](media/9ca68d40-a5d9-49d7-92a4-c581688b5926.png)
  
## <a name="related-topics"></a><span data-ttu-id="834c2-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="834c2-118">Related Topics</span></span>

[<span data-ttu-id="834c2-119">Documentation et ressources pour Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="834c2-119">Microsoft 365 Business documentation and resources</span></span>](https://go.microsoft.com/fwlink/p/?linkid=853701)
  
[<span data-ttu-id="834c2-120">Prise en main de Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="834c2-120">Get started with Microsoft 365 Business</span></span>](microsoft-365-business-overview.md)
  
[<span data-ttu-id="834c2-121">Gérer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="834c2-121">Manage Microsoft 365 Business</span></span>](manage.md)
  
[<span data-ttu-id="834c2-122">Définir des configurations d'application pour les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="834c2-122">Set device configurations for Windows 10 PCs</span></span>](protection-settings-for-windows-10-pcs.md)
  

