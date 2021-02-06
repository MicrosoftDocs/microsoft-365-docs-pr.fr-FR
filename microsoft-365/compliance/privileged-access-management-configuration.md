---
title: Prise en main de la gestion des accès privilégiés
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- m365-security-compliance
- m365solution-insiderrisk
- m365initiative-compliance
ms.custom:
- Ent_Solutions
- seo-marvel-apr2020
ms.assetid: ''
description: Utilisez cet article pour en savoir plus sur l’activation et la configuration de la gestion des accès privilégiés dans Office 365.
ms.openlocfilehash: 0b8d79c3012ecd321d7b00c1566aa557077d55f1
ms.sourcegitcommit: eac5d9f759f290d3c51cafaf335a1a1c43ded927
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "50126531"
---
# <a name="get-started-with-privileged-access-management"></a><span data-ttu-id="cdb72-103">Prise en main de la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="cdb72-103">Get started with privileged access management</span></span>

<span data-ttu-id="cdb72-104">Cette rubrique vous guide tout au long de l’activation et de la configuration de la gestion des accès privilégiés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-104">This topic guides you through enabling and configuring privileged access management in your organization.</span></span> <span data-ttu-id="cdb72-105">Vous pouvez utiliser le Centre d’administration Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser l’accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="cdb72-105">You can use either the Microsoft 365 admin center or Exchange Management PowerShell to manage and use privileged access.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="cdb72-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="cdb72-106">Before you begin</span></span>

<span data-ttu-id="cdb72-107">Avant de commencer à gérer les accès privilégiés, vous devez confirmer votre abonnement [Microsoft 365](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans) et les modules.</span><span class="sxs-lookup"><span data-stu-id="cdb72-107">Before you get started with privileged access management, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans) and any add-ons.</span></span> <span data-ttu-id="cdb72-108">Pour accéder à la gestion des accès privilégiés et l’utiliser, votre organisation doit avoir l’un des abonnements ou modules suivants :</span><span class="sxs-lookup"><span data-stu-id="cdb72-108">To access and use privileged access management, your organization must have one of the following subscriptions or add-ons:</span></span>

- <span data-ttu-id="cdb72-109">Abonnement Microsoft 365 E5 (version payante ou d’essai)</span><span class="sxs-lookup"><span data-stu-id="cdb72-109">Microsoft 365 E5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="cdb72-110">Abonnement Microsoft 365 E3 (ou abonnement Office 365 E3 + Abonnement Enterprise Mobility and Security E3) + module de conformité Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="cdb72-110">Microsoft 365 E3 subscription (or Office 365 E3 subscription + Enterprise Mobility and Security E3 subscription) + the Microsoft 365 E5 Compliance add-on</span></span>
- <span data-ttu-id="cdb72-111">Tout abonnement Microsoft 365, Office 365, Exchange, SharePoint ou OneDrive Entreprise + le module de gestion des risques internes Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="cdb72-111">Any Microsoft 365, Office 365, Exchange, SharePoint, or OneDrive for Business subscription + the Microsoft 365 E5 Insider Risk Management add-on</span></span>  
- <span data-ttu-id="cdb72-112">Abonnement Microsoft 365 A5 (version payante ou d’essai)</span><span class="sxs-lookup"><span data-stu-id="cdb72-112">Microsoft 365 A5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="cdb72-113">Abonnement Microsoft 365 A3 (ou abonnement Office 365 A3 + abonnement Enterprise Mobility and Security A3) + module de conformité Microsoft A5</span><span class="sxs-lookup"><span data-stu-id="cdb72-113">Microsoft 365 A3 subscription (or Office 365 A3 subscription + Enterprise Mobility and Security A3 subscription) + the Microsoft A5 Compliance add-on</span></span>
- <span data-ttu-id="cdb72-114">Tout abonnement Microsoft 365, Office 365, Exchange, SharePoint ou OneDrive Éducation + le module de gestion des risques internes Microsoft 365 A5</span><span class="sxs-lookup"><span data-stu-id="cdb72-114">Any Microsoft 365, Office 365, Exchange, SharePoint, or OneDrive for Education subscription + the Microsoft 365 A5 Insider Risk Management add-on</span></span>
- <span data-ttu-id="cdb72-115">Abonnement Office 365 Entreprise E5 (version payante ou d’essai)</span><span class="sxs-lookup"><span data-stu-id="cdb72-115">Office 365 Enterprise E5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="cdb72-116">Abonnement Office 365 Entreprise E3 + module de conformité avancée Office 365 (non disponible pour les nouveaux abonnements, voir la remarque)</span><span class="sxs-lookup"><span data-stu-id="cdb72-116">Office 365 Enterprise E3 subscription + the Office 365 Advanced Compliance add-on (no longer available for new subscriptions, see note)</span></span>

<span data-ttu-id="cdb72-117">Les utilisateurs qui envoient des demandes de gestion des accès privilégiés et y répondent doivent se voir attribuer l’une des licences ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="cdb72-117">Users submitting and responding to privileged access management requests must be assigned one of the licenses above.</span></span>

>[!IMPORTANT]
><span data-ttu-id="cdb72-118">La conformité avancée Office 365 n’est plus vendue en tant qu’abonnement autonome.</span><span class="sxs-lookup"><span data-stu-id="cdb72-118">Office 365 Advanced Compliance is no longer sold as a standalone subscription.</span></span> <span data-ttu-id="cdb72-119">Lorsque les abonnements actuels expirent, les clients doivent passer à l’un des abonnements ci-dessus, qui contient les mêmes fonctionnalités de conformité ou des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cdb72-119">When current subscriptions expire, customers should transition to one of the subscriptions above, which contain the same or additional compliance features.</span></span>

<span data-ttu-id="cdb72-120">Si vous n’avez pas de plan Office 365 Entreprise E5 existant et que vous souhaitez essayer la gestion des accès [](https://www.microsoft.com/microsoft-365/enterprise) privilégiés, vous pouvez ajouter [Microsoft 365](/office365/admin/try-or-buy-microsoft-365) à votre abonnement Office 365 existant ou vous inscrire à une version d’essai de Microsoft 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="cdb72-120">If you don't have an existing Office 365 Enterprise E5 plan and want to try privileged access management, you can [add Microsoft 365](/office365/admin/try-or-buy-microsoft-365) to your existing Office 365 subscription or [sign up for a trial](https://www.microsoft.com/microsoft-365/enterprise) of Microsoft 365 Enterprise E5.</span></span>

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="cdb72-121">Activer et configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="cdb72-121">Enable and configure privileged access management</span></span>

<span data-ttu-id="cdb72-122">Suivez ces étapes pour configurer et utiliser l’accès privilégié dans votre organisation :</span><span class="sxs-lookup"><span data-stu-id="cdb72-122">Follow these steps to set up and use privileged access in your organization:</span></span>

- [<span data-ttu-id="cdb72-123">Étape 1 : Créer un groupe d’approbation</span><span class="sxs-lookup"><span data-stu-id="cdb72-123">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="cdb72-124">Avant de commencer à utiliser l’accès privilégié, déterminez qui a besoin de l’autorité d’approbation pour les demandes entrantes permettant d’accéder à des tâches avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="cdb72-124">Before you start using privilege access, determine who needs approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="cdb72-125">Tout utilisateur faisant partie du groupe d’approbateurs peut approuver les demandes d’accès.</span><span class="sxs-lookup"><span data-stu-id="cdb72-125">Any user who is part of the Approvers' group is able to approve access requests.</span></span> <span data-ttu-id="cdb72-126">Ce groupe est activé en créant un groupe de sécurité à messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdb72-126">This group is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="cdb72-127">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="cdb72-127">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="cdb72-128">Les accès privilégiés doivent être activés de manière explicite dans Office 365 avec le groupe d’approbateurs par défaut, y compris un ensemble de comptes système que vous souhaitez exclure du contrôle d’accès par gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="cdb72-128">Privileged access must be explicitly enabled in Office 365 with the default approver group, including a set of system accounts that you want excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="cdb72-129">Étape 3 : Créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="cdb72-129">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="cdb72-130">La création d’une stratégie d’approbation vous permet de définir les exigences d’approbation spécifiques d’une tâche spécifique.</span><span class="sxs-lookup"><span data-stu-id="cdb72-130">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="cdb72-131">Les options type d’approbation sont **Automatiques** ou **Manuelles**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-131">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="cdb72-132">Étape 4 : Envoyer/approuver des demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="cdb72-132">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="cdb72-133">Une fois activé, l’accès privilégié nécessite des approbations pour toutes les tâches auxquelles une stratégie d’approbation associée est définie.</span><span class="sxs-lookup"><span data-stu-id="cdb72-133">Once enabled, privileged access requires approvals for any task that has an associated approval policy defined.</span></span> <span data-ttu-id="cdb72-134">Pour les tâches incluses dans une stratégie d’approbation, les utilisateurs doivent demander et se voir autoriser d’accès afin d’obtenir les autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="cdb72-134">For tasks included in an approval policy, users must request and be granted access approval to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="cdb72-135">Une fois l’approbation accordée, l’utilisateur demandeur peut exécuter la tâche prévue et l’accès privilégié autorise et exécute la tâche au nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cdb72-135">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on behalf of the user.</span></span> <span data-ttu-id="cdb72-136">L’approbation reste valide pendant la durée demandée (la durée par défaut est de 4 heures), période durant laquelle le demandeur peut effectuer la tâche prévue plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="cdb72-136">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="cdb72-137">Toutes ces réalisations sont enregistrées et mises à disposition pour l’audit sur la sécurité et la conformité.</span><span class="sxs-lookup"><span data-stu-id="cdb72-137">All such executions are logged and made available for security and compliance auditing.</span></span> 

>[!NOTE]
><span data-ttu-id="cdb72-138">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l’accès privilégié, suivez les étapes de la procédure de connexion à Exchange Online PowerShell à l’aide de l’authentification [multifacteur](/powershell/exchange/connect-to-exchange-online-powershell#connect-to-exchange-online-powershell-using-mfa) pour vous connecter à Exchange Online PowerShell avec vos informations d’identification Office 365.</span><span class="sxs-lookup"><span data-stu-id="cdb72-138">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](/powershell/exchange/connect-to-exchange-online-powershell#connect-to-exchange-online-powershell-using-mfa) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="cdb72-139">Il n’est pas nécessaire d’activer l’authentification multifacteur pour que votre organisation utilise les étapes permettant d’activer l’accès privilégié lors de la connexion à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cdb72-139">You do not need to enable multi-factor authentication for your organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="cdb72-140">La connexion avec l’authentification multifacteur crée un jeton OAuth qui est utilisé par l’accès privilégié pour la signature de vos demandes.</span><span class="sxs-lookup"><span data-stu-id="cdb72-140">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="cdb72-141"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="cdb72-141"><a name="step1"> </a></span></span>

## <a name="step-1-create-an-approvers-group"></a><span data-ttu-id="cdb72-142">Étape 1 : Créer un groupe d’approbation</span><span class="sxs-lookup"><span data-stu-id="cdb72-142">Step 1: Create an approver's group</span></span>

1. <span data-ttu-id="cdb72-143">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-143">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="cdb72-144">Dans le Centre d’administration, allez à **Groupes**  >  **Ajouter un groupe.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-144">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="cdb72-145">Sélectionnez **le groupe de** sécurité à messagerie, puis complétez les champs Nom, Adresse de **messagerie** du groupe et **Description** du nouveau groupe. </span><span class="sxs-lookup"><span data-stu-id="cdb72-145">Select **mail-enabled security group** and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="cdb72-146">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="cdb72-146">Save the group.</span></span> <span data-ttu-id="cdb72-147"> La configuration totale du groupe peut prendre quelques minutes et s’affiche dans le Centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cdb72-147">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="cdb72-148">Sélectionnez le groupe du nouvel approuveur et sélectionnez **Modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="cdb72-148">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="cdb72-149">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="cdb72-149">Save the group.</span></span>

<span data-ttu-id="cdb72-150"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="cdb72-150"><a name="step2"> </a></span></span>

## <a name="step-2-enable-privileged-access"></a><span data-ttu-id="cdb72-151">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="cdb72-151">Step 2: Enable privileged access</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-152">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-152">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="cdb72-153">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-153">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="cdb72-154">Dans le Centre d’administration, accédez à   >  **Paramètres Org Settings**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-154">In the Admin Center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-155">Activez **le contrôle Exiger des approbations pour les tâches privilégiées.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-155">Enable the **Require approvals for privileged tasks** control.</span></span>

4. <span data-ttu-id="cdb72-156">Affectez le groupe de l’approuveur que vous avez créé à l’étape 1 en tant que groupe **d’approbations par défaut.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-156">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="cdb72-157">**Enregistrer** et **fermer**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-157">**Save** and **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-158">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-158">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-159">Pour activer l’accès privilégié et affecter le groupe de l’approuveur, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-159">To enable privileged access and to assign the approver's group, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```

<span data-ttu-id="cdb72-160">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-160">Example:</span></span>

```PowerShell
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', 'sys2@fabrikamorg.onmicrosoft.com')
```

>[!NOTE]
><span data-ttu-id="cdb72-161">La fonctionnalité comptes système est mise à disposition pour garantir que certaines automatisations au sein de vos organisations peuvent fonctionner sans dépendance sur l’accès privilégié. Toutefois, il est recommandé que ces exclusions soient exceptionnelles et que celles autorisées doivent être approuvées et auditées régulièrement.</span><span class="sxs-lookup"><span data-stu-id="cdb72-161">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="cdb72-162"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="cdb72-162"><a name="step3"> </a></span></span>

## <a name="step-3-create-an-access-policy"></a><span data-ttu-id="cdb72-163">Étape 3 : Créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="cdb72-163">Step 3: Create an access policy</span></span>

<span data-ttu-id="cdb72-164">Vous pouvez créer et configurer jusqu’à 30 stratégies d’accès privilégié pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-164">You can create and configure up to 30 privileged access policies for your organization.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-165">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-165">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="cdb72-166">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-166">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="cdb72-167">Dans le Centre d’administration, accédez à   >  **Paramètres Org Settings**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-167">In the Admin Center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-168">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-168">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="cdb72-169">Sélectionnez **Configurer des stratégies** et **ajouter une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-169">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="cdb72-170">Dans les champs de la baisse, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="cdb72-170">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="cdb72-171">**Type de stratégie** : tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="cdb72-171">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="cdb72-172">**Étendue de la stratégie** : Exchange</span><span class="sxs-lookup"><span data-stu-id="cdb72-172">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="cdb72-173">**Nom de la stratégie** : sélection parmi les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="cdb72-173">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="cdb72-174">**Type d’approbation** : manuel ou automatique</span><span class="sxs-lookup"><span data-stu-id="cdb72-174">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="cdb72-175">**Groupe d’approbation** : sélection du groupe d’approbateurs créé à l’Étape 1.</span><span class="sxs-lookup"><span data-stu-id="cdb72-175">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="cdb72-176">Sélectionnez **Créer,** puis **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-176">Select **Create** and then **Close**.</span></span> <span data-ttu-id="cdb72-177">La configuration et l’activé de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="cdb72-177">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-178">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-178">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-179">Pour créer et définir une stratégie d’approbation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-179">To create and define an approval policy, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```

<span data-ttu-id="cdb72-180">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-180">Example:</span></span>

```PowerShell
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="cdb72-181"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="cdb72-181"><a name="step4"> </a></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="cdb72-182">Étape 4 : Envoyer/approuver des demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="cdb72-182">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="cdb72-183">Demander une autorisation d’élévation pour l’exécution de tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="cdb72-183">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="cdb72-184">Les demandes d’accès privilégié sont valables pendant 24 heures après l’envoi de la demande.</span><span class="sxs-lookup"><span data-stu-id="cdb72-184">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="cdb72-185">En cas de rejet ou de refus, les demandes expirent et l’accès n’est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="cdb72-185">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-186">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-186">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="cdb72-187">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb72-187">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="cdb72-188">Dans le Centre d’administration, accédez à   >  **Paramètres Org Settings**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-188">In the Admin Center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-189">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-189">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="cdb72-190">Sélectionnez **Nouvelle requête**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-190">Select **New request**.</span></span> <span data-ttu-id="cdb72-191">Dans les champs de la baisse, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="cdb72-191">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="cdb72-192">**Type de demande** : tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="cdb72-192">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="cdb72-193">**Étendue de la demande** : Exchange</span><span class="sxs-lookup"><span data-stu-id="cdb72-193">**Request scope**: Exchange</span></span>

    <span data-ttu-id="cdb72-194">**Demande pour** : sélection parmi les stratégies disponibles</span><span class="sxs-lookup"><span data-stu-id="cdb72-194">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="cdb72-195">**Durée (heures)**  : nombre d’heures d’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="cdb72-195">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="cdb72-196">Le nombre d’heures qui peuvent être demandées n’est pas limité.</span><span class="sxs-lookup"><span data-stu-id="cdb72-196">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="cdb72-197">**Commentaires :** champ texte pour les commentaires liés à votre demande d’accès</span><span class="sxs-lookup"><span data-stu-id="cdb72-197">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="cdb72-198">Sélectionnez **Enregistrer,** puis **Fermer.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-198">Select **Save** and then **Close**.</span></span> <span data-ttu-id="cdb72-199">Votre demande est envoyée au groupe de l’approuveur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="cdb72-199">Your request will be sent to the approver's group via email.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-200">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-200">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-201">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et envoyer une demande d’approbation au groupe de l’approuveur :</span><span class="sxs-lookup"><span data-stu-id="cdb72-201">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>

```PowerShell
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```

<span data-ttu-id="cdb72-202">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-202">Example:</span></span>

```PowerShell
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```

### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="cdb72-203">Afficher le statut des demandes d’élévation</span><span class="sxs-lookup"><span data-stu-id="cdb72-203">View status of elevation requests</span></span>

<span data-ttu-id="cdb72-204">Une fois qu’une demande d’approbation est créée, l’état de la demande d’élévation peut être examiné dans le Centre d’administration ou dans Exchange Management PowerShell à l’aide de l’ID de demande associé.</span><span class="sxs-lookup"><span data-stu-id="cdb72-204">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-205">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-205">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="cdb72-206">Connectez-vous [au Centre d’administration Microsoft 365](https://admin.microsoft.com) avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb72-206">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="cdb72-207">Dans le Centre d’administration, accédez à **Paramètres** De l’organisation  >  **Paramètres** Sécurité  >  **& Accès**  >  **privilégié à la confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-207">In the admin center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-208">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-208">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="cdb72-209">Sélectionnez **Affichage** pour filtrer les demandes envoyées par **état En attente,** **Approuvé,** Refusé **ou** **Customer Lockbox.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-209">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-210">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-210">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-211">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher l’état d’une demande d’approbation pour un ID de demande spécifique :</span><span class="sxs-lookup"><span data-stu-id="cdb72-211">Run the following command in Exchange Online PowerShell to view an approval request status for a specific request ID:</span></span>

```PowerShell
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```

<span data-ttu-id="cdb72-212">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-212">Example:</span></span>

```PowerShell
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="cdb72-213">Approbation d’une demande d’autorisation d’élévation</span><span class="sxs-lookup"><span data-stu-id="cdb72-213">Approving an elevation authorization request</span></span>

<span data-ttu-id="cdb72-214">Lorsqu’une demande d’approbation est créée, les membres du groupe d’approbation approprié reçoivent une notification par courrier électronique et peuvent approuver la demande associée à l’ID de demande.</span><span class="sxs-lookup"><span data-stu-id="cdb72-214">When an approval request is created, members of the relevant approver group receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="cdb72-215">Le demandeur est informé de l’approbation ou du refus par message électronique.</span><span class="sxs-lookup"><span data-stu-id="cdb72-215">The requestor is notified of the request approval or denial via email message.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-216">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-216">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="cdb72-217">Connectez-vous [au Centre d’administration Microsoft 365](https://admin.microsoft.com) avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb72-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="cdb72-218">Dans le Centre d’administration, accédez à **Paramètres** De l’organisation  >  **Paramètres** Sécurité  >  **& Accès**  >  **privilégié à la confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-218">In the admin center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-219">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="cdb72-220">Sélectionnez une demande répertoriée pour afficher les détails et prendre des mesures sur la demande.</span><span class="sxs-lookup"><span data-stu-id="cdb72-220">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="cdb72-221">Sélectionnez **Approuver** pour approuver la demande ou **Refuser** pour refuser la demande.</span><span class="sxs-lookup"><span data-stu-id="cdb72-221">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="cdb72-222">Les demandes précédemment approuvées peuvent être révoquées en sélectionnant **Révoquer.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-222">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-223">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-223">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-224">Pour approuver une demande d’autorisation d’élévation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-224">To approve an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```

<span data-ttu-id="cdb72-225">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-225">Example:</span></span>

```PowerShell
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="cdb72-226">Pour refuser une demande d’autorisation d’élévation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-226">To deny an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```

<span data-ttu-id="cdb72-227">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cdb72-227">Example:</span></span>

```PowerShell
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="cdb72-228">Supprimer une stratégie d’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-228">Delete a privileged access policy in Office 365</span></span>

<span data-ttu-id="cdb72-229">Si elle n’est plus nécessaire dans votre organisation, vous pouvez supprimer une stratégie d’accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="cdb72-229">If it is no longer needed in your organization, you can delete a privileged access policy.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-230">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-230">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="cdb72-231">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-231">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="cdb72-232">Dans le Centre d’administration, accédez à **Paramètres** De l’organisation Paramètres Sécurité & Accès privilégié à  >    >    >  **la confidentialité.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-232">In the admin center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-233">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-233">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="cdb72-234">Sélectionnez **Configurer les stratégies.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-234">Select **Configure policies**.</span></span>

5. <span data-ttu-id="cdb72-235">Sélectionnez la stratégie à supprimer, puis **sélectionnez Supprimer la stratégie.**</span><span class="sxs-lookup"><span data-stu-id="cdb72-235">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="cdb72-236">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-236">Select **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-237">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-237">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-238">Pour supprimer une stratégie d’accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-238">To delete a privileged access policy, run the following command in Exchange Online Powershell:</span></span>

```PowerShell
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="cdb72-239">Désactiver l’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-239">Disable privileged access in Office 365</span></span>

<span data-ttu-id="cdb72-240">Si nécessaire, vous pouvez désactiver la gestion des accès privilégiés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-240">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="cdb72-241">La désactivation de l’accès privilégié ne supprime pas les stratégies d’approbation ou les groupes d’approbation associés.</span><span class="sxs-lookup"><span data-stu-id="cdb72-241">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="cdb72-242">Dans le Centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cdb72-242">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="cdb72-243">Connectez-vous [au Centre d’administration Microsoft 365](https://admin.microsoft.com) avec les informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cdb72-243">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="cdb72-244">Dans le Centre d’administration, accédez à   >  **Paramètres Org Settings**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="cdb72-244">In the Admin Center, go to **Settings** > **Org Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="cdb72-245">Activez **la commande Exiger des approbations pour le contrôle d’accès** privilégié.</span><span class="sxs-lookup"><span data-stu-id="cdb72-245">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="cdb72-246">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="cdb72-246">In Exchange Management PowerShell</span></span>

<span data-ttu-id="cdb72-247">Pour désactiver l’accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="cdb72-247">To disable privileged access, run the following command in Exchange Online Powershell:</span></span>

```PowerShell
Disable-ElevatedAccessControl
```
