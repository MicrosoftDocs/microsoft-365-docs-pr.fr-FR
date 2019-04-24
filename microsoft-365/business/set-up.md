---
title: Installer Microsoft 365 Entreprise à l'aide de l'Assistant Installation
ms.author: sirkkuw
author: Sirkkuw
manager: scotv
ms.audience: Admin
ms.topic: article
f1_keywords:
- O365E_M365SetupBanner
- BCS365_M365SetupBanner
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Adm_O365
- M365-subscription-management
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez comment configurer Microsoft 365 entreprise en suivant quatre étapes.
ms.openlocfilehash: a1c8a41c3e291983276280a063248bdd10a7f85a
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283896"
---
# <a name="set-up-microsoft-365-business-by-using-the-setup-wizard"></a><span data-ttu-id="cc6e3-103">Installer Microsoft 365 Entreprise à l'aide de l'Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="cc6e3-103">Set up Microsoft 365 Business by using the setup wizard</span></span>

<span data-ttu-id="cc6e3-104">Suivez les étapes décrites ci-dessous 1-4.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-104">Complete steps 1-4 below.</span></span>
  
### <a name="set-up-microsoft-365-business"></a><span data-ttu-id="cc6e3-105">Configurer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cc6e3-105">Set up Microsoft 365 Business</span></span>

<span data-ttu-id="cc6e3-106">Regardez une vidéo sur la configuration de Microsoft 365 entreprise lorsque vous n'avez pas d'Active Directory local:</span><span class="sxs-lookup"><span data-stu-id="cc6e3-106">Watch a video on how to set up Microsoft 365 Business when you don't have an on-premises Active Directory:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/0705c337-f3e8-4d28-bb6c-530cd28e99f2?autoplay=false]
  
<span data-ttu-id="cc6e3-107">Les étapes de configuration incluent des informations pour les configurations qui incluent Active Directory local.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-107">The set-up steps include information for setups that include local Active Directory.</span></span> <span data-ttu-id="cc6e3-108">Si vous souhaitez continuer à accéder aux appareils joints à un domaine, lisez les articles suivants pour obtenir deux méthodes différentes d'activation de ce dernier, puis effectuez les étapes suivantes avant d'exécuter l'Assistant Installation:</span><span class="sxs-lookup"><span data-stu-id="cc6e3-108">If you want to continue to access domain-joined devices, read the following articles for two different way of enabling that, and complete the steps before you run the Setup wizard:</span></span>
  
- [<span data-ttu-id="cc6e3-109">Activer la gestion des appareils Windows 10 associés à un domaine par Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cc6e3-109">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business</span></span>](manage-windows-devices.md)
    
    <span data-ttu-id="cc6e3-110">-Il s'agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-110">-This is the recommended way.</span></span>
    
- [<span data-ttu-id="cc6e3-111">Accéder aux ressources locales à partir d'un appareil joint à Azure AD dans Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="cc6e3-111">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business</span></span>](access-resources.md)
    
### <a name="step-1-personalize-sign-in"></a><span data-ttu-id="cc6e3-112">Étape 1: personnalisation de la connexion</span><span class="sxs-lookup"><span data-stu-id="cc6e3-112">Step 1: Personalize sign-in</span></span>

1. <span data-ttu-id="cc6e3-p102">Connectez-vous à [Microsoft 365 Business](https://portal.microsoft.com) avec vos informations d'identification d'administrateur général. Sélectionnez la vignette **Administrateur** pour accéder au Centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-p102">Sign in to [Microsoft 365 Business](https://portal.microsoft.com) by using your global admin credentials. Choose the **Admin** tile to go to the admin center.</span></span> 
    
2. <span data-ttu-id="cc6e3-115">Sélectionnez **Commencer la configuration** (selon votre situation, il est possible que ce soit **Poursuivre la configuration** qui soit affiché) dans le Centre d'administration pour démarrer l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-115">Choose **Start setup** (depending on your state you may see **Continue setup** instead) in the admin center to start the wizard.</span></span> 
    
3. <span data-ttu-id="cc6e3-116">Entrez le nom de domaine que vous voulez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-116">Enter the domain name you want to use (like contoso.com).</span></span>
    
    <span data-ttu-id="cc6e3-117">Entrez votre domaine même si vous l'avez déjà confirmé, par exemple lors de l'utilisation d'Azure AD Connect.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-117">Go ahead and enter your domain even if you have verified it while using Azure AD Connect, for example.</span></span> <span data-ttu-id="cc6e3-118">Les deux étapes suivantes ne s'appliquent pas si vous avez utilisé Azure AD Connect pour vérifier votre domaine.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-118">The following two steps do not apply to you if you used Azure AD Connect to verify your domain.</span></span>
    
4. <span data-ttu-id="cc6e3-119">Suivez les étapes de l'Assistant pour [créer des enregistrements DNS auprès d'un fournisseur d'hébergement DNS pour Office 365](https://support.office.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) qui vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-119">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://support.office.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) that verifies you own the domain.</span></span> 
    
    <span data-ttu-id="cc6e3-120">Vous pouvez voir un exemple de vidéo de [vidéo: Setup Office 365 dans le nouveau centre d'administration](https://support.office.com/article/a8c2002a-34bc-4ab3-93d8-9b5156c48bf8).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-120">You can view an example video of [Video: Setup Office 365 in the new Admin Center](https://support.office.com/article/a8c2002a-34bc-4ab3-93d8-9b5156c48bf8).</span></span> <span data-ttu-id="cc6e3-121">Veuillez noter que cette vidéo n'inclut pas les étapes de protection des données de Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-121">Note that this video does not include the data protection steps of Microsoft 365 Business.</span></span>
    
    ![Screenshot of the Business Cloud Suite setup wizard.](media/3c4fd40c-2de1-4a87-8ee0-78d3928c7bb7.png)
  
### <a name="step-2-add-users-and-assign-licenses"></a><span data-ttu-id="cc6e3-123">Étape 2: ajouter des utilisateurs et attribuer des licences</span><span class="sxs-lookup"><span data-stu-id="cc6e3-123">Step 2: Add users and assign licenses</span></span>

1. <span data-ttu-id="cc6e3-124">Vous pouvez ajouter des utilisateurs à ce stade ou [ajouter des utilisateurs plus tard](add-users-m365b.md) dans le centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-124">You can add users here, or you can [add users later](add-users-m365b.md) in the admin center.</span></span> 
    
    <span data-ttu-id="cc6e3-125">Une licence Microsoft 365 Entreprise est automatiquement attribuée aux utilisateurs que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-125">Any users you add get automatically assigned a Microsoft 365 Business license.</span></span>
    
2. <span data-ttu-id="cc6e3-p105">Si votre abonnement Microsoft 365 Entreprise est associé à des utilisateurs existants (par exemple, si vous utilisiez Azure AD Connect), vous avez la possibilité de leur attribuer des licences à ce stade. Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-p105">If your Microsoft 365 Business subscription has existing users (for example, if you used Azure AD Connect) , you will get an option to assign licenses to them now. Go ahead and add licenses to them as well.</span></span>
    
3. <span data-ttu-id="cc6e3-p106">Vous avez également la possibilité de partager des informations d'identification avec les nouveaux utilisateurs que vous ajoutez. Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-p106">You will also get an option to share credentials with the new users you added. You can choose to print them out, email them, or download them.</span></span>
    
4. <span data-ttu-id="cc6e3-130">Ignorez la migration des messages e-mail et sélectionnez **Suivant** dans la page **Migrer les messages e-mail**.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-130">Skip migrating email messages and choose **Next** on **Migrate email messages** page.</span></span> 
    
    <span data-ttu-id="cc6e3-131">Si vous effectuez une migration à partir d'un autre fournisseur de courrier et que vous souhaitez copier vos données ultérieurement, vous pouvez migrer le [courrier électronique et les contacts vers Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-131">If you are moving from another email provider and want to copy your data later, you can [Migrate email and contacts to Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span></span>
    
    ![Screenshot of two new users added in the setup wizard](media/8f729967-5c65-4ceb-b737-18119db40564.png)
  
### <a name="step-3-connect-your-domain"></a><span data-ttu-id="cc6e3-133">Étape 3: Connectez votre domaine</span><span class="sxs-lookup"><span data-stu-id="cc6e3-133">Step 3: Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="cc6e3-134">Si vous avez choisi d'utiliser le domaine. onmicrosoft ou Azure AD Connect, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-134">If you chose to use the .onmicrosoft domain, or used Azure AD Connect, you will not see this step.</span></span> 
  
<span data-ttu-id="cc6e3-135">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-135">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="cc6e3-136">L'Assistant Configuration détecte généralement votre bureau d'enregistrement et vous fournit un lien vers des instructions détaillées vous permettant de mettre à jour vos enregistrements NS sur le site web du bureau d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-136">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website.</span></span> <span data-ttu-id="cc6e3-137">Si ce n'est pas le cas, [Modifiez les serveurs de noms pour configurer Office 365 avec n'importe quel](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2)Bureau d'enregistrement de domaine.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-137">If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span>
    
2. <span data-ttu-id="cc6e3-138">La messagerie électronique et d'autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-138">Email and other services will be set up for you</span></span>
    
### <a name="step-4-manage-devices-and-work-files"></a><span data-ttu-id="cc6e3-139">Étape 4: gérer les appareils et les fichiers de travail</span><span class="sxs-lookup"><span data-stu-id="cc6e3-139">Step 4: Manage devices and work files</span></span>

1. <span data-ttu-id="cc6e3-140">Dans la page **Protéger les fichiers professionnels sur vos appareils mobiles**, définissez les paramètres **Protéger les fichiers professionnels en cas de perte ou de vol des appareils** et **Gérer la manière dont les utilisateurs accèdent aux fichiers Office sur les appareils mobiles** sur **Activé**.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-140">On the **Protect work files on your mobile devices** page set both **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** settings to **On**.</span></span> <span data-ttu-id="cc6e3-141">Vous pouvez également accéder à chaque sous-paramètre en cliquant sur les chevrons en regard de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-141">You can also access each sub-setting by clicking the chevrons next to each setting.</span></span>
  
  <span data-ttu-id="cc6e3-142">Tous les fichiers de travail de vos utilisateurs sous licence sont maintenant protégés sur les appareils iOS et Android, dès qu'ils installent les [applications Office](set-up-mobile-devices.md) (et s'authentifient avec leurs informations d'identification Microsoft 365 entreprise).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-142">All of your licensed users' work files are now protected on iOS and Android devices, as soon as they [install Office apps](set-up-mobile-devices.md) (and authenticate with their Microsoft 365 Business credentials).</span></span> 
  
  ![Screenshot of protect work files on your mobile devices page](media/3139a9aa-6228-4e74-8166-c6a886d7319f.PNG)
  
2. <span data-ttu-id="cc6e3-144">Sur la page **définir la configuration des appareils Windows 10** , définissez le paramètre sécurisEr les **appareils Windows 10** sur **activé**.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-144">On the **Set Windows 10 device configuration** page, set **Secure Windows 10 Devices** setting to **On**.</span></span>
  
   <span data-ttu-id="cc6e3-145">Vous pouvez également accéder à chaque sous-paramètre en cliquant sur le chevron en regard de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-145">You can also access each sub-setting by clicking the chevron next to it.</span></span>
  
3. <span data-ttu-id="cc6e3-146">Définissez le paramètre **Installer Office sur les appareils Windows 10** sur **Oui** si tous vos utilisateurs ont des ordinateurs Windows 10 et aucune installation Office existante ou des installations Office « Démarrer en un clic ».</span><span class="sxs-lookup"><span data-stu-id="cc6e3-146">Set the **Install Office on Windows 10 Devices** setting to **Yes** if all of your users have Windows 10 computers, and either no existing Office installs, or click-to-run Office installs.</span></span> <span data-ttu-id="cc6e3-147">Si ce n'est pas le cas, définissez cette option sur **Non**.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-147">If this is not the case, set this option to **No**.</span></span> <span data-ttu-id="cc6e3-148">Vous pouvez [automatiquement installer Office](auto-install-or-uninstall-office.md) plus tard à partir du centre d'administration, une fois que vous aurez préparé les ordinateurs des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-148">You can [automatically install Office](auto-install-or-uninstall-office.md) later from the admin center after you have prepared the user computers.</span></span> <span data-ttu-id="cc6e3-149">Pour obtenir des instructions, consultez la rubrique [Prepare for Office client installation](prepare-for-office-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-149">For instructions, see [prepare for Office client installation](prepare-for-office-client-deployment.md).</span></span>
  
    <span data-ttu-id="cc6e3-150">Les fichiers de travail des utilisateurs sous licence sur les appareils Windows 10 seront projetés dès qu'ils rejoignent [leur appareil Windows 10](set-up-windows-devices.md) à un domaine Microsoft 365 Business Azure ad ou [installer Windows 10 sur un nouvel ordinateur](https://support.office.com/article/c654bd23-d256-4ac7-8fba-0c993bf5a771.aspx) tout en rejoignant simultanément Microsoft 365 Domaine Business Azure AD.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-150">The licensed users' work files on Windows 10 devices will be projected as soon as they [join their Windows 10 device](set-up-windows-devices.md) to a Microsoft 365 Business Azure AD domain or [install Windows 10 on a new computer](https://support.office.com/article/c654bd23-d256-4ac7-8fba-0c993bf5a771.aspx) while simultaneously joining the Microsoft 365 Business Azure AD domain.</span></span> 
  
4. <span data-ttu-id="cc6e3-151">Cliquez sur **Suivant** pour terminer la configuration.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-151">Click **Next** and you are done with setup.</span></span> 
  
    <span data-ttu-id="cc6e3-152">Merci de nous faire part de vos commentaires à cette étape pour nous aider à améliorer l'expérience.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-152">Please leave us feedback at this step to help us improve the experience.</span></span>
  
    ![Screenshot of Prepare Windows 10 devices page](media/bff701c1-48a3-44f4-aa95-9d959d57c85b.PNG)
  
## <a name="additional-security-settings"></a><span data-ttu-id="cc6e3-154">Paramètres de sécurité supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cc6e3-154">Additional security settings</span></span>

<span data-ttu-id="cc6e3-155">Outre le paramètre de sécurité et de conformité dans l'Assistant Installation, vous pouvez également configurer les paramètres supplémentaires suivants:</span><span class="sxs-lookup"><span data-stu-id="cc6e3-155">In addition to the security and compliance setting in the setup wizard, you can also set up the following additional settings:</span></span>
  
- <span data-ttu-id="cc6e3-156">ConFigurez la protection contre les pièces jointes potentiellement dangereuses.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-156">Set up protection against unsafe attachments.</span></span> <span data-ttu-id="cc6e3-157">**Protection avancée contre les menaces** (ATP) identifie le contenu malveillant, puis bloque la remise de pièces jointes potentiellement dangereuses, ce qui vous permet de vous protéger contre les schémas de hameçonnage et les infections par ransomware.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-157">**Advanced Threat Protection** (ATP) identifies malicious content and then blocks delivery of unsafe attachments, helping protect you against phishing schemes and ransomware infections.</span></span> <span data-ttu-id="cc6e3-158">Pour activer la protection des pièces jointes, consultez la rubrique [set up Office 365 ATP Safe Attachments Policies](https://support.office.com/article/078eb946-819a-4e13-8673-fe0c0ad3a775#setpolicy).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-158">To activate attachment protection, see [Set up Office 365 ATP Safe Attachments policies](https://support.office.com/article/078eb946-819a-4e13-8673-fe0c0ad3a775#setpolicy).</span></span>
    
- <span data-ttu-id="cc6e3-159">Protégez votre environnement lorsque les utilisateurs cliquent sur des liens malveillants.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-159">Protect your environment when users click malicious links.</span></span> <span data-ttu-id="cc6e3-160">La fonctionnalité ATP examine les liens dans les courriers électroniques lorsqu'un utilisateur clique dessus.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-160">ATP examines links in email at the time a user clicks them.</span></span> <span data-ttu-id="cc6e3-161">Si un lien n'est pas sécurisé, l'utilisateur est averti de ne pas visiter le site ou d'être informé que le site a été bloqué.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-161">If a link is unsafe, the user is warned not to visit the site or informed that the site has been blocked.</span></span> <span data-ttu-id="cc6e3-162">Cela permet de vous protéger contre les schémas de phishing.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-162">This helps protect against phishing schemes.</span></span> <span data-ttu-id="cc6e3-163">[Configurez les stratégies de liens approuvés office 365 ATP](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#reveddefaultscc) ou configurez [les stratégies de liens fiables Office 365 ATP](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#addemailpolscc).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-163">[Set up Office 365 ATP Safe Links policies](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#reveddefaultscc) or [Set up Office 365 ATP Safe Links policies](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#addemailpolscc).</span></span>
    
- <span data-ttu-id="cc6e3-164">Vous pouvez conserver tout le contenu des boîtes aux lettres, y compris les éléments supprimés, en mettant la boîte aux lettres entière d'un utilisateur en **conservation pour litige**.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-164">You can preserve all mailbox content including deleted items by putting a user's entire mailbox on **litigation hold**.</span></span> <span data-ttu-id="cc6e3-165">Pour obtenir des instructions, voir</span><span class="sxs-lookup"><span data-stu-id="cc6e3-165">For instructions, see</span></span> 
- <span data-ttu-id="cc6e3-166">ConFigurez la rétention du [courrier électronique avec archivAge Exchange Online](security-features.md#set-up-email-retention-with-exchange-online-archiving).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-166">[Set up email retention with Exchange Online Archiving](security-features.md#set-up-email-retention-with-exchange-online-archiving).</span></span>
    
- <span data-ttu-id="cc6e3-167">ConFigurez des **stratégies**de rétention personnalisées, par exemple, pour les conserver pendant une période de temps spécifique ou supprimer définitivement le contenu à la fin de la période de rétention.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-167">Set up customized **retention policies**, for example, to preserve for a specific amount of time or delete content permanently at the end of the retention period.</span></span> <span data-ttu-id="cc6e3-168">Vous pouvez activer des stratégies de rétention personnalisées dans le centre de sécurité et de conformité, accédez à rétention de **gouvernance** \> \*\*\*\* des données, puis suivez les étapes de l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-168">You can enable customized retention policies in the Securities and compliance center, go to **Data governance** \> **Retention**, and then follow the steps in the wizard.</span></span> <span data-ttu-id="cc6e3-169">Pour en savoir plus, consultez la rubrique [vue d'ensemble des stratégies de](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423)rétention.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-169">To learn more, see [Overview of retention policies](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="cc6e3-170">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="cc6e3-170">Next steps</span></span>

<span data-ttu-id="cc6e3-171">Pour les utilisateurs qui disposent d'une licence, l'étape suivante consiste à configurer des appareils.</span><span class="sxs-lookup"><span data-stu-id="cc6e3-171">For the users that have their licenses, the next step is to set up devices.</span></span><br/> <span data-ttu-id="cc6e3-172">Pour plus d'informations, voir [Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business](set-up-windows-devices.md) et [Configurer des appareils mobiles pour les utilisateurs de Microsoft 365 Business](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-172">See [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md) and [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md).</span></span> <br/><span data-ttu-id="cc6e3-173">Pour obtenir des liens vers des rubriques relatives à la définition de stratégies de protection des applications et des appareils, et à la suppression de données sur les appareils des utilisateurs, consultez l'article [Gérer Microsoft 365 Business](manage.md).</span><span class="sxs-lookup"><span data-stu-id="cc6e3-173">See [Manage Microsoft 365 Business](manage.md) for links to topics on how to set device and app protection polices, and how to remove data from user devices.</span></span> 
  


