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
ms.openlocfilehash: 6f6cfc5bef9b93af08fcc9b703b29facb9a7c576
ms.sourcegitcommit: d7975c391e03eeb96e29c1d02e77d2a1433ea67c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "48920698"
---
# <a name="use-preservation-lock-to-restrict-changes-to-retention-policies-and-retention-label-policies"></a><span data-ttu-id="72dc4-103">Utiliser le verrouillage de conservation pour restreindre les modifications apportées aux stratégies de rétention et d’étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="72dc4-103">Use Preservation Lock to restrict changes to retention policies and retention label policies</span></span>

><span data-ttu-id="72dc4-104">*[Guide de sécurité et conformité pour les licences Microsoft 365](https://aka.ms/ComplianceSD).*</span><span class="sxs-lookup"><span data-stu-id="72dc4-104">*[Microsoft 365 licensing guidance for security & compliance](https://aka.ms/ComplianceSD).*</span></span>

<span data-ttu-id="72dc4-105">Le verrouillage de la conservation verrouille une stratégie de rétention ou une étiquette de rétention de sorte que personne, y compris l’administrateur général, ne puisse désactiver la stratégie, la supprimer ou la rendre moins restrictive.</span><span class="sxs-lookup"><span data-stu-id="72dc4-105">Preservation Lock locks a retention policy or retention label policy so that no one—including a global admin—can turn off the policy, delete the policy, or make it less restrictive.</span></span> <span data-ttu-id="72dc4-106">Cette configuration peut être nécessaire pour les exigences réglementaires et contribuer à la protection contre les administrateurs malveillants.</span><span class="sxs-lookup"><span data-stu-id="72dc4-106">This configuration might be needed for regulatory requirements and can help safeguard against rogue administrators.</span></span>

<span data-ttu-id="72dc4-107">Lorsqu’une stratégie de rétention est verrouillée :</span><span class="sxs-lookup"><span data-stu-id="72dc4-107">When a policy for retention is locked:</span></span>

- <span data-ttu-id="72dc4-108">Personne ne peut la désactiver</span><span class="sxs-lookup"><span data-stu-id="72dc4-108">No one can turn it off</span></span>
- <span data-ttu-id="72dc4-109">Vous pouvez ajouter des emplacements, mais pas les supprimer</span><span class="sxs-lookup"><span data-stu-id="72dc4-109">Locations can be added but not removed</span></span>
- <span data-ttu-id="72dc4-110">Vous pouvez prolonger une période de rétention, mais pas la réduire</span><span class="sxs-lookup"><span data-stu-id="72dc4-110">You can extend a retention period but not decrease it</span></span>

<span data-ttu-id="72dc4-111">En bref, une stratégie verrouillée peut être augmentée ou prolongée, mais elle ne peut pas être réduite ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="72dc4-111">In summary, a locked policy can be increased or extended, but it can't be reduced or turned off.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="72dc4-112">Avant de verrouiller une stratégie de rétention ou d’étiquette de rétention, il est essentiel de comprendre l’impact et de confirmer qu’il est exigé de votre organisation qu’elle respecte des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="72dc4-112">Before you lock a retention policy or retention label policy, it's critical that you understand the impact and confirm whether it's required for your organization.</span></span> <span data-ttu-id="72dc4-113">Par exemple, il peut être nécessaire de répondre à des exigences réglementaires.</span><span class="sxs-lookup"><span data-stu-id="72dc4-113">For example, it might be needed to meet regulatory requirements.</span></span> <span data-ttu-id="72dc4-114">Les administrateurs ne pourront pas désactiver ou supprimer ces stratégies une fois le verrouillage de conservation appliqué.</span><span class="sxs-lookup"><span data-stu-id="72dc4-114">Administrators won't be able to disable or delete these policies after the preservation lock is applied.</span></span>

<span data-ttu-id="72dc4-115">Configurez un verrou de conservation une fois que vous avez créé une [stratégie de rétention](create-retention-policies.md) ou une stratégie d’étiquette de rétention que vous [publiez](create-apply-retention-labels.md) ou que vous [appliquez automatiquement](apply-retention-labels-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="72dc4-115">Configure Preservation Lock after you've created a [retention policy](create-retention-policies.md), or a retention label policy that you [publish](create-apply-retention-labels.md) or [auto-apply](apply-retention-labels-automatically.md).</span></span> 

## <a name="how-to-lock-a-retention-policy-or-retention-label-policy"></a><span data-ttu-id="72dc4-116">Verrouillage d’une stratégie de rétention ou d’étiquette de rétention</span><span class="sxs-lookup"><span data-stu-id="72dc4-116">How to lock a retention policy or retention label policy</span></span>

<span data-ttu-id="72dc4-117">Vous devez utiliser PowerShell si vous avez besoin d’utiliser le verrouillage de conservation.</span><span class="sxs-lookup"><span data-stu-id="72dc4-117">You must use PowerShell if you need to use Preservation Lock.</span></span> <span data-ttu-id="72dc4-118">Les administrateurs ne pouvant pas désactiver ou supprimer une stratégie de rétention après application d’un verrouillage de conservation, l’activation de cette fonctionnalité n’est pas disponible dans l’interface utilisateur pour se protéger contre une configuration accidentelle.</span><span class="sxs-lookup"><span data-stu-id="72dc4-118">Because administrators can't disable or delete a policy for retention after this lock is applied, enabling this feature is not available in the UI to safeguard against accidental configuration.</span></span>

<span data-ttu-id="72dc4-119">Toutes les stratégies de rétention et de prise en charge de la configuration verrouillage de la conservation.</span><span class="sxs-lookup"><span data-stu-id="72dc4-119">All policies for retention and with any configuration support Preservation Lock.</span></span>

1. <span data-ttu-id="72dc4-120">[Se connecter à l’interface PowerShell du Centre de sécurité et conformité](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="72dc4-120">[Connect to Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/connect-to-scc-powershell).</span></span>

2. <span data-ttu-id="72dc4-121">Recherchez le nom de la stratégie que vous voulez verrouiller en exécutant [Get-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy).</span><span class="sxs-lookup"><span data-stu-id="72dc4-121">Find the name of the policy that you want to lock by running [Get-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/get-retentioncompliancepolicy).</span></span> <span data-ttu-id="72dc4-122">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="72dc4-122">For example:</span></span>
    
   ![Liste des stratégies de rétention dans PowerShell](../media/retention-policy-preservation-lock-get-retentioncompliancepolicy.PNG)

3. <span data-ttu-id="72dc4-124">Pour placer un verrou de conservation sur votre stratégie, exécutez l’applet de commande [RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) avec le nom de la stratégie et le paramètre *RestrictiveRetention* défini sur « true » :</span><span class="sxs-lookup"><span data-stu-id="72dc4-124">To place a Preservation Lock on your policy, run the [Set-RetentionCompliancePolicy](https://docs.microsoft.com/powershell/module/exchange/set-retentioncompliancepolicy) cmdlet with the name of the policy, and the *RestrictiveRetention* parameter set to true:</span></span>
    
    ```powershell
    Set-RetentionCompliancePolicy -Identity "<Name of Policy>" –RestrictiveRetention $true
    ```
    
    <span data-ttu-id="72dc4-125">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="72dc4-125">For example:</span></span>
    
    ![Paramètre RestrictiveRetention dans PowerShell](../media/retention-policy-preservation-lock-restrictiveretention.PNG)
    
     <span data-ttu-id="72dc4-127">Lorsque vous y êtes invité, lisez et accusez réception des restrictions incluses dans cette configuration en entrant **Y** :</span><span class="sxs-lookup"><span data-stu-id="72dc4-127">When prompted, read and acknowledge the restrictions that come with this configuration by entering **Y** :</span></span>
    
   ![Invite à confirmer que vous souhaitez verrouiller une stratégie de rétention dans PowerShell](../media/retention-policy-preservation-lock-confirmation-prompt.PNG)

<span data-ttu-id="72dc4-129">Un verrou de conservation est désormais placé sur la stratégie.</span><span class="sxs-lookup"><span data-stu-id="72dc4-129">A Preservation Lock is now placed on the policy.</span></span> <span data-ttu-id="72dc4-130">Pour confirmer, réexécutez `Get-RetentionCompliancePolicy` , mais indiquez le nom de la stratégie et affichez les paramètres de stratégie :</span><span class="sxs-lookup"><span data-stu-id="72dc4-130">To confirm, run `Get-RetentionCompliancePolicy` again, but specify the policy name and display the policy parameters:</span></span>

```powershell
Get-RetentionCompliancePolicy -Identity "<Name of Policy>" |Fl
```

<span data-ttu-id="72dc4-131">Vous devriez voir que **RestrictiveRetention** est paramétré sur **True**.</span><span class="sxs-lookup"><span data-stu-id="72dc4-131">You should see **RestrictiveRetention** is set to **True**.</span></span> <span data-ttu-id="72dc4-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="72dc4-132">For example:</span></span>

![Stratégie verrouillée avec tous les paramètres affichés dans PowerShell](../media/retention-policy-preservation-lock-locked-policy.PNG)

## <a name="see-also"></a><span data-ttu-id="72dc4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72dc4-134">See also</span></span>

[<span data-ttu-id="72dc4-135">Ressources pour vous aider à respecter les réglementations en matière de gouvernance des informations et de gestion des enregistrements</span><span class="sxs-lookup"><span data-stu-id="72dc4-135">Resources to help you meet regulatory requirements for information governance and records management</span></span>](retention-regulatory-requirements.md)
