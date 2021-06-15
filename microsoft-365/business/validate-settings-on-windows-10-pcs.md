---
title: Valider les paramètres de protection des applications pour Windows 10 PC
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
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
- OKR_SMB_M365
- seo-marvel-mar
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: fae8819d-7235-495f-9f07-d016f545887f
description: Découvrez comment vérifier que les paramètres Microsoft 365 protection des applications pour les entreprises ont pris effet sur les appareils Windows 10 utilisateurs.
ms.openlocfilehash: 464a246a0da65dcffeb70946287ce4fa0e67ae7c
ms.sourcegitcommit: be929f79751c0c52dfa6bd98a854432a0c63faf0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "52925256"
---
# <a name="validate-device-protection-settings-for-windows-10-pcs"></a><span data-ttu-id="ae568-103">Valider les paramètres de protection des appareils Windows 10 PC</span><span class="sxs-lookup"><span data-stu-id="ae568-103">Validate device protection settings for Windows 10 PCs</span></span>

## <a name="verify-that-windows-10-device-policies-are-set"></a><span data-ttu-id="ae568-104">Vérifier que les Windows 10 d’appareil sont définies</span><span class="sxs-lookup"><span data-stu-id="ae568-104">Verify that Windows 10 device policies are set</span></span>

<span data-ttu-id="ae568-105">Une fois [les stratégies d’appareils](protection-settings-for-windows-10-pcs.md)définies, l’application de la stratégie sur les appareils des utilisateurs peut prendre jusqu’à quelques heures.</span><span class="sxs-lookup"><span data-stu-id="ae568-105">After you [set up devices policies](protection-settings-for-windows-10-pcs.md), it may take up to a few hours for the policy to take effect on users' devices.</span></span> <span data-ttu-id="ae568-106">Vous pouvez vérifier que les stratégies ont pris effet en regardant différents écrans Windows Paramètres sur les appareils des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ae568-106">You can confirm that the policies took effect by looking at various Windows Settings screens on the users' devices.</span></span> <span data-ttu-id="ae568-107">Étant donné que les utilisateurs ne pourront pas modifier les paramètres Windows Update et Antivirus Windows Defender sur leurs appareils Windows 10, de nombreuses options seront grisées.</span><span class="sxs-lookup"><span data-stu-id="ae568-107">Because the users won't be able to modify the Windows Update and Windows Defender Antivirus settings on their Windows 10 devices, many options will be grayed out.</span></span>
  
1. <span data-ttu-id="ae568-108">Go to **Paramètres** \> **Update &amp; security** \> **Windows Update** Restart \> **options** and confirm that all settings are grayed out.</span><span class="sxs-lookup"><span data-stu-id="ae568-108">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Restart options** and confirm that all settings are grayed out.</span></span> 
    
    ![Toutes les options de redémarrage sont grisées.](../media/31308da9-18b0-47c5-bbf6-d5fa6747c376.png)
  
2. <span data-ttu-id="ae568-110">Go to **Paramètres** \> **Update &amp; security** \> **Windows Update** Advanced \> **options** and confirm that all settings are grayed out.</span><span class="sxs-lookup"><span data-stu-id="ae568-110">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** and confirm that all settings are grayed out.</span></span> 
    
    ![Windows Les options de mises à jour avancées sont toutes grisées.](../media/049cf281-d503-4be9-898b-c0a3286c7fc2.png)
  
3. <span data-ttu-id="ae568-112">Go to **Paramètres** \> **Update &amp; security** \> **Windows Update** Advanced \> **options** Choose how \> **updates are delivered**.</span><span class="sxs-lookup"><span data-stu-id="ae568-112">Go to **Settings** \> **Update &amp; security** \> **Windows Update** \> **Advanced options** \> **Choose how updates are delivered**.</span></span>
    
    <span data-ttu-id="ae568-113">Confirmez que vous pouvez voir le message (en rouge) que certains paramètres sont masqués ou gérés par votre organisation, et que toutes les options sont grisées.</span><span class="sxs-lookup"><span data-stu-id="ae568-113">Confirm that you can see the message (in red) that some settings are hidden or managed by your organization, and all the options are grayed out.</span></span>
    
    ![Choisissez la manière dont les mises à jour sont remis page indique que les paramètres sont masqués ou gérés par votre organisation.](../media/6b3e37c5-da41-4afd-9983-b4f406216b59.png)
  
4. <span data-ttu-id="ae568-115">Pour ouvrir le Centre de sécurité  Windows Defender, Paramètres mettre à jour la sécurité Windows Defender cliquez sur Ouvrir Windows Defender Paramètres de protection antivirus contre les menaces du Centre de \> **&amp;** \>  \>  \> **&amp;** \> **&amp; sécurité.**</span><span class="sxs-lookup"><span data-stu-id="ae568-115">To open the Windows Defender Security Center, go to **Settings** \> **Update &amp; security** \> **Windows Defender** \> click **Open Windows Defender Security Center** \> **Virus &amp; thread protection** \> **Virus &amp; threat protection settings**.</span></span> 
    
5. <span data-ttu-id="ae568-116">Vérifiez que toutes les options sont grisées.</span><span class="sxs-lookup"><span data-stu-id="ae568-116">Verify that all options are grayed out.</span></span> 
    
    ![Les paramètres de protection contre les virus et les menaces sont grisés.](../media/9ca68d40-a5d9-49d7-92a4-c581688b5926.png)
  
## <a name="related-topics"></a><span data-ttu-id="ae568-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae568-118">Related Topics</span></span>

[<span data-ttu-id="ae568-119">Microsoft 365 documentation et ressources pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="ae568-119">Microsoft 365 for business documentation and resources</span></span>](./index.yml)
  
[<span data-ttu-id="ae568-120">Mise en place Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="ae568-120">Get started with Microsoft 365 for business</span></span>](microsoft-365-business-overview.md)
  
[<span data-ttu-id="ae568-121">Gérer Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="ae568-121">Manage Microsoft 365 for business</span></span>](manage.md)
  
[<span data-ttu-id="ae568-122">Définir des configurations d'application pour les PC Windows 10</span><span class="sxs-lookup"><span data-stu-id="ae568-122">Set device configurations for Windows 10 PCs</span></span>](protection-settings-for-windows-10-pcs.md)
