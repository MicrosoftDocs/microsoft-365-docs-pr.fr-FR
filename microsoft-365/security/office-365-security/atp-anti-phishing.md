---
title: Fonctionnalités anti-hameçonnage ATP dans Office 365
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 5076d0f6-7a59-4d6c-bd07-ba95033f0682
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Découvrez les fonctionnalités anti-hameçonnage qui font partie de la protection avancée contre les menaces d’Office 365 pour assurer la protection contre les attaques par hameçonnage & de la sonde.
ms.openlocfilehash: dda94145dfbef7466ebd8e1fb9f01d592515f598
ms.sourcegitcommit: 5e8901e7e571f20ede04f460bd3e7077dda004ca
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/25/2020
ms.locfileid: "44875416"
---
# <a name="atp-anti-phishing-capabilities-in-office-365"></a><span data-ttu-id="32b34-103">Fonctionnalités anti-hameçonnage ATP dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-103">ATP anti-phishing capabilities in Office 365</span></span>

<span data-ttu-id="32b34-104">La protection anti-hameçonnage ATP fait partie de la [protection avancée contre les menaces d’Office 365](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="32b34-104">ATP anti-phishing is part of [Office 365 Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="32b34-105">La fonctionnalité anti-hameçonnage de PACM applique un ensemble de modèles d’apprentissage automatique, ainsi que des algorithmes de détection d’emprunt d’identité aux messages entrants pour offrir une protection contre les attaques par hameçonnage et harponnage.</span><span class="sxs-lookup"><span data-stu-id="32b34-105">ATP anti-phishing applies a set of machine learning models together with impersonation detection algorithms to incoming messages to provide protection for commodity and spear phishing attacks.</span></span> <span data-ttu-id="32b34-106">Tous les messages sont soumis à un ensemble complet de modèles d’apprentissage automatique formés pour détecter les messages de hameçonnage, ainsi qu’un ensemble d’algorithmes avancés permettant de se protéger contre diverses attaques par emprunt d’identité d’utilisateur et de domaine.</span><span class="sxs-lookup"><span data-stu-id="32b34-106">All messages are subject to an extensive set of machine learning models trained to detect phishing messages, together with a set of advanced algorithms used to protect against various user and domain impersonation attacks.</span></span> <span data-ttu-id="32b34-107">La protection anti-hameçonnage ATP protège votre organisation en fonction des stratégies définies par vos administrateurs Office 365 global ou de sécurité.</span><span class="sxs-lookup"><span data-stu-id="32b34-107">ATP anti-phishing protects your organization according to polices that are set by your Office 365 global or security administrators.</span></span>
  
<span data-ttu-id="32b34-108">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="32b34-108">To learn more, see [Set up anti-phishing policies in Office 365](set-up-anti-phishing-policies.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="32b34-109">La protection contre le hameçonnage (ATP) est disponible uniquement dans la protection avancée contre les menaces, qui est incluse dans les abonnements, tels que [microsoft 365 entreprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 entreprise E5, Office 365 éducation a5, etc. Si votre organisation dispose d’un abonnement Office 365 qui n’inclut pas Office 365 ATP, vous pouvez acheter l’ATP en tant que module complémentaire.</span><span class="sxs-lookup"><span data-stu-id="32b34-109">ATP anti-phishing is only available in Advanced Threat Protection, which is included in subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has an Office 365 subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="32b34-110">Pour plus d’informations, consultez la rubrique [offres et tarifs de protection avancée contre les menaces office 365](https://products.office.com/exchange/advance-threat-protection) , ainsi que la [Description du service Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="32b34-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>

## <a name="how-atp-anti-phishing-works"></a><span data-ttu-id="32b34-111">Fonctionnement de la protection anti-hameçonnage ATP</span><span class="sxs-lookup"><span data-stu-id="32b34-111">How ATP anti-phishing works</span></span>

<span data-ttu-id="32b34-112">La protection contre le hameçonnage (ATP) vérifie les messages entrants pour les indicateurs que le message peut être un hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="32b34-112">ATP anti-phishing checks incoming messages for indicators that the message may be phishing.</span></span> <span data-ttu-id="32b34-113">Chaque fois qu’un utilisateur est couvert par une stratégie de protection avancée contre les menaces (pièces jointes fiables, liens fiables ou anti-hameçonnage), le message entrant est évalué par plusieurs modèles d’apprentissage automatique qui analysent le message afin de déterminer si la stratégie s’applique au message et si l’action appropriée est effectuée, en fonction de la stratégie configurée.</span><span class="sxs-lookup"><span data-stu-id="32b34-113">Whenever a user is covered by an ATP policy (safe attachments, safe links or anti-phishing) the incoming message is evaluated by multiple machine learning models that analyze the message to determine if the policy applies to the message and the appropriate action is taken, based on the configured policy.</span></span>
  
<span data-ttu-id="32b34-114">La protection contre le hameçonnage (ATP) permet aux administrateurs globaux d’Office 365 ou aux administrateurs de sécurité de définir des stratégies qui fournissent une protection contre les attaques par hameçonnage qui incluent l’emprunt d’identité des utilisateurs ou des domaines.</span><span class="sxs-lookup"><span data-stu-id="32b34-114">ATP anti-phishing allows Office 365 global administrators or security admins to define policies that provide protection against phishing attacks that include impersonation of either users or domains.</span></span> <span data-ttu-id="32b34-115">(ou les deux).</span><span class="sxs-lookup"><span data-stu-id="32b34-115">(or both).</span></span> <span data-ttu-id="32b34-116">Les administrateurs globaux d’Office 365 ou les administrateurs de sécurité définissent, dans la stratégie, les utilisateurs et les domaines qui doivent être protégés contre les attaques par emprunt d’identité en utilisant une liste fixe d’utilisateurs ou de domaines ou en utilisant l’intelligence des boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="32b34-116">Office 365 global administrators or security admins define within the policy which user and domains should be protected from impersonation attacks using either a fixed list of users or domains or by using mailbox intelligence.</span></span> <span data-ttu-id="32b34-117">La boîte aux lettres est une compréhension approfondie des habitudes de messagerie et des contacts personnels d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32b34-117">Mailbox intelligence is an advanced understanding of a user's email habits and personal contacts.</span></span> <span data-ttu-id="32b34-118">La fonctionnalité ATP apprend comment chaque utilisateur individuel communique avec d’autres utilisateurs à l’intérieur et à l’extérieur de l’organisation et crée un plan de ces relations.</span><span class="sxs-lookup"><span data-stu-id="32b34-118">ATP learns how each individual user communicates with other users inside and outside the organization and builds up a map of these relationships.</span></span> <span data-ttu-id="32b34-119">Cette carte permet à l’ATP de comprendre plus de détails sur la façon de s’assurer que les messages corrects sont identifiés comme emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="32b34-119">This map allows ATP to understand more details about how to ensure the right messages are identified as impersonation.</span></span>
  
<span data-ttu-id="32b34-120">Les stratégies anti-hameçonnage ATP peuvent être appliquées à un ensemble spécifique de personnes ou de groupes dans votre organisation, ou à un domaine entier ou à tous vos domaines personnalisés.</span><span class="sxs-lookup"><span data-stu-id="32b34-120">ATP anti-phishing polices can be applied to a specific set of people or groups in your organization, or to an entire domain or all of your custom domains.</span></span> <span data-ttu-id="32b34-121">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="32b34-121">To learn more, see [Set up anti-phishing policies in Office 365](set-up-anti-phishing-policies.md).</span></span>
  
## <a name="how-to-get-atp-anti-phishing"></a><span data-ttu-id="32b34-122">Comment obtenir une protection contre le hameçonnage</span><span class="sxs-lookup"><span data-stu-id="32b34-122">How to get ATP anti-phishing</span></span>

<span data-ttu-id="32b34-123">Les fonctionnalités anti-hameçonnage ATP font partie de la [protection avancée contre les menaces](office-365-atp.md); Toutefois, la protection contre le hameçonnage ATP s’applique lorsque les stratégies anti-hameçonnage sont définies.</span><span class="sxs-lookup"><span data-stu-id="32b34-123">ATP Anti-Phishing features are part of [Advanced Threat Protection](office-365-atp.md); however, ATP anti-phishing protection applies when anti-phishing policies are defined.</span></span> <span data-ttu-id="32b34-124">(Par exemple, une stratégie basée sur l’emprunt d’identité.) Consultez la rubrique [configurer des stratégies anti-hameçonnage dans Office 365](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="32b34-124">(One example is an impersonation-based policy.) See [Set up anti-phishing policies in Office 365](set-up-anti-phishing-policies.md).</span></span>
  
## <a name="how-to-know-if-atp-anti-phishing-is-in-place"></a><span data-ttu-id="32b34-125">Comment savoir si la protection contre le hameçonnage est mise en place</span><span class="sxs-lookup"><span data-stu-id="32b34-125">How to know if ATP anti-phishing is in place</span></span>

<span data-ttu-id="32b34-126">Les stratégies anti-hameçonnage ATP doivent être définies afin que la protection soit effective.</span><span class="sxs-lookup"><span data-stu-id="32b34-126">ATP anti-phishing policies must be defined in order for protection to be in effect.</span></span> <span data-ttu-id="32b34-127">Consultez-la tout d’abord pour vérifier que la protection est en place.</span><span class="sxs-lookup"><span data-stu-id="32b34-127">Check this first to verify protection is in place.</span></span>

<span data-ttu-id="32b34-128">De plus, des rapports sont disponibles pour illustrer le fonctionnement du service pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="32b34-128">In addition, reports are available to show how the service is working for your organization.</span></span> <span data-ttu-id="32b34-129">Pour en savoir plus, consultez la rubrique [afficher les rapports pour Office 365 Advanced Threat Protection](view-reports-for-atp.md).</span><span class="sxs-lookup"><span data-stu-id="32b34-129">To learn more, see [View reports for Office 365 Advanced Threat Protection](view-reports-for-atp.md).</span></span>

<span data-ttu-id="32b34-130">Pour que les modèles d’apprentissage de l’anti-hameçonnage ATP soient actifs pour un utilisateur particulier, cet utilisateur doit faire partie d’une stratégie de [pièces jointes approuvées ATP](atp-safe-attachments.md)définie, de [liens approuvés ATP](atp-safe-links.md)ou d’une stratégie anti-hameçonnage ATP.</span><span class="sxs-lookup"><span data-stu-id="32b34-130">For ATP anti-phishing machine learning models to be active for a particular user, that user must be part of a defined [ATP Safe attachments](atp-safe-attachments.md), [ATP Safe Links](atp-safe-links.md), or ATP Anti-Phishing policy.</span></span> 

<span data-ttu-id="32b34-131">Le tableau suivant décrit quelques exemples de scénarios.</span><span class="sxs-lookup"><span data-stu-id="32b34-131">The following table describes a few example scenarios.</span></span> <span data-ttu-id="32b34-132">Dans chacun de ces exemples, l’organisation utilise Office 365 entreprise E5, qui inclut la protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="32b34-132">In each of these examples, the organization is using Office 365 Enterprise E5, which includes Advanced Threat Protection.</span></span>
  
|<span data-ttu-id="32b34-133">**Exemple de scénario**</span><span class="sxs-lookup"><span data-stu-id="32b34-133">**Example scenario**</span></span>|<span data-ttu-id="32b34-134">**Est-ce que la protection contre le hameçonnage ATP s’applique dans ce cas ?**</span><span class="sxs-lookup"><span data-stu-id="32b34-134">**Does ATP anti-phishing apply in this case?**</span></span>|
|:-----|:-----|
|<span data-ttu-id="32b34-135">L’organisation de Pat a Office 365 entreprise E5, mais personne n’a défini de stratégie pour les pièces jointes approuvées pour la protection avancée contre les menaces, les liens fiables ATP ou l’hameçonnage avancé ATP.</span><span class="sxs-lookup"><span data-stu-id="32b34-135">Pat's organization has Office 365 Enterprise E5, but no one has defined any policies for ATP safe attachments, ATP safe links or ATP advanced phishing yet.</span></span>|<span data-ttu-id="32b34-136">Non.</span><span class="sxs-lookup"><span data-stu-id="32b34-136">No.</span></span> <span data-ttu-id="32b34-137">Bien que la fonctionnalité soit disponible, au moins une stratégie ATP doit être définie pour que les modèles d’apprentissage de l’ordinateur ATP fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="32b34-137">Although the feature is available, at least one ATP policy must be defined in order for the ATP machine learning models to work.</span></span> <span data-ttu-id="32b34-138">Pour l’emprunt d’identité, une stratégie anti-hameçonnage de protection avancée contre les menaces doit également être mise en place.</span><span class="sxs-lookup"><span data-stu-id="32b34-138">For impersonation an ATP anti-phishing policy must also be in place.</span></span>|
|<span data-ttu-id="32b34-139">Lee est un employé du service des ventes de contoso.</span><span class="sxs-lookup"><span data-stu-id="32b34-139">Lee is an employee in the sales department at Contoso.</span></span> <span data-ttu-id="32b34-140">L’organisation de Lee a une stratégie anti-hameçonnage ATP qui s’applique uniquement aux employés financiers.</span><span class="sxs-lookup"><span data-stu-id="32b34-140">Lee's organization has an ATP anti-phishing policy in place that applies to finance employees only.</span></span>|<span data-ttu-id="32b34-141">Non.</span><span class="sxs-lookup"><span data-stu-id="32b34-141">No.</span></span> <span data-ttu-id="32b34-142">Dans ce cas, la protection contre le hameçonnage ATP (modèles d’ordinateur et protection contre l’usurpation d’identité) s’applique aux employés financiers, mais ce n’est pas le cas pour d’autres employés, y compris le service des ventes.</span><span class="sxs-lookup"><span data-stu-id="32b34-142">In this case, ATP anti-phishing (machine models and impersonation protection) would apply to finance employees, but other employees, including the sales department, would not.</span></span>|
|<span data-ttu-id="32b34-143">Hier, un administrateur Office 365 de la société Jean a configuré une stratégie anti-hameçonnage ATP qui s’applique à tous les employés.</span><span class="sxs-lookup"><span data-stu-id="32b34-143">Yesterday, an Office 365 administrator at Jean's organization set up an ATP anti-phishing policy that applies to all employees.</span></span> <span data-ttu-id="32b34-144">Plus tôt aujourd’hui, Jean a reçu un message électronique qui inclut un emprunt d’identité couvert par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="32b34-144">Earlier today, Jean received an email message that includes an impersonation covered by the policy.</span></span>|<span data-ttu-id="32b34-145">Oui.</span><span class="sxs-lookup"><span data-stu-id="32b34-145">Yes.</span></span> <span data-ttu-id="32b34-146">Dans cet exemple, Jean a une licence pour la protection avancée contre les menaces, et une stratégie anti-hameçonnage ATP incluant Jean a été définie.</span><span class="sxs-lookup"><span data-stu-id="32b34-146">In this example, Jean has a license for Advanced Threat Protection, and an ATP anti-phishing policy that includes Jean has been defined.</span></span> <span data-ttu-id="32b34-147">Il faut environ 30 minutes pour qu’une nouvelle stratégie prenne effet sur l’ensemble des centres de communication ; étant donné qu’un jour a passé dans ce cas, la stratégie doit être en vigueur.</span><span class="sxs-lookup"><span data-stu-id="32b34-147">It typically takes about 30 minutes for a new policy to take effect across datacenters; since a day has passed in this case, the policy should be in effect.</span></span>|

## <a name="related-topics"></a><span data-ttu-id="32b34-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32b34-148">Related topics</span></span>

[<span data-ttu-id="32b34-149">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-149">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="32b34-150">Protection anti-hameçonnage dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-150">Anti-phishing protection in Office 365</span></span>](anti-phishing-protection.md)
  
[<span data-ttu-id="32b34-151">Configurer des stratégies anti-hameçonnage dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-151">Set up anti-phishing policies in Office 365</span></span>](set-up-anti-phishing-policies.md)
  
[<span data-ttu-id="32b34-152">Liens approuvés ATP dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-152">ATP safe links in Office 365</span></span>](atp-safe-links.md)
  
[<span data-ttu-id="32b34-153">Configurer des stratégies de liens fiables ATP dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-153">Set up ATP safe links policies in Office 365</span></span>](set-up-atp-safe-links-policies.md)
  
[<span data-ttu-id="32b34-154">Pièces jointes approuvées ATP dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-154">ATP safe attachments in Office 365</span></span>](atp-safe-attachments.md)
  
[<span data-ttu-id="32b34-155">Configuration des stratégies de pièces jointes approuvées ATP dans Office 365</span><span class="sxs-lookup"><span data-stu-id="32b34-155">Set up ATP safe attachments policies in Office 365</span></span>](set-up-atp-safe-attachments-policies.md)
  
[<span data-ttu-id="32b34-156">Afficher les rapports de protection contre les menaces avancées</span><span class="sxs-lookup"><span data-stu-id="32b34-156">View the reports for Advanced Threat Protection</span></span>](view-reports-for-atp.md)