---
title: Lancer votre portail à l’aide du Programmeur de lancement du portail
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
description: Cet article explique comment lancer votre portail à l’aide du Programmeur de lancement du portail
ms.openlocfilehash: e39f00dbc63ae7f1dcaf907d9c67df2c1683efc6
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50926141"
---
# <a name="launch-your-portal-using-the-portal-launch-scheduler"></a><span data-ttu-id="6f9f9-103">Lancer votre portail à l’aide du Programmeur de lancement du portail</span><span class="sxs-lookup"><span data-stu-id="6f9f9-103">Launch your portal using the Portal Launch Scheduler</span></span>

<span data-ttu-id="6f9f9-104">Un portail est un site SharePoint sur votre intranet et qui comporte un grand nombre d’internautes qui utilisent du contenu sur le site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-104">A portal is a SharePoint site on your intranet that has a large number of site viewers who consume content on the site.</span></span> <span data-ttu-id="6f9f9-105">Le lancement de votre portail par vagues est une partie importante de la garantie que les utilisateurs ont une expérience fluide et performante d’accès à un nouveau portail SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-105">Launching your portal in waves is an important part of ensuring users have a smooth and performant experience accessing a new SharePoint Online portal.</span></span> 

<span data-ttu-id="6f9f9-106">Le lancement par vagues est un moyen clé de déployer votre portail, comme détaillé dans la planification de votre plan de déploiement de lancement de portail [dans SharePoint Online.](./planportallaunchroll-out.md?view=o365-worldwide)</span><span class="sxs-lookup"><span data-stu-id="6f9f9-106">Launching in waves is a key way to roll-out your portal, as detailed in [Planning your portal launch roll-out plan in SharePoint Online](./planportallaunchroll-out.md?view=o365-worldwide).</span></span> <span data-ttu-id="6f9f9-107">Le Programme de lancement du portail est conçu pour vous aider à suivre une approche de déploiement wave/progressive en gérant les redirections pour le nouveau portail.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-107">The Portal Launch Scheduler is designed to help you follow a wave / phased roll-out approach by managing the redirects for the new portal.</span></span> <span data-ttu-id="6f9f9-108">Pendant chacune des vagues, vous pouvez recueillir les commentaires des utilisateurs et surveiller les performances pendant chaque vague de déploiement.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-108">During each of the waves, you can gather user feedback and monitor performance during each wave of deployment.</span></span> <span data-ttu-id="6f9f9-109">Cela a l’avantage d’introduire le portail lentement, de vous donner la possibilité de suspendre et de résoudre les problèmes avant de poursuivre la vague suivante, et de garantir finalement une expérience positive pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-109">This has the advantage of slowly introducing the portal, giving you the option to pause and resolve issues before proceeding with the next wave, and ultimately ensuring a positive experience for your users.</span></span> 

<span data-ttu-id="6f9f9-110">Il existe deux types de redirection :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-110">There are two types of redirection:</span></span> 
- <span data-ttu-id="6f9f9-111">bidirectionnel : lancer un nouveau portail SharePoint Online moderne pour remplacer un portail SharePoint classique ou moderne existant</span><span class="sxs-lookup"><span data-stu-id="6f9f9-111">bidirectional: launch a new modern SharePoint Online portal to replace an existing SharePoint classic or modern portal</span></span> 
- <span data-ttu-id="6f9f9-112">redirection de page temporaire : lancer un nouveau portail SharePoint Online moderne sans portail SharePoint existant</span><span class="sxs-lookup"><span data-stu-id="6f9f9-112">temporary page redirection: launch a new modern SharePoint Online portal with no existing SharePoint portal</span></span>

<span data-ttu-id="6f9f9-113">Le programme de lancement du portail est disponible uniquement pour lancer des portails SharePoint Online modernes (c’est-à-dire, des sites de communication).</span><span class="sxs-lookup"><span data-stu-id="6f9f9-113">The portal launch scheduler is only available to launch modern SharePoint Online portals (i.e. communication sites).</span></span> <span data-ttu-id="6f9f9-114">Les lancements doivent être programmés au moins 7 jours à l’avance.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-114">Launches must be scheduled at least 7 days in advance.</span></span> <span data-ttu-id="6f9f9-115">Le nombre de vagues requis est déterminé par le nombre d’utilisateurs attendu.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-115">The number of waves required is determined by the expected number of users.</span></span> <span data-ttu-id="6f9f9-116">Avant de planifier un lancement de portail, l’outil Diagnostic de page pour [SharePoint](./page-diagnostics-for-spo.md) doit être exécuté pour vérifier que la page d’accueil du portail est saine.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-116">Before scheduling a portal launch, the [Page Diagnostics for SharePoint tool](./page-diagnostics-for-spo.md) must be run to verify that the home page on the portal is healthy.</span></span> <span data-ttu-id="6f9f9-117">À la fin du lancement du portail, tous les utilisateurs ayant des autorisations sur le site pourront accéder au nouveau site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-117">At the end of the portal launch, all users with permissions to the site will be able to access the new site.</span></span> 

<span data-ttu-id="6f9f9-118">Pour plus d’informations sur le lancement d’un portail réussi, suivez les principes, pratiques et recommandations de base détaillés dans La création, le lancement et la maintenance d’un [portail sain.](/sharepoint/portal-health)</span><span class="sxs-lookup"><span data-stu-id="6f9f9-118">For more information about launching a successful portal, follow the basic principles, practices, and recommendations detailed in [Creating, launching and maintaining a healthy portal](/sharepoint/portal-health).</span></span> 

> [!NOTE]
> <span data-ttu-id="6f9f9-119">Cette fonctionnalité n’est pas disponible pour les plans Office 365 Germany, Office 365 géré par 21Vianet (Chine) ou Microsoft 365 pour le gouvernement américain.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-119">This feature is not available for Office 365 Germany, Office 365 operated by 21Vianet (China), or Microsoft 365 US Government plans.</span></span>

## <a name="app-setup-and-connecting-to-sharepoint-online"></a><span data-ttu-id="6f9f9-120">Configuration de l’application et connexion à SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6f9f9-120">App setup and connecting to SharePoint Online</span></span>
1. <span data-ttu-id="6f9f9-121">[Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="6f9f9-121">[Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f9f9-p104">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à Ajouter ou supprimer des programmes et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="6f9f9-p104">If you installed a previous version of the SharePoint Online Management Shell, go to Add or remove programs and uninstall "SharePoint Online Management Shell." </span></span><br><span data-ttu-id="6f9f9-123">Dans la page du Centre de téléchargement, sélectionnez votre langue, puis cliquez sur le bouton Télécharger.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-123">On the Download Center page, select your language and then click the Download button.</span></span> <span data-ttu-id="6f9f9-124">Vous serez invité à choisir entre le téléchargement d’un fichier .msi x64 et x86.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-124">You'll be asked to choose between downloading a x64 and x86 .msi file.</span></span> <span data-ttu-id="6f9f9-125">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-125">Download the x64 file if you're running the 64-bit version of Windows or the x86 file if you're running the 32-bit version.</span></span> <span data-ttu-id="6f9f9-126">En cas de doute, consultez [Quelle est la version du système d’exploitation Windows que j’utilise ?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="6f9f9-126">If you don't know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span> <span data-ttu-id="6f9f9-127">Une fois le fichier téléchargé, exécutez-le, puis suivez les étapes de l'Assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-127">After the file downloads, run it and follow the steps in the Setup Wizard.</span></span>

2. <span data-ttu-id="6f9f9-128">Connectez-vous à SharePoint en tant qu’[administrateur général ou administrateur SharePoint](/sharepoint/sharepoint-admin-role) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-128">Connect to SharePoint as a [global admin or SharePoint admin](/sharepoint/sharepoint-admin-role) in Microsoft 365.</span></span> <span data-ttu-id="6f9f9-129">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="6f9f9-129">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>


## <a name="view-any-existing-portal-launch-setups"></a><span data-ttu-id="6f9f9-130">Afficher les configurations de lancement de portail existantes</span><span class="sxs-lookup"><span data-stu-id="6f9f9-130">View any existing portal launch setups</span></span>

<span data-ttu-id="6f9f9-131">Pour voir s’il existe des configurations de lancement de portail :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-131">To see if there are existing portal launch configurations:</span></span>

   ```PowerShell
   Get-SPOPortalLaunchWaves -LaunchSiteUrl <object> -DisplayFormat <object>
   ```

## <a name="schedule-a-portal-launch-on-the-site"></a><span data-ttu-id="6f9f9-132">Planifier un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="6f9f9-132">Schedule a portal launch on the site</span></span>

<span data-ttu-id="6f9f9-133">Le nombre de vagues requises dépend de la taille de lancement attendue.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-133">The number of waves required depends on your expected launch size.</span></span> 
- <span data-ttu-id="6f9f9-134">Moins de 10 000 utilisateurs : 1 vague</span><span class="sxs-lookup"><span data-stu-id="6f9f9-134">Less than 10k users: 1 wave</span></span>
- <span data-ttu-id="6f9f9-135">10 000 à 30 000 utilisateurs : 3 vagues</span><span class="sxs-lookup"><span data-stu-id="6f9f9-135">10k to 30k users: 3 waves</span></span> 
- <span data-ttu-id="6f9f9-136">30 000 à 100 000 utilisateurs : 5 vagues</span><span class="sxs-lookup"><span data-stu-id="6f9f9-136">30k+ to 100k users: 5 waves</span></span>
- <span data-ttu-id="6f9f9-137">Plus de 100 000 utilisateurs : 5 vagues et contactez votre équipe de compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="6f9f9-137">More than 100k users: 5 waves and contact your Microsoft account team</span></span>

### <a name="steps-for-bidirectional-redirection"></a><span data-ttu-id="6f9f9-138">Étapes de redirection bidirectionnelle</span><span class="sxs-lookup"><span data-stu-id="6f9f9-138">Steps for bidirectional redirection</span></span>

<span data-ttu-id="6f9f9-139">La redirection bidirectionnelle implique le lancement d’un nouveau portail SharePoint Online moderne pour remplacer un portail SharePoint classique ou moderne existant.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-139">Bidirectional redirection involves launching a new modern SharePoint Online portal to replace an existing SharePoint classic or modern portal.</span></span> <span data-ttu-id="6f9f9-140">Les utilisateurs en vagues actives sont redirigés vers le nouveau site, qu’ils naviguent vers l’ancien ou le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-140">Users in active waves will be redirected to the new site regardless of whether they navigate to the old or new site.</span></span> <span data-ttu-id="6f9f9-141">Les utilisateurs d’une vague non lancée qui tentent d’accéder au nouveau site sont redirigés vers l’ancien site jusqu’à ce que leur vague soit lancée.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-141">Users in a non-launched wave that try to access the new site will be redirected back to the old site until their wave is launched.</span></span> 

<span data-ttu-id="6f9f9-142">La redirection est uniquement prise en charge entre la page d’accueil par défaut sur l’ancien site et la page d’accueil par défaut sur le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-142">We only support redirection between the default home page on the old site and the default home page on the new site.</span></span> <span data-ttu-id="6f9f9-143">Si vous avez des administrateurs ou des propriétaires qui ont besoin d’accéder aux anciens et nouveaux sites sans être redirigés, assurez-vous qu’ils sont répertoriés à l’aide du `WaveOverrideUsers` paramètre.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-143">Should you have administrators or owners that need access to the old and new sites without being redirected, ensure they are listed using the `WaveOverrideUsers` parameter.</span></span>

<span data-ttu-id="6f9f9-144">Pour migrer les utilisateurs d’un site SharePoint existant vers un nouveau site SharePoint de manière par étape :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-144">To migrate users from an existing SharePoint site to a new SharePoint site in a staged manner:</span></span>

1. <span data-ttu-id="6f9f9-145">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-145">Run the following command to designate portal launch waves.</span></span>
   
   ```PowerShell
    New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType Bidirectional -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
    ```

<span data-ttu-id="6f9f9-146">Exemple :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-146">Example:</span></span>
   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType Bidirectional -RedirectUrl "https://contoso.sharepoint.com/teams/oldsite" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
[{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
{Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"}, 
{Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="6f9f9-147">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-147">Complete validation.</span></span> <span data-ttu-id="6f9f9-148">La redirection peut prendre entre 5 et 10 minutes pour terminer sa configuration dans le service.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-148">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span> 

### <a name="steps-for-redirection-to-temporary-page"></a><span data-ttu-id="6f9f9-149">Étapes de redirection vers une page temporaire</span><span class="sxs-lookup"><span data-stu-id="6f9f9-149">Steps for redirection to temporary page</span></span>

<span data-ttu-id="6f9f9-150">La redirection de page temporaire doit être utilisée lorsqu’il n’existe aucun portail SharePoint existant.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-150">Temporary page redirection should be used when no existing SharePoint portal exists.</span></span> <span data-ttu-id="6f9f9-151">Les utilisateurs sont dirigés vers un nouveau portail SharePoint Online moderne de manière par étape.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-151">Users are directed to a new modern SharePoint Online portal in a staged manner.</span></span> <span data-ttu-id="6f9f9-152">Si un utilisateur est dans une vague qui n’a pas été lancée, il est redirigé vers une page temporaire (toute URL).</span><span class="sxs-lookup"><span data-stu-id="6f9f9-152">If a user is in a wave that has not been launched, they will be redirected to a temporary page (any URL).</span></span> 

1. <span data-ttu-id="6f9f9-153">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-153">Run the following command to designate portal launch waves.</span></span>
   
      ```PowerShell
    New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType ToTemporaryPage -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
    ```

<span data-ttu-id="6f9f9-154">Exemple :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-154">Example:</span></span>
   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType ToTemporaryPage -RedirectUrl "https://portal.contoso.com/UnderConstruction.aspx" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
[{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
{Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"}, 
{Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="6f9f9-155">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-155">Complete validation.</span></span> <span data-ttu-id="6f9f9-156">La redirection peut prendre entre 5 et 10 minutes pour terminer sa configuration dans le service.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-156">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span> 

## <a name="pause-or-restart-a-portal-launch-on-the-site"></a><span data-ttu-id="6f9f9-157">Suspendre ou redémarrer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="6f9f9-157">Pause or restart a portal launch on the site</span></span>

1. <span data-ttu-id="6f9f9-158">Pour interrompre un lancement du portail en cours et empêcher temporairement les progressions de vague à venir, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-158">To pause a portal launch in progress and temporarily prevent upcoming wave progressions from occurring, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Pause - LaunchSiteUrl <object>
   ```
2. <span data-ttu-id="6f9f9-159">Vérifier que tous les utilisateurs sont redirigés vers l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-159">Validate that all users are redirected to the old site.</span></span> 

3. <span data-ttu-id="6f9f9-160">Pour redémarrer un lancement du portail qui a été suspendu, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="6f9f9-160">To restart a portal launch that's been paused, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Restart - LaunchSiteUrl <object>
   ```
   
4. <span data-ttu-id="6f9f9-161">Vérifier que la redirection est maintenant restaurée.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-161">Validate that the redirection is now restored.</span></span> 

## <a name="delete-a-portal-launch-on-the-site"></a><span data-ttu-id="6f9f9-162">Supprimer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="6f9f9-162">Delete a portal launch on the site</span></span>

1. <span data-ttu-id="6f9f9-163">Exécutez la commande suivante pour supprimer un lancement de portail prévu ou en cours pour un site.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-163">Run the following command to delete a portal launch scheduled or in progress for a site.</span></span>

   ```PowerShell
   Remove-SPOPortalLaunchWaves -LaunchSiteUrl <object>
   ```

2. <span data-ttu-id="6f9f9-164">Vérifier qu’aucune redirection ne se produit pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6f9f9-164">Validate that no redirection happens for all users.</span></span>

## <a name="learn-more"></a><span data-ttu-id="6f9f9-165">Si vous souhaitez en savoir plus</span><span class="sxs-lookup"><span data-stu-id="6f9f9-165">Learn more</span></span>
[<span data-ttu-id="6f9f9-166">Planification de votre plan de déploiement de lancement de portail dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6f9f9-166">Planning your portal launch roll-out plan in SharePoint Online</span></span>](./planportallaunchroll-out.md)