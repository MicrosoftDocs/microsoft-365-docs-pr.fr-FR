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
ms.collection: Adm_O365
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
search.appverid:
- BCS160
- MET150
ms.assetid: 6e7a2dfd-8ec4-4eb7-8390-3ee103e5fece
description: Découvrez comment configurer Microsoft 365 Business en quatre étapes.
ms.openlocfilehash: f57239b884bd2e186c0bc01973130a10fa4cfe84
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866845"
---
# <a name="set-up-microsoft-365-business-by-using-the-setup-wizard"></a><span data-ttu-id="a25f8-103">Installer Microsoft 365 Entreprise à l'aide de l'Assistant Installation</span><span class="sxs-lookup"><span data-stu-id="a25f8-103">Set up Microsoft 365 Business by using the setup wizard</span></span>

<span data-ttu-id="a25f8-104">Effectuez les étapes 1 à 4 ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a25f8-104">Complete steps 1-4 below.</span></span>
  
### <a name="set-up-microsoft-365-business"></a><span data-ttu-id="a25f8-105">Configurer Microsoft 365 Business</span><span class="sxs-lookup"><span data-stu-id="a25f8-105">Set up Microsoft 365 Business</span></span>

<span data-ttu-id="a25f8-106">Regardez une vidéo sur la façon de configurer Microsoft 365 Business lorsque vous n’avez pas Active Directory local :</span><span class="sxs-lookup"><span data-stu-id="a25f8-106">Watch a video on how to set up Microsoft 365 Business when you don't have an on-premises Active Directory:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/0705c337-f3e8-4d28-bb6c-530cd28e99f2?autoplay=false]
  
<span data-ttu-id="a25f8-p101">Les étapes de configuration contiennent des informations pour les installations comprenant Active Directory local. Si vous souhaitez continuer à accéder à des périphériques à un domaine, lisez les articles suivants pour deux différemment de l’activation qui et effectuer les étapes avant d’exécuter l’Assistant installation :</span><span class="sxs-lookup"><span data-stu-id="a25f8-p101">The set-up steps include information for setups that include local Active Directory. If you want to continue to access domain-joined devices, read the following articles for two different way of enabling that, and complete the steps before you run the Setup wizard:</span></span>
  
- [<span data-ttu-id="a25f8-109">Permettre à un domaine aux périphériques Windows 10 devant être gérés par Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="a25f8-109">Enable domain-joined Windows 10 devices to be managed by Microsoft 365 Business</span></span>](manage-windows-devices.md)
    
    <span data-ttu-id="a25f8-110">-Il s’agit de la méthode recommandée.</span><span class="sxs-lookup"><span data-stu-id="a25f8-110">-This is the recommended way.</span></span>
    
- [<span data-ttu-id="a25f8-111">Accès aux ressources à partir d’un périphérique joint à AD Azure dans Microsoft 365 Business sur site</span><span class="sxs-lookup"><span data-stu-id="a25f8-111">Access on-premises resources from an Azure AD-joined device in Microsoft 365 Business</span></span>](access-resources.md)
    
### <a name="step-1-personalize-sign-in"></a><span data-ttu-id="a25f8-112">Étape 1 : Personnaliser connexion</span><span class="sxs-lookup"><span data-stu-id="a25f8-112">Step 1: Personalize sign-in</span></span>

1. <span data-ttu-id="a25f8-p102">Connectez-vous à [Microsoft 365 Business](https://portal.microsoft.com) avec vos informations d'identification d'administrateur général. Sélectionnez la vignette **Administrateur** pour accéder au Centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p102">Sign in to [Microsoft 365 Business](https://portal.microsoft.com) by using your global admin credentials. Choose the **Admin** tile to go to the admin center.</span></span> 
    
2. <span data-ttu-id="a25f8-115">Sélectionnez **Commencer la configuration** (selon votre situation, il est possible que ce soit **Poursuivre la configuration** qui soit affiché) dans le Centre d'administration pour démarrer l'Assistant.</span><span class="sxs-lookup"><span data-stu-id="a25f8-115">Choose **Start setup** (depending on your state you may see **Continue setup** instead) in the admin center to start the wizard.</span></span> 
    
3. <span data-ttu-id="a25f8-116">Entrez le nom de domaine que vous voulez utiliser (par exemple, contoso.com).</span><span class="sxs-lookup"><span data-stu-id="a25f8-116">Enter the domain name you want to use (like contoso.com).</span></span>
    
    <span data-ttu-id="a25f8-p103">Continuez et entrez votre domaine, même si vous l’avez vérifié à l’aide d’Azure AD Connect, par exemple. Les deux étapes suivantes ne s’appliquent pas à vous si vous avez utilisé Azure AD se connecter pour vérifier votre domaine.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p103">Go ahead and enter your domain even if you have verified it while using Azure AD Connect, for example. The following two steps do not apply to you if you used Azure AD Connect to verify your domain.</span></span>
    
4. <span data-ttu-id="a25f8-119">Suivez les étapes de l’Assistant pour [créer des enregistrements DNS à n’importe quel fournisseur d’hébergement DNS pour Office 365](https://support.office.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) vérifie que vous êtes propriétaire du domaine.</span><span class="sxs-lookup"><span data-stu-id="a25f8-119">Follow the steps in the wizard to [Create DNS records at any DNS hosting provider for Office 365](https://support.office.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166) that verifies you own the domain.</span></span> 
    
    <span data-ttu-id="a25f8-p104">Vous pouvez afficher une vidéo de l’exemple de [vidéo : le programme d’installation Office 365 dans le nouveau centre d’administration](https://support.office.com/article/a8c2002a-34bc-4ab3-93d8-9b5156c48bf8). Notez que cette vidéo n’inclut pas les étapes de protection de données de Microsoft 365 Business.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p104">You can view an example video of [Video: Setup Office 365 in the new Admin Center](https://support.office.com/article/a8c2002a-34bc-4ab3-93d8-9b5156c48bf8). Note that this video does not include the data protection steps of Microsoft 365 Business.</span></span>
    
    ![Screenshot of the Business Cloud Suite setup wizard.](media/3c4fd40c-2de1-4a87-8ee0-78d3928c7bb7.png)
  
### <a name="step-2-add-users-and-assign-licenses"></a><span data-ttu-id="a25f8-123">Étape 2 : Ajouter des utilisateurs et attribution de licences</span><span class="sxs-lookup"><span data-stu-id="a25f8-123">Step 2: Add users and assign licenses</span></span>

1. <span data-ttu-id="a25f8-124">Vous pouvez ajouter des utilisateurs à ce stade ou [ajouter des utilisateurs plus tard](add-users-m365b.md) dans le centre d'administration.</span><span class="sxs-lookup"><span data-stu-id="a25f8-124">You can add users here, or you can [add users later](add-users-m365b.md) in the admin center.</span></span> 
    
    <span data-ttu-id="a25f8-125">Une licence Microsoft 365 Entreprise est automatiquement attribuée aux utilisateurs que vous ajoutez.</span><span class="sxs-lookup"><span data-stu-id="a25f8-125">Any users you add get automatically assigned a Microsoft 365 Business license.</span></span>
    
2. <span data-ttu-id="a25f8-p105">Si votre abonnement Microsoft 365 Entreprise est associé à des utilisateurs existants (par exemple, si vous utilisiez Azure AD Connect), vous avez la possibilité de leur attribuer des licences à ce stade. Poursuivez et ajoutez des licences pour eux aussi.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p105">If your Microsoft 365 Business subscription has existing users (for example, if you used Azure AD Connect) , you will get an option to assign licenses to them now. Go ahead and add licenses to them as well.</span></span>
    
3. <span data-ttu-id="a25f8-p106">Vous avez également la possibilité de partager des informations d'identification avec les nouveaux utilisateurs que vous ajoutez. Vous pouvez choisir de les imprimer, de les envoyer par e-mail ou de les télécharger.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p106">You will also get an option to share credentials with the new users you added. You can choose to print them out, email them, or download them.</span></span>
    
4. <span data-ttu-id="a25f8-130">Ignorez la migration des messages e-mail et sélectionnez **Suivant** dans la page **Migrer les messages e-mail**.</span><span class="sxs-lookup"><span data-stu-id="a25f8-130">Skip migrating email messages and choose **Next** on **Migrate email messages** page.</span></span> 
    
    <span data-ttu-id="a25f8-131">Si vous déplacez à partir d’un autre fournisseur de messagerie électronique et que vous souhaitez copier vos données ultérieurement, vous pouvez [migrer e-mail et les contacts vers Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span><span class="sxs-lookup"><span data-stu-id="a25f8-131">If you are moving from another email provider and want to copy your data later, you can [Migrate email and contacts to Office 365](https://support.office.com/article/a3e3bddb-582e-4133-8670-e61b9f58627e).</span></span>
    
    ![Screenshot of two new users added in the setup wizard](media/8f729967-5c65-4ceb-b737-18119db40564.png)
  
### <a name="step-3-connect-your-domain"></a><span data-ttu-id="a25f8-133">Étape 3 : Connectez-vous à votre domaine</span><span class="sxs-lookup"><span data-stu-id="a25f8-133">Step 3: Connect your domain</span></span>

> [!NOTE]
> <span data-ttu-id="a25f8-134">Si vous avez choisi d’utiliser le domaine .onmicrosoft ou utilisé Azure AD se connecter, vous ne verrez pas cette étape.</span><span class="sxs-lookup"><span data-stu-id="a25f8-134">If you chose to use the .onmicrosoft domain, or used Azure AD Connect, you will not see this step.</span></span> 
  
<span data-ttu-id="a25f8-135">Pour configurer des services, vous devez mettre à jour des enregistrements au niveau de votre hôte DNS ou de votre bureau d'enregistrement de domaines.</span><span class="sxs-lookup"><span data-stu-id="a25f8-135">To set up services, you have to update some records at your DNS host or domain registrar.</span></span>
  
1. <span data-ttu-id="a25f8-p107">Généralement, l’Assistant installation détecte votre serveur d’inscriptions et vous donne un lien vers des instructions pas à pas pour mettre à jour vos enregistrements NS sur le site Web du serveur d’inscriptions. Le cas contraire, [modifier des serveurs de noms pour configurer Office 365 avec les domaines](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span><span class="sxs-lookup"><span data-stu-id="a25f8-p107">The setup wizard typically detects your registrar and gives you a link to step-by-step instructions for updating your NS records at the registrar website. If it doesn't, [Change nameservers to set up Office 365 with any domain registrar](https://support.office.com/article/a8b487a9-2a45-4581-9dc4-5d28a47010a2).</span></span>
    
2. <span data-ttu-id="a25f8-138">La messagerie électronique et d'autres services sont configurés pour vous.</span><span class="sxs-lookup"><span data-stu-id="a25f8-138">Email and other services will be set up for you</span></span>
    
### <a name="step-4-manage-devices-and-work-files"></a><span data-ttu-id="a25f8-139">Étape 4 : Gestion des périphériques et des fichiers de travail</span><span class="sxs-lookup"><span data-stu-id="a25f8-139">Step 4: Manage devices and work files</span></span>

1. <span data-ttu-id="a25f8-p108">**Protéger les fichiers de travail sur des appareils mobiles** page attribuer **sur** **protéger les fichiers de travail lorsque les périphériques sont perdus ou volés** et paramètres **gérer comment les utilisateurs d’accès aux fichiers Office sur des appareils mobiles** . Vous pouvez également accéder à chaque paramètre sous-fonctionnalités en cliquant sur les chevrons en regard de chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="a25f8-p108">On the **Protect work files on your mobile devices** page set both **Protect work files when devices are lost or stolen** and **Manage how users access Office files on mobile devices** settings to **On**. You can also access each sub-setting by clicking the chevrons next to each setting.</span></span>
  
  <span data-ttu-id="a25f8-142">Tous les fichiers de travail de vos utilisateurs sous licence sont maintenant protégées sur les périphériques iOS ou Android, dès qu’ils [installer des applications Office](set-up-mobile-devices.md) (et s’authentifier auprès de leurs informations d’identification Microsoft 365 Business).</span><span class="sxs-lookup"><span data-stu-id="a25f8-142">All of your licensed users' work files are now protected on iOS and Android devices, as soon as they [install Office apps](set-up-mobile-devices.md) (and authenticate with their Microsoft 365 Business credentials).</span></span> 
  
  ![Screenshot of protect work files on your mobile devices page](media/3139a9aa-6228-4e74-8166-c6a886d7319f.PNG)
  
2. <span data-ttu-id="a25f8-144">Dans la page **configuration du périphérique définir Windows 10** , affectez au paramètre **Sécuriser Windows 10 périphériques** **activé**.</span><span class="sxs-lookup"><span data-stu-id="a25f8-144">On the **Set Windows 10 device configuration** page, set **Secure Windows 10 Devices** setting to **On**.</span></span>
  
   <span data-ttu-id="a25f8-145">Vous pouvez également accéder à chaque paramètre sous-fonctionnalités en cliquant sur le chevron située en regard.</span><span class="sxs-lookup"><span data-stu-id="a25f8-145">You can also access each sub-setting by clicking the chevron next to it.</span></span>
  
3. <span data-ttu-id="a25f8-p109">Définir le paramètre **Installer Office sur les périphériques Windows 10** **Oui** si tous les utilisateurs ont des ordinateurs Windows 10, et n’installe soit aucun Office existante, ou installe Office de click-to-run. Si ce n’est pas le cas, définissez cette option sur **No**. Vous pouvez [installer automatiquement Office](auto-install-or-uninstall-office.md) à partir du centre d’administration une fois que vous avez préparé les ordinateurs des utilisateurs. Pour plus d’informations, voir [Préparation de l’installation du client Office](prepare-for-office-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="a25f8-p109">Set the **Install Office on Windows 10 Devices** setting to **Yes** if all of your users have Windows 10 computers, and either no existing Office installs, or click-to-run Office installs. If this is not the case, set this option to **No**. You can [automatically install Office](auto-install-or-uninstall-office.md) later from the admin center after you have prepared the user computers. For instructions, see [prepare for Office client installation](prepare-for-office-client-deployment.md).</span></span>
  
    <span data-ttu-id="a25f8-150">Fichiers de travail des utilisateurs sous licence sur les appareils Windows 10 seront projetées dès qu’ils [participer à leur appareil Windows 10](set-up-windows-devices.md) à un domaine d’entreprise Microsoft 365 Azure AD ou [installer Windows 10 sur un nouvel ordinateur](https://support.office.com/article/c654bd23-d256-4ac7-8fba-0c993bf5a771.aspx) tout en joignant simultanément le 365 Microsoft Domaine d’entreprise Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a25f8-150">The licensed users' work files on Windows 10 devices will be projected as soon as they [join their Windows 10 device](set-up-windows-devices.md) to a Microsoft 365 Business Azure AD domain or [install Windows 10 on a new computer](https://support.office.com/article/c654bd23-d256-4ac7-8fba-0c993bf5a771.aspx) while simultaneously joining the Microsoft 365 Business Azure AD domain.</span></span> 
  
4. <span data-ttu-id="a25f8-151">Cliquez sur **Suivant** pour terminer la configuration.</span><span class="sxs-lookup"><span data-stu-id="a25f8-151">Click **Next** and you are done with setup.</span></span> 
  
    <span data-ttu-id="a25f8-152">Merci de nous faire part de vos commentaires à cette étape pour nous aider à améliorer l'expérience.</span><span class="sxs-lookup"><span data-stu-id="a25f8-152">Please leave us feedback at this step to help us improve the experience.</span></span>
  
    ![Screenshot of Prepare Windows 10 devices page](media/bff701c1-48a3-44f4-aa95-9d959d57c85b.PNG)
  
## <a name="additional-security-settings"></a><span data-ttu-id="a25f8-154">Paramètres de sécurité supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a25f8-154">Additional security settings</span></span>

<span data-ttu-id="a25f8-155">En plus de la sécurité et la définition de la conformité dans l’Assistant installation, vous pouvez également configurer les paramètres supplémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="a25f8-155">In addition to the security and compliance setting in the setup wizard, you can also set up the following additional settings:</span></span>
  
- <span data-ttu-id="a25f8-p110">Configurer la protection contre les pièces jointes non sécurisés. **Protection contre les menaces de avancée** (DAV) identifie un contenu malveillant et bloque la remise des pièces jointes non sécurisés, vous protéger contre les schémas de phishing et infection de logiciels. Pour activer la protection de la pièce jointe, voir [définir des stratégies Office 365 DAV approuvés en pièce jointe](https://support.office.com/article/078eb946-819a-4e13-8673-fe0c0ad3a775#setpolicy).</span><span class="sxs-lookup"><span data-stu-id="a25f8-p110">Set up protection against unsafe attachments. **Advanced Threat Protection** (ATP) identifies malicious content and then blocks delivery of unsafe attachments, helping protect you against phishing schemes and ransomware infections. To activate attachment protection, see [Set up Office 365 ATP Safe Attachments policies](https://support.office.com/article/078eb946-819a-4e13-8673-fe0c0ad3a775#setpolicy).</span></span>
    
- <span data-ttu-id="a25f8-p111">Lorsque les utilisateurs cliquent sur les liens malveillants de protéger votre environnement. DAV examine les liens dans le message électronique à la fois qu'un utilisateur clique dessus. Si un lien est non sécurisé, l’utilisateur est averti ne pas sur le site ou informé que le site a été bloqué. Cela permet de protéger contre le phishing. [Définir des stratégies Office 365 DAV fiables liens](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#reveddefaultscc) ou [définir des stratégies Office 365 DAV fiables liens](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#addemailpolscc).</span><span class="sxs-lookup"><span data-stu-id="a25f8-p111">Protect your environment when users click malicious links. ATP examines links in email at the time a user clicks them. If a link is unsafe, the user is warned not to visit the site or informed that the site has been blocked. This helps protect against phishing schemes. [Set up Office 365 ATP Safe Links policies](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#reveddefaultscc) or [Set up Office 365 ATP Safe Links policies](https://support.office.com/article/bdd5372d-775e-4442-9c1b-609627b94b5d#addemailpolscc).</span></span>
    
- <span data-ttu-id="a25f8-p112">Vous pouvez conserver tous les contenus de boîte aux lettres, y compris les éléments supprimés en plaçant les boîtes aux lettres entière d’un utilisateur pour litige **hold**. Pour plus d’informations, voir</span><span class="sxs-lookup"><span data-stu-id="a25f8-p112">You can preserve all mailbox content including deleted items by putting a user's entire mailbox on **litigation hold**. For instructions, see</span></span> 
- <span data-ttu-id="a25f8-166">[Configurer la conservation des e-mails avec l’archivage Exchange Online](security-features.md#set-up-email-retention-with-exchange-online-archiving).</span><span class="sxs-lookup"><span data-stu-id="a25f8-166">[Set up email retention with Exchange Online Archiving](security-features.md#set-up-email-retention-with-exchange-online-archiving).</span></span>
    
- <span data-ttu-id="a25f8-p113">Configurer des **stratégies de rétention**personnalisées, par exemple, à conserver pour une durée spécifique ou supprimer définitivement du contenu à la fin de la période de rétention. Vous pouvez activer les stratégies de rétention personnalisée dans le centre de conformité, accédez à **la gouvernance des données** et les titres \> **rétention**, puis suivez les étapes décrites dans l’Assistant. Pour plus d’informations, voir [vue d’ensemble des stratégies de rétention](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span><span class="sxs-lookup"><span data-stu-id="a25f8-p113">Set up customized **retention policies**, for example, to preserve for a specific amount of time or delete content permanently at the end of the retention period. You can enable customized retention policies in the Securities and compliance center, go to **Data governance** \> **Retention**, and then follow the steps in the wizard. To learn more, see [Overview of retention policies](https://support.office.com/article/5e377752-700d-4870-9b6d-12bfc12d2423).</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="a25f8-170">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="a25f8-170">Next steps</span></span>

<span data-ttu-id="a25f8-171">Pour les utilisateurs qui disposent d'une licence, l'étape suivante consiste à configurer des appareils.</span><span class="sxs-lookup"><span data-stu-id="a25f8-171">For the users that have their licenses, the next step is to set up devices.</span></span><br/> <span data-ttu-id="a25f8-172">Pour plus d'informations, voir [Configurer des appareils Windows pour les utilisateurs de Microsoft 365 Business](set-up-windows-devices.md) et [Configurer des appareils mobiles pour les utilisateurs de Microsoft 365 Business](set-up-mobile-devices.md).</span><span class="sxs-lookup"><span data-stu-id="a25f8-172">See [Set up Windows devices for Microsoft 365 Business users](set-up-windows-devices.md) and [Set up mobile devices for Microsoft 365 Business users](set-up-mobile-devices.md).</span></span> <br/><span data-ttu-id="a25f8-173">Pour obtenir des liens vers des rubriques relatives à la définition de stratégies de protection des applications et des appareils, et à la suppression de données sur les appareils des utilisateurs, consultez l'article [Gérer Microsoft 365 Business](manage.md).</span><span class="sxs-lookup"><span data-stu-id="a25f8-173">See [Manage Microsoft 365 Business](manage.md) for links to topics on how to set device and app protection polices, and how to remove data from user devices.</span></span> 
  


