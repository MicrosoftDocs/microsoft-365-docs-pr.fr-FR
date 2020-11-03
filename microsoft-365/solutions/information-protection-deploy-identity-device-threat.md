---
title: Utiliser l’identité, l’appareil et la protection contre les menaces pour le règlement de confidentialité des données
ms.author: bcarter
author: brendacarter
f1.keywords:
- NOCSH
manager: laurawi
ms.date: 06/09/2020
audience: ITPro
ms.topic: article
ms.prod: microsoft-365-enterprise
localization_priority: Normal
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
- m365solution-infoprotection
- m365solution-scenario
ms.custom: ''
description: Empêchez les violations de données personnelles grâce aux services d’identité, de périphérique et de protection contre les menaces de Microsoft 365.
ms.openlocfilehash: 321b60efbdabe62b14502df4a16dd2dcec4b9cef
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48847177"
---
# <a name="use-identity-device-and-threat-protection-for-data-privacy-regulation"></a><span data-ttu-id="35589-103">Utiliser l’identité, l’appareil et la protection contre les menaces pour le règlement de confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="35589-103">Use identity, device, and threat protection for data privacy regulation</span></span>

<span data-ttu-id="35589-104">Microsoft 365 fournit un certain nombre de fonctionnalités d’identité, de protection des appareils et de protection contre les menaces que les organisations peuvent utiliser pour se conformer aux réglementations de conformité liées à la confidentialité des données.</span><span class="sxs-lookup"><span data-stu-id="35589-104">Microsoft 365 provides a number of identity, device, and threat protection capabilities that organizations can employ to help comply with data privacy-related compliance regulations.</span></span> <span data-ttu-id="35589-105">Cet article décrit les réglementations relatives à la confidentialité des données dans ces domaines et fournit une liste des services et fonctionnalités Microsoft 365 associés avec des liens vers des informations supplémentaires pour vous aider à répondre aux besoins de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="35589-105">This article describes what the data privacy regulations require in these areas and provides a listing of related Microsoft 365 features and services with links to more information to help you address implementation requirements.</span></span>

## <a name="how-identity-device-and-threat-protection-relate-to-data-privacy-regulation"></a><span data-ttu-id="35589-106">Relation entre l’identité, l’appareil et la protection contre les menaces et le règlement sur la confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="35589-106">How identity, device, and threat protection relate to data privacy regulation</span></span>

<span data-ttu-id="35589-107">Bien que les réglementations relatives à la confidentialité des données varient en fonction de leur spécificité, l’essence de ce qu’elles appellent est incorporée dans l’article 5 (1) (f) du RGPD, qui indique les points suivants :</span><span class="sxs-lookup"><span data-stu-id="35589-107">While the data privacy regulations vary in their specificity, the essence of what they call for is embodied in the GDPR’s Article 5(1)(f), which states that:</span></span> 

- <span data-ttu-id="35589-108">Les données personnelles doivent être traitées de manière à garantir une sécurité appropriée des données personnelles, y compris la protection contre le traitement non autorisé ou illégal et contre la perte accidentelle, la destruction ou les dégâts, à l’aide de mesures techniques ou organisationnelles appropriées (« intégrité et confidentialité »).</span><span class="sxs-lookup"><span data-stu-id="35589-108">Personal data shall be processed in a manner that ensures appropriate security of the personal data, including protection against unauthorized or unlawful processing and against accidental loss, destruction or damage, using appropriate technical or organizational measures ('integrity and confidentiality').</span></span>

<span data-ttu-id="35589-109">Étant donné que les violations de données personnelles sont souvent dues à une compromission administrative ou à un compte d’utilisateur final et à un accès système malveillant.</span><span class="sxs-lookup"><span data-stu-id="35589-109">Because personal data breaches are often caused by administrative or end-user account compromise and malicious system access.</span></span> <span data-ttu-id="35589-110">Par exemple, un compte administrateur hack peut entraîner l’exfiltration des numéros de carte de crédit des clients ou d’autres informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="35589-110">For example, an admin account hack can result in exfiltration of customer credit card numbers or other personal information.</span></span> <span data-ttu-id="35589-111">Toutes les protections d’identité, de périphérique et de menace généralement recommandées avec Microsoft 365 peuvent être implémentées, qui seront reflétées dans votre score de conformité, dans le gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="35589-111">All the generally advisable identity, device, and threat protection available with Microsoft 365 potentially should be implemented, which will be reflected in your compliance score, found in Compliance Manager.</span></span>

## <a name="using-the-results-of-your-assessment-work-and-compliance-manager"></a><span data-ttu-id="35589-112">Utilisation des résultats de votre analyse et du gestionnaire de conformité</span><span class="sxs-lookup"><span data-stu-id="35589-112">Using the results of your assessment work and Compliance Manager</span></span>

<span data-ttu-id="35589-113">Le gestionnaire de conformité inclut la protection des identités, des périphériques et des menaces à l’aide des catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="35589-113">Compliance Manager includes identity, device, and threat protection using these categories:</span></span>

- <span data-ttu-id="35589-114">Identity correspond à la catégorie d' **accès au contrôle**</span><span class="sxs-lookup"><span data-stu-id="35589-114">Identity corresponds to the **Control Access** category</span></span>
- <span data-ttu-id="35589-115">Le périphérique correspond à la catégorie **gérer les appareils** .</span><span class="sxs-lookup"><span data-stu-id="35589-115">Device corresponds to the **Manage Devices** category</span></span>
- <span data-ttu-id="35589-116">Protection contre les menaces correspond à la catégorie **protéger contre les menaces**</span><span class="sxs-lookup"><span data-stu-id="35589-116">Threat protection corresponds to the **Protect Against Threats** category</span></span>
 
<span data-ttu-id="35589-117">Si ces éléments sont sélectionnés dans notre ensemble d’exemples de quatre principales réglementations de confidentialité des données, le gestionnaire de conformité indique 90 actions d’amélioration, dont la plupart sont notées « 27 ».</span><span class="sxs-lookup"><span data-stu-id="35589-117">If these are selected across our sample set of four major data privacy regulations, Compliance Manager specifies 90 improvement actions, most of which are scored a "27".</span></span> <span data-ttu-id="35589-118">Étant donné qu’un tel grand nombre est appelé par le gestionnaire de conformité pour ces catégories, certaines des plus courantes sont répertoriées ici, à des fins de référence.</span><span class="sxs-lookup"><span data-stu-id="35589-118">Since such a large number are called out by Compliance Manager for these categories, some of the more common ones are listed here, for reference.</span></span>

<span data-ttu-id="35589-119">Utilisez [Azure Active Directory (Azure AD)](https://azure.microsoft.com/services/active-directory/) pour l’identité et la catégorie d' **accès au contrôle** , avec lequel vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="35589-119">Use [Azure Active Directory (Azure AD)](https://azure.microsoft.com/services/active-directory/) for identity and the **Control Access** category, with which you can:</span></span>

- <span data-ttu-id="35589-120">Implémenter l’authentification resistante à la relecture (pour éviter les attaques de « l’homme en milieu »)</span><span class="sxs-lookup"><span data-stu-id="35589-120">Implement replay-resistant authentication (to prevent “Man in the middle” attacks)</span></span>
- <span data-ttu-id="35589-121">Bloquer l’authentification héritée.</span><span class="sxs-lookup"><span data-stu-id="35589-121">Block legacy authentication.</span></span>
- <span data-ttu-id="35589-122">Configurez les risques utilisateur et les stratégies de risque de connexion utilisateur.</span><span class="sxs-lookup"><span data-stu-id="35589-122">Configure user risk and user sign-in risk policies.</span></span>
- <span data-ttu-id="35589-123">Activer l’accès conditionnel et l’authentification multifacteur (MFA) pour les administrateurs et les non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="35589-123">Enable Conditional Access and multi-factor authentication (MFA) for admins and non-admins.</span></span>
- <span data-ttu-id="35589-124">Configurez et appliquez des stratégies de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="35589-124">Configure and enforce password policies.</span></span>
- <span data-ttu-id="35589-125">Restreignez l’accès aux comptes privilégiés avec Azure AD Privileged Identity Management.</span><span class="sxs-lookup"><span data-stu-id="35589-125">Restrict access to privileged accounts with Azure AD Privileged Identity Management.</span></span>
- <span data-ttu-id="35589-126">Désactiver l’accès lors de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="35589-126">Disable access upon termination.</span></span>
- <span data-ttu-id="35589-127">Audit des comptes d’utilisateur et des modifications d’État.</span><span class="sxs-lookup"><span data-stu-id="35589-127">Audit user accounts and status changes.</span></span>
- <span data-ttu-id="35589-128">Passez en revue les groupes de rôles et les modifications administratives.</span><span class="sxs-lookup"><span data-stu-id="35589-128">Review role group and administrative changes.</span></span>

<span data-ttu-id="35589-129">Utilisez le [Gestionnaire de points de terminaison Microsoft](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager) pour les appareils et la catégorie **gérer les appareils** , avec lequel vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="35589-129">Use [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager) for devices and the **Manage Devices** category, with which you can:</span></span>

- <span data-ttu-id="35589-130">Blocage de la prison et des appareils mobiles enracinés.</span><span class="sxs-lookup"><span data-stu-id="35589-130">Block jail broken and rooted mobile devices.</span></span>
- <span data-ttu-id="35589-131">Configurez Intune pour la gestion des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="35589-131">Configure Intune for mobile device management.</span></span>
- <span data-ttu-id="35589-132">Créer des stratégies de conformité pour les appareils Android, iOS, macOS et Windows.</span><span class="sxs-lookup"><span data-stu-id="35589-132">Create compliance policies for Android, iOS, macOS and Windows devices.</span></span>
- <span data-ttu-id="35589-133">Créez un profil de configuration d’appareil pour Android, iOS, macOS et appareils Windows.</span><span class="sxs-lookup"><span data-stu-id="35589-133">Create a device configuration profile for Android, iOS, macOS and Windows devices.</span></span>
- <span data-ttu-id="35589-134">Créez des stratégies de protection des applications pour iOS et Windows.</span><span class="sxs-lookup"><span data-stu-id="35589-134">Create app protection policies for iOS and Windows.</span></span>
- <span data-ttu-id="35589-135">Masquer les informations avec l’écran de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="35589-135">Conceal information with lock screen.</span></span>
- <span data-ttu-id="35589-136">Implémenter des stratégies de mot de passe pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="35589-136">Implement password policies for mobile devices.</span></span>
- <span data-ttu-id="35589-137">Exiger que les appareils mobiles soient verrouillés lors de l’inactivité.</span><span class="sxs-lookup"><span data-stu-id="35589-137">Require mobile devices to lock upon inactivity.</span></span>
- <span data-ttu-id="35589-138">Exigez la réinitialisation des appareils mobiles sur plusieurs échecs de connexion.</span><span class="sxs-lookup"><span data-stu-id="35589-138">Require mobile devices to wipe on multiple sign-in failures.</span></span>

<span data-ttu-id="35589-139">Utilisez [Exchange Online Protection et Microsoft Defender pour Office 365](../security/office-365-security/office-365-atp.md) pour la catégorie **protéger contre les menaces** , avec lequel vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="35589-139">Use [Exchange Online Protection and Microsoft Defender for Office 365](../security/office-365-security/office-365-atp.md) for the **Protect Against Threats** category, with which you can:</span></span>

- <span data-ttu-id="35589-140">Activer l’authentification des expéditeurs (SPF, DMARC et DKIM).</span><span class="sxs-lookup"><span data-stu-id="35589-140">Enable sender authentication (SPF, DMARC and DKIM).</span></span>
- <span data-ttu-id="35589-141">Configurez Microsoft Defender pour les stratégies anti-hameçonnage d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="35589-141">Set up Microsoft Defender for Office 365 anti-phishing policies.</span></span>
- <span data-ttu-id="35589-142">Implémenter des pièces jointes fiables.</span><span class="sxs-lookup"><span data-stu-id="35589-142">Implement Safe Attachments.</span></span>
- <span data-ttu-id="35589-143">Implémenter des liens fiables.</span><span class="sxs-lookup"><span data-stu-id="35589-143">Implement Safe Links.</span></span>
- <span data-ttu-id="35589-144">Implémenter des stratégies de détection et de réponse contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="35589-144">Implement malware detection and response policies.</span></span>
- <span data-ttu-id="35589-145">Implémenter des stratégies de courrier indésirable entrant et sortant.</span><span class="sxs-lookup"><span data-stu-id="35589-145">Implement outbound and inbound spam policies.</span></span>

### <a name="references"></a><span data-ttu-id="35589-146">Référenç</span><span class="sxs-lookup"><span data-stu-id="35589-146">References:</span></span>

- [<span data-ttu-id="35589-147">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="35589-147">Common identity and device access policies</span></span>](../security/office-365-security/identity-access-policies.md)
- [<span data-ttu-id="35589-148">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="35589-148">Protect against threats in Office 365</span></span>](https://support.office.com/article/protect-against-threats-in-office-365-b10023f6-f30f-45d3-b3ad-b71aa4aa0d58)
- [<span data-ttu-id="35589-149">Pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="35589-149">Safe Attachments</span></span>](../security/office-365-security/atp-safe-attachments.md)
- [<span data-ttu-id="35589-150">Liens fiables</span><span class="sxs-lookup"><span data-stu-id="35589-150">Safe Links</span></span>](../security/office-365-security/atp-safe-links.md)
- [<span data-ttu-id="35589-151">Documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="35589-151">Safe Documents</span></span>](../security/office-365-security/safe-docs.md)
