---
title: Utiliser le verrouillage de conservation pour restreindre les modifications apportées aux stratégies de rétention et d’étiquettes de rétention
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Priority
search.appverid:
- MOE150
- MET150
description: Utilisez un verrou de conservation avec les stratégies de rétention et les stratégies d’étiquette de conservation pour vous aider à respecter les exigences réglementaires et à vous protéger des administrateurs malveillants.
ms.openlocfilehash: 9890c73495bd14ea7264f3314f6313254ef1bf6b
ms.sourcegitcommit: a0cddd1f888edb940717e434cda2dbe62e5e9475
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "49612986"
---
# <a name="use-preservation-lock-to-restrict-changes-to-retention-policies-and-retention-label-policies"></a><span data-ttu-id="3a282-103">Utiliser le verrouillage de conservation pour restreindre les modifications apportées aux stratégies de rétention et d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="3a282-103">Use Preservation Lock to restrict changes to retention policies and retention label policies</span></span>

><span data-ttu-id="3a282-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="3a282-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="3a282-105">Le verrouillage de la conservation verrouille une stratégie de rétention ou une étiquette de rétention de sorte que personne, y compris l’administrateur général, ne puisse désactiver la stratégie, la supprimer ou la rendre moins restrictive.</span><span class="sxs-lookup"><span data-stu-id="3a282-105">Preservation Lock locks a retention policy or retention label policy so that no one—including a global admin—can turn off the policy, delete the policy, or make it less restrictive.</span></span> <span data-ttu-id="3a282-106">Cette configuration peut être nécessaire pour les exigences réglementaires et contribuer à la protection contre les administrateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="3a282-106">This configuration might be needed for regulatory requirements and can help safeguard against rogue administrators.</span></span>

<span data-ttu-id="3a282-107">Lorsqu’une stratégie de rétention est verrouillée :</span><span class="sxs-lookup"><span data-stu-id="3a282-107">When a retention policy is locked:</span></span>

- <span data-ttu-id="3a282-108">Personne ne peut désactiver ou supprimer la stratégie</span><span class="sxs-lookup"><span data-stu-id="3a282-108">No one can disable the policy or delete it</span></span>
- <span data-ttu-id="3a282-109">Vous pouvez ajouter des emplacements, mais pas les supprimer</span><span class="sxs-lookup"><span data-stu-id="3a282-109">Locations can be added but not removed</span></span>
- <span data-ttu-id="3a282-110">Vous pouvez prolonger la période de rétention, mais pas la réduire</span><span class="sxs-lookup"><span data-stu-id="3a282-110">You can extend the retention period but not decrease it</span></span>

<span data-ttu-id="3a282-111">Lorsqu’une stratégie d’étiquette de rétention est verrouillée :</span><span class="sxs-lookup"><span data-stu-id="3a282-111">When a retention label policy is locked:</span></span>

- <span data-ttu-id="3a282-112">Personne ne peut désactiver ou supprimer la stratégie</span><span class="sxs-lookup"><span data-stu-id="3a282-112">No one can disable the policy or delete it</span></span>
- <span data-ttu-id="3a282-113">Vous pouvez ajouter des emplacements, mais pas les supprimer</span><span class="sxs-lookup"><span data-stu-id="3a282-113">Locations can be added but not removed</span></span>
- <span data-ttu-id="3a282-114">Vous pouvez ajouter des étiquettes, mais pas les supprimer</span><span class="sxs-lookup"><span data-stu-id="3a282-114">Labels can be added but not removed</span></span>

<span data-ttu-id="3a282-115">En bref, vous pouvez augmenter ou prolonger une stratégie verrouillée, mais vous ne pouvez pas la réduire ou la désactiver.</span><span class="sxs-lookup"><span data-stu-id="3a282-115">In summary, a locked policy can be increased or extended, but it can't be reduced or turned off.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3a282-116">Avant de verrouiller une stratégie de rétention ou d’étiquette de rétention, il est essentiel de comprendre l’impact et de confirmer qu’il est exigé de votre organisation qu’elle respecte des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="3a282-116">Before you lock a retention policy or retention label policy, it's critical that you understand the impact and confirm whether it's required for your organization.</span></span> <span data-ttu-id="3a282-117">Par exemple, il peut être nécessaire de répondre à des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="3a282-117">For example, it might be needed to meet regulatory requirements.</span></span> <span data-ttu-id="3a282-118">Les administrateurs ne pourront pas désactiver ou supprimer ces stratégies une fois le verrouillage de conservation appliqué.</span><span class="sxs-lookup"><span data-stu-id="3a282-118">Administrators won't be able to disable or delete these policies after the preservation lock is applied.</span></span>

<span data-ttu-id="3a282-119">Configurez un verrou de conservation une fois que vous avez créé une [stratégie de rétention](create-retention-policies.md) ou une stratégie d’étiquette de rétention que vous [publiez](create-apply-retention-labels.md) ou que vous [appliquez automatiquement](apply-retention-labels-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="3a282-119">Configure Preservation Lock after you've created a [retention policy](create-retention-policies.md), or a retention label policy that you [publish](create-apply-retention-labels.md) or [auto-apply](apply-retention-labels-automatically.md).</span></span> 

> [!NOTE]
> <span data-ttu-id="3a282-120">Le verrouillage d’une stratégie d’étiquette n’empêche pas un administrateur de réduire la période de rétention dans une étiquette incluse dans la stratégie verrouillée.</span><span class="sxs-lookup"><span data-stu-id="3a282-120">Locking a label policy doesn't prevent an administrator from reducing the retention period in a label that is included in the locked policy.</span></span> <span data-ttu-id="3a282-121">Vous pouvez répondre à cette exigence, avec d’autres restrictions, lorsque vous configurez une étiquette pour marquer des éléments comme [enregistrements réglementaires](records-management.md#records).</span><span class="sxs-lookup"><span data-stu-id="3a282-121">That requirement, with other restrictions, can be met when you configure a label to mark items as a [regulatory record](records-management.md#records).</span></span>

## <a name="how-to-lock-a-retention-policy-or-retention-label-policy"></a><span data-ttu-id="3a282-122">Verrouillage d’une stratégie de rétention ou d’étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="3a282-122">How to lock a retention policy or retention label policy</span></span>

<span data-ttu-id="3a282-123">Vous devez utiliser PowerShell si vous avez besoin d’utiliser le verrouillage de conservation.</span><span class="sxs-lookup"><span data-stu-id="3a282-123">You must use PowerShell if you need to use Preservation Lock.</span></span> <span data-ttu-id="3a282-124">Les administrateurs ne pouvant pas désactiver ou supprimer une stratégie de rétention après application d’un verrouillage de conservation, l’activation de cette fonctionnalité n’est pas disponible dans l’interface utilisateur pour se protéger contre une configuration accidentelle.</span><span class="sxs-lookup"><span data-stu-id="3a282-124">Because administrators can't disable or delete a policy for retention after this lock is applied, enabling this feature is not available in the UI to safeguard against accidental configuration.</span></span>

<span data-ttu-id="3a282-125">Toutes les stratégies de rétention et de prise en charge de la configuration verrouillage de la conservation.</span><span class="sxs-lookup"><span data-stu-id="3a282-125">All policies for retention and with any configuration support Preservation Lock.</span></span>

1. <span data-ttu-id="3a282-126">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="3a282-126">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="3a282-127">Recherchez le nom de la stratégie que vous voulez verrouiller en exécutant [Get-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy).</span><span class="sxs-lookup"><span data-stu-id="3a282-127">Find the name of the policy that you want to lock by running [Get-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy).</span></span> <span data-ttu-id="3a282-128">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3a282-128">For example:</span></span>
    
   ![Liste des stratégies de rétention dans PowerShell](../media/retention-policy-preservation-lock-get-retentioncompliancepolicy.PNG)

3. <span data-ttu-id="3a282-130">Pour placer un verrou de conservation sur votre stratégie, exécutez l’applet de commande [RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) avec le nom de la stratégie et le paramètre *RestrictiveRetention* défini sur « true » :</span><span class="sxs-lookup"><span data-stu-id="3a282-130">To place a Preservation Lock on your policy, run the [Set-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) cmdlet with the name of the policy, and the *RestrictiveRetention* parameter set to true:</span></span>
    
    ```powershell
    Set-RetentionCompliancePolicy -Identity "<Name of Policy>" –RestrictiveRetention $true
    ```
    
    <span data-ttu-id="3a282-131">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3a282-131">For example:</span></span>
    
    ![Paramètre RestrictiveRetention dans PowerShell](../media/retention-policy-preservation-lock-restrictiveretention.PNG)
    
     <span data-ttu-id="3a282-133">Lorsque vous y êtes invité, lisez et accusez réception des restrictions incluses dans cette configuration en entrant **Y**:</span><span class="sxs-lookup"><span data-stu-id="3a282-133">When prompted, read and acknowledge the restrictions that come with this configuration by entering **Y**:</span></span>
    
   ![Invite à confirmer que vous souhaitez verrouiller une stratégie de rétention dans PowerShell](../media/retention-policy-preservation-lock-confirmation-prompt.PNG)

<span data-ttu-id="3a282-135">Un verrou de conservation est désormais placé sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="3a282-135">A Preservation Lock is now placed on the policy.</span></span> <span data-ttu-id="3a282-136">Pour confirmer, réexécutez `Get-RetentionCompliancePolicy` , mais indiquez le nom de la stratégie et affichez les paramètres de stratégie :</span><span class="sxs-lookup"><span data-stu-id="3a282-136">To confirm, run `Get-RetentionCompliancePolicy` again, but specify the policy name and display the policy parameters:</span></span>

```powershell
Get-RetentionCompliancePolicy -Identity "<Name of Policy>" |Fl
```

<span data-ttu-id="3a282-137">Vous devriez voir que **RestrictiveRetention** est paramétré sur **True**.</span><span class="sxs-lookup"><span data-stu-id="3a282-137">You should see **RestrictiveRetention** is set to **True**.</span></span> <span data-ttu-id="3a282-138">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="3a282-138">For example:</span></span>

![Stratégie verrouillée avec tous les paramètres affichés dans PowerShell](../media/retention-policy-preservation-lock-locked-policy.PNG)

## <a name="see-also"></a><span data-ttu-id="3a282-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a282-140">See also</span></span>

[<span data-ttu-id="3a282-141">Ressources pour vous aider à respecter les réglementations en matière de gouvernance des informations et de gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="3a282-141">Resources to help you meet regulatory requirements for information governance and records management</span></span>](retention-regulatory-requirements.md)
