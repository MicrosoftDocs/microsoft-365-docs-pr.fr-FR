---
title: Intégration des tickets ServiceNow dans le centre de sécurité et le centre de sécurité Microsoft 365
description: Découvrez comment créer et suivre des tickets dans ServiceNow à partir du centre de sécurité et du centre de sécurité Microsoft 365.
keywords: sécurité, Microsoft 365, M365, conformité, centre de conformité, centre de sécurité, ServiceNow, tickets, tâches, neige, connexion
ms.prod: w10
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
ms.openlocfilehash: d258bf3ec4c04eafd22e850329ca925b4c974e94
ms.sourcegitcommit: 41bc923bb31598cea8f02923792c1cd786e39616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2020
ms.locfileid: "45086666"
---
# <a name="integrate-servicenow-tickets-into-the-microsoft-365-security-center-and-compliance-center"></a><span data-ttu-id="58aa9-104">Intégration des tickets ServiceNow dans le centre de sécurité et le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="58aa9-104">Integrate ServiceNow tickets into the Microsoft 365 security center and compliance center</span></span>

[!include[Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="58aa9-105">ServiceNow est une plateforme de Cloud Computing populaire qui permet aux entreprises de gérer les flux de travail numériques pour les opérations d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="58aa9-105">ServiceNow is a popular cloud computing platform that helps companies manage digital workflows for enterprise operations.</span></span> <span data-ttu-id="58aa9-106">La plate-forme actuelle possède des flux de travail informatiques, des flux de travail d’employés et des flux de travail client.</span><span class="sxs-lookup"><span data-stu-id="58aa9-106">Their Now platform has IT workflows, employee workflows, and customer workflows.</span></span> [<span data-ttu-id="58aa9-107">En savoir plus sur ServiceNow</span><span class="sxs-lookup"><span data-stu-id="58aa9-107">Learn more about ServiceNow</span></span>](https://www.servicenow.com/)

<span data-ttu-id="58aa9-108">Microsoft s’est associé à ServiceNow pour permettre aux administrateurs informatiques de gérer plus facilement leurs tickets et leurs tâches sur les deux plateformes.</span><span class="sxs-lookup"><span data-stu-id="58aa9-108">Microsoft has partnered with ServiceNow to make it easier for IT admins to manage their tickets and tasks in both platforms.</span></span> <span data-ttu-id="58aa9-109">Le centre de [sécurité microsoft 365](overview-security-center.md) et le [Centre de conformité Microsoft 365](https://docs.microsoft.commicrosoft-365/compliance/microsoft-365-compliance-center) sont en cours d’amélioration avec la possibilité de créer et suivre en mode natif des tickets dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-109">[Microsoft 365 security center](overview-security-center.md) and the [Microsoft 365 compliance center](https://docs.microsoft.commicrosoft-365/compliance/microsoft-365-compliance-center) are being enhanced with the ability to natively create and track tickets in ServiceNow.</span></span>

- [<span data-ttu-id="58aa9-110">**Gérer les tickets ServiceNow dans le centre de sécurité**</span><span class="sxs-lookup"><span data-stu-id="58aa9-110">**Manage ServiceNow tickets in the security center**</span></span>](tickets-security-center.md)
- <span data-ttu-id="58aa9-111">**Gérer les tickets ServiceNow dans le centre de conformité** (bientôt disponible)</span><span class="sxs-lookup"><span data-stu-id="58aa9-111">**Manage ServiceNow tickets in the compliance center** (coming soon)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="58aa9-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="58aa9-112">Prerequisites</span></span>

<span data-ttu-id="58aa9-113">Avoir accès au centre de sécurité Microsoft 365 ou au centre de conformité et une instance ServiceNow avec :</span><span class="sxs-lookup"><span data-stu-id="58aa9-113">Have access to the Microsoft 365 security center or compliance center and a ServiceNow instance with:</span></span>  

* <span data-ttu-id="58aa9-114">Kingston ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="58aa9-114">Kingston or higher version</span></span>
* <span data-ttu-id="58aa9-115">Disposer des informations d’identification d’administrateur AIM</span><span class="sxs-lookup"><span data-stu-id="58aa9-115">Have admin HI credentials</span></span>
* <span data-ttu-id="58aa9-116">Disposer des privilèges d’administrateur sur l’instance de votre fournisseur cible</span><span class="sxs-lookup"><span data-stu-id="58aa9-116">Have admin privileges on your target vendor instance</span></span>

<span data-ttu-id="58aa9-117">ServiceNow recommande que les utilisateurs conservent les paramètres par défaut dans votre instance de ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-117">ServiceNow recommends that users keep default settings in your ServiceNow instance.</span></span> <span data-ttu-id="58aa9-118">Les personnalisations peuvent entraîner des erreurs lors de la fin de la liste de vérification de l’installation et de l’intégration avec le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="58aa9-118">Having customizations could cause errors when completing the installation checklist and integration with the Microsoft 365 security center.</span></span>

## <a name="data-exchange"></a><span data-ttu-id="58aa9-119">Échange de données</span><span class="sxs-lookup"><span data-stu-id="58aa9-119">Data exchange</span></span>

<span data-ttu-id="58aa9-120">Lorsque vous connectez le centre de sécurité Microsoft 365 ou le centre de conformité à ServiceNow, Microsoft reçoit les données supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="58aa9-120">When you connect the Microsoft 365 security center or compliance center to ServiceNow, Microsoft receives the following additional data:</span></span>

* <span data-ttu-id="58aa9-121">Nom de l’instance ServiceNow</span><span class="sxs-lookup"><span data-stu-id="58aa9-121">ServiceNow instance name</span></span>
* <span data-ttu-id="58aa9-122">ID client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="58aa9-122">ServiceNow client ID</span></span>
* <span data-ttu-id="58aa9-123">Clé secrète client ServiceNow</span><span class="sxs-lookup"><span data-stu-id="58aa9-123">ServiceNow client secret</span></span>
* <span data-ttu-id="58aa9-124">Jetons d’accès ServiceNow & d’actualisation</span><span class="sxs-lookup"><span data-stu-id="58aa9-124">ServiceNow access & refresh tokens</span></span>

<span data-ttu-id="58aa9-125">Lorsque vous créez un ticket ServiceNow à partir du centre de sécurité Microsoft 365 ou du centre de conformité, les données suivantes sont envoyées à ServiceNow :</span><span class="sxs-lookup"><span data-stu-id="58aa9-125">When you create a ServiceNow ticket from the Microsoft 365 security center or compliance center, the following data is sent to ServiceNow:</span></span>

* <span data-ttu-id="58aa9-126">ID d’utilisateur qui initie la création du ticket</span><span class="sxs-lookup"><span data-stu-id="58aa9-126">User ID that initiates the ticket creation</span></span>
* <span data-ttu-id="58aa9-127">Nom de la tâche</span><span class="sxs-lookup"><span data-stu-id="58aa9-127">Task name</span></span>
* <span data-ttu-id="58aa9-128">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="58aa9-128">Task description</span></span>
* <span data-ttu-id="58aa9-129">Priorité</span><span class="sxs-lookup"><span data-stu-id="58aa9-129">Priority</span></span>
* <span data-ttu-id="58aa9-130">Date d’échéance</span><span class="sxs-lookup"><span data-stu-id="58aa9-130">Due date</span></span>
* <span data-ttu-id="58aa9-131">Source de recommandation (recommandation de l’utilisateur ou recommandation de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58aa9-131">Recommendation source (User recommendation or Microsoft recommendation)</span></span>
* <span data-ttu-id="58aa9-132">Catégorie de recommandation (périphériques, données, applications, identité, infrastructure)</span><span class="sxs-lookup"><span data-stu-id="58aa9-132">Recommendation category (Devices, Data, Apps, Identity, Infrastructure)</span></span>

## <a name="connect-to-servicenow"></a><span data-ttu-id="58aa9-133">Se connecter à ServiceNow</span><span class="sxs-lookup"><span data-stu-id="58aa9-133">Connect to ServiceNow</span></span>

<span data-ttu-id="58aa9-134">Pour savoir comment vous connecter à ServiceNow, accédez à [la création et au suivi des tickets ServiceNow dans le centre de sécurité Microsoft 365](tickets-security-center.md) .</span><span class="sxs-lookup"><span data-stu-id="58aa9-134">Go to [Create and track ServiceNow tickets in the Microsoft 365 security center](tickets-security-center.md) to learn how to connect to ServiceNow.</span></span> <span data-ttu-id="58aa9-135">La connexion à partir du centre de conformité Microsoft 365 sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="58aa9-135">Connecting from the Microsoft 365 compliance center is coming soon.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="58aa9-136">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="58aa9-136">Troubleshooting</span></span>

### <a name="you-receive-an-error-in-the-first-step-of-the-installation-checklist-oauth-creation"></a><span data-ttu-id="58aa9-137">Vous recevez une erreur dans la première étape de la liste de vérification de l’installation (création OAuth)</span><span class="sxs-lookup"><span data-stu-id="58aa9-137">You receive an error in the first step of the installation checklist (OAuth creation)</span></span>

<span data-ttu-id="58aa9-138">**Message d’erreur**: l’opération de lecture sur « oauth_entity » de l’étendue « x_mioms_m365ticket » a été refusée en raison de la stratégie d’accès aux étendues de la table</span><span class="sxs-lookup"><span data-stu-id="58aa9-138">**Error Message**: Read operation against 'oauth_entity' from scope 'x_mioms_m365ticket' has been refused due to the table's cross-scope access policy</span></span>

<span data-ttu-id="58aa9-139">L’application part du principe que n’importe quel administrateur de l’instance de ServiceNow peut créer et lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="58aa9-139">The app assumes any admin on the ServiceNow instance can create and read OAuth entities.</span></span> <span data-ttu-id="58aa9-140">Cette erreur peut être due à une personnalisation sur votre instance de ServiceNow, ce qui limite les personnes autorisées à créer/lire des entités OAuth.</span><span class="sxs-lookup"><span data-stu-id="58aa9-140">This error could be caused due to a customization on your instance of ServiceNow, which restricts who can create/read OAuth entities.</span></span>

<span data-ttu-id="58aa9-141">**ServiceNow recommande que les utilisateurs conservent les fonctionnalités par défaut.**</span><span class="sxs-lookup"><span data-stu-id="58aa9-141">**ServiceNow recommends that users keep default functionality.**</span></span>

<span data-ttu-id="58aa9-142">Définissez les configurations des tables « registres des applications » sur par défaut :</span><span class="sxs-lookup"><span data-stu-id="58aa9-142">Set the "application registries" table configurations to default:</span></span>

* <span data-ttu-id="58aa9-143">Label = registres de l’application</span><span class="sxs-lookup"><span data-stu-id="58aa9-143">Label = Application Registeries</span></span>
* <span data-ttu-id="58aa9-144">Nom = oauth_entity</span><span class="sxs-lookup"><span data-stu-id="58aa9-144">Name = oauth_entity</span></span>
* <span data-ttu-id="58aa9-145">Accessible à partir de = toutes les étendues d’application</span><span class="sxs-lookup"><span data-stu-id="58aa9-145">Accessible from = All application scopes</span></span>
* <span data-ttu-id="58aa9-146">Lecture possible = case à cocher activée</span><span class="sxs-lookup"><span data-stu-id="58aa9-146">Can read = check box selected</span></span>

### <a name="how-to-validate-the-oauth-entity-created-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="58aa9-147">Procédure de validation de l’entité OAuth créée pour Microsoft 365 Security & Compliance Connector</span><span class="sxs-lookup"><span data-stu-id="58aa9-147">How to validate the OAuth entity created for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="58aa9-148">Accédez à la table des registres des applications (**Menu > système oauth > application Registry**) dans ServiceNow et recherchez l’entité OAuth créée par vous, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="58aa9-148">Go to application registries table (**Menu > System OAuth > Application Registry**) in ServiceNow and find the OAuth entity created by you, with the name that you assigned it.</span></span>

### <a name="logging-in-as-the-integration-user"></a><span data-ttu-id="58aa9-149">Connexion en tant qu’utilisateur de l’intégration</span><span class="sxs-lookup"><span data-stu-id="58aa9-149">Logging in as the integration user</span></span>

<span data-ttu-id="58aa9-150">Avant d’autoriser la connexion entre le centre de sécurité Microsoft 365 et ServiceNow, veillez à utiliser le nom d’utilisateur et le mot de passe d’intégration que vous avez créés lors des étapes d’installation.</span><span class="sxs-lookup"><span data-stu-id="58aa9-150">Before you authorize the connection between Microsoft 365 security center and ServiceNow, make sure you use the integration user login and password you created in the installation steps.</span></span> <span data-ttu-id="58aa9-151">N’utilisez pas vos informations d’identification personnelles.</span><span class="sxs-lookup"><span data-stu-id="58aa9-151">Do not use your personal credentials.</span></span>

1. <span data-ttu-id="58aa9-152">Accédez à la page Authorization (autorisation) dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-152">Go the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="58aa9-153">Si vous êtes connecté avec vos informations d’identification personnelles, sélectionnez le lien qui ne se trouve **pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="58aa9-153">If you are signed in with your personal credentials, select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="58aa9-154">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="58aa9-154">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="58aa9-155">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-155">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="58aa9-156">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="58aa9-156">Proceed with the setup steps.</span></span>

### <a name="how-to-validate-the-integration-user-created-with-the-installation-checklist-for-microsoft-365-security--compliance-connector"></a><span data-ttu-id="58aa9-157">Procédure de validation de l’utilisateur d’intégration créé avec la liste de vérification d’installation pour le connecteur de sécurité & conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="58aa9-157">How to validate the Integration User created with the installation checklist for Microsoft 365 Security & Compliance connector</span></span>

<span data-ttu-id="58aa9-158">Accédez à la table utilisateurs **(Menu > l’administration des utilisateurs > les utilisateurs**) dans ServiceNow et recherchez l’utilisateur d’intégration que vous avez créé, avec le nom que vous lui avez attribué.</span><span class="sxs-lookup"><span data-stu-id="58aa9-158">Go to Users Table **(Menu > User Administration > Users**) in ServiceNow and find the Integration user created by you, with the name that you assigned it.</span></span>

### <a name="your-company-has-single-sign-on-enabled-which-prevents-you-from-connecting-to-servicenow-through-the-microsoft-365-security-center"></a><span data-ttu-id="58aa9-159">Votre entreprise a activé l’authentification unique, ce qui vous empêche de vous connecter à ServiceNow via le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="58aa9-159">Your company has single sign-on enabled which prevents you from connecting to ServiceNow through the Microsoft 365 security center</span></span>

<span data-ttu-id="58aa9-160">Si votre entreprise a activé l’authentification unique et que vous recevez une erreur ou si la connexion échoue, suivez l’une des deux solutions.</span><span class="sxs-lookup"><span data-stu-id="58aa9-160">If your company has enabled single sign-on and you receive an error or login is unsuccessful, follow one of the two solutions.</span></span>

#### <a name="log-into-servicenow-as-the-integration-user"></a><span data-ttu-id="58aa9-161">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration.</span><span class="sxs-lookup"><span data-stu-id="58aa9-161">Log into ServiceNow as the integration user</span></span>

1. <span data-ttu-id="58aa9-162">Revenez à la page autorisation dans ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-162">Navigate back to the authorization page in ServiceNow.</span></span>
2. <span data-ttu-id="58aa9-163">Sélectionnez le lien qui **n’est pas** dans le coin supérieur droit.</span><span class="sxs-lookup"><span data-stu-id="58aa9-163">Select the **Not You** link in the upper right-hand corner.</span></span>
3. <span data-ttu-id="58aa9-164">Connectez-vous à ServiceNow en tant qu’utilisateur d’intégration que vous avez créé précédemment à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="58aa9-164">Log in to ServiceNow as the integration user you created previously from the installation checklist.</span></span>  
4. <span data-ttu-id="58aa9-165">Sélectionnez **autoriser** dans la page ServiceNow pour demander si le connecteur sécurité + conformité peut se connecter à votre compte ServiceNow.</span><span class="sxs-lookup"><span data-stu-id="58aa9-165">Select **Allow** in the ServiceNow page that asks whether the Security + Compliance Connector can connect to your ServiceNow account.</span></span>
5. <span data-ttu-id="58aa9-166">Suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="58aa9-166">Proceed with the setup steps.</span></span>

#### <a name="create-a-security-admin-user"></a><span data-ttu-id="58aa9-167">Créer un utilisateur d’administrateur de sécurité</span><span class="sxs-lookup"><span data-stu-id="58aa9-167">Create a security admin user</span></span>

1. <span data-ttu-id="58aa9-168">Créez un utilisateur avec des privilèges d’administrateur de sécurité dans Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="58aa9-168">Create a user with security admin privileges in Azure Active Directory.</span></span> <span data-ttu-id="58aa9-169">L’utilisateur doit avoir les mêmes nom et adresse de messagerie que l’utilisateur d’intégration que vous avez créé à partir de la liste de vérification d’installation.</span><span class="sxs-lookup"><span data-stu-id="58aa9-169">The user needs to have the same name and email address as the integration user you created from the Installation Checklist.</span></span> <span data-ttu-id="58aa9-170">Vous pouvez supprimer le rôle d’administrateur de sécurité une fois la connexion et la connexion terminées.</span><span class="sxs-lookup"><span data-stu-id="58aa9-170">You can remove the security admin role once login and connection has been completed.</span></span>
2. <span data-ttu-id="58aa9-171">Connectez-vous au centre de sécurité Microsoft 365 en tant qu’utilisateur et suivez les étapes de configuration.</span><span class="sxs-lookup"><span data-stu-id="58aa9-171">Log in to the Microsoft 365 security center as this user and follow the setup steps.</span></span>

### <a name="ip-filtering"></a><span data-ttu-id="58aa9-172">Filtrage IP</span><span class="sxs-lookup"><span data-stu-id="58aa9-172">IP filtering</span></span>

<span data-ttu-id="58aa9-173">Si vous avez activé le filtrage IP, vous devrez peut-être autoriser explicitement les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="58aa9-173">If you have enabled IP filtering, you may need to explicitly allow IP addresses.</span></span> <span data-ttu-id="58aa9-174">Pour plus d’informations sur l’autorisation des plages IP dans ServiceNow, voir [contrôle d’accès aux adresses IP](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/login/task/t_AccessControl.html) .</span><span class="sxs-lookup"><span data-stu-id="58aa9-174">See [IP Address Access Control](https://docs.servicenow.com/bundle/orlando-platform-administration/page/administer/login/task/t_AccessControl.html) for information on how to allow IP ranges in ServiceNow.</span></span> <span data-ttu-id="58aa9-175">Consultez la rubrique [Azure IP Ranges and service Tags-public Cloud](https://www.microsoft.com/en-us/download/details.aspx?id=56519) pour obtenir la liste des adresses IP à autoriser.</span><span class="sxs-lookup"><span data-stu-id="58aa9-175">See [Azure IP Ranges and Service Tags - Public Cloud](https://www.microsoft.com/en-us/download/details.aspx?id=56519) for a list of IP addresses to allow.</span></span>

### <a name="installation-is-complete-but-dont-see-tickets-and-cant-share"></a><span data-ttu-id="58aa9-176">L’installation est terminée, mais ne vois pas les tickets et ne peut pas partager</span><span class="sxs-lookup"><span data-stu-id="58aa9-176">Installation is complete but don't see tickets and can't share</span></span>

<span data-ttu-id="58aa9-177">Si les étapes d’installation et de configuration sont terminées, mais que vous ne voyez pas les cartes ServiceNow sur la page d’accueil et que vous ne pouvez pas partager de ServiceNow à partir du score de sécurité Microsoft, vérifiez l’état de la page de mise en service sur https://security.microsoft.com/ticketProvisioning .</span><span class="sxs-lookup"><span data-stu-id="58aa9-177">If the installation and setup steps have been completed, but you don't see the ServiceNow cards on the home page and can't share to ServiceNow from Microsoft Secure Score, check the status of the provisioning page at https://security.microsoft.com/ticketProvisioning.</span></span> <span data-ttu-id="58aa9-178">Sélectionnez **autoriser** et revenir à la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="58aa9-178">Select **Authorize** and return to the home page.</span></span> <span data-ttu-id="58aa9-179">Les cartes doivent apparaître.</span><span class="sxs-lookup"><span data-stu-id="58aa9-179">The cards should appear.</span></span>

## <a name="resources"></a><span data-ttu-id="58aa9-180">Ressources</span><span class="sxs-lookup"><span data-stu-id="58aa9-180">Resources</span></span>

- [<span data-ttu-id="58aa9-181">Gérer les tickets ServiceNow dans le centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="58aa9-181">Manage ServiceNow tickets in the security center</span></span>](tickets-security-center.md)