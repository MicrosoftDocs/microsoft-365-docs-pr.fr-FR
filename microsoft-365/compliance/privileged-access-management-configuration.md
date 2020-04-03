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
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: Utilisez cette rubrique pour en savoir plus sur la configuration de la gestion des accès privilégiés.
ms.openlocfilehash: 8c5a0a342c9cabf643bff5e20fc3b64f938c61b7
ms.sourcegitcommit: 8edad75338cf74712ca1ab5d6631b9b52ff54410
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2020
ms.locfileid: "43115990"
---
# <a name="get-started-with-privileged-access-management"></a><span data-ttu-id="b0b85-103">Prise en main de la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="b0b85-103">Get started with privileged access management</span></span>

<span data-ttu-id="b0b85-104">Cette rubrique vous guide tout au long de l’activation et de la configuration de la gestion des accès privilégiés dans votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b85-104">This topic guides you through enabling and configuring privileged access management in your Office 365 organization.</span></span> <span data-ttu-id="b0b85-105">Vous pouvez utiliser le centre d’administration Microsoft 365 ou Exchange Management PowerShell pour gérer et utiliser l’accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="b0b85-105">You can use either the Microsoft 365 Admin Center or Exchange Management PowerShell to manage and use privileged access.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="b0b85-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b0b85-106">Before you begin</span></span>

<span data-ttu-id="b0b85-107">Avant de commencer à utiliser la gestion des accès privilégiés, vous devez confirmer votre [abonnement Microsoft 365](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans) et tous les modules complémentaires.</span><span class="sxs-lookup"><span data-stu-id="b0b85-107">Before you get started with privileged access management, you should confirm your [Microsoft 365 subscription](https://www.microsoft.com/microsoft-365/compare-all-microsoft-365-plans) and any add-ons.</span></span> <span data-ttu-id="b0b85-108">Pour accéder à la gestion des accès privilégiés et l’utiliser, votre organisation doit disposer de l’un des abonnements ou des modules complémentaires suivants :</span><span class="sxs-lookup"><span data-stu-id="b0b85-108">To access and use privileged access management, your organization must have one of the following subscriptions or add-ons:</span></span>

- <span data-ttu-id="b0b85-109">Abonnement Microsoft 365 E5 (payant ou version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="b0b85-109">Microsoft 365 E5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="b0b85-110">Microsoft 365 E3 Subscription (ou Office 365 E3 subscription + Enterprise Mobility and Security E3 subscription) + The Microsoft 365 E5 Compliance Add-on</span><span class="sxs-lookup"><span data-stu-id="b0b85-110">Microsoft 365 E3 subscription (or Office 365 E3 subscription + Enterprise Mobility and Security E3 subscription) + the Microsoft 365 E5 Compliance add-on</span></span>
- <span data-ttu-id="b0b85-111">Tout abonnement Microsoft 365, Office 365, Exchange, SharePoint ou OneDrive entreprise + le module complémentaire de gestion des risques de l’Insider de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="b0b85-111">Any Microsoft 365, Office 365, Exchange, SharePoint, or OneDrive for Business subscription + the Microsoft 365 E5 Insider Risk Management add-on</span></span>  
- <span data-ttu-id="b0b85-112">Abonnement Microsoft 365 a5 (payant ou version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="b0b85-112">Microsoft 365 A5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="b0b85-113">Abonnement Microsoft 365 a3 (ou abonnement Office 365 a3 + abonnement Enterprise Mobility and Security a3) + le complément Microsoft a5 Compliance</span><span class="sxs-lookup"><span data-stu-id="b0b85-113">Microsoft 365 A3 subscription (or Office 365 A3 subscription + Enterprise Mobility and Security A3 subscription) + the Microsoft A5 Compliance add-on</span></span>
- <span data-ttu-id="b0b85-114">Tout abonnement Microsoft 365, Office 365, Exchange, SharePoint ou OneDrive éducation + le complément de gestion des risques Microsoft 365 a5 Insider</span><span class="sxs-lookup"><span data-stu-id="b0b85-114">Any Microsoft 365, Office 365, Exchange, SharePoint, or OneDrive for Education subscription + the Microsoft 365 A5 Insider Risk Management add-on</span></span>
- <span data-ttu-id="b0b85-115">Office 365 entreprise E5 abonnement (payant ou version d’évaluation)</span><span class="sxs-lookup"><span data-stu-id="b0b85-115">Office 365 Enterprise E5 subscription (paid or trial version)</span></span>
- <span data-ttu-id="b0b85-116">Office 365 entreprise E3 abonnement + le complément Office 365 Advanced Compliance (qui n’est plus disponible pour les nouveaux abonnements, reportez-vous à la rubrique note)</span><span class="sxs-lookup"><span data-stu-id="b0b85-116">Office 365 Enterprise E3 subscription + the Office 365 Advanced Compliance add-on (no longer available for new subscriptions, see note)</span></span>

<span data-ttu-id="b0b85-117">Les utilisateurs qui envoient et répondent aux demandes de gestion des accès privilégiés doivent disposer de l’une des licences ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b0b85-117">Users submitting and responding to privileged access management requests must be assigned one of the licenses above.</span></span>

>[!IMPORTANT]
><span data-ttu-id="b0b85-118">Office 365 Advanced Compliance n’est plus vendu en tant qu’abonnement autonome.</span><span class="sxs-lookup"><span data-stu-id="b0b85-118">Office 365 Advanced Compliance is no longer sold as a standalone subscription.</span></span> <span data-ttu-id="b0b85-119">Lorsque les abonnements actuels arrivent à expiration, les clients doivent effectuer une transition vers l’un des abonnements ci-dessus, qui contiennent les mêmes fonctionnalités de conformité ou des fonctionnalités de conformité supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b0b85-119">When current subscriptions expire, customers should transition to one of the subscriptions above, which contain the same or additional compliance features.</span></span>

<span data-ttu-id="b0b85-120">Si vous ne disposez pas d’un plan Microsoft 365 entreprise E5 existant et que vous souhaitez essayer la gestion des accès privilégiés, vous pouvez [Ajouter microsoft 365](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) à votre abonnement Office 365 existant ou [vous inscrire pour obtenir une version d’évaluation](https://www.microsoft.com/microsoft-365/enterprise) de Microsoft 365 entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="b0b85-120">If you don't have an existing Microsoft 365 Enterprise E5 plan and want to try privileged access management, you can [add Microsoft 365](https://docs.microsoft.com/office365/admin/try-or-buy-microsoft-365) to your existing Office 365 subscription or [sign up for a trial](https://www.microsoft.com/microsoft-365/enterprise) of Microsoft 365 Enterprise E5.</span></span>

## <a name="enable-and-configure-privileged-access-management"></a><span data-ttu-id="b0b85-121">Activer et configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="b0b85-121">Enable and configure privileged access management</span></span>

<span data-ttu-id="b0b85-122">Procédez comme suit pour configurer et utiliser l’accès privilégié dans votre organisation Office 365 :</span><span class="sxs-lookup"><span data-stu-id="b0b85-122">Follow these steps to set up and use privileged access in your Office 365 organization:</span></span>

- [<span data-ttu-id="b0b85-123">Étape 1 : créer un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="b0b85-123">Step 1: Create an approver's group</span></span>](privileged-access-management-configuration.md#step1)

    <span data-ttu-id="b0b85-124">Avant de commencer à utiliser l’accès par privilège, déterminez qui a besoin de l’autorité d’approbation pour les demandes entrantes d’accès à des tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="b0b85-124">Before you start using privilege access, determine who needs approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="b0b85-125">Tout utilisateur qui fait partie du groupe approbateurs est en mesure d’approuver les demandes d’accès.</span><span class="sxs-lookup"><span data-stu-id="b0b85-125">Any user who is part of the Approvers' group is able to approve access requests.</span></span> <span data-ttu-id="b0b85-126">Ce groupe est activé par la création d’un groupe de sécurité à extension messagerie dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b85-126">This group is enabled by creating a mail-enabled security group in Office 365.</span></span>

- [<span data-ttu-id="b0b85-127">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="b0b85-127">Step 2: Enable privileged access</span></span>](privileged-access-management-configuration.md#step2)

    <span data-ttu-id="b0b85-128">L’accès privilégié doit être explicitement activé dans Office 365 avec le groupe d’approbateurs par défaut, y compris un ensemble de comptes système que vous souhaitez exclure du contrôle d’accès gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="b0b85-128">Privileged access must be explicitly enabled in Office 365 with the default approver group, including a set of system accounts that you want excluded from the privileged access management access control.</span></span>

- [<span data-ttu-id="b0b85-129">Étape 3 : créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="b0b85-129">Step 3: Create an access policy</span></span>](privileged-access-management-configuration.md#step3)

    <span data-ttu-id="b0b85-130">La création d’une stratégie d’approbation vous permet de définir les exigences d’approbation spécifiques au niveau des tâches individuelles.</span><span class="sxs-lookup"><span data-stu-id="b0b85-130">Creating an approval policy allows you to define the specific approval requirements scoped at individual tasks.</span></span> <span data-ttu-id="b0b85-131">Les options type d’approbation sont **automatique** ou **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-131">The approval type options are **Auto** or **Manual**.</span></span>

- [<span data-ttu-id="b0b85-132">Étape 4 : soumettre/approuver des demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="b0b85-132">Step 4: Submit/approve privileged access requests</span></span>](privileged-access-management-configuration.md#step4)

    <span data-ttu-id="b0b85-133">Une fois activé, l’accès privilégié nécessite des approbations pour toutes les tâches auxquelles une stratégie d’approbation associée est définie.</span><span class="sxs-lookup"><span data-stu-id="b0b85-133">Once enabled, privileged access requires approvals for any task that has an associated approval policy defined.</span></span> <span data-ttu-id="b0b85-134">Pour les tâches comprises dans une stratégie d’approbation, les utilisateurs doivent demander une approbation d’accès et leur accorder les autorisations nécessaires pour exécuter la tâche.</span><span class="sxs-lookup"><span data-stu-id="b0b85-134">For tasks included in an approval policy, users must request and be granted access approval to have permissions necessary to execute the task.</span></span>

<span data-ttu-id="b0b85-135">Une fois que l’approbation est accordée, l’utilisateur qui a effectué la demande peut exécuter la tâche prévue et l’accès privilégié autorise et exécute la tâche au nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0b85-135">After approval is granted, the requesting user can execute the intended task and privileged access will authorize and execute the task on behalf of the user.</span></span> <span data-ttu-id="b0b85-136">L’approbation reste valide pour la durée demandée (la durée par défaut est de 4 heures), pendant laquelle le demandeur peut exécuter la tâche prévue plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="b0b85-136">The approval remains valid for the requested duration (default duration is 4 hours), during which the requester can execute the intended task multiple times.</span></span> <span data-ttu-id="b0b85-137">Toutes les exécutions de ce type sont enregistrées et mises à disposition pour l’audit de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="b0b85-137">All such executions are logged and made available for security and compliance auditing.</span></span> 

>[!NOTE]
><span data-ttu-id="b0b85-138">Si vous souhaitez utiliser Exchange Management PowerShell pour activer et configurer l’accès privilégié, suivez les étapes de la [page connexion à Exchange Online PowerShell à l’aide de l’authentification multifacteur](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) pour vous connecter à Exchange Online PowerShell avec vos informations d’identification Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b85-138">If you want to use Exchange Management PowerShell to enable and configure privileged access, follow the steps in [Connect to Exchange Online PowerShell using Multi-Factor authentication](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/mfa-connect-to-exchange-online-powershell?view=exchange-ps) to connect to Exchange Online PowerShell with your Office 365 credentials.</span></span> <span data-ttu-id="b0b85-139">Vous n’avez pas besoin d’activer l’authentification multifacteur pour votre organisation Office 365 pour utiliser les étapes d’activation de l’accès privilégié lors de la connexion à Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b0b85-139">You do not need to enable multi-factor authentication for your Office 365 organization to use the steps to enable privileged access while connecting to Exchange Online PowerShell.</span></span> <span data-ttu-id="b0b85-140">La connexion avec l’authentification multifacteur crée un jeton OAuth qui est utilisé par un accès privilégié pour signer vos demandes.</span><span class="sxs-lookup"><span data-stu-id="b0b85-140">Connecting with multi-factor authentication creates an OAuth token that is used by privileged access for signing your requests.</span></span>

<span data-ttu-id="b0b85-141"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="b0b85-141"><a name="step1"> </a></span></span>

## <a name="step-1-create-an-approvers-group"></a><span data-ttu-id="b0b85-142">Étape 1 : créer un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="b0b85-142">Step 1: Create an approver's group</span></span>

1. <span data-ttu-id="b0b85-143">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-143">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b0b85-144">Dans le centre d’administration, accédez à **groupes** > **Ajouter un groupe**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-144">In the Admin Center, go to **Groups** > **Add a group**.</span></span>

3. <span data-ttu-id="b0b85-145">Sélectionnez **groupe de sécurité à extension messagerie** , puis renseignez les champs **nom**, **adresse de messagerie du groupe**et **Description** pour le nouveau groupe.</span><span class="sxs-lookup"><span data-stu-id="b0b85-145">Select **mail-enabled security group** and then complete the **Name**, **Group email address**, and **Description** fields for the new group.</span></span>

4. <span data-ttu-id="b0b85-146">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="b0b85-146">Save the group.</span></span> <span data-ttu-id="b0b85-147">La configuration complète du groupe peut prendre quelques minutes et s’afficher dans le centre d’administration Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="b0b85-147">It may take a few minutes for the group to be fully configured and to appear in the Microsoft 365 admin center.</span></span>

5. <span data-ttu-id="b0b85-148">Sélectionnez le nouveau groupe approbateur et sélectionnez **modifier** pour ajouter des utilisateurs au groupe.</span><span class="sxs-lookup"><span data-stu-id="b0b85-148">Select the new approver's group and select **edit** to add users to the group.</span></span>

6. <span data-ttu-id="b0b85-149">Enregistrez le groupe.</span><span class="sxs-lookup"><span data-stu-id="b0b85-149">Save the group.</span></span>

<span data-ttu-id="b0b85-150"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="b0b85-150"><a name="step2"> </a></span></span>

## <a name="step-2-enable-privileged-access"></a><span data-ttu-id="b0b85-151">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="b0b85-151">Step 2: Enable privileged access</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-152">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-152">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="b0b85-153">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-153">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b0b85-154">Dans le centre d’administration, accédez à **paramètres > paramètres > sécurité & confidentialité** > des**accès privilégiés**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-154">In the Admin Center, go to **Settings > Settings > Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-155">Activez le contrôle **exiger des approbations pour les tâches privilégiées** .</span><span class="sxs-lookup"><span data-stu-id="b0b85-155">Enable the **Require approvals for privileged tasks** control.</span></span>

4. <span data-ttu-id="b0b85-156">Affectez le groupe d’approbateurs que vous avez créé à l’étape 1 comme **groupe d’approbateurs par défaut**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-156">Assign the approver's group you created in Step 1 as the **Default approvers group**.</span></span>

5. <span data-ttu-id="b0b85-157">**Enregistrer** et **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-157">**Save** and **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-158">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-158">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-159">Pour activer l’accès privilégié et attribuer le groupe de l’approbateur, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-159">To enable privileged access and to assign the approver's group, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Enable-ElevatedAccessControl -AdminGroup '<default approver group>' -SystemAccounts @('<systemAccountUPN1>','<systemAccountUPN2>')
```

<span data-ttu-id="b0b85-160">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-160">Example:</span></span>

```PowerShell
Enable-ElevatedAccessControl -AdminGroup 'pamapprovers@fabrikam.onmicrosoft.com' -SystemAccounts @('sys1@fabrikamorg.onmicrosoft.com', sys2@fabrikamorg.onmicrosoft.com')
```

>[!NOTE]
><span data-ttu-id="b0b85-161">La fonctionnalité comptes système est mise à disposition pour garantir que certaines automations au sein de vos organisations peuvent fonctionner sans dépendance sur l’accès privilégié, mais il est recommandé que ces exclusions soient exceptionnelles et que celles autorisées soient approuvées et auditées régulièrement.</span><span class="sxs-lookup"><span data-stu-id="b0b85-161">System accounts feature is made available to ensure certain automations within your organizations can work without dependency on privileged access, however it is recommended that such exclusions be exceptional and those allowed should be approved and audited regularly.</span></span>

<span data-ttu-id="b0b85-162"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="b0b85-162"><a name="step3"> </a></span></span>

## <a name="step-3-create-an-access-policy"></a><span data-ttu-id="b0b85-163">Étape 3 : créer une stratégie d’accès</span><span class="sxs-lookup"><span data-stu-id="b0b85-163">Step 3: Create an access policy</span></span>

<span data-ttu-id="b0b85-164">Vous pouvez créer et configurer jusqu’à 30 stratégies d’accès privilégié pour votre organisation Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0b85-164">You can create and configure up to 30 privileged access policies for your Office 365 organization.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-165">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-165">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="b0b85-166">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-166">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b0b85-167">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-167">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-168">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-168">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="b0b85-169">Sélectionnez **configurer les stratégies** et sélectionnez **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-169">Select **Configure policies** and select **Add a policy**.</span></span>

5. <span data-ttu-id="b0b85-170">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="b0b85-170">From the drop-down fields, select the appropriate values for your organization:</span></span>
    
    <span data-ttu-id="b0b85-171">**Type de stratégie**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="b0b85-171">**Policy type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="b0b85-172">**Étendue de stratégie**: Exchange</span><span class="sxs-lookup"><span data-stu-id="b0b85-172">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="b0b85-173">**Nom**de la stratégie : sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="b0b85-173">**Policy name**: Select from the available policies</span></span>

    <span data-ttu-id="b0b85-174">**Type d’approbation**: manuelle ou automatique</span><span class="sxs-lookup"><span data-stu-id="b0b85-174">**Approval type**: Manual or Auto</span></span>

    <span data-ttu-id="b0b85-175">**Groupe d’approbation**: sélectionnez le groupe approbateurs créé à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="b0b85-175">**Approval group**: Select the approvers group created in Step 1</span></span>

6. <span data-ttu-id="b0b85-176">Sélectionnez **créer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-176">Select **Create** and then **Close**.</span></span> <span data-ttu-id="b0b85-177">La configuration et l’activation de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="b0b85-177">It may take a few minutes for the policy to be fully configured and enabled.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-178">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-178">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-179">Pour créer et définir une stratégie d’approbation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-179">To create and define an approval policy, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
New-ElevatedAccessApprovalPolicy -Task 'Exchange\<exchange management cmdlet name>' -ApprovalType <Manual, Auto> -ApproverGroup '<default/custom approver group>'
```

<span data-ttu-id="b0b85-180">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-180">Example:</span></span>

```PowerShell
New-ElevatedAccessApprovalPolicy -Task 'Exchange\New-MoveRequest' -ApprovalType Manual -ApproverGroup 'mbmanagers@fabrikamorg.onmicrosoft.com'
```

<span data-ttu-id="b0b85-181"><a name="step4"> </a></span><span class="sxs-lookup"><span data-stu-id="b0b85-181"><a name="step4"> </a></span></span>

## <a name="step-4-submitapprove-privileged-access-requests"></a><span data-ttu-id="b0b85-182">Étape 4 : soumettre/approuver des demandes d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="b0b85-182">Step 4: Submit/approve privileged access requests</span></span>

### <a name="requesting-elevation-authorization-to-execute-privileged-tasks"></a><span data-ttu-id="b0b85-183">Demande d’une autorisation d’élévation pour exécuter des tâches privilégiées</span><span class="sxs-lookup"><span data-stu-id="b0b85-183">Requesting elevation authorization to execute privileged tasks</span></span>

<span data-ttu-id="b0b85-184">Les demandes d’accès privilégié sont valides jusqu’à 24 heures après l’envoi de la demande.</span><span class="sxs-lookup"><span data-stu-id="b0b85-184">Requests for privileged access are valid for up to 24 hours after the request is submitted.</span></span> <span data-ttu-id="b0b85-185">Si elles ne sont pas approuvées ou refusées, les demandes expirent et l’accès n’est pas approuvé.</span><span class="sxs-lookup"><span data-stu-id="b0b85-185">If not approved or denied, the requests expire and access is not approved.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-186">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-186">In the Microsoft 365 Admin Center</span></span>

1. <span data-ttu-id="b0b85-187">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide de vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="b0b85-187">Sign into the [Microsoft 365 Admin Center](https://admin.microsoft.com) using your credentials.</span></span>

2. <span data-ttu-id="b0b85-188">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-188">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-189">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-189">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="b0b85-190">Sélectionnez **nouvelle demande**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-190">Select **New request**.</span></span> <span data-ttu-id="b0b85-191">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="b0b85-191">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="b0b85-192">**Type de demande**: tâche, rôle ou groupe de rôles</span><span class="sxs-lookup"><span data-stu-id="b0b85-192">**Request type**: Task, Role, or Role Group</span></span>

    <span data-ttu-id="b0b85-193">**Étendue**de la demande : Exchange</span><span class="sxs-lookup"><span data-stu-id="b0b85-193">**Request scope**: Exchange</span></span>

    <span data-ttu-id="b0b85-194">**Demande**: sélectionnez parmi les stratégies disponibles.</span><span class="sxs-lookup"><span data-stu-id="b0b85-194">**Request for**: Select from the available policies</span></span>

    <span data-ttu-id="b0b85-195">**Durée (heures)**: nombre d’heures d’accès demandé.</span><span class="sxs-lookup"><span data-stu-id="b0b85-195">**Duration (hours)**: Number of hours of requested access.</span></span> <span data-ttu-id="b0b85-196">Il n’y a pas de limite sur le nombre d’heures qui peuvent être demandées.</span><span class="sxs-lookup"><span data-stu-id="b0b85-196">There isn't a limit on the number of hours that can be requested.</span></span>

    <span data-ttu-id="b0b85-197">**Commentaires**: champ de texte pour les commentaires liés à votre demande d’accès</span><span class="sxs-lookup"><span data-stu-id="b0b85-197">**Comments**: Text field for comments related to your access request</span></span>

5. <span data-ttu-id="b0b85-198">Sélectionnez **Enregistrer** , puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-198">Select **Save** and then **Close**.</span></span> <span data-ttu-id="b0b85-199">Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="b0b85-199">Your request will be sent to the approver's group via email.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-200">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-200">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-201">Exécutez la commande suivante dans Exchange Online PowerShell pour créer et soumettre une demande d’approbation au groupe de l’approbateur :</span><span class="sxs-lookup"><span data-stu-id="b0b85-201">Run the following command in Exchange Online PowerShell to create and submit an approval request to the approver's group:</span></span>

```PowerShell
New-ElevatedAccessRequest -Task 'Exchange\<exchange management cmdlet name>' -Reason '<appropriate reason>' -DurationHours <duration in hours>
```

<span data-ttu-id="b0b85-202">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-202">Example:</span></span>

```PowerShell
New-ElevatedAccessRequest -Task 'Exchange\New-MoveRequest' -Reason 'Attempting to fix the user mailbox error' -DurationHours 4
```

### <a name="view-status-of-elevation-requests"></a><span data-ttu-id="b0b85-203">Afficher l’état des demandes d’élévation</span><span class="sxs-lookup"><span data-stu-id="b0b85-203">View status of elevation requests</span></span>

<span data-ttu-id="b0b85-204">Après la création d’une demande d’approbation, l’état de la demande d’élévation peut être révisé dans le centre d’administration ou dans Exchange Management PowerShell à l’aide de l’ID de demande associé.</span><span class="sxs-lookup"><span data-stu-id="b0b85-204">After an approval request is created, elevation request status can be reviewed in the admin center or in Exchange Management PowerShell using the associated with request ID.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-205">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-205">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="b0b85-206">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="b0b85-206">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="b0b85-207">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-207">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-208">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-208">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="b0b85-209">Sélectionnez **affichage** pour filtrer les demandes soumises par état **en attente**, **approuvé**, **refusé**ou **référentiel sécurisé du client** .</span><span class="sxs-lookup"><span data-stu-id="b0b85-209">Select **View** to filter submitted requests by **Pending**, **Approved**, **Denied**, or **Customer Lockbox** status.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-210">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-210">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-211">Exécutez la commande suivante dans Exchange Online PowerShell pour afficher l’état d’une demande d’approbation pour un ID de demande spécifique :</span><span class="sxs-lookup"><span data-stu-id="b0b85-211">Run the following command in Exchange Online PowerShell to view an approval request status for a specific request ID:</span></span>

```PowerShell
Get-ElevatedAccessRequest -Identity <request ID> | select RequestStatus
```

<span data-ttu-id="b0b85-212">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-212">Example:</span></span>

```PowerShell
Get-ElevatedAccessRequest -Identity 28560ed0-419d-4cc3-8f5b-603911cbd450 | select RequestStatus
```

### <a name="approving-an-elevation-authorization-request"></a><span data-ttu-id="b0b85-213">Approbation d’une demande d’autorisation d’élévation</span><span class="sxs-lookup"><span data-stu-id="b0b85-213">Approving an elevation authorization request</span></span>

<span data-ttu-id="b0b85-214">Lorsqu’une demande d’approbation est créée, les membres du groupe d’approbateur approprié reçoivent une notification par courrier électronique et peuvent approuver la demande associée à l’ID de demande.</span><span class="sxs-lookup"><span data-stu-id="b0b85-214">When an approval request is created, members of the relevant approver group receive an email notification and can approve the request associated with the request ID.</span></span> <span data-ttu-id="b0b85-215">Le demandeur est informé de la demande d’approbation ou de refus via un message électronique.</span><span class="sxs-lookup"><span data-stu-id="b0b85-215">The requestor is notified of the request approval or denial via email message.</span></span>

#### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-216">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-216">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="b0b85-217">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) avec vos informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="b0b85-217">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with your credentials.</span></span>

2. <span data-ttu-id="b0b85-218">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-218">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-219">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-219">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="b0b85-220">Sélectionnez une demande répertoriée pour afficher les détails et agir sur la demande.</span><span class="sxs-lookup"><span data-stu-id="b0b85-220">Select a listed request to view the details and to take action on the request.</span></span>

5. <span data-ttu-id="b0b85-221">Sélectionnez **approuver** pour approuver la demande ou **refuser** pour la refuser.</span><span class="sxs-lookup"><span data-stu-id="b0b85-221">Select **Approve** to approve the request or select **Deny** to deny the request.</span></span> <span data-ttu-id="b0b85-222">Les demandes précédemment approuvées peuvent avoir un accès révoqué en sélectionnant **Revoke**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-222">Previously approved requests can have access revoked by selecting **Revoke**.</span></span>

#### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-223">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-223">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-224">Pour approuver une demande d’autorisation d’élévation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-224">To approve an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Approve-ElevatedAccessRequest -RequestId <request id> -Comment '<approval comment>'
```

<span data-ttu-id="b0b85-225">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-225">Example:</span></span>

```PowerShell
Approve-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<approval comment>'
```

<span data-ttu-id="b0b85-226">Pour refuser une demande d’autorisation d’élévation, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-226">To deny an elevation authorization request, run the following command in Exchange Online PowerShell:</span></span>

```PowerShell
Deny-ElevatedAccessRequest -RequestId <request id> -Comment '<denial comment>'
```

<span data-ttu-id="b0b85-227">Exemple :</span><span class="sxs-lookup"><span data-stu-id="b0b85-227">Example:</span></span>

```PowerShell
Deny-ElevatedAccessRequest -RequestId a4bc1bdf-00a1-42b4-be65-b6c63d6be279 -Comment '<denial comment>'
```

## <a name="delete-a-privileged-access-policy-in-office-365"></a><span data-ttu-id="b0b85-228">Supprimer une stratégie d’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-228">Delete a privileged access policy in Office 365</span></span>

<span data-ttu-id="b0b85-229">Si elle n’est plus nécessaire dans votre organisation, vous pouvez supprimer une stratégie d’accès privilégié.</span><span class="sxs-lookup"><span data-stu-id="b0b85-229">If it is no longer needed in your organization, you can delete a privileged access policy.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-230">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-230">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="b0b85-231">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification d’un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-231">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b0b85-232">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-232">In the admin center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-233">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-233">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="b0b85-234">Sélectionnez **configurer les stratégies**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-234">Select **Configure policies**.</span></span>

5. <span data-ttu-id="b0b85-235">Sélectionnez la stratégie à supprimer, puis **Supprimer la stratégie**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-235">Select the policy you want to delete, then select **Remove Policy**.</span></span>

6. <span data-ttu-id="b0b85-236">Sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-236">Select **Close**.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-237">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-237">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-238">Pour supprimer une stratégie d’accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-238">To delete a privileged access policy, run the following command in Exchange Online Powershell:</span></span>

```PowerShell
Remove-ElevatedAccessApprovalPolicy -Identity <identity GUID of the policy you want to delete>
```

## <a name="disable-privileged-access-in-office-365"></a><span data-ttu-id="b0b85-239">Désactivation de l’accès privilégié dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-239">Disable privileged access in Office 365</span></span>

<span data-ttu-id="b0b85-240">Si nécessaire, vous pouvez désactiver la gestion des accès privilégiés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-240">If needed, you can disable privileged access management for your organization.</span></span> <span data-ttu-id="b0b85-241">La désactivation de l’accès privilégié ne supprime pas les stratégies d’approbation ou les groupes d’approbateurs associés.</span><span class="sxs-lookup"><span data-stu-id="b0b85-241">Disabling privileged access does not delete any associated approval policies or approver groups.</span></span>

### <a name="in-the-microsoft-365-admin-center"></a><span data-ttu-id="b0b85-242">Dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="b0b85-242">In the Microsoft 365 admin center</span></span>

1. <span data-ttu-id="b0b85-243">Connectez-vous au [Centre d’administration Microsoft 365](https://admin.microsoft.com) avec des informations d’identification pour un compte d’administrateur de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b0b85-243">Sign into the [Microsoft 365 admin center](https://admin.microsoft.com) with credentials for an admin account in your organization.</span></span>

2. <span data-ttu-id="b0b85-244">Dans le centre d’administration, accédez à **paramètres** > **Security & Privacy** > **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="b0b85-244">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="b0b85-245">Activez l' **autorisation exiger des approbations pour le contrôle d’accès privilégié** .</span><span class="sxs-lookup"><span data-stu-id="b0b85-245">Enable the **Require approvals for privileged access** control.</span></span>

### <a name="in-exchange-management-powershell"></a><span data-ttu-id="b0b85-246">Dans Exchange Management PowerShell</span><span class="sxs-lookup"><span data-stu-id="b0b85-246">In Exchange Management PowerShell</span></span>

<span data-ttu-id="b0b85-247">Pour désactiver l’accès privilégié, exécutez la commande suivante dans Exchange Online PowerShell :</span><span class="sxs-lookup"><span data-stu-id="b0b85-247">To disable privileged access, run the following command in Exchange Online Powershell:</span></span>

```PowerShell
Disable-ElevatedAccessControl
```
