---
title: Lancer votre portail à l’aide du planificateur de lancement du portail
ms.author: jhendr
author: jhendr
manager: pamgreen
audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- SPO_Content
f1.keywords:
- CSH
ms.custom: Adm_O365
search.appverid:
- SPO160
- MET150
description: Cet article explique comment lancer votre portail à l’aide du planificateur de lancement de portail
ms.openlocfilehash: 929492742fd140654bd13be8165093ee10647c6d
ms.sourcegitcommit: da34ac08c7d029c2c42d4428d0bb03fd57c448be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "48999578"
---
# <a name="launch-your-portal-using-the-portal-launch-scheduler"></a><span data-ttu-id="dfa50-103">Lancer votre portail à l’aide du planificateur de lancement du portail</span><span class="sxs-lookup"><span data-stu-id="dfa50-103">Launch your portal using the Portal Launch Scheduler</span></span>

<span data-ttu-id="dfa50-104">Vous pouvez lancer votre portail à l’aide du planificateur de lancement de portail en validant d’abord la capacité de l’administrateur client à configurer une vague pour un nouveau portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-104">You can launch your portal using the Portal Launch Scheduler by first validating the tenant admin's ability to setup a waves for a new portal.</span></span> <span data-ttu-id="dfa50-105">L’administrateur peut ensuite valider une redirection de demandes en fonction de l’existence d’un utilisateur dans les ondes actives.</span><span class="sxs-lookup"><span data-stu-id="dfa50-105">Then the admin can validate a redirection of requests, based on the existence of a user in the active waves.</span></span>

<span data-ttu-id="dfa50-106">Pour plus d’informations sur le lancement d’un portail réussi, suivez les principes de base, les pratiques et les recommandations détaillés dans la rubrique [création, lancement et maintenance d’un portail intègre](https://go.microsoft.com/fwlink/?linkid=2105838).</span><span class="sxs-lookup"><span data-stu-id="dfa50-106">For more information about launching a successful portal, follow the basic principles, practices, and recommendations detailed in the [Creating, launching and maintaining a healthy portal](https://go.microsoft.com/fwlink/?linkid=2105838).</span></span> 

## <a name="app-setup"></a><span data-ttu-id="dfa50-107">Installation de l’application</span><span class="sxs-lookup"><span data-stu-id="dfa50-107">App setup</span></span>
1. <span data-ttu-id="dfa50-108">Désinstallez-le si vous disposez `Microsoft.Online.SharePoint.PowerShell` d’un ordinateur existant dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="dfa50-108">Uninstall if there an existing `Microsoft.Online.SharePoint.PowerShell` from your machine through the control panel.</span></span>
2. <span data-ttu-id="dfa50-109">Sur PowerShell `Install-Module -Name Microsoft.Online.SharePoint.PowerShell` .</span><span class="sxs-lookup"><span data-stu-id="dfa50-109">On PowerShell pass `Install-Module -Name Microsoft.Online.SharePoint.PowerShell`.</span></span>

## <a name="connect-to-sharepoint-online"></a><span data-ttu-id="dfa50-110">Se connecter à SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="dfa50-110">Connect to SharePoint Online</span></span>
1. <span data-ttu-id="dfa50-111">Ouvrez [SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) dans Windows.</span><span class="sxs-lookup"><span data-stu-id="dfa50-111">Open the [SharePoint Online Management Shell](https://docs.microsoft.com/powershell/sharepoint/sharepoint-online/connect-sharepoint-online) in Windows.</span></span>
2. <span data-ttu-id="dfa50-112">Connectez-vous à votre client en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="dfa50-112">Connect to your tenant as an admin.</span></span>
   - `Connect-SPOService -Url "https://*-admin.sharepoint.com" -Credential "username”`
3.  <span data-ttu-id="dfa50-113">Entrez votre mot de passe lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="dfa50-113">Supply your password when prompted.</span></span>

## <a name="command-to-get-an-existing-setup"></a><span data-ttu-id="dfa50-114">Commande pour obtenir une configuration existante</span><span class="sxs-lookup"><span data-stu-id="dfa50-114">Command to get an existing setup</span></span>

<span data-ttu-id="dfa50-115">Pour afficher les configurations de lancement de portail existantes :</span><span class="sxs-lookup"><span data-stu-id="dfa50-115">To view existing portal launch configurations:</span></span>

1. <span data-ttu-id="dfa50-116">Transmettre `Get-SPOPortalLaunchWaves  -LaunchSiteUrl  https://*.sharepoint.com/sites/newsite` .</span><span class="sxs-lookup"><span data-stu-id="dfa50-116">Pass `Get-SPOPortalLaunchWaves  -LaunchSiteUrl  https://*.sharepoint.com/sites/newsite`.</span></span>
2. <span data-ttu-id="dfa50-117">Transmettez le paramètre supplémentaire `-DisplayFormat Raw` si vous souhaitez voir la collection Wave au format RAW.</span><span class="sxs-lookup"><span data-stu-id="dfa50-117">Pass the additional parameter `-DisplayFormat Raw` if you wish to see the wave collection formatted as a raw input format.</span></span>

## <a name="commands-for-bi-directional-redirection"></a><span data-ttu-id="dfa50-118">Commandes de redirection bidirectionnelle</span><span class="sxs-lookup"><span data-stu-id="dfa50-118">Commands for bi-directional redirection</span></span>

<span data-ttu-id="dfa50-119">Pour migrer les anciens utilisateurs de site vers le nouveau site de manière intermédiaire :</span><span class="sxs-lookup"><span data-stu-id="dfa50-119">To migrate old site users to the new site in a staged manner:</span></span>

1. <span data-ttu-id="dfa50-120">Créez des vagues de lancement de portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-120">Create Portal launch waves.</span></span>
   - <span data-ttu-id="dfa50-121">Ceci s’applique uniquement lors de la phase de test de la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="dfa50-121">This is only applicable in the early release test phase.</span></span>
   - <span data-ttu-id="dfa50-122">Pour tester immédiatement l’impact de la modification, assurez-vous que la première vague `LaunchDateUtc` est définie sur la date actuelle.</span><span class="sxs-lookup"><span data-stu-id="dfa50-122">To test the impact of the change immediately, make sure the first wave `LaunchDateUtc` is set to the current date.</span></span> <span data-ttu-id="dfa50-123">Si vous ne fournissez pas cet indicateur, vous obtenez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dfa50-123">If you do not supply this flag, you get an error message.</span></span> <span data-ttu-id="dfa50-124">Cette erreur se produit car les lancements en production doivent être planifiés au moins 7 jours à l’avance.</span><span class="sxs-lookup"><span data-stu-id="dfa50-124">This error happens because launches in production must be scheduled at least 7 days in advance.</span></span>

  `New-SPOPortalLaunchWaves  -LaunchSiteUrl "https://*.sharepoint.com/sites/newsite" -RedirectionType Bidirectional -RedirectUrl "https://*.sharepoint.com/sites/oldsite" -ExpectedNumberOfUsers LessThan10kUsers -WaveOverrideUsers "*@microsoft.com" -Waves ' [{Name:"Wave 1", Groups:["Viewers SG1"], LaunchDateUtc:"2020/10/14"}, {Name:"Wave 2", Groups:["Viewers SG2"], LaunchDateUtc:"2020/10/15"}]' -IsTesting $true`

2. <span data-ttu-id="dfa50-125">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="dfa50-125">Complete validation.</span></span>
  - <span data-ttu-id="dfa50-126">La redirection peut prendre jusqu’à 5 minutes pour terminer sa configuration au sein du service ; par conséquent, veuillez patienter avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="dfa50-126">It can take up to 5 minutes for the redirection to complete its configuration across the service, so please wait before continuing.</span></span>
  - <span data-ttu-id="dfa50-127">Si vous vous connectez avec l’utilisateur spécifié en tant que `WaveOverrideUsers` , aucune modification n’est apportée.</span><span class="sxs-lookup"><span data-stu-id="dfa50-127">If you login with the user specified as `WaveOverrideUsers`, then nothing changes.</span></span> <span data-ttu-id="dfa50-128">Vous devez rester sur le site sur lequel vous avez accédé.</span><span class="sxs-lookup"><span data-stu-id="dfa50-128">You should be staying at the site you navigated to.</span></span>
  - <span data-ttu-id="dfa50-129">Connectez-vous avec un utilisateur qui fait partie des *visionneuses SG1*.</span><span class="sxs-lookup"><span data-stu-id="dfa50-129">Login with a user who is part of *Viewers SG1*.</span></span>
    - <span data-ttu-id="dfa50-130">Accédez à l’ancien site et vous devez être redirigé vers le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-130">Navigate to the old site and you should be redirected to the new site.</span></span>
    - <span data-ttu-id="dfa50-131">Accédez au nouveau site et restez sur le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-131">Navigate to the new site and you should be stay on the new site.</span></span>
    - <span data-ttu-id="dfa50-132">Connectez-vous avec l’utilisateur dans les *visionneuses SG2* et accédez à l’ancien site et restez sur l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-132">Log with user in *Viewers SG2* and navigate to the old site and stay on the old site.</span></span>
    - <span data-ttu-id="dfa50-133">Accédez au nouveau site et vous devez être redirigé vers l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-133">Navigate to the new site and you should be redirected to the old site.</span></span>

3. <span data-ttu-id="dfa50-134">Suspendre le lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-134">Pause Portal launch.</span></span>
  - <span data-ttu-id="dfa50-135">Si vous devez suspendre les ondes de lancement, vous pouvez les suspendre pendant « x » jours.</span><span class="sxs-lookup"><span data-stu-id="dfa50-135">If you need to pause the launch waves, you can pause them for "x" number of days.</span></span> <span data-ttu-id="dfa50-136">La définition `Status` de la suspension de l’indicateur empêche toute progression des vagues à venir.</span><span class="sxs-lookup"><span data-stu-id="dfa50-136">Setting the `Status` flag to pause prevents all upcoming wave progressions.</span></span> 
  - <span data-ttu-id="dfa50-137">`Set-SPOPortalLaunchWaves -Status Pause - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span><span class="sxs-lookup"><span data-stu-id="dfa50-137">`Set-SPOPortalLaunchWaves -Status Pause - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span></span>
  - <span data-ttu-id="dfa50-138">Cela permet de valider que tous les utilisateurs sont redirigés vers l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-138">This validates that all users are redirected to the old site.</span></span>

4. <span data-ttu-id="dfa50-139">Redémarrez la progression du lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-139">Restart the portal launch progression.</span></span> 
  - <span data-ttu-id="dfa50-140">`Set-SPOPortalLaunchWaves -Status Restart - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span><span class="sxs-lookup"><span data-stu-id="dfa50-140">`Set-SPOPortalLaunchWaves -Status Restart - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span></span>
  - <span data-ttu-id="dfa50-141">Vérifiez que la redirection est maintenant restaurée.</span><span class="sxs-lookup"><span data-stu-id="dfa50-141">Validate that the redirection is now restored.</span></span>

5. <span data-ttu-id="dfa50-142">Supprimer un portail lancer le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="dfa50-142">Delete a portal launch setup.</span></span>
  - <span data-ttu-id="dfa50-143">`Remove-SPOPortalLaunchWaves -LaunchSiteUrl https://*.sharepoint.com/sites/NewSite`.</span><span class="sxs-lookup"><span data-stu-id="dfa50-143">`Remove-SPOPortalLaunchWaves -LaunchSiteUrl https://*.sharepoint.com/sites/NewSite`.</span></span>
  - <span data-ttu-id="dfa50-144">Vérifiez qu’aucune redirection ne se produit pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dfa50-144">Validate that no redirection happens for all users.</span></span>

## <a name="commands-for-redirection-to-temporary-page"></a><span data-ttu-id="dfa50-145">Commandes de redirection vers une page temporaire</span><span class="sxs-lookup"><span data-stu-id="dfa50-145">Commands for redirection to temporary page</span></span>

<span data-ttu-id="dfa50-146">Suivez ces étapes si vous n’avez pas de site précédent et si vous ne souhaitez pas que les utilisateurs qui ne sont pas dans l’atterrissage se déplacent sur la nouvelle page de portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-146">Follow these steps if you have no previous site and you want to omit users not in the wave from landing on the new portal page.</span></span>

<span data-ttu-id="dfa50-147">Pour créer une page temporaire dans l’un des sites :</span><span class="sxs-lookup"><span data-stu-id="dfa50-147">To create a temporary page in any of the sites:</span></span>

1. <span data-ttu-id="dfa50-148">Créer une vague de lancement de portail.</span><span class="sxs-lookup"><span data-stu-id="dfa50-148">Create a Portal launch Wave.</span></span>
   - `New-SPOPortalLaunchWaves  -LaunchSiteUrl "https://*.sharepoint.com/sites/NewSite" -RedirectionType ToTemporaryPage -RedirectUrl "https://*.sharepoint.com/sites/OldSite" -ExpectedNumberOfUsers From10kTo30kUsers -WaveOverrideUsers *@microsoft.com -Waves [{Name:"Wave 1", Groups:["Viewers SG1"], LaunchDateUtc:"2020/10/14"}, {Name:"Wave 2", Groups:["Viewers SG2"], LaunchDateUtc:"2020/10/15"}]' -IsTesting $true`

2. <span data-ttu-id="dfa50-149">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="dfa50-149">Complete validation.</span></span>

  - <span data-ttu-id="dfa50-150">Patientez cinq minutes avant de poursuivre, car l’action peut prendre jusqu’à cinq minutes.</span><span class="sxs-lookup"><span data-stu-id="dfa50-150">Wait five minutes before continuing, as the action can take up to five minutes to complete.</span></span>
  - <span data-ttu-id="dfa50-151">Connectez-vous à l’utilisateur qui fait partie des *observateurs SG1* et :</span><span class="sxs-lookup"><span data-stu-id="dfa50-151">Log with the user who is part of *Viewers SG1* and:</span></span>
     - <span data-ttu-id="dfa50-152">Accédez au nouveau site, et vous devez rester sur le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="dfa50-152">Navigate to the new site, and you should be stay on the new site.</span></span>
     - <span data-ttu-id="dfa50-153">Naviguez jusqu’à la page Temp, et vous devez rester sur la page Temp.</span><span class="sxs-lookup"><span data-stu-id="dfa50-153">Navigate to the temp page, and you should be stay on the temp page.</span></span>
  - <span data-ttu-id="dfa50-154">Connectez-vous à l’utilisateur qui fait partie des *visionneuses SG2* et :</span><span class="sxs-lookup"><span data-stu-id="dfa50-154">Log with the user who is part of *Viewers SG2* and:</span></span>
     - <span data-ttu-id="dfa50-155">Naviguez jusqu’au nouveau site, et vous devez être redirigé vers la page Temp.</span><span class="sxs-lookup"><span data-stu-id="dfa50-155">Navigate to the new site, and you should be redirected to the temp page.</span></span>
     - <span data-ttu-id="dfa50-156">Accédez à la page Temp et restez sur la page Temp.</span><span class="sxs-lookup"><span data-stu-id="dfa50-156">Navigate to the temp page, and you should stay on the temp page.</span></span>

3. <span data-ttu-id="dfa50-157">Supprimer un portail lancer le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="dfa50-157">Delete a portal launch setup.</span></span>
  - <span data-ttu-id="dfa50-158">`Remove-SPOPortalLaunchWaves - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span><span class="sxs-lookup"><span data-stu-id="dfa50-158">`Remove-SPOPortalLaunchWaves - LaunchSiteUrl  https://*.sharepoint.com/sites/NewSite`.</span></span>
  - <span data-ttu-id="dfa50-159">Vérifiez qu’aucune redirection ne se produit pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="dfa50-159">Validate that no redirection happens for all users.</span></span>

## <a name="learn-more"></a><span data-ttu-id="dfa50-160">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="dfa50-160">Learn more</span></span>
[<span data-ttu-id="dfa50-161">Planification de votre plan de déploiement de lancement de portail dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="dfa50-161">Planning your portal launch roll-out plan in SharePoint Online</span></span>](https://docs.microsoft.com/microsoft-365/Enterprise/Planportallaunchroll-out)