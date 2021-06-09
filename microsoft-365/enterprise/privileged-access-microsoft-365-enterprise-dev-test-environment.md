---
title: Gestion des accès privilégiés pour votre environnement de test Microsoft 365 entreprise
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- M365-security-compliance
ms.custom: Ent_TLGs
description: Utilisez ce guide de laboratoire de test pour activer la gestion des accès privilégiés de votre Microsoft 365 environnement de test d’entreprise.
ms.openlocfilehash: e9684ebd2aa147049dadfbda9408257ff801aff0
ms.sourcegitcommit: eac5d9f759f290d3c51cafaf335a1a1c43ded927
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "50126416"
---
# <a name="privileged-access-management-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="c80f7-103">Gestion des accès privilégiés pour votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="c80f7-103">Privileged access management for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="c80f7-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements Microsoft 365'entreprise et Office 365 Entreprise test.*</span><span class="sxs-lookup"><span data-stu-id="c80f7-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="c80f7-105">Cet article explique comment configurer la gestion des accès privilégiés pour renforcer la sécurité dans votre Microsoft 365 environnement de test d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c80f7-105">This article describes how to configure privileged access management to increase security in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="c80f7-106">La configuration de la gestion de l’accès privé implique trois phases :</span><span class="sxs-lookup"><span data-stu-id="c80f7-106">Configuring priviledged access management involves three phases:</span></span>
- [<span data-ttu-id="c80f7-107">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="c80f7-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="c80f7-108">Phase 2 : Configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="c80f7-108">Phase 2: Configure privileged access management</span></span>](#phase-2-configure-privileged-access-management)
- [<span data-ttu-id="c80f7-109">Phase 3 : Vérifier que l’approbation est requise pour les tâches avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="c80f7-109">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>](#phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="c80f7-111">Pour obtenir une carte visuelle de tous les articles de la pile Microsoft 365 guide de laboratoire de test pour entreprise, Microsoft 365 pour la pile de guides de laboratoire de [test d’entreprise.](../downloads/Microsoft365EnterpriseTLGStack.pdf)</span><span class="sxs-lookup"><span data-stu-id="c80f7-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="c80f7-112">Phase 1 : Créer votre environnement de test Microsoft 365 entreprise</span><span class="sxs-lookup"><span data-stu-id="c80f7-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="c80f7-113">Si vous souhaitez configurer la gestion des accès privilégiés de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère.](lightweight-base-configuration-microsoft-365-enterprise.md)</span><span class="sxs-lookup"><span data-stu-id="c80f7-113">If you want to configure privileged access management in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="c80f7-114">Si vous souhaitez configurer la gestion des accès privilégiés dans une entreprise simulée, suivez les instructions de [l’authentification directe.](pass-through-auth-m365-ent-test-environment.md)</span><span class="sxs-lookup"><span data-stu-id="c80f7-114">If you want to configure privileged access management in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
>[!NOTE]
><span data-ttu-id="c80f7-115">Le test de la gestion des accès privilégiés ne nécessite pas l’environnement de test d’entreprise simulée, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c80f7-115">Testing privileged access management doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services forest.</span></span> <span data-ttu-id="c80f7-116">Il est fourni ici en tant qu’option afin que vous pouvez tester la gestion des accès privilégiés et l’expérimenter dans un environnement qui représente une organisation classique.</span><span class="sxs-lookup"><span data-stu-id="c80f7-116">It's provided here as an option so that you can test privileged access management and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-configure-privileged-access-management"></a><span data-ttu-id="c80f7-117">Phase 2 : Configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="c80f7-117">Phase 2: Configure privileged access management</span></span>

<span data-ttu-id="c80f7-118">Dans cette phase, configurez un groupe d’approbations et activez la gestion des accès privilégiés pour votre Microsoft 365 environnement de test d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c80f7-118">In this phase, configure an approvers group and enable privileged access management for your Microsoft 365 for enterprise test environment.</span></span> <span data-ttu-id="c80f7-119">Pour plus d’informations et une vue d’ensemble de la gestion des accès privilégiés, voir [Privileged access management](../compliance/privileged-access-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c80f7-119">For additional details and an overview of privileged access management, see [Privileged access management](../compliance/privileged-access-management-overview.md).</span></span>

<span data-ttu-id="c80f7-120">Pour configurer et utiliser l’accès privilégié dans votre organisation, effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="c80f7-120">To set up and use privileged access in your organization, perform the following steps.</span></span>

#### <a name="step-1-create-an-approvers-group"></a>[<span data-ttu-id="c80f7-121">Étape 1 : Créer un groupe d’approbation</span><span class="sxs-lookup"><span data-stu-id="c80f7-121">Step 1: Create an approver's group</span></span>](../compliance/privileged-access-management-configuration.md#step-1-create-an-approvers-group)

<span data-ttu-id="c80f7-122">Avant de commencer à utiliser l’accès privilégié, déterminez qui aura l’autorité d’approbation pour les demandes entrantes d’accès aux tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="c80f7-122">Before you start using privileged access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="c80f7-123">Tous les utilisateurs qui font partie du groupe d’approbations peuvent approuver les demandes d’accès.</span><span class="sxs-lookup"><span data-stu-id="c80f7-123">All users who are part of the Approvers’ group can approve access requests.</span></span> <span data-ttu-id="c80f7-124">Pour utiliser l’accès privilégié, vous devez créer un groupe de sécurité à messagerie dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="c80f7-124">To use privileged access, you must create a mail-enabled security group in Microsoft 365.</span></span> <span data-ttu-id="c80f7-125">Dans votre environnement de test, nommez le nouveau groupe de sécurité « Privileged Access Approvers » et ajoutez l'« Utilisateur 3 » précédemment créé lors des étapes précédentes du guide de laboratoire de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-125">In your test environment, name the new security group "Privileged Access Approvers" and add the "User 3" that was previously created in previous test lab guide steps.</span></span>

#### <a name="step-2-enable-privileged-access"></a>[<span data-ttu-id="c80f7-126">Étape 2 : Activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="c80f7-126">Step 2: Enable privileged access</span></span>](../compliance/privileged-access-management-configuration.md#step-2-enable-privileged-access)

<span data-ttu-id="c80f7-127">L’accès privilégié doit être explicitement allumé dans Microsoft 365 avec le groupe d’approbations par défaut, et il doit inclure un ensemble de comptes système que vous souhaitez exclure du contrôle d’accès de gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="c80f7-127">Privileged access needs to be explicitly turned on in Microsoft 365 with the default approver group, and it must include a set of system accounts that you want excluded from the privileged access management access control.</span></span> <span data-ttu-id="c80f7-128">Veillez à activer l’accès privilégié dans votre organisation avant de commencer la phase 3 de ce guide.</span><span class="sxs-lookup"><span data-stu-id="c80f7-128">Be sure to enable privileged access in your organization before starting Phase 3 of this guide.</span></span>

## <a name="phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks"></a><span data-ttu-id="c80f7-129">Phase 3 : Vérifier que l’approbation est requise pour les tâches avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="c80f7-129">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>

<span data-ttu-id="c80f7-130">Dans cette phase, vérifiez que la stratégie d’accès privilégié fonctionne et que les utilisateurs ont besoin d’approbation pour exécuter des tâches définies avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="c80f7-130">In this phase, verify that the privileged access policy is working and that users require approval to execute defined elevated and privileged tasks.</span></span>

### <a name="test-the-ability-to-execute-a-task-not-defined-in-a-privileged-access-policy"></a><span data-ttu-id="c80f7-131">Tester la possibilité d’exécuter une tâche NON définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="c80f7-131">Test the ability to execute a task NOT defined in a privileged access policy</span></span>

<span data-ttu-id="c80f7-132">Tout d’abord, connectez-vous à Exchange PowerShell avec les informations d’identification d’un utilisateur configuré en tant qu’administrateur général dans votre environnement de test et essayez de créer une règle de journal.</span><span class="sxs-lookup"><span data-stu-id="c80f7-132">First, connect to Exchange Management PowerShell with the credentials of a user configured as a Global Administrator in your test environment and attempt to create a new Journal rule.</span></span> <span data-ttu-id="c80f7-133">La [tâche New-JournalRule](/powershell/module/exchange/new-journalrule) n’est actuellement pas définie dans une stratégie d’accès privilégié pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="c80f7-133">The [New-JournalRule](/powershell/module/exchange/new-journalrule) task is not currently defined in a privileged access policy for your organization.</span></span>

1. <span data-ttu-id="c80f7-134">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell de **Microsoft Corporation** Microsoft Exchange Online  >  **Remote PowerShell Module** à l’aide du compte d’administrateur global pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-134">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

1. <span data-ttu-id="c80f7-135">Dans Exchange PowerShell Gestion, créez une règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c80f7-135">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule1" -Recipient joe@contoso.onmicrosoft.com -JournalEmailAddress barbara@adatum.com -Scope Global -Enabled $true
   ```

1. <span data-ttu-id="c80f7-136">Vous voyez que la nouvelle règle de journal a été correctement créée dans Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c80f7-136">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

### <a name="create-a-new-privileged-access-policy-for-the-new-journalrule-task"></a><span data-ttu-id="c80f7-137">Créer une stratégie d’accès privilégié pour la New-JournalRule de travail</span><span class="sxs-lookup"><span data-stu-id="c80f7-137">Create a new privileged access policy for the New-JournalRule task</span></span>

>[!NOTE]
><span data-ttu-id="c80f7-138">Si vous n’avez pas déjà effectué les étapes 1 et 2 de la phase 2 de ce guide, assurez-vous de suivre les étapes pour créer un groupe d’approbation nommé « Approvers d’accès privilégié » afin d’activer l’accès privilégié dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-138">If you haven't already completed the Steps 1 and 2 from Phase 2 of this guide, be sure follow the steps to create an approver's group named "Privilege Access Approvers" to enable privileged access in your test environment.</span></span>

1. <span data-ttu-id="c80f7-139">Connectez-vous au [centre Microsoft 365'administration](https://admin.microsoft.com) à l’aide des informations d’identification du compte d’administrateur global de votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-139">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="c80f7-140">Dans le Centre d’administration, accédez **à Paramètres**  >  **sécurité & confidentialité**  >  **privilégié.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-140">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="c80f7-141">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-141">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="c80f7-142">Sélectionnez **Configurer les stratégies,** puis **ajoutez une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-142">Select **Configure policies**, and then select **Add a policy**.</span></span>

5. <span data-ttu-id="c80f7-143">Dans les champs de listes, sélectionnez ou entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c80f7-143">From the drop-down fields, select or enter the following values:</span></span>

    <span data-ttu-id="c80f7-144">**Type de stratégie**: Tâche</span><span class="sxs-lookup"><span data-stu-id="c80f7-144">**Policy type**: Task</span></span>

    <span data-ttu-id="c80f7-145">**Étendue de la stratégie** : Exchange</span><span class="sxs-lookup"><span data-stu-id="c80f7-145">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="c80f7-146">**Nom de la stratégie**: nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="c80f7-146">**Policy name**: New Journal Rule</span></span>

    <span data-ttu-id="c80f7-147">**Type d’approbation**: Manuel</span><span class="sxs-lookup"><span data-stu-id="c80f7-147">**Approval type**: Manual</span></span>

    <span data-ttu-id="c80f7-148">**Groupe d’approbation**: approbations d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="c80f7-148">**Approval group**: Privileged Access Approvers</span></span>

6. <span data-ttu-id="c80f7-149">Sélectionnez **Créer**, puis sélectionnez **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="c80f7-149">Select **Create**, and then select **Close**.</span></span> <span data-ttu-id="c80f7-150">La configuration et l’activé de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="c80f7-150">It may take a few minutes for the policy to be fully configured and enabled.</span></span> <span data-ttu-id="c80f7-151">Veillez à laisser le temps à la stratégie d’être entièrement activée avant de tester l’exigence d’approbation à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="c80f7-151">Be sure to allow time for the policy to be fully enabled before testing the approval requirement in the next step.</span></span>

### <a name="test-approval-requirement-for-the-new-journalrule-task-defined-in-a-privileged-access-policy"></a><span data-ttu-id="c80f7-152">Tester l’approbation requise pour la tâche New-JournalRule définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="c80f7-152">Test approval requirement for the New-JournalRule task defined in a privileged access policy</span></span>

1. <span data-ttu-id="c80f7-153">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell de **Microsoft Corporation** Microsoft Exchange Online  >  **Remote PowerShell Module** à l’aide d’un compte d’administrateur global pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-153">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using an using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="c80f7-154">Dans Exchange PowerShell Gestion, créez une règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c80f7-154">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
   ```

3. <span data-ttu-id="c80f7-155">Affichez l’erreur « Autorisations insuffisantes » dans Exchange PowerShell de gestion :</span><span class="sxs-lookup"><span data-stu-id="c80f7-155">View the "Insufficient permissions" error in Exchange Management PowerShell:</span></span>

   ```ExchangeManagementPowerShell
   Insufficient permissions. Please raise an elevated access request for this task.
       + CategoryInfo          : NotSpecified: (:) [], LocalizedException
       + FullyQualifiedErrorId : [Server=CY1PR00MB0220,RequestId=7b8c7470-ddd0-4528-a01e-5e20ecc9bd54,TimeStamp=9/19/2018
       7:38:34 PM] [FailureCategory=Cmdlet-LocalizedException] 882BD051
       + PSComputerName        : outlook.office365.com
   ```

### <a name="request-access-to-create-a-new-journal-rule-using-the-new-journalrule-task"></a><span data-ttu-id="c80f7-156">Demander l’accès pour créer une règle de journal à l’aide New-JournalRule tâche</span><span class="sxs-lookup"><span data-stu-id="c80f7-156">Request access to create a new Journal Rule using the New-JournalRule task</span></span>

1. <span data-ttu-id="c80f7-157">Connectez-vous au [centre Microsoft 365'administration](https://admin.microsoft.com) à l’aide du compte d’administrateur global de votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-157">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="c80f7-158">Dans le Centre d’administration, accédez **à Paramètres**  >  **sécurité & confidentialité**  >  **privilégié.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-158">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="c80f7-159">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-159">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="c80f7-160">Sélectionnez **Nouvelle requête**.</span><span class="sxs-lookup"><span data-stu-id="c80f7-160">Select **New request**.</span></span> <span data-ttu-id="c80f7-161">Dans les champs de la baisse, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c80f7-161">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="c80f7-162">**Type de requête**: Tâche</span><span class="sxs-lookup"><span data-stu-id="c80f7-162">**Request type**: Task</span></span>

    <span data-ttu-id="c80f7-163">**Étendue de la demande** : Exchange</span><span class="sxs-lookup"><span data-stu-id="c80f7-163">**Request scope**: Exchange</span></span>

    <span data-ttu-id="c80f7-164">**Demande pour**: Nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="c80f7-164">**Request for**: New Journal Rule</span></span>

    <span data-ttu-id="c80f7-165">**Durée (heures)**: 2</span><span class="sxs-lookup"><span data-stu-id="c80f7-165">**Duration (hours)**: 2</span></span>

    <span data-ttu-id="c80f7-166">**Commentaires :** Demander l’autorisation de créer une règle de journal</span><span class="sxs-lookup"><span data-stu-id="c80f7-166">**Comments**: Request permission to create a new Journal Rule</span></span>

5. <span data-ttu-id="c80f7-167">Sélectionnez **Enregistrer,** puis **Fermez.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-167">Select **Save**, and then select **Close**.</span></span> <span data-ttu-id="c80f7-168">Votre demande est envoyée au groupe de l’approuveur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="c80f7-168">Your request will be sent to the approver's group via email.</span></span>

### <a name="approve-privileged-access-request-for-the-creation-of-a-new-journal-rule"></a><span data-ttu-id="c80f7-169">Approuver une demande d’accès privilégié pour la création d’une nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="c80f7-169">Approve privileged access request for the creation of a new Journal Rule</span></span>

1. <span data-ttu-id="c80f7-170">Connectez-vous au Centre d’administration [Microsoft 365](https://admin.microsoft.com) à l’aide des informations d’identification de l’utilisateur 3 dans votre environnement de test (membre du groupe de sécurité « Privileged Access Approvers » dans votre environnement de test).</span><span class="sxs-lookup"><span data-stu-id="c80f7-170">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using the credentials for User 3 in your test environment (member of the "Privileged Access Approvers" security group in your test environment).</span></span>

2. <span data-ttu-id="c80f7-171">Dans le Centre d’administration, accédez **à Paramètres**  >  **sécurité & confidentialité**  >  **privilégié.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="c80f7-172">Sélectionnez **Gérer les stratégies et les demandes d’accès.**</span><span class="sxs-lookup"><span data-stu-id="c80f7-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="c80f7-173">Sélectionnez la demande en attente, puis **sélectionnez Approuver** pour accorder l’accès au compte d’administrateur global pour créer une règle de journal.</span><span class="sxs-lookup"><span data-stu-id="c80f7-173">Select the pending request, and then select **Approve** to grant access to the Global Admin account to create a new Journal Rule.</span></span> <span data-ttu-id="c80f7-174">Le compte d’administrateur global (l’utilisateur demandeur) reçoit une confirmation par courrier électronique pour confirmer que l’approbation a été accordée.</span><span class="sxs-lookup"><span data-stu-id="c80f7-174">The Global Admin account (the requesting user) will receive an email confirmation that approval was granted.</span></span>

### <a name="test-creating-a-new-journal-rule-with-privileged-access-approved-for-the-new-journalrule-task"></a><span data-ttu-id="c80f7-175">Tester la création d’une règle de journal avec un accès privilégié approuvé pour la New-JournalRule de journal</span><span class="sxs-lookup"><span data-stu-id="c80f7-175">Test creating a new Journal Rule with privileged access approved for the New-JournalRule task</span></span>

1. <span data-ttu-id="c80f7-176">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell de **Microsoft Corporation** Microsoft Exchange Online  >  **Remote PowerShell Module** à l’aide du compte d’administrateur global pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-176">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

1. <span data-ttu-id="c80f7-177">Dans Exchange PowerShell Gestion, créez une règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="c80f7-177">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
   ```

1. <span data-ttu-id="c80f7-178">Vous voyez que la nouvelle règle de journal a été correctement créée dans Exchange PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c80f7-178">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

## <a name="next-step"></a><span data-ttu-id="c80f7-179">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c80f7-179">Next step</span></span>

<span data-ttu-id="c80f7-180">Explorez [d’autres fonctionnalités de protection](m365-enterprise-test-lab-guides.md#information-protection) des informations dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="c80f7-180">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="c80f7-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c80f7-181">See also</span></span>

[<span data-ttu-id="c80f7-182">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="c80f7-182">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="c80f7-183">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="c80f7-183">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="c80f7-184">Documentation Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="c80f7-184">Microsoft 365 for enterprise documentation</span></span>](/microsoft-365-enterprise/)
