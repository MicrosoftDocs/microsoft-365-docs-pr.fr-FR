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
ms.openlocfilehash: 6a191cf323e180fa77614eb09bae4185228a5029
ms.sourcegitcommit: e7bf23df4852b78912229d1d38ec475223597f34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "49087666"
---
# <a name="launch-your-portal-using-the-portal-launch-scheduler"></a><span data-ttu-id="625c0-103">Lancer votre portail à l’aide du planificateur de lancement du portail</span><span class="sxs-lookup"><span data-stu-id="625c0-103">Launch your portal using the Portal Launch Scheduler</span></span>

<span data-ttu-id="625c0-104">Un portail est un site SharePoint sur votre intranet et qui comporte un grand nombre d’internautes qui utilisent du contenu sur le site.</span><span class="sxs-lookup"><span data-stu-id="625c0-104">A portal is a SharePoint site on your intranet that has a large number of site viewers who consume content on the site.</span></span> <span data-ttu-id="625c0-105">Le lancement de votre portail dans les vagues est une partie importante de la façon de s’assurer que les utilisateurs ont une expérience fluide et performante qui accèdent à un nouveau portail SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="625c0-105">Launching your portal in waves is an important part of ensuring users have a smooth and performant experience accessing a new SharePoint Online portal.</span></span> 

<span data-ttu-id="625c0-106">Le lancement dans les vagues est un moyen clé de déployer votre portail, comme indiqué dans [la planification de votre plan de déploiement du lancement de portail dans SharePoint Online](https://docs.microsoft.com/en-us/microsoft-365/Enterprise/Planportallaunchroll-out?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="625c0-106">Launching in waves is a key way to roll-out your portal, as detailed in [Planning your portal launch roll-out plan in SharePoint Online](https://docs.microsoft.com/en-us/microsoft-365/Enterprise/Planportallaunchroll-out?view=o365-worldwide).</span></span> <span data-ttu-id="625c0-107">Le planificateur de lancement de portail est conçu pour vous aider à suivre une approche de déploiement Wave/phase en gérant les redirections pour le nouveau portail.</span><span class="sxs-lookup"><span data-stu-id="625c0-107">The Portal Launch Scheduler is designed to help you follow a wave / phased roll-out approach by managing the redirects for the new portal.</span></span> <span data-ttu-id="625c0-108">Pendant chacune des vagues, vous pouvez recueillir les commentaires des utilisateurs et surveiller les performances pendant chaque vague de déploiement.</span><span class="sxs-lookup"><span data-stu-id="625c0-108">During each of the waves, you can gather user feedback and monitor performance during each wave of deployment.</span></span> <span data-ttu-id="625c0-109">Cela présente l’avantage d’introduire lentement le portail, ce qui vous permet de suspendre et de résoudre les problèmes avant de passer à la prochaine vague, et de garantir une expérience positive pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="625c0-109">This has the advantage of slowly introducing the portal, giving you the option to pause and resolve issues before proceeding with the next wave, and ultimately ensuring a positive experience for your users.</span></span> 

<span data-ttu-id="625c0-110">Il existe deux types de redirection :</span><span class="sxs-lookup"><span data-stu-id="625c0-110">There are two types of redirection:</span></span> 
- <span data-ttu-id="625c0-111">bidirectionnel : lancer un nouveau portail SharePoint Online moderne pour remplacer un portail classique ou moderne SharePoint existant</span><span class="sxs-lookup"><span data-stu-id="625c0-111">bidirectional: launch a new modern SharePoint Online portal to replace an existing SharePoint classic or modern portal</span></span> 
- <span data-ttu-id="625c0-112">redirection temporaire des pages : lancer un nouveau portail SharePoint Online moderne sans portail SharePoint existant</span><span class="sxs-lookup"><span data-stu-id="625c0-112">temporary page redirection: launch a new modern SharePoint Online portal with no existing SharePoint portal</span></span>

<span data-ttu-id="625c0-113">Le planificateur de lancement du portail est uniquement disponible pour lancer des portails SharePoint Online modernes, comme les sites de communication et les sites d’équipe modernes.</span><span class="sxs-lookup"><span data-stu-id="625c0-113">The portal launch scheduler is only available to launch modern SharePoint Online portals, like communication sites and modern team sites.</span></span> <span data-ttu-id="625c0-114">Les lancements doivent être planifiés au moins 7 jours à l’avance.</span><span class="sxs-lookup"><span data-stu-id="625c0-114">Launches must be scheduled at least 7 days in advance.</span></span> <span data-ttu-id="625c0-115">Le nombre d’ondes requises est déterminé par le nombre d’utilisateurs attendu.</span><span class="sxs-lookup"><span data-stu-id="625c0-115">The number of waves required is determined by the expected number of users.</span></span> <span data-ttu-id="625c0-116">Avant de planifier le lancement d’un portail, l' [outil Diagnostics de la page pour SharePoint](https://aka.ms/perftool) doit être exécuté pour vérifier que la page d’accueil du portail est intègre.</span><span class="sxs-lookup"><span data-stu-id="625c0-116">Before scheduling a portal launch, the [Page Diagnostics for SharePoint tool](https://aka.ms/perftool) must be run to verify that the home page on the portal is healthy.</span></span> <span data-ttu-id="625c0-117">À la fin du lancement du portail, tous les utilisateurs disposant d’autorisations sur le site seront en mesure d’accéder au nouveau site.</span><span class="sxs-lookup"><span data-stu-id="625c0-117">At the end of the portal launch, all users with permissions to the site will be able to access the new site.</span></span> 

<span data-ttu-id="625c0-118">Pour plus d’informations sur le lancement d’un portail réussi, suivez les principes de base, les pratiques et les recommandations détaillés dans [Creating, lancement and Maintaining a successful Portal](https://docs.microsoft.com/sharepoint/portal-health).</span><span class="sxs-lookup"><span data-stu-id="625c0-118">For more information about launching a successful portal, follow the basic principles, practices, and recommendations detailed in [Creating, launching and maintaining a healthy portal](https://docs.microsoft.com/sharepoint/portal-health).</span></span> 

> [!NOTE]
> <span data-ttu-id="625c0-119">Cette fonctionnalité n’est pas disponible pour Office 365 Germany, Office 365 géré par 21Vianet (Chine) ou Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="625c0-119">This feature is not available for Office 365 Germany, Office 365 operated by 21Vianet (China), or Microsoft 365 US Government plans.</span></span>

## <a name="app-setup-and-connecting-to-sharepoint-online"></a><span data-ttu-id="625c0-120">Installation de l’application et connexion à SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="625c0-120">App setup and connecting to SharePoint Online</span></span>
1. <span data-ttu-id="625c0-121">[Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="625c0-121">[Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

    > [!NOTE]
    > <span data-ttu-id="625c0-p104">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à Ajouter ou supprimer des programmes et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="625c0-p104">If you installed a previous version of the SharePoint Online Management Shell, go to Add or remove programs and uninstall "SharePoint Online Management Shell." </span></span><br><span data-ttu-id="625c0-123">Dans la page du Centre de téléchargement, sélectionnez votre langue, puis cliquez sur le bouton Télécharger.</span><span class="sxs-lookup"><span data-stu-id="625c0-123">On the Download Center page, select your language and then click the Download button.</span></span> <span data-ttu-id="625c0-124">Vous serez invité à choisir entre le téléchargement d’un fichier .msi x64 et x86.</span><span class="sxs-lookup"><span data-stu-id="625c0-124">You'll be asked to choose between downloading a x64 and x86 .msi file.</span></span> <span data-ttu-id="625c0-125">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="625c0-125">Download the x64 file if you're running the 64-bit version of Windows or the x86 file if you're running the 32-bit version.</span></span> <span data-ttu-id="625c0-126">En cas de doute, consultez [Quelle est la version du système d’exploitation Windows que j’utilise ?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="625c0-126">If you don't know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span> <span data-ttu-id="625c0-127">Une fois le fichier téléchargé, exécutez-le, puis suivez les étapes de l'Assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="625c0-127">After the file downloads, run it and follow the steps in the Setup Wizard.</span></span>

2. <span data-ttu-id="625c0-128">Connectez-vous à SharePoint en tant qu’[administrateur général ou administrateur SharePoint](/sharepoint/sharepoint-admin-role) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="625c0-128">Connect to SharePoint as a [global admin or SharePoint admin](/sharepoint/sharepoint-admin-role) in Microsoft 365.</span></span> <span data-ttu-id="625c0-129">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="625c0-129">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>


## <a name="view-any-existing-portal-launch-setups"></a><span data-ttu-id="625c0-130">Afficher les configurations de lancement de portail existantes</span><span class="sxs-lookup"><span data-stu-id="625c0-130">View any existing portal launch setups</span></span>

<span data-ttu-id="625c0-131">Pour voir s’il existe des configurations de lancement de portail existantes :</span><span class="sxs-lookup"><span data-stu-id="625c0-131">To see if there are existing portal launch configurations:</span></span>

   ```PowerShell
   Get-SPOPortalLaunchWaves -LaunchSiteUrl <object> -DisplayFormat <object>
   ```

## <a name="schedule-a-portal-launch-on-the-site"></a><span data-ttu-id="625c0-132">Planifier un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="625c0-132">Schedule a portal launch on the site</span></span>

<span data-ttu-id="625c0-133">Le nombre d’ondes requises dépend de la taille de lancement attendue.</span><span class="sxs-lookup"><span data-stu-id="625c0-133">The number of waves required depends on your expected launch size.</span></span> 
- <span data-ttu-id="625c0-134">Moins de 10 000 utilisateurs : 1 vague</span><span class="sxs-lookup"><span data-stu-id="625c0-134">Less than 10k users: 1 wave</span></span>
- <span data-ttu-id="625c0-135">10 000 à 30k utilisateurs : 3 vagues</span><span class="sxs-lookup"><span data-stu-id="625c0-135">10k to 30k users: 3 waves</span></span> 
- <span data-ttu-id="625c0-136">30k + 100 000 utilisateurs : 5 ondulations</span><span class="sxs-lookup"><span data-stu-id="625c0-136">30k+ to 100k users: 5 waves</span></span>
- <span data-ttu-id="625c0-137">Plus de 100 000 utilisateurs : 5 ondulations et contacter votre équipe de compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="625c0-137">More than 100k users: 5 waves and contact your Microsoft account team</span></span>

### <a name="steps-for-bi-directional-redirection"></a><span data-ttu-id="625c0-138">Étapes de la redirection bidirectionnelle</span><span class="sxs-lookup"><span data-stu-id="625c0-138">Steps for bi-directional redirection</span></span>

<span data-ttu-id="625c0-139">La redirection bidirectionnelle implique le lancement d’un nouveau portail SharePoint Online moderne pour remplacer un portail classique ou moderne SharePoint existant.</span><span class="sxs-lookup"><span data-stu-id="625c0-139">Bidirectional redirection involves launching a new modern SharePoint Online portal to replace an existing SharePoint classic or modern portal.</span></span> <span data-ttu-id="625c0-140">Les utilisateurs des ondes actives seront redirigés vers le nouveau site, qu’ils naviguaient vers l’ancien ou le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="625c0-140">Users in active waves will be redirected to the new site regardless of whether they navigate to the old or new site.</span></span> <span data-ttu-id="625c0-141">Les utilisateurs d’une vague non lancée qui tentent d’accéder au nouveau site sont redirigés vers l’ancien site jusqu’à ce que leur vague soit lancée.</span><span class="sxs-lookup"><span data-stu-id="625c0-141">Users in a non-launched wave that try to access the new site will be redirected back to the old site until their wave is launched.</span></span> <span data-ttu-id="625c0-142">Si vous avez des administrateurs ou des propriétaires qui ont besoin d’accéder aux anciens et aux nouveaux sites sans être redirigés, vérifiez qu’ils sont répertoriés à l’aide du `WaveOverrideUsers` paramètre.</span><span class="sxs-lookup"><span data-stu-id="625c0-142">Should you have administrators or owners that need access to the old and new sites without being redirected, ensure they are listed using the `WaveOverrideUsers` parameter.</span></span> 

<span data-ttu-id="625c0-143">Pour migrer des utilisateurs à partir d’un site SharePoint existant vers un nouveau site SharePoint de manière intermédiaire :</span><span class="sxs-lookup"><span data-stu-id="625c0-143">To migrate users from an existing SharePoint site to a new SharePoint site in a staged manner:</span></span>

1. <span data-ttu-id="625c0-144">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="625c0-144">Run the following command to designate portal launch waves.</span></span>
   
   ```PowerShell
    New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType Bidirectional -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
    ```

<span data-ttu-id="625c0-145">Exemple :</span><span class="sxs-lookup"><span data-stu-id="625c0-145">Example:</span></span>
   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType Bidirectional -RedirectUrl "https://contoso.sharepoint.com/teams/oldsite" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
[{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
{Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"}, 
{Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="625c0-146">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="625c0-146">Complete validation.</span></span> <span data-ttu-id="625c0-147">La redirection peut prendre 5-10 minutes pour terminer sa configuration au sein du service.</span><span class="sxs-lookup"><span data-stu-id="625c0-147">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span> 

### <a name="steps-for-redirection-to-temporary-page"></a><span data-ttu-id="625c0-148">Étapes de la redirection vers la page temporaire</span><span class="sxs-lookup"><span data-stu-id="625c0-148">Steps for redirection to temporary page</span></span>

<span data-ttu-id="625c0-149">La redirection de page temporaire doit être utilisée lorsqu’il n’existe aucun portail SharePoint existant.</span><span class="sxs-lookup"><span data-stu-id="625c0-149">Temporary page redirection should be used when no existing SharePoint portal exists.</span></span> <span data-ttu-id="625c0-150">Les utilisateurs sont dirigés vers un nouveau portail SharePoint Online moderne de manière intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="625c0-150">Users are directed to a new modern SharePoint Online portal in a staged manner.</span></span> <span data-ttu-id="625c0-151">Si un utilisateur est dans une vague qui n’a pas été lancée, il est redirigé vers une page temporaire (n’importe quelle URL).</span><span class="sxs-lookup"><span data-stu-id="625c0-151">If a user is in a wave that has not been launched, they will be redirected to a temporary page (any URL).</span></span> 

1. <span data-ttu-id="625c0-152">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="625c0-152">Run the following command to designate portal launch waves.</span></span>
   
      ```PowerShell
    New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType ToTemporaryPage -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
    ```

<span data-ttu-id="625c0-153">Exemple :</span><span class="sxs-lookup"><span data-stu-id="625c0-153">Example:</span></span>
   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType ToTemporaryPage -RedirectUrl "https://portal.contoso.com/UnderConstruction.aspx" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
[{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
{Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"}, 
{Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="625c0-154">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="625c0-154">Complete validation.</span></span> <span data-ttu-id="625c0-155">La redirection peut prendre 5-10 minutes pour terminer sa configuration au sein du service.</span><span class="sxs-lookup"><span data-stu-id="625c0-155">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span> 
   - `New-SPOPortalLaunchWaves  -LaunchSiteUrl "https://*.sharepoint.com/sites/newsite" -RedirectionType Bidirectional -RedirectUrl "https://*.sharepoint.com/sites/oldsite" -ExpectedNumberOfUsers LessThan10kUsers -WaveOverrideUsers "*@microsoft.com" -Waves ' [{Name:"Wave 1", Groups:["Viewers SG1"], LaunchDateUtc:"2020/10/14"}, {Name:"Wave 2", Groups:["Viewers SG2"], LaunchDateUtc:"2020/10/15"}]' -IsTesting $true`

## <a name="pause-or-restart-a-portal-launch-on-the-site"></a><span data-ttu-id="625c0-156">Suspendre ou redémarrer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="625c0-156">Pause or restart a portal launch on the site</span></span>

1. <span data-ttu-id="625c0-157">Pour suspendre le lancement d’un portail en cours et empêcher temporairement les progrès à venir, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="625c0-157">To pause a portal launch in progress and temporarily prevent upcoming wave progressions from occurring, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Pause - LaunchSiteUrl <object>
   ```
2. <span data-ttu-id="625c0-158">Vérifiez que tous les utilisateurs sont redirigés vers l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="625c0-158">Validate that all users are redirected to the old site.</span></span> 

3. <span data-ttu-id="625c0-159">Pour redémarrer un lancement de portail suspendu, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="625c0-159">To restart a portal launch that's been paused, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Restart - LaunchSiteUrl <object>
   ```
   
4. <span data-ttu-id="625c0-160">Vérifiez que la redirection est maintenant restaurée.</span><span class="sxs-lookup"><span data-stu-id="625c0-160">Validate that the redirection is now restored.</span></span> 

## <a name="delete-a-portal-launch-on-the-site"></a><span data-ttu-id="625c0-161">Supprimer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="625c0-161">Delete a portal launch on the site</span></span>
1. <span data-ttu-id="625c0-162">Créer une vague de lancement de portail.</span><span class="sxs-lookup"><span data-stu-id="625c0-162">Create a Portal launch Wave.</span></span>
  - `New-SPOPortalLaunchWaves  -LaunchSiteUrl "https://*.sharepoint.com/sites/NewSite" -RedirectionType ToTemporaryPage -RedirectUrl "https://*.sharepoint.com/sites/OldSite" -ExpectedNumberOfUsers From10kTo30kUsers -WaveOverrideUsers *@microsoft.com -Waves [{Name:"Wave 1", Groups:["Viewers SG1"], LaunchDateUtc:"2020/10/14"}, {Name:"Wave 2", Groups:["Viewers SG2"], LaunchDateUtc:"2020/10/15"}]' -IsTesting $true`

2. <span data-ttu-id="625c0-163">Exécutez la commande suivante pour supprimer un lancement de portail planifié ou en cours pour un site.</span><span class="sxs-lookup"><span data-stu-id="625c0-163">Run the following command to delete a portal launch scheduled or in progress for a site.</span></span>

   ```PowerShell
   Remove-SPOPortalLaunchWaves -LaunchSiteUrl <object>
   ```

3. <span data-ttu-id="625c0-164">Vérifiez qu’aucune redirection ne se produit pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="625c0-164">Validate that no redirection happens for all users.</span></span>

## <a name="learn-more"></a><span data-ttu-id="625c0-165">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="625c0-165">Learn more</span></span>
[<span data-ttu-id="625c0-166">Planification de votre plan de déploiement de lancement de portail dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="625c0-166">Planning your portal launch roll-out plan in SharePoint Online</span></span>](https://docs.microsoft.com/microsoft-365/Enterprise/Planportallaunchroll-out)
