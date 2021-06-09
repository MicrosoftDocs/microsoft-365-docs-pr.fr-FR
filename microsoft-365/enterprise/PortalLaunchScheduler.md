---
title: Lancer votre portail à l’aide du programme de lancement du portail
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
description: Cet article décrit comment lancer votre portail à l’aide du programme de lancement du portail
ms.openlocfilehash: bf01f6ae93b424543a6a509f89961a1b7a0c9ad7
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841665"
---
# <a name="launch-your-portal-using-the-sharepoint-portal-launch-scheduler"></a><span data-ttu-id="25e23-103">Lancer votre portail à l’aide du SharePoint de lancement du portail</span><span class="sxs-lookup"><span data-stu-id="25e23-103">Launch your portal using the SharePoint Portal launch scheduler</span></span>

<span data-ttu-id="25e23-104">Un portail est un site de communication SharePoint sur votre intranet qui présente un trafic élevé : un site qui compte entre 10 000 et plus de 100 000 visiteurs sur plusieurs semaines.</span><span class="sxs-lookup"><span data-stu-id="25e23-104">A portal is a SharePoint communication site on your intranet that is high-traffic – a site that has anywhere from 10,000 to over 100,000 viewers over the course of several weeks.</span></span> <span data-ttu-id="25e23-105">Utilisez le programme de lancement du portail pour lancer votre portail afin de garantir aux utilisateurs une expérience d’affichage fluide lors de l’accès à SharePoint portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-105">Use the Portal launch scheduler to launch your portal to ensure users have a smooth viewing experience when accessing your new SharePoint portal.</span></span>
<br>
<br>
<span data-ttu-id="25e23-106">Le programme de lancement du portail est conçu pour vous aider à suivre une approche de déploiement par étapes en par lots de visionneuses par vagues et en gérant les redirections d’URL pour le nouveau portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-106">The Portal launch scheduler is designed to help you follow a phased roll-out approach by batching viewers in waves and managing the URL redirects for the new portal.</span></span> <span data-ttu-id="25e23-107">Au cours du lancement de chaque vague, vous pouvez recueillir les commentaires des utilisateurs, surveiller les performances du portail et suspendre le lancement pour résoudre les problèmes avant de poursuivre la vague suivante.</span><span class="sxs-lookup"><span data-stu-id="25e23-107">During the launch of each wave, you can gather user feedback, monitor portal performance, and pause the launch to resolve issues before proceeding with the next wave.</span></span> <span data-ttu-id="25e23-108">En savoir plus sur la [façon de planifier un lancement de portail dans SharePoint](/microsoft-365/Enterprise/Planportallaunchroll-out?view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="25e23-108">Learn more about how to [plan a portal launch in SharePoint](/microsoft-365/Enterprise/Planportallaunchroll-out?view=o365-worldwide).</span></span>

<span data-ttu-id="25e23-109">**Il existe deux types de redirections :**</span><span class="sxs-lookup"><span data-stu-id="25e23-109">**There are two types of redirections:**</span></span>

- <span data-ttu-id="25e23-110">**Bidirectionnel**: lancer un nouveau portail SharePoint moderne pour remplacer un portail SharePoint classique ou moderne existant</span><span class="sxs-lookup"><span data-stu-id="25e23-110">**Bidirectional**: launch a new modern SharePoint portal to replace an existing SharePoint classic or modern portal</span></span>
- <span data-ttu-id="25e23-111">**Rediriger vers une page temporaire**: lancer un nouveau portail SharePoint moderne sans portail SharePoint existant</span><span class="sxs-lookup"><span data-stu-id="25e23-111">**Redirect to a temporary page**: launch a new modern SharePoint portal with no existing SharePoint portal</span></span>

<span data-ttu-id="25e23-112">Les autorisations de site doivent être définies séparément des vagues dans le cadre du lancement.</span><span class="sxs-lookup"><span data-stu-id="25e23-112">Site permissions must be set up separately from waves as part of the launch.</span></span> <span data-ttu-id="25e23-113">Par exemple, si vous publiez un portail à l’échelle de l’organisation, vous pouvez définir des autorisations sur « Tout le monde sauf les utilisateurs externes », puis séparer vos utilisateurs en vagues à l’aide de groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="25e23-113">For example, if you are releasing an organization-wide portal, you can set permissions to “Everyone except external users,” then separate your users into waves using security groups.</span></span> <span data-ttu-id="25e23-114">L’ajout d’un groupe de sécurité à une vague ne lui donne pas accès au site.</span><span class="sxs-lookup"><span data-stu-id="25e23-114">Adding a security group to a wave does not give that security group access to the site.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="25e23-115">Cette fonctionnalité sera accessible à partir du panneau **Paramètres** sur la page d’accueil des sites de communication SharePoint pour les clients de publication ciblée à partir de mai 2021 et sera disponible pour tous les clients d’ici juillet 2021.</span><span class="sxs-lookup"><span data-stu-id="25e23-115">This feature will be accessible from the **Settings** panel on the home page of SharePoint communication sites for Targeted release customers starting in May 2021 and will become available to all customers by July 2021</span></span>
> - <span data-ttu-id="25e23-116">La version PowerShell de cet outil est disponible aujourd’hui</span><span class="sxs-lookup"><span data-stu-id="25e23-116">The PowerShell version of this tool is available today</span></span>
> - <span data-ttu-id="25e23-117">Cette fonctionnalité ne peut être utilisée que sur les sites de communication SharePoint modernes</span><span class="sxs-lookup"><span data-stu-id="25e23-117">This feature can only be used on modern SharePoint communication sites</span></span>
> - <span data-ttu-id="25e23-118">Vous devez avoir des autorisations de propriétaire de site pour personnaliser et planifier le lancement d’un portail</span><span class="sxs-lookup"><span data-stu-id="25e23-118">You must have site owner permissions for the site to customize and schedule the launch of a portal</span></span>
> - <span data-ttu-id="25e23-119">Les lancements doivent être programmés au moins sept jours à l’avance et chaque vague peut durer entre un et sept jours.</span><span class="sxs-lookup"><span data-stu-id="25e23-119">Launches must be scheduled at least seven days in advance and each wave can last one to seven days</span></span>
> - <span data-ttu-id="25e23-120">Le nombre de vagues requis est automatiquement déterminé par le nombre d’utilisateurs attendu</span><span class="sxs-lookup"><span data-stu-id="25e23-120">The number of waves required is automatically determined by the expected number of users</span></span>
> - <span data-ttu-id="25e23-121">Avant de planifier le lancement d’un portail, l’outil Diagnostic de page [pour SharePoint](https://aka.ms/perftool) doit être exécuté pour vérifier que la page d’accueil du site est saine</span><span class="sxs-lookup"><span data-stu-id="25e23-121">Before scheduling a portal launch, the [Page Diagnostics for SharePoint tool](https://aka.ms/perftool) must be run to verify that the home page of the site is healthy</span></span>
> - <span data-ttu-id="25e23-122">À la fin du lancement, tous les utilisateurs ayant des autorisations sur le site pourront accéder au nouveau site.</span><span class="sxs-lookup"><span data-stu-id="25e23-122">At the end of the launch, all users with permissions to the site will be able to access the new site</span></span>
> - <span data-ttu-id="25e23-123">Si votre organisation utilise [Connections,](/SharePoint/viva-connections)les utilisateurs peuvent voir l’icône de votre organisation dans la barre d’application Microsoft Teams. Toutefois, lorsque l’icône est sélectionnée, les utilisateurs ne pourront pas accéder au portail tant que leur vague n’aura pas été lancée.</span><span class="sxs-lookup"><span data-stu-id="25e23-123">If your organization is using [Viva Connections](/SharePoint/viva-connections), users may see your organization's icon in the Microsoft Teams app bar, however when the icon is selected users will not be able to access the portal until their wave has launched</span></span>
> - <span data-ttu-id="25e23-124">Cette fonctionnalité n’est pas disponible pour Office 365 Germany, Office 365 géré par 21Vianet (Chine) ou Microsoft 365 plans pour le gouvernement américain</span><span class="sxs-lookup"><span data-stu-id="25e23-124">This feature is not available for Office 365 Germany, Office 365 operated by 21Vianet (China), or Microsoft 365 US Government plans</span></span>

## <a name="understand-the-differences-between-portal-launch-scheduler-options"></a><span data-ttu-id="25e23-125">Comprendre les différences entre les options du programme de planification de lancement du portail :</span><span class="sxs-lookup"><span data-stu-id="25e23-125">Understand the differences between Portal launch scheduler options:</span></span>

<span data-ttu-id="25e23-126">Auparavant, les lancements de portail pouvaient uniquement être programmés SharePoint PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25e23-126">Formerly, portal launches could only be scheduled through SharePoint PowerShell.</span></span> <span data-ttu-id="25e23-127">Vous avez maintenant deux options pour vous aider à planifier et gérer le lancement de votre portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-127">Now, you have two options to help you schedule and manage your portal's launch.</span></span> <span data-ttu-id="25e23-128">Découvrez les principales différences entre les deux outils :</span><span class="sxs-lookup"><span data-stu-id="25e23-128">Learn about the key differences between both tools:</span></span>

<span data-ttu-id="25e23-129">**SharePoint Version de PowerShell :**</span><span class="sxs-lookup"><span data-stu-id="25e23-129">**SharePoint PowerShell version:**</span></span>

- <span data-ttu-id="25e23-130">Les informations d’identification d’administrateur sont requises [pour SharePoint PowerShell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)</span><span class="sxs-lookup"><span data-stu-id="25e23-130">Admin credentials are required to use [SharePoint PowerShell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell)</span></span>
- <span data-ttu-id="25e23-131">Exigence minimale d’une vague</span><span class="sxs-lookup"><span data-stu-id="25e23-131">Minimum requirement of one wave</span></span>
- <span data-ttu-id="25e23-132">Planifier votre lancement en fonction du fuseau horaire UTC (Temps universel coordonné)</span><span class="sxs-lookup"><span data-stu-id="25e23-132">Schedule your launch based on Coordinated Universal Time (UTC) time zone</span></span>

<span data-ttu-id="25e23-133">**Version du produit :**</span><span class="sxs-lookup"><span data-stu-id="25e23-133">**In-product version:**</span></span>

- <span data-ttu-id="25e23-134">Les informations d’identification du propriétaire du site sont requises</span><span class="sxs-lookup"><span data-stu-id="25e23-134">Site owner credentials are required</span></span>
- <span data-ttu-id="25e23-135">Exigence minimale de deux vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-135">Minimum requirement of two waves</span></span>
- <span data-ttu-id="25e23-136">Planifier votre lancement en fonction du fuseau horaire local du portail, comme indiqué dans les paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="25e23-136">Schedule your launch based on the portal's local time zone as indicated in regional settings</span></span>

## <a name="get-started-using-the-portal-launch-scheduler"></a><span data-ttu-id="25e23-137">Commencer à utiliser le programme de lancement du portail</span><span class="sxs-lookup"><span data-stu-id="25e23-137">Get started using the Portal launch scheduler</span></span>

1. <span data-ttu-id="25e23-138">Avant d’utiliser l’outil de planification de lancement du portail, ajoutez tous les utilisateurs qui auront besoin d’accéder à ce [site](https://support.microsoft.com/office/share-a-site-958771a8-d041-4eb8-b51c-afea2eae3658) via les **autorisations** site en tant que propriétaire du site, membre du site ou visiteur.</span><span class="sxs-lookup"><span data-stu-id="25e23-138">Before using the Portal launch scheduler tool, [add all users who will need access to this site](https://support.microsoft.com/office/share-a-site-958771a8-d041-4eb8-b51c-afea2eae3658) through **Site permissions** as a Site owner, Site member, or Visitor.</span></span>

2. <span data-ttu-id="25e23-139">Commencez ensuite à planifier le lancement de votre portail en accédant au programme de lancement du portail de deux manières :</span><span class="sxs-lookup"><span data-stu-id="25e23-139">Then, start scheduling your portal’s launch by accessing the Portal launch scheduler in one of two ways:</span></span>

   <span data-ttu-id="25e23-140">**Option 1**: les premières fois que vous modifiez et repupuyez les modifications apportées à votre page d’accueil (ou jusqu’à la version 3.0 de la page d’accueil), vous êtes invité à utiliser l’outil de planification de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-140">**Option 1**: The first few times you edit and republish changes to your home page - or up until home page version 3.0 - you will be prompted to use the Portal launch scheduler tool.</span></span> <span data-ttu-id="25e23-141">Sélectionnez **Planifier le lancement** pour aller de l’avant avec la planification.</span><span class="sxs-lookup"><span data-stu-id="25e23-141">Select **Schedule launch** to move forward with scheduling.</span></span> <span data-ttu-id="25e23-142">Vous pouvez également **sélectionner Republish** pour republier vos modifications de page sans planifier le lancement.</span><span class="sxs-lookup"><span data-stu-id="25e23-142">Or select **Republish** to republish your page edits without scheduling the launch.</span></span>

   ![Image de l’invite d’utilisation du programme de lancement du portail lors de la republier de la page d’accueil](../media/portal-launch-republish-2.png)

   <span data-ttu-id="25e23-144">**Option 2**: à tout moment, vous pouvez accéder à la page d’accueil du site de communication SharePoint, sélectionner **Paramètres** puis planifier le lancement du **site** pour planifier le lancement de votre portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-144">**Option 2**: At any time, you can navigate to the SharePoint communication site home page, select **Settings** and then **Schedule site launch** to schedule your portal’s launch.</span></span>

   ![Image du volet Paramètres avec planification d’un lancement de site mis en évidence](../media/portal-launch-settings-2.png)

3. <span data-ttu-id="25e23-146">Ensuite, confirmez le score d’état du portail et a amélioré le portail si nécessaire à l’aide de l’outil [Diagnostics](https://aka.ms/perftool) de page pour SharePoint jusqu’à ce que votre portail reçoit un **score** d’état d’santé.</span><span class="sxs-lookup"><span data-stu-id="25e23-146">Next, confirm the portal’s health score and make improvements to the portal if needed using the [Page Diagnostics for SharePoint](https://aka.ms/perftool) tool until your portal receives a **Healthy** score.</span></span> <span data-ttu-id="25e23-147">Puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="25e23-147">Then, select **Next**.</span></span>

   ![Image de l’outil de planification de lancement du portail](../media/portal-launch-panel-2.png)

   > [!NOTE]
   > <span data-ttu-id="25e23-149">Le nom et la description du site ne peuvent pas être modifiés à partir du programme de lancement du portail et peuvent être modifiés en sélectionnant **Paramètres** puis les informations du **site** dans la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="25e23-149">The site name and description can’t be edited from the Portal launch scheduler and instead can be changed by selecting **Settings** and then **Site information** from the home page.</span></span>

4. <span data-ttu-id="25e23-150">Sélectionnez **le nombre d’utilisateurs attendus** dans la baisse.</span><span class="sxs-lookup"><span data-stu-id="25e23-150">Select the **Number of expected users** from the drop-down.</span></span> <span data-ttu-id="25e23-151">Cette figure représente le nombre d’utilisateurs qui auront probablement besoin d’accéder au site.</span><span class="sxs-lookup"><span data-stu-id="25e23-151">This figure represents the number of users who will most likely need access to the site.</span></span> <span data-ttu-id="25e23-152">Le programme de lancement du portail détermine automatiquement le nombre idéal de vagues en fonction des utilisateurs attendus comme ceci :</span><span class="sxs-lookup"><span data-stu-id="25e23-152">The Portal launch scheduler will automatically determine the ideal number of waves depending on the expected users like this:</span></span>

   - <span data-ttu-id="25e23-153">Moins de 10 000 utilisateurs : deux vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-153">Less than 10k users: Two waves</span></span>
   - <span data-ttu-id="25e23-154">10 000 à 30 000 utilisateurs : trois vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-154">10k to 30k users: Three waves</span></span>
   - <span data-ttu-id="25e23-155">30 000 à 100 000 utilisateurs : cinq vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-155">30k+ to 100k users: Five waves</span></span>
   - <span data-ttu-id="25e23-156">Plus de 100 000 utilisateurs : cinq vagues et contactez microsoft via les étapes répertoriées dans la section Portail de lancement avec plus de 100 000 utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="25e23-156">More than 100k users: Five waves and contact your Microsoft via the steps listed in Launch portal with over 100k users section.</span></span>

5. <span data-ttu-id="25e23-157">Ensuite, déterminez le **type de redirection** nécessaire :</span><span class="sxs-lookup"><span data-stu-id="25e23-157">Then, determine the **Type of redirect** needed:</span></span>

   <span data-ttu-id="25e23-158">Option 1 : envoyer les utilisateurs vers une **page SharePoint existante (bidirectionnelle)** : utilisez cette option lors du lancement d’un nouveau portail SharePoint moderne pour remplacer un portail SharePoint existant.</span><span class="sxs-lookup"><span data-stu-id="25e23-158">**Option 1: Send users to an existing SharePoint page (bidirectional)** – Use this option when launching a new modern SharePoint portal to replace an existing SharePoint portal.</span></span> <span data-ttu-id="25e23-159">Les utilisateurs en vagues actives sont redirigés vers le nouveau site, qu’ils naviguent vers l’ancien ou le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="25e23-159">Users in active waves will be redirected to the new site regardless of whether they navigate to the old or new site.</span></span> <span data-ttu-id="25e23-160">Les utilisateurs d’une vague non lancée qui tentent d’accéder au nouveau site sont redirigés vers l’ancien site jusqu’à ce que leur vague soit lancée.</span><span class="sxs-lookup"><span data-stu-id="25e23-160">Users in a non-launched wave that try to access the new site will be redirected back to the old site until their wave is launched.</span></span>

   > [!NOTE]
   > <span data-ttu-id="25e23-161">Lorsque vous utilisez l’option bidirectionnelle, la personne qui planifiera le lancement doit également avoir des autorisations de propriétaire de site sur l’SharePoint portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-161">When using the bidirectional option, the person scheduling the launch must also have site owner permissions to the other SharePoint portal.</span></span>

   <span data-ttu-id="25e23-162">**Option 2 :** Envoyer les utilisateurs vers une page temporaire auto-genrée (redirection de page temporaire) : utilisez une redirection de page temporaire lorsqu’il n’existe aucun portail SharePoint existant.</span><span class="sxs-lookup"><span data-stu-id="25e23-162">**Option 2: Send users to an autogenerated temporary page (temporary page redirection)** – Use a temporary page redirection should be used when no existing SharePoint portal exists.</span></span> <span data-ttu-id="25e23-163">Les utilisateurs sont dirigés vers un nouveau portail SharePoint moderne et si un utilisateur est dans une vague qui n’a pas été lancée, il est redirigé vers une page temporaire.</span><span class="sxs-lookup"><span data-stu-id="25e23-163">Users are directed to a new modern SharePoint portal and if a user is in a wave that has not been launched, they will be redirected to a temporary page.</span></span>

   <span data-ttu-id="25e23-164">**Option 3 : Envoyer** des utilisateurs vers une page externe : fournissez une URL externe à une expérience de page d’accueil temporaire jusqu’à ce que la vague de l’utilisateur soit lancée.</span><span class="sxs-lookup"><span data-stu-id="25e23-164">**Option 3: Send users to an external page** – Provide an external URL to a temporary landing page experience until the user’s wave is launched.</span></span>

6. <span data-ttu-id="25e23-165">Décomposez votre audience en vagues.</span><span class="sxs-lookup"><span data-stu-id="25e23-165">Break up your audience into waves.</span></span> <span data-ttu-id="25e23-166">Ajoutez jusqu’à 20 groupes de sécurité par vague.</span><span class="sxs-lookup"><span data-stu-id="25e23-166">Add up to 20 security groups per wave.</span></span> <span data-ttu-id="25e23-167">Les détails des vagues peuvent être modifiés jusqu’au lancement de chaque vague.</span><span class="sxs-lookup"><span data-stu-id="25e23-167">Wave details can be edited up until the launch of each wave.</span></span> <span data-ttu-id="25e23-168">Chaque vague peut durer au moins un jour (24 heures) et au maximum sept jours.</span><span class="sxs-lookup"><span data-stu-id="25e23-168">Each wave can last at minimum one day (24 hours) and at most seven days.</span></span> <span data-ttu-id="25e23-169">Cela permet à SharePoint et à votre environnement technique d’insérabler et de s’adapter au grand volume d’utilisateurs du site.</span><span class="sxs-lookup"><span data-stu-id="25e23-169">This allows SharePoint and your technical environment an opportunity to acclimate and scale to the large volume of site users.</span></span> <span data-ttu-id="25e23-170">Lors de la planification d’un lancement via l’interface utilisateur, le fuseau horaire est basé sur les paramètres régionaux du site.</span><span class="sxs-lookup"><span data-stu-id="25e23-170">When scheduling a launch through the UI, the time zone is based on the site’s regional settings.</span></span>

   > [!NOTE]
   >
   > - <span data-ttu-id="25e23-171">Par défaut, le planning de lancement du portail est automatiquement de 2 vagues au minimum.</span><span class="sxs-lookup"><span data-stu-id="25e23-171">The Portal launch scheduler will automatically default to a minimum of 2 waves.</span></span> <span data-ttu-id="25e23-172">Toutefois, la version PowerShell de cet outil autorise la vague 1.</span><span class="sxs-lookup"><span data-stu-id="25e23-172">However, the PowerShell version of this tool will allow for 1 wave.</span></span>
   > - <span data-ttu-id="25e23-173">Microsoft 365 groupes ne sont pas pris en charge par cette version du programme de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-173">Microsoft 365 groups are not supported by this version of the Portal launch scheduler.</span></span>

7. <span data-ttu-id="25e23-174">Déterminez qui doit afficher le site immédiatement et entrez leurs informations dans le champ **Utilisateurs exemptés des vagues.**</span><span class="sxs-lookup"><span data-stu-id="25e23-174">Determine who needs to view the site right away and enter their information into the **Users exempt from waves** field.</span></span> <span data-ttu-id="25e23-175">Ces utilisateurs sont exclus des vagues et ne sont pas redirigés avant, pendant ou après le lancement.</span><span class="sxs-lookup"><span data-stu-id="25e23-175">These users are excluded from waves and will not be redirected before, during, or after the launch.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25e23-176">Jusqu’à 50 utilisateurs ou groupes de sécurité distincts peuvent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="25e23-176">Up to 50 distinct users or security groups max can be added.</span></span> <span data-ttu-id="25e23-177">Utilisez des groupes de sécurité lorsque vous avez besoin de plus de 50 personnes pour accéder au portail avant le lancement des vagues.</span><span class="sxs-lookup"><span data-stu-id="25e23-177">Use security groups when you need more than 50 individuals to get access to the portal before the waves start launching.</span></span>

8. <span data-ttu-id="25e23-178">Confirmez les détails du lancement du portail et sélectionnez **Planifier.**</span><span class="sxs-lookup"><span data-stu-id="25e23-178">Confirm portal launch details and select **Schedule**.</span></span> <span data-ttu-id="25e23-179">Une fois le lancement programmé, toutes les modifications apportées à la page d’accueil du portail SharePoint doivent recevoir un résultat de diagnostic sain avant que le lancement du portail reprenne.</span><span class="sxs-lookup"><span data-stu-id="25e23-179">Once the launch has been scheduled, any changes to the SharePoint portal home page will need to receive a healthy diagnostic result before the portal launch will resume.</span></span>

### <a name="launch-a-portal-with-over-100k-users"></a><span data-ttu-id="25e23-180">Lancer un portail avec plus de 100 000 utilisateurs</span><span class="sxs-lookup"><span data-stu-id="25e23-180">Launch a portal with over 100k users</span></span>

<span data-ttu-id="25e23-181">Si vous envisagez de lancer un portail avec plus de 100 000 utilisateurs, envoyez une demande de support en suivant les étapes répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="25e23-181">If you are planning to launch a portal with over 100,000 users, submit a support request following the steps listed below.</span></span> <span data-ttu-id="25e23-182">Veillez à inclure toutes les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="25e23-182">Make sure to include all the requested information.</span></span>

<span data-ttu-id="25e23-183">**Procédez comme suit :**</span><span class="sxs-lookup"><span data-stu-id="25e23-183">**Follow these steps:**</span></span>

1. <span data-ttu-id="25e23-184">Accédez à <https://admin.microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="25e23-184">Go to <https://admin.microsoft.com>.</span></span>
2. <span data-ttu-id="25e23-185">Vérifier que vous utilisez la nouvelle prévisualisation du Centre d’administration</span><span class="sxs-lookup"><span data-stu-id="25e23-185">Ensure you are using the new admin center preview</span></span>
3. <span data-ttu-id="25e23-186">Dans le volet de navigation de gauche, sélectionnez **Support,** puis **sélectionnez Nouvelle demande de service**</span><span class="sxs-lookup"><span data-stu-id="25e23-186">On the left navigational pane, select **Support**, and then select **New Service Request**</span></span>

   <span data-ttu-id="25e23-187">Cette opération active le volet **Besoin d'aide ?** sur le côté droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="25e23-187">This will activate the **Need Help?** pane on the right-hand side of your screen.</span></span>

4. <span data-ttu-id="25e23-188">Pour **décrire brièvement votre problème,** entrez « Lancer SharePoint portail avec 100 000 utilisateurs »</span><span class="sxs-lookup"><span data-stu-id="25e23-188">For **Briefly describe your issue**, enter "Launch SharePoint Portal with 100k users"</span></span></br>
5. <span data-ttu-id="25e23-189">Ensuite, sélectionnez **Contacter le support technique**</span><span class="sxs-lookup"><span data-stu-id="25e23-189">Then, select **Contact Support**</span></span>
6. <span data-ttu-id="25e23-190">Sous **Description,** entrez « Lancer SharePoint portail avec 100 000 utilisateurs »</span><span class="sxs-lookup"><span data-stu-id="25e23-190">Under **Description**, enter "Launch SharePoint Portal with 100k users"</span></span>
7. <span data-ttu-id="25e23-191">Remplissez les informations restantes, puis sélectionnez **Me contacter**</span><span class="sxs-lookup"><span data-stu-id="25e23-191">Fill out the remaining information, and then select **Contact me**</span></span>
8. <span data-ttu-id="25e23-192">Une fois le ticket créé, veillez à fournir à l’agent de support les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="25e23-192">After the ticket has been created, ensure you provide the support agent with the following information:</span></span>
   - <span data-ttu-id="25e23-193">URL du portail</span><span class="sxs-lookup"><span data-stu-id="25e23-193">Portal URL's</span></span>
   - <span data-ttu-id="25e23-194">Nombre d’utilisateurs attendus</span><span class="sxs-lookup"><span data-stu-id="25e23-194">Number of users expected</span></span>
   - <span data-ttu-id="25e23-195">Planification de lancement estimée</span><span class="sxs-lookup"><span data-stu-id="25e23-195">Estimated launch schedule</span></span>

## <a name="make-changes-to-a-scheduled-portal-launch"></a><span data-ttu-id="25e23-196">Apporter des modifications à un lancement de portail programmé</span><span class="sxs-lookup"><span data-stu-id="25e23-196">Make changes to a scheduled portal launch</span></span>

<span data-ttu-id="25e23-197">Les détails du lancement peuvent être modifiés pour chaque vague jusqu’à la date de lancement de la vague.</span><span class="sxs-lookup"><span data-stu-id="25e23-197">Launch details can be edited for each wave up until the date of the wave’s launch.</span></span>

1. <span data-ttu-id="25e23-198">Pour modifier les détails du lancement du portail, **accédez à Paramètres** puis sélectionnez **Planifier le lancement du site.**</span><span class="sxs-lookup"><span data-stu-id="25e23-198">To edit portal launch details, navigate to **Settings** and select **Schedule site launch**.</span></span>
2. <span data-ttu-id="25e23-199">Ensuite, sélectionnez **Modifier.**</span><span class="sxs-lookup"><span data-stu-id="25e23-199">Then, select **Edit**.</span></span>
3. <span data-ttu-id="25e23-200">Lorsque vous avez terminé d’effectuer vos modifications, sélectionnez **Mettre à jour.**</span><span class="sxs-lookup"><span data-stu-id="25e23-200">When you are finished making your edits, select **Update**.</span></span>

## <a name="delete-a-scheduled-portal-launch"></a><span data-ttu-id="25e23-201">Supprimer un lancement de portail programmé</span><span class="sxs-lookup"><span data-stu-id="25e23-201">Delete a scheduled portal launch</span></span>

<span data-ttu-id="25e23-202">Les lancements programmés à l’aide de l’outil de planification de lancement du portail peuvent être annulés ou supprimés à tout moment, même si certaines vagues ont déjà été lancées.</span><span class="sxs-lookup"><span data-stu-id="25e23-202">Launches scheduled using the Portal launch scheduler tool can be canceled, or deleted, at any time even if some waves have already been launched.</span></span>

1. <span data-ttu-id="25e23-203">Pour annuler le lancement de votre portail, accédez à **Paramètres** et **planifier le lancement du site.**</span><span class="sxs-lookup"><span data-stu-id="25e23-203">To cancel your portal’s launch, navigate to **Settings** and **Schedule site launch**.</span></span>

2. <span data-ttu-id="25e23-204">Ensuite, **sélectionnez Supprimer,** puis, lorsque vous voyez le message ci-dessous, **sélectionnez Supprimer** à nouveau.</span><span class="sxs-lookup"><span data-stu-id="25e23-204">Then, select **Delete** and then when you see the message below select **Delete** again.</span></span>

   ![Image de l’outil de planification de lancement du portail](../media/portal-launch-delete-2.png)

## <a name="use-the-powershell-portal-launch-scheduler"></a><span data-ttu-id="25e23-206">Utiliser le programme de lancement du portail PowerShell</span><span class="sxs-lookup"><span data-stu-id="25e23-206">Use the PowerShell Portal launch scheduler</span></span>

<span data-ttu-id="25e23-207">À l’origine, l’outil de planification de lancement du portail SharePoint était disponible uniquement via [SharePoint PowerShell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell) et continuera d’être pris en charge via PowerShell pour les clients qui préfèrent utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="25e23-207">The SharePoint Portal launch scheduler tool was originally only available via [SharePoint PowerShell](/powershell/sharepoint/sharepoint-online/introduction-sharepoint-online-management-shell) and will continue to be supported through PowerShell for customers who prefer this method.</span></span> <span data-ttu-id="25e23-208">Les mêmes remarques au début de cet article s’appliquent aux deux versions du programme de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-208">The same notes at the beginning of this article apply to both versions of the Portal launch scheduler.</span></span>

> [!NOTE]
> <span data-ttu-id="25e23-209">Vous avez besoin d’autorisations d’administrateur pour SharePoint PowerShell.</span><span class="sxs-lookup"><span data-stu-id="25e23-209">You need administrator permissions to use SharePoint PowerShell.</span></span>
> <span data-ttu-id="25e23-210">Les détails de lancement du portail pour les lancements créés dans PowerShell s’affichent et peuvent être gérés dans le nouvel outil de planification de lancement du portail dans SharePoint.</span><span class="sxs-lookup"><span data-stu-id="25e23-210">Portal launch details for launches created in PowerShell will appear and can be managed in the new Portal launch scheduler tool in SharePoint.</span></span>

### <a name="app-setup-and-connecting-to-sharepoint-online"></a><span data-ttu-id="25e23-211">Configuration de l’application et connexion à SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="25e23-211">App setup and connecting to SharePoint Online</span></span>

1. <span data-ttu-id="25e23-212">[Téléchargez la dernière version de SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span><span class="sxs-lookup"><span data-stu-id="25e23-212">[Download the latest SharePoint Online Management Shell](https://go.microsoft.com/fwlink/p/?LinkId=255251).</span></span>

    > [!NOTE]
    > <span data-ttu-id="25e23-p118">Si vous avez installé une version antérieure de SharePoint Online Management Shell, accédez à Ajouter ou supprimer des programmes et désinstaller « SharePoint Online Management Shell ».</span><span class="sxs-lookup"><span data-stu-id="25e23-p118">If you installed a previous version of the SharePoint Online Management Shell, go to Add or remove programs and uninstall "SharePoint Online Management Shell." </span></span><br><span data-ttu-id="25e23-214">Dans la page du Centre de téléchargement, sélectionnez votre langue, puis cliquez sur le bouton Télécharger.</span><span class="sxs-lookup"><span data-stu-id="25e23-214">On the Download Center page, select your language and then click the Download button.</span></span> <span data-ttu-id="25e23-215">Vous serez invité à choisir entre le téléchargement d’un fichier .msi x64 et x86.</span><span class="sxs-lookup"><span data-stu-id="25e23-215">You'll be asked to choose between downloading a x64 and x86 .msi file.</span></span> <span data-ttu-id="25e23-216">Téléchargez le fichier x64 si vous exécutez la version 64 bits de Windows ou le fichier x86 si vous exécutez la version 32 bits.</span><span class="sxs-lookup"><span data-stu-id="25e23-216">Download the x64 file if you're running the 64-bit version of Windows or the x86 file if you're running the 32-bit version.</span></span> <span data-ttu-id="25e23-217">En cas de doute, consultez [Quelle est la version du système d’exploitation Windows que j’utilise ?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span><span class="sxs-lookup"><span data-stu-id="25e23-217">If you don't know, see [Which version of Windows operating system am I running?](https://support.microsoft.com/help/13443/windows-which-operating-system).</span></span> <span data-ttu-id="25e23-218">Une fois le fichier téléchargé, exécutez-le, puis suivez les étapes de l'Assistant d'installation.</span><span class="sxs-lookup"><span data-stu-id="25e23-218">After the file downloads, run it and follow the steps in the Setup Wizard.</span></span>

2. <span data-ttu-id="25e23-219">Connectez-vous à SharePoint en tant qu’[administrateur général ou administrateur SharePoint](/sharepoint/sharepoint-admin-role) dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25e23-219">Connect to SharePoint as a [global admin or SharePoint admin](/sharepoint/sharepoint-admin-role) in Microsoft 365.</span></span> <span data-ttu-id="25e23-220">Pour savoir comment procéder, reportez-vous à l’article [Prise en main de SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span><span class="sxs-lookup"><span data-stu-id="25e23-220">To learn how, see [Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online).</span></span>

### <a name="view-any-existing-portal-launch-setups"></a><span data-ttu-id="25e23-221">Afficher les configurations de lancement de portail existantes</span><span class="sxs-lookup"><span data-stu-id="25e23-221">View any existing portal launch setups</span></span>

<span data-ttu-id="25e23-222">Pour voir s’il existe des configurations de lancement de portail :</span><span class="sxs-lookup"><span data-stu-id="25e23-222">To see if there are existing portal launch configurations:</span></span>

   ```PowerShell
   Get-SPOPortalLaunchWaves -LaunchSiteUrl <object> -DisplayFormat <object>
   ```

### <a name="schedule-a-portal-launch-on-the-site"></a><span data-ttu-id="25e23-223">Planifier un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="25e23-223">Schedule a portal launch on the site</span></span>

<span data-ttu-id="25e23-224">Le nombre de vagues requises dépend de la taille de lancement attendue.</span><span class="sxs-lookup"><span data-stu-id="25e23-224">The number of waves required depends on your expected launch size.</span></span>

- <span data-ttu-id="25e23-225">Moins de 10 000 utilisateurs : une vague</span><span class="sxs-lookup"><span data-stu-id="25e23-225">Less than 10k users: One wave</span></span>
- <span data-ttu-id="25e23-226">10 000 à 30 000 utilisateurs : trois vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-226">10k to 30k users: Three waves</span></span> 
- <span data-ttu-id="25e23-227">30 000 à 100 000 utilisateurs : cinq vagues</span><span class="sxs-lookup"><span data-stu-id="25e23-227">30k+ to 100k users: Five waves</span></span>
- <span data-ttu-id="25e23-228">Plus de 100 000 utilisateurs : cinq vagues et contactez votre équipe de compte Microsoft</span><span class="sxs-lookup"><span data-stu-id="25e23-228">More than 100k users: Five waves and contact your Microsoft account team</span></span>

#### <a name="steps-for-bidirectional-redirection"></a><span data-ttu-id="25e23-229">Étapes de redirection bidirectionnelle</span><span class="sxs-lookup"><span data-stu-id="25e23-229">Steps for bidirectional redirection</span></span>

<span data-ttu-id="25e23-230">La redirection bidirectionnelle implique le lancement d’un nouveau portail SharePoint Online pour remplacer un portail SharePoint classique ou moderne existant.</span><span class="sxs-lookup"><span data-stu-id="25e23-230">Bidirectional redirection involves launching a new modern SharePoint Online portal to replace an existing SharePoint classic or modern portal.</span></span> <span data-ttu-id="25e23-231">Les utilisateurs en vagues actives sont redirigés vers le nouveau site, qu’ils naviguent vers l’ancien ou le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="25e23-231">Users in active waves will be redirected to the new site regardless of whether they navigate to the old or new site.</span></span> <span data-ttu-id="25e23-232">Les utilisateurs d’une vague non lancée qui tentent d’accéder au nouveau site sont redirigés vers l’ancien site jusqu’à ce que leur vague soit lancée.</span><span class="sxs-lookup"><span data-stu-id="25e23-232">Users in a non-launched wave that try to access the new site will be redirected back to the old site until their wave is launched.</span></span>

<span data-ttu-id="25e23-233">La redirection est uniquement prise en charge entre la page d’accueil par défaut sur l’ancien site et la page d’accueil par défaut sur le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="25e23-233">We only support redirection between the default home page on the old site and the default home page on the new site.</span></span> <span data-ttu-id="25e23-234">Si vous avez des administrateurs ou des propriétaires qui ont besoin d’accéder aux anciens et nouveaux sites sans être redirigés, assurez-vous qu’ils sont répertoriés à l’aide du `WaveOverrideUsers` paramètre.</span><span class="sxs-lookup"><span data-stu-id="25e23-234">Should you have administrators or owners that need access to the old and new sites without being redirected, ensure they are listed using the `WaveOverrideUsers` parameter.</span></span>

<span data-ttu-id="25e23-235">Pour migrer les utilisateurs d’un site SharePoint existant vers un nouveau site SharePoint de manière par étape :</span><span class="sxs-lookup"><span data-stu-id="25e23-235">To migrate users from an existing SharePoint site to a new SharePoint site in a staged manner:</span></span>

1. <span data-ttu-id="25e23-236">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-236">Run the following command to designate portal launch waves.</span></span>

   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType Bidirectional -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
   ```

   <span data-ttu-id="25e23-237">Exemple :</span><span class="sxs-lookup"><span data-stu-id="25e23-237">Example:</span></span>

   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType Bidirectional -RedirectUrl "https://contoso.sharepoint.com/teams/oldsite" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
   [{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
   {Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"},
   {Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="25e23-238">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="25e23-238">Complete validation.</span></span> <span data-ttu-id="25e23-239">La redirection peut prendre entre 5 et 10 minutes pour terminer sa configuration dans le service.</span><span class="sxs-lookup"><span data-stu-id="25e23-239">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span>

#### <a name="steps-for-redirection-to-temporary-page"></a><span data-ttu-id="25e23-240">Étapes de redirection vers une page temporaire</span><span class="sxs-lookup"><span data-stu-id="25e23-240">Steps for redirection to temporary page</span></span>

<span data-ttu-id="25e23-241">La redirection de page temporaire doit être utilisée lorsqu’il n’existe SharePoint portail existant.</span><span class="sxs-lookup"><span data-stu-id="25e23-241">Temporary page redirection should be used when no existing SharePoint portal exists.</span></span> <span data-ttu-id="25e23-242">Les utilisateurs sont dirigés vers un nouveau portail SharePoint Online moderne de manière par étape.</span><span class="sxs-lookup"><span data-stu-id="25e23-242">Users are directed to a new modern SharePoint Online portal in a staged manner.</span></span> <span data-ttu-id="25e23-243">Si un utilisateur est dans une vague qui n’a pas été lancée, il est redirigé vers une page temporaire (toute URL).</span><span class="sxs-lookup"><span data-stu-id="25e23-243">If a user is in a wave that has not been launched, they will be redirected to a temporary page (any URL).</span></span>

1. <span data-ttu-id="25e23-244">Exécutez la commande suivante pour désigner les vagues de lancement du portail.</span><span class="sxs-lookup"><span data-stu-id="25e23-244">Run the following command to designate portal launch waves.</span></span>

   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl <object> -RedirectionType ToTemporaryPage -RedirectUrl <string> -ExpectedNumberOfUsers <object> -WaveOverrideUsers <object> -Waves <object>
   ```

   <span data-ttu-id="25e23-245">Exemple :</span><span class="sxs-lookup"><span data-stu-id="25e23-245">Example:</span></span>

   ```PowerShell
   New-SPOPortalLaunchWaves -LaunchSiteUrl "https://contoso.sharepoint.com/teams/newsite" -RedirectionType ToTemporaryPage -RedirectUrl "https://portal.contoso.com/UnderConstruction.aspx" -ExpectedNumberOfUsers 10kTo30kUsers -WaveOverrideUsers "admin@contoso.com" -Waves ' 
   [{Name:"Wave 1", Groups:["Viewers 1"], LaunchDateUtc:"2020/10/14"}, 
   {Name:"Wave 2", Groups:["Viewers 2"], LaunchDateUtc:"2020/10/15"},
   {Name:"Wave 3", Groups:["Viewers 3"], LaunchDateUtc:"2020/10/16"}]'
   ```

2. <span data-ttu-id="25e23-246">Validation complète.</span><span class="sxs-lookup"><span data-stu-id="25e23-246">Complete validation.</span></span> <span data-ttu-id="25e23-247">La redirection peut prendre entre 5 et 10 minutes pour terminer sa configuration dans le service.</span><span class="sxs-lookup"><span data-stu-id="25e23-247">It can take 5-10 minutes for the redirection to complete its configuration across the service.</span></span>

### <a name="pause-or-restart-a-portal-launch-on-the-site"></a><span data-ttu-id="25e23-248">Suspendre ou redémarrer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="25e23-248">Pause or restart a portal launch on the site</span></span>

1. <span data-ttu-id="25e23-249">Pour interrompre un lancement du portail en cours et empêcher temporairement les progressions de vague à venir, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="25e23-249">To pause a portal launch in progress and temporarily prevent upcoming wave progressions from occurring, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Pause - LaunchSiteUrl <object>
   ```

2. <span data-ttu-id="25e23-250">Vérifier que tous les utilisateurs sont redirigés vers l’ancien site.</span><span class="sxs-lookup"><span data-stu-id="25e23-250">Validate that all users are redirected to the old site.</span></span>

3. <span data-ttu-id="25e23-251">Pour redémarrer un lancement du portail qui a été suspendu, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="25e23-251">To restart a portal launch that's been paused, run the following command:</span></span>

   ```PowerShell
   Set-SPOPortalLaunchWaves -Status Restart - LaunchSiteUrl <object>
   ```

4. <span data-ttu-id="25e23-252">Vérifier que la redirection est maintenant restaurée.</span><span class="sxs-lookup"><span data-stu-id="25e23-252">Validate that the redirection is now restored.</span></span>

### <a name="delete-a-portal-launch-on-the-site"></a><span data-ttu-id="25e23-253">Supprimer un lancement de portail sur le site</span><span class="sxs-lookup"><span data-stu-id="25e23-253">Delete a portal launch on the site</span></span>

1. <span data-ttu-id="25e23-254">Exécutez la commande suivante pour supprimer un lancement de portail prévu ou en cours pour un site.</span><span class="sxs-lookup"><span data-stu-id="25e23-254">Run the following command to delete a portal launch scheduled or in progress for a site.</span></span>

   ```PowerShell
   Remove-SPOPortalLaunchWaves -LaunchSiteUrl <object>
   ```

2. <span data-ttu-id="25e23-255">Vérifier qu’aucune redirection ne se produit pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="25e23-255">Validate that no redirection happens for all users.</span></span>

## <a name="learn-more"></a><span data-ttu-id="25e23-256">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="25e23-256">Learn more</span></span>

[<span data-ttu-id="25e23-257">Planification de votre plan de déploiement de lancement de portail dans SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="25e23-257">Planning your portal launch roll-out plan in SharePoint Online</span></span>](./planportallaunchroll-out.md)

[<span data-ttu-id="25e23-258">Planifier votre site de communication</span><span class="sxs-lookup"><span data-stu-id="25e23-258">Plan your communication site</span></span>](https://support.microsoft.com/office/plan-your-sharepoint-communication-site-35d9adfe-d5cc-462f-a63a-bae7f2529182)
