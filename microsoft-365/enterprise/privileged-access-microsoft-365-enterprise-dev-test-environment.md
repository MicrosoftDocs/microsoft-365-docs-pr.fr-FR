---
title: Gestion des accès privilégiés pour votre environnement de test Microsoft 365 pour les entreprises
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
description: Utilisez ce guide de laboratoire de test pour activer la gestion des accès privilégiés pour votre environnement de test Microsoft 365 pour les entreprises.
ms.openlocfilehash: 24ca7a6408a4290c54dd2bcd7c3f6061eb8f6c05
ms.sourcegitcommit: 53ff1fe6d6143b0bf011031eea9b85dc01ae4f74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "48487587"
---
# <a name="privileged-access-management-for-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="f4d5d-103">Gestion des accès privilégiés pour votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="f4d5d-103">Privileged access management for your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="f4d5d-104">*Ce guide de laboratoire de test peut être utilisé pour les environnements de test Microsoft 365 pour les environnements de test d’entreprise et Office 365.*</span><span class="sxs-lookup"><span data-stu-id="f4d5d-104">*This Test Lab Guide can be used for both Microsoft 365 for enterprise and Office 365 Enterprise test environments.*</span></span>

<span data-ttu-id="f4d5d-105">Cet article explique comment configurer la gestion des accès privilégiés pour renforcer la sécurité dans votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-105">This article describes how to configure privileged access management to increase security in your Microsoft 365 for enterprise test environment.</span></span>

<span data-ttu-id="f4d5d-106">La configuration de la gestion des accès privilégiés comprend trois phases :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-106">Configuring priviledged access management involves three phases:</span></span>
- [<span data-ttu-id="f4d5d-107">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="f4d5d-107">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>](#phase-1-build-out-your-microsoft-365-for-enterprise-test-environment)
- [<span data-ttu-id="f4d5d-108">Phase 2 : configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="f4d5d-108">Phase 2: Configure privileged access management</span></span>](#phase-2-configure-privileged-access-management)
- [<span data-ttu-id="f4d5d-109">Phase 3 : vérifier que l’approbation est requise pour les tâches avec privilèges élevés et privilégiées</span><span class="sxs-lookup"><span data-stu-id="f4d5d-109">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>](#phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks)

![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon.png)

> [!TIP]
> <span data-ttu-id="f4d5d-111">Pour obtenir un plan de tous les Articles de la pile de guide de laboratoire de test Microsoft 365 pour Enterprise, accédez à [Microsoft 365 pour la pile de guide de laboratoire de test d’entreprise](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span><span class="sxs-lookup"><span data-stu-id="f4d5d-111">For a visual map to all the articles in the Microsoft 365 for enterprise Test Lab Guide stack, go to [Microsoft 365 for enterprise Test Lab Guide Stack](../downloads/Microsoft365EnterpriseTLGStack.pdf).</span></span>
  
## <a name="phase-1-build-out-your-microsoft-365-for-enterprise-test-environment"></a><span data-ttu-id="f4d5d-112">Phase 1 : créer votre environnement de test Microsoft 365 pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="f4d5d-112">Phase 1: Build out your Microsoft 365 for enterprise test environment</span></span>

<span data-ttu-id="f4d5d-113">Si vous souhaitez configurer la gestion des accès privilégiés de manière légère avec la configuration minimale requise, suivez les instructions de la [configuration de base légère](lightweight-base-configuration-microsoft-365-enterprise.md).</span><span class="sxs-lookup"><span data-stu-id="f4d5d-113">If you want to configure privileged access management in a lightweight way with the minimum requirements, follow the instructions in [Lightweight base configuration](lightweight-base-configuration-microsoft-365-enterprise.md).</span></span>
  
<span data-ttu-id="f4d5d-114">Si vous souhaitez configurer la gestion des accès privilégiés dans une entreprise simulée, suivez les instructions de l' [authentification directe](pass-through-auth-m365-ent-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f4d5d-114">If you want to configure privileged access management in a simulated enterprise, follow the instructions in [Pass-through authentication](pass-through-auth-m365-ent-test-environment.md).</span></span>
  
>[!NOTE]
><span data-ttu-id="f4d5d-115">Le test de la gestion des accès privilégiés ne nécessite pas l’environnement de test d’entreprise simulé, qui inclut un intranet simulé connecté à Internet et la synchronisation d’annuaires pour une forêt des services de domaine Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-115">Testing privileged access management doesn't require the simulated enterprise test environment, which includes a simulated intranet connected to the internet and directory synchronization for an Active Directory Domain Services forest.</span></span> <span data-ttu-id="f4d5d-116">Elle est fournie ici en tant qu’option qui vous permet de tester la gestion des accès privilégiés et de l’expérimenter dans un environnement qui représente une organisation type.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-116">It's provided here as an option so that you can test privileged access management and experiment with it in an environment that represents a typical organization.</span></span>

## <a name="phase-2-configure-privileged-access-management"></a><span data-ttu-id="f4d5d-117">Phase 2 : configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="f4d5d-117">Phase 2: Configure privileged access management</span></span>

<span data-ttu-id="f4d5d-118">Dans cette phase, configurez un groupe approbateurs et activez la gestion des accès privilégiés pour votre environnement de test Microsoft 365 pour les entreprises.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-118">In this phase, configure an approvers group and enable privileged access management for your Microsoft 365 for enterprise test environment.</span></span> <span data-ttu-id="f4d5d-119">Pour plus d’informations et pour obtenir une vue d’ensemble de la gestion des accès privilégiés, consultez la rubrique [gestion des accès privilégiés](../compliance/privileged-access-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f4d5d-119">For additional details and an overview of privileged access management, see [Privileged access management](../compliance/privileged-access-management-overview.md).</span></span>

<span data-ttu-id="f4d5d-120">Pour configurer et utiliser l’accès privilégié dans votre organisation, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-120">To set up and use privileged access in your organization, perform the following steps.</span></span>

#### <a name="step-1-create-an-approvers-group"></a>[<span data-ttu-id="f4d5d-121">Étape 1 : créer un groupe d’approbateurs</span><span class="sxs-lookup"><span data-stu-id="f4d5d-121">Step 1: Create an approver's group</span></span>](../compliance/privileged-access-management-configuration.md#step-1-create-an-approvers-group)

<span data-ttu-id="f4d5d-122">Avant de commencer à utiliser l’accès privilégié, déterminez qui disposera de l’autorité d’approbation pour les demandes entrantes d’accès à des tâches élevées et privilégiées.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-122">Before you start using privileged access, determine who will have approval authority for incoming requests for access to elevated and privileged tasks.</span></span> <span data-ttu-id="f4d5d-123">Tous les utilisateurs qui font partie du groupe approbateurs peuvent approuver les demandes d’accès.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-123">All users who are part of the Approvers’ group can approve access requests.</span></span> <span data-ttu-id="f4d5d-124">Pour utiliser l’accès privilégié, vous devez créer un groupe de sécurité à extension messagerie dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-124">To use privileged access, you must create a mail-enabled security group in Microsoft 365.</span></span> <span data-ttu-id="f4d5d-125">Dans votre environnement de test, nommez le nouveau groupe de sécurité « approbateurs d’accès privilégié » et ajoutez « User 3 » précédemment créé dans les étapes précédentes du Guide de laboratoire de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-125">In your test environment, name the new security group "Privileged Access Approvers" and add the "User 3" that was previously created in previous test lab guide steps.</span></span>

#### <a name="step-2-enable-privileged-access"></a>[<span data-ttu-id="f4d5d-126">Étape 2 : activer l’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="f4d5d-126">Step 2: Enable privileged access</span></span>](../compliance/privileged-access-management-configuration.md#step-2-enable-privileged-access)

<span data-ttu-id="f4d5d-127">L’accès privilégié doit être activé de manière explicite dans Microsoft 365 avec le groupe d’approbateurs par défaut, et il doit inclure un ensemble de comptes système que vous souhaitez exclure du contrôle d’accès gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-127">Privileged access needs to be explicitly turned on in Microsoft 365 with the default approver group, and it must include a set of system accounts that you want excluded from the privileged access management access control.</span></span> <span data-ttu-id="f4d5d-128">Veillez à activer l’accès privilégié dans votre organisation avant de commencer la phase 3 de ce guide.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-128">Be sure to enable privileged access in your organization before starting Phase 3 of this guide.</span></span>

## <a name="phase-3-verify-that-approval-is-required-for-elevated-and-privileged-tasks"></a><span data-ttu-id="f4d5d-129">Phase 3 : vérifier que l’approbation est requise pour les tâches avec privilèges élevés et privilégiées</span><span class="sxs-lookup"><span data-stu-id="f4d5d-129">Phase 3: Verify that approval is required for elevated and privileged tasks</span></span>

<span data-ttu-id="f4d5d-130">Dans cette phase, vérifiez que la stratégie d’accès privilégié fonctionne et que les utilisateurs ont besoin d’une approbation pour exécuter des tâches élevées et privilégiées définies.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-130">In this phase, verify that the privileged access policy is working and that users require approval to execute defined elevated and privileged tasks.</span></span>

### <a name="test-the-ability-to-execute-a-task-not-defined-in-a-privileged-access-policy"></a><span data-ttu-id="f4d5d-131">Tester la possibilité d’exécuter une tâche non définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="f4d5d-131">Test the ability to execute a task NOT defined in a privileged access policy</span></span>

<span data-ttu-id="f4d5d-132">Tout d’abord, connectez-vous à Exchange Management PowerShell avec les informations d’identification d’un utilisateur configuré en tant qu’administrateur général dans votre environnement de test et essayez de créer une nouvelle règle de journal.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-132">First, connect to Exchange Management PowerShell with the credentials of a user configured as a Global Administrator in your test environment and attempt to create a new Journal rule.</span></span> <span data-ttu-id="f4d5d-133">La tâche [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/new-journalrule) n’est actuellement pas définie dans une stratégie d’accès privilégié pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-133">The [New-JournalRule](https://docs.microsoft.com/powershell/module/exchange/new-journalrule) task is not currently defined in a privileged access policy for your organization.</span></span>

1. <span data-ttu-id="f4d5d-134">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell du **Microsoft Corporation**  >  **module Microsoft Exchange Online PowerShell** à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-134">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

1. <span data-ttu-id="f4d5d-135">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-135">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule1" -Recipient joe@contoso.onmicrosoft.com -JournalEmailAddress barbara@adatum.com -Scope Global -Enabled $true
   ```

1. <span data-ttu-id="f4d5d-136">Affichage de la création de la nouvelle règle de journal dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-136">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

### <a name="create-a-new-privileged-access-policy-for-the-new-journalrule-task"></a><span data-ttu-id="f4d5d-137">Créer une stratégie d’accès privilégié pour la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="f4d5d-137">Create a new privileged access policy for the New-JournalRule task</span></span>

>[!NOTE]
><span data-ttu-id="f4d5d-138">Si vous n’avez pas encore effectué les étapes 1 et 2 de la phase 2 de ce guide, assurez-vous de suivre les étapes nécessaires pour créer un groupe d’approbateurs nommé « approbateurs d’accès aux privilèges » afin d’activer l’accès privilégié dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-138">If you haven't already completed the Steps 1 and 2 from Phase 2 of this guide, be sure follow the steps to create an approver's group named "Privilege Access Approvers" to enable privileged access in your test environment.</span></span>

1. <span data-ttu-id="f4d5d-139">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide des informations d’identification du compte d’administrateur global pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-139">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using credentials the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="f4d5d-140">Dans le centre d’administration, accédez à **paramètres**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-140">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f4d5d-141">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-141">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f4d5d-142">Sélectionnez **configurer les stratégies**, puis **Ajouter une stratégie**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-142">Select **Configure policies**, and then select **Add a policy**.</span></span>

5. <span data-ttu-id="f4d5d-143">Dans les champs de liste déroulante, sélectionnez ou entrez les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-143">From the drop-down fields, select or enter the following values:</span></span>

    <span data-ttu-id="f4d5d-144">**Type de stratégie**: tâche</span><span class="sxs-lookup"><span data-stu-id="f4d5d-144">**Policy type**: Task</span></span>

    <span data-ttu-id="f4d5d-145">**Étendue de la stratégie** : Exchange</span><span class="sxs-lookup"><span data-stu-id="f4d5d-145">**Policy scope**: Exchange</span></span>

    <span data-ttu-id="f4d5d-146">**Nom**de la stratégie : nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="f4d5d-146">**Policy name**: New Journal Rule</span></span>

    <span data-ttu-id="f4d5d-147">**Type d’approbation**: Manuel</span><span class="sxs-lookup"><span data-stu-id="f4d5d-147">**Approval type**: Manual</span></span>

    <span data-ttu-id="f4d5d-148">**Groupe d’approbation**: approbateurs des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="f4d5d-148">**Approval group**: Privileged Access Approvers</span></span>

6. <span data-ttu-id="f4d5d-149">Sélectionnez **créer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-149">Select **Create**, and then select **Close**.</span></span> <span data-ttu-id="f4d5d-150">La configuration et l’activation de la stratégie peuvent prendre quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-150">It may take a few minutes for the policy to be fully configured and enabled.</span></span> <span data-ttu-id="f4d5d-151">Veillez à laisser le temps nécessaire pour que la stratégie soit entièrement activée avant de tester les conditions d’approbation à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-151">Be sure to allow time for the policy to be fully enabled before testing the approval requirement in the next step.</span></span>

### <a name="test-approval-requirement-for-the-new-journalrule-task-defined-in-a-privileged-access-policy"></a><span data-ttu-id="f4d5d-152">Conditions requises en matière d’approbation de test pour la tâche New-JournalRule définie dans une stratégie d’accès privilégié</span><span class="sxs-lookup"><span data-stu-id="f4d5d-152">Test approval requirement for the New-JournalRule task defined in a privileged access policy</span></span>

1. <span data-ttu-id="f4d5d-153">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell du module **Microsoft**  >  **Exchange Online PowerShell** à l’aide d’un compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-153">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using an using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="f4d5d-154">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-154">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
   ```

3. <span data-ttu-id="f4d5d-155">Affichez l’erreur « autorisations insuffisantes » dans Exchange Management PowerShell :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-155">View the "Insufficient permissions" error in Exchange Management PowerShell:</span></span>

   ```ExchangeManagementPowerShell
   Insufficient permissions. Please raise an elevated access request for this task.
       + CategoryInfo          : NotSpecified: (:) [], LocalizedException
       + FullyQualifiedErrorId : [Server=CY1PR00MB0220,RequestId=7b8c7470-ddd0-4528-a01e-5e20ecc9bd54,TimeStamp=9/19/2018
       7:38:34 PM] [FailureCategory=Cmdlet-LocalizedException] 882BD051
       + PSComputerName        : outlook.office365.com
   ```

### <a name="request-access-to-create-a-new-journal-rule-using-the-new-journalrule-task"></a><span data-ttu-id="f4d5d-156">Demander l’accès pour créer une nouvelle règle de journal à l’aide de la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="f4d5d-156">Request access to create a new Journal Rule using the New-JournalRule task</span></span>

1. <span data-ttu-id="f4d5d-157">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-157">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using the Global Admin account for your test environment.</span></span>

2. <span data-ttu-id="f4d5d-158">Dans le centre d’administration, accédez à **paramètres**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-158">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f4d5d-159">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-159">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f4d5d-160">Sélectionnez **nouvelle demande**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-160">Select **New request**.</span></span> <span data-ttu-id="f4d5d-161">Dans les champs de liste déroulante, sélectionnez les valeurs appropriées pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-161">From the drop-down fields, select the appropriate values for your organization:</span></span>

    <span data-ttu-id="f4d5d-162">**Type de demande**: tâche</span><span class="sxs-lookup"><span data-stu-id="f4d5d-162">**Request type**: Task</span></span>

    <span data-ttu-id="f4d5d-163">**Étendue de la demande** : Exchange</span><span class="sxs-lookup"><span data-stu-id="f4d5d-163">**Request scope**: Exchange</span></span>

    <span data-ttu-id="f4d5d-164">**Demande**: nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="f4d5d-164">**Request for**: New Journal Rule</span></span>

    <span data-ttu-id="f4d5d-165">**Durée (heures)**: 2</span><span class="sxs-lookup"><span data-stu-id="f4d5d-165">**Duration (hours)**: 2</span></span>

    <span data-ttu-id="f4d5d-166">**Commentaires**: demander l’autorisation de créer une nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="f4d5d-166">**Comments**: Request permission to create a new Journal Rule</span></span>

5. <span data-ttu-id="f4d5d-167">Sélectionnez **Enregistrer**, puis **Fermer**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-167">Select **Save**, and then select **Close**.</span></span> <span data-ttu-id="f4d5d-168">Votre demande sera envoyée au groupe de l’approbateur par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-168">Your request will be sent to the approver's group via email.</span></span>

### <a name="approve-privileged-access-request-for-the-creation-of-a-new-journal-rule"></a><span data-ttu-id="f4d5d-169">Approuver une demande d’accès privilégié pour la création d’une nouvelle règle de journal</span><span class="sxs-lookup"><span data-stu-id="f4d5d-169">Approve privileged access request for the creation of a new Journal Rule</span></span>

1. <span data-ttu-id="f4d5d-170">Connectez-vous au [Centre d’administration 365 de Microsoft](https://admin.microsoft.com) à l’aide des informations d’identification de l’utilisateur 3 dans votre environnement de test (membre du groupe de sécurité « approbateurs avec accès privilégié » dans votre environnement de test).</span><span class="sxs-lookup"><span data-stu-id="f4d5d-170">Sign in to the [Microsoft 365 admin center](https://admin.microsoft.com) using the credentials for User 3 in your test environment (member of the "Privileged Access Approvers" security group in your test environment).</span></span>

2. <span data-ttu-id="f4d5d-171">Dans le centre d’administration, accédez à **paramètres**  >  **Security & Privacy**  >  **Privileged Access**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-171">In the Admin Center, go to **Settings** > **Security & Privacy** > **Privileged access**.</span></span>

3. <span data-ttu-id="f4d5d-172">Sélectionnez **gérer les stratégies d’accès et les demandes**.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-172">Select **Manage access policies and requests**.</span></span>

4. <span data-ttu-id="f4d5d-173">Sélectionnez la demande en attente, puis sélectionnez **approuver** pour accorder l’accès au compte d’administrateur général afin de créer une nouvelle règle de journal.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-173">Select the pending request, and then select **Approve** to grant access to the Global Admin account to create a new Journal Rule.</span></span> <span data-ttu-id="f4d5d-174">Le compte d’administrateur global (l’utilisateur qui effectue la demande) reçoit un message confirmant que l’approbation a été accordée.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-174">The Global Admin account (the requesting user) will receive an email confirmation that approval was granted.</span></span>

### <a name="test-creating-a-new-journal-rule-with-privileged-access-approved-for-the-new-journalrule-task"></a><span data-ttu-id="f4d5d-175">Tester la création d’une nouvelle règle de journal avec un accès privilégié approuvé pour la tâche New-JournalRule</span><span class="sxs-lookup"><span data-stu-id="f4d5d-175">Test creating a new Journal Rule with privileged access approved for the New-JournalRule task</span></span>

1. <span data-ttu-id="f4d5d-176">Sur votre ordinateur local, ouvrez et connectez-vous au module Exchange Online Remote PowerShell du **Microsoft Corporation**  >  **module Microsoft Exchange Online PowerShell** à l’aide du compte d’administrateur général pour votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-176">On your local computer, open and sign in to the Exchange Online Remote PowerShell Module at **Microsoft Corporation** > **Microsoft Exchange Online Remote PowerShell Module** using the Global Admin account for your test environment.</span></span>

1. <span data-ttu-id="f4d5d-177">Dans Exchange Management PowerShell, créez une nouvelle règle de journal pour votre organisation :</span><span class="sxs-lookup"><span data-stu-id="f4d5d-177">In Exchange Management PowerShell, create a new Journal rule for your organization:</span></span>

   ```ExchangeManagementPowerShell
   New-JournalRule -Name "JournalRule2" -Recipient user1@<your subscription domain> -JournalEmailAddress user1@<your subscription domain> -Scope Global -Enabled $true
   ```

1. <span data-ttu-id="f4d5d-178">Affichage de la création de la nouvelle règle de journal dans Exchange Management PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-178">View that the new Journal Rule was successfully created in Exchange Management PowerShell.</span></span>

## <a name="next-step"></a><span data-ttu-id="f4d5d-179">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="f4d5d-179">Next step</span></span>

<span data-ttu-id="f4d5d-180">Découvrez les fonctionnalités et les fonctionnalités de [protection des informations](m365-enterprise-test-lab-guides.md#information-protection) supplémentaires dans votre environnement de test.</span><span class="sxs-lookup"><span data-stu-id="f4d5d-180">Explore additional [information protection](m365-enterprise-test-lab-guides.md#information-protection) features and capabilities in your test environment.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4d5d-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4d5d-181">See also</span></span>

[<span data-ttu-id="f4d5d-182">Microsoft 365 pour les entreprises Guides de laboratoire d'essai</span><span class="sxs-lookup"><span data-stu-id="f4d5d-182">Microsoft 365 for enterprise Test Lab Guides</span></span>](m365-enterprise-test-lab-guides.md)

[<span data-ttu-id="f4d5d-183">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="f4d5d-183">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="f4d5d-184">Documentation Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="f4d5d-184">Microsoft 365 for enterprise documentation</span></span>](https://docs.microsoft.com/microsoft-365-enterprise/)
