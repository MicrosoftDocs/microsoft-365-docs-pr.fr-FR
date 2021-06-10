---
title: Utiliser la protection des identités, des appareils et des menaces pour la réglementation sur la confidentialité des données
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
description: Empêcher les violations de données personnelles avec des services de protection contre les identités, appareils et menaces Microsoft 365.
ms.openlocfilehash: 5e08ef574e199769e572b3836b3323dc88fc4bbd
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51199464"
---
# <a name="use-identity-device-and-threat-protection-for-data-privacy-regulation"></a><span data-ttu-id="f7945-103">Utiliser la protection des identités, des appareils et des menaces pour la réglementation sur la confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="f7945-103">Use identity, device, and threat protection for data privacy regulation</span></span>

<span data-ttu-id="f7945-104">Microsoft 365 offre un certain nombre de fonctionnalités de protection contre les menaces, les appareils et les identités que les organisations peuvent utiliser pour se conformer aux réglementations de conformité liées à la confidentialité des données.</span><span class="sxs-lookup"><span data-stu-id="f7945-104">Microsoft 365 provides a number of identity, device, and threat protection capabilities that organizations can employ to help comply with data privacy-related compliance regulations.</span></span> <span data-ttu-id="f7945-105">Cet article décrit les exigences des réglementations en matière de confidentialité des données dans ces domaines et fournit une liste des fonctionnalités et services Microsoft 365 connexes avec des liens vers des informations supplémentaires pour vous aider à répondre aux exigences d’implémentation.</span><span class="sxs-lookup"><span data-stu-id="f7945-105">This article describes what the data privacy regulations require in these areas and provides a listing of related Microsoft 365 features and services with links to more information to help you address implementation requirements.</span></span>

## <a name="how-identity-device-and-threat-protection-relate-to-data-privacy-regulation"></a><span data-ttu-id="f7945-106">Relation entre l’identité, l’appareil et la protection contre les menaces par rapport à la réglementation sur la confidentialité des données</span><span class="sxs-lookup"><span data-stu-id="f7945-106">How identity, device, and threat protection relate to data privacy regulation</span></span>

<span data-ttu-id="f7945-107">Bien que les réglementations en matière de confidentialité des données varient en fonction de leur spécificité, la nature de ce qu’elles appellent est incorporée dans l’article 5(1)(f) du R GDPR, qui stipule que :</span><span class="sxs-lookup"><span data-stu-id="f7945-107">While the data privacy regulations vary in their specificity, the essence of what they call for is embodied in the GDPR’s Article 5(1)(f), which states that:</span></span>

- <span data-ttu-id="f7945-108">Les données personnelles doivent être traitées d’une manière qui garantit la sécurité appropriée des données personnelles, y compris la protection contre le traitement non autorisé ou illégal et contre les pertes, destructions ou dommages accidentels, à l’aide de mesures techniques ou organisationnelles appropriées (intégrité et confidentialité).</span><span class="sxs-lookup"><span data-stu-id="f7945-108">Personal data shall be processed in a manner that ensures appropriate security of the personal data, including protection against unauthorized or unlawful processing and against accidental loss, destruction or damage, using appropriate technical or organizational measures ('integrity and confidentiality').</span></span>

<span data-ttu-id="f7945-109">Étant donné que les violations de données personnelles sont souvent dues à une compromission de compte d’administration ou d’utilisateur final et à un accès malveillant au système.</span><span class="sxs-lookup"><span data-stu-id="f7945-109">Because personal data breaches are often caused by administrative or end-user account compromise and malicious system access.</span></span> <span data-ttu-id="f7945-110">Par exemple, un piratage de compte d’administrateur peut entraîner l’exfiltration de numéros de carte de crédit client ou d’autres informations personnelles.</span><span class="sxs-lookup"><span data-stu-id="f7945-110">For example, an admin account hack can result in exfiltration of customer credit card numbers or other personal information.</span></span> <span data-ttu-id="f7945-111">Toutes les protections généralement conseillées en matière d’identité, d’appareil et de menaces disponibles avec Microsoft 365 doivent potentiellement être implémentées, ce qui sera reflété dans votre score de conformité, disponible dans le Gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="f7945-111">All the generally advisable identity, device, and threat protection available with Microsoft 365 potentially should be implemented, which will be reflected in your compliance score, found in Compliance Manager.</span></span>

## <a name="using-the-results-of-your-assessment-work-and-compliance-manager"></a><span data-ttu-id="f7945-112">Utilisation des résultats de votre travail d’évaluation et du Gestionnaire de conformité</span><span class="sxs-lookup"><span data-stu-id="f7945-112">Using the results of your assessment work and Compliance Manager</span></span>

<span data-ttu-id="f7945-113">Le Gestionnaire de conformité inclut la protection contre les identités, les appareils et les menaces à l’aide des catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7945-113">Compliance Manager includes identity, device, and threat protection using these categories:</span></span>

- <span data-ttu-id="f7945-114">L’identité correspond à la **catégorie Contrôle d’accès**</span><span class="sxs-lookup"><span data-stu-id="f7945-114">Identity corresponds to the **Control Access** category</span></span>
- <span data-ttu-id="f7945-115">L’appareil correspond à la **catégorie Gérer les appareils**</span><span class="sxs-lookup"><span data-stu-id="f7945-115">Device corresponds to the **Manage Devices** category</span></span>
- <span data-ttu-id="f7945-116">La protection contre les menaces correspond à la **catégorie Protéger contre les menaces**</span><span class="sxs-lookup"><span data-stu-id="f7945-116">Threat protection corresponds to the **Protect Against Threats** category</span></span>
 
<span data-ttu-id="f7945-117">Si celles-ci sont sélectionnées dans notre exemple de quatre réglementations majeures en matière de confidentialité des données, le Gestionnaire de conformité spécifie 90 actions d’amélioration, dont la plupart ont le niveau « 27 ».</span><span class="sxs-lookup"><span data-stu-id="f7945-117">If these are selected across our sample set of four major data privacy regulations, Compliance Manager specifies 90 improvement actions, most of which are scored a "27".</span></span> <span data-ttu-id="f7945-118">Étant donné qu’un nombre aussi élevé est appelé par le Gestionnaire de conformité pour ces catégories, certaines des plus courantes sont répertoriées ici, à titre de référence.</span><span class="sxs-lookup"><span data-stu-id="f7945-118">Since such a large number are called out by Compliance Manager for these categories, some of the more common ones are listed here, for reference.</span></span>

<span data-ttu-id="f7945-119">Utilisez [Azure Active Directory (Azure AD)](https://azure.microsoft.com/services/active-directory/) pour l’identité et la catégorie **d’accès** au contrôle, avec laquelle vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f7945-119">Use [Azure Active Directory (Azure AD)](https://azure.microsoft.com/services/active-directory/) for identity and the **Control Access** category, with which you can:</span></span>

- <span data-ttu-id="f7945-120">Implémenter une authentification résistant à la relecture (pour empêcher les attaques « De l’homme au milieu » )</span><span class="sxs-lookup"><span data-stu-id="f7945-120">Implement replay-resistant authentication (to prevent “Man in the middle” attacks)</span></span>
- <span data-ttu-id="f7945-121">Bloquer l’authentification héritée.</span><span class="sxs-lookup"><span data-stu-id="f7945-121">Block legacy authentication.</span></span>
- <span data-ttu-id="f7945-122">Configurez les stratégies de risque de l’utilisateur et de la connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="f7945-122">Configure user risk and user sign-in risk policies.</span></span>
- <span data-ttu-id="f7945-123">Activer l’accès conditionnel et l’authentification multifacteur (MFA) pour les administrateurs et les non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="f7945-123">Enable Conditional Access and multi-factor authentication (MFA) for admins and non-admins.</span></span>
- <span data-ttu-id="f7945-124">Configurer et appliquer des stratégies de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f7945-124">Configure and enforce password policies.</span></span>
- <span data-ttu-id="f7945-125">Restreindre l’accès aux comptes privilégiés avec Azure AD Privileged Identity Management.</span><span class="sxs-lookup"><span data-stu-id="f7945-125">Restrict access to privileged accounts with Azure AD Privileged Identity Management.</span></span>
- <span data-ttu-id="f7945-126">Désactiver l’accès lors de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f7945-126">Disable access upon termination.</span></span>
- <span data-ttu-id="f7945-127">Auditer les comptes d’utilisateur et les changements d’état.</span><span class="sxs-lookup"><span data-stu-id="f7945-127">Audit user accounts and status changes.</span></span>
- <span data-ttu-id="f7945-128">Passer en revue les modifications administratives et de groupe de rôles.</span><span class="sxs-lookup"><span data-stu-id="f7945-128">Review role group and administrative changes.</span></span>

<span data-ttu-id="f7945-129">Utilisez [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager) pour les appareils et la catégorie **Gérer** les appareils, avec laquelle vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f7945-129">Use [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager) for devices and the **Manage Devices** category, with which you can:</span></span>

- <span data-ttu-id="f7945-130">Bloquez les appareils mobiles rompus et racines.</span><span class="sxs-lookup"><span data-stu-id="f7945-130">Block jail broken and rooted mobile devices.</span></span>
- <span data-ttu-id="f7945-131">Configurez Intune pour la gestion des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f7945-131">Configure Intune for mobile device management.</span></span>
- <span data-ttu-id="f7945-132">Créez des stratégies de conformité pour les appareils Android, iOS, macOS et Windows mobiles.</span><span class="sxs-lookup"><span data-stu-id="f7945-132">Create compliance policies for Android, iOS, macOS and Windows devices.</span></span>
- <span data-ttu-id="f7945-133">Créez un profil de configuration d’appareil pour les appareils Android, iOS, macOS Windows appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f7945-133">Create a device configuration profile for Android, iOS, macOS and Windows devices.</span></span>
- <span data-ttu-id="f7945-134">Créez des stratégies de protection des applications pour iOS et Windows.</span><span class="sxs-lookup"><span data-stu-id="f7945-134">Create app protection policies for iOS and Windows.</span></span>
- <span data-ttu-id="f7945-135">Masquer les informations à l’écran de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="f7945-135">Conceal information with lock screen.</span></span>
- <span data-ttu-id="f7945-136">Implémenter des stratégies de mot de passe pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f7945-136">Implement password policies for mobile devices.</span></span>
- <span data-ttu-id="f7945-137">Exiger que les appareils mobiles se verrouillent en cas d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="f7945-137">Require mobile devices to lock upon inactivity.</span></span>
- <span data-ttu-id="f7945-138">Exiger que les appareils mobiles s’effacent en cas d’échec de plusieurs connecteurs.</span><span class="sxs-lookup"><span data-stu-id="f7945-138">Require mobile devices to wipe on multiple sign-in failures.</span></span>

<span data-ttu-id="f7945-139">Utilisez [Exchange Online Protection et Microsoft Defender pour Office 365](../security/office-365-security/defender-for-office-365.md)  la catégorie Protéger contre les menaces, avec laquelle vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="f7945-139">Use [Exchange Online Protection and Microsoft Defender for Office 365](../security/office-365-security/defender-for-office-365.md) for the **Protect Against Threats** category, with which you can:</span></span>

- <span data-ttu-id="f7945-140">Activer l’authentification de l’expéditeur (SPF, DMARC et DKIM).</span><span class="sxs-lookup"><span data-stu-id="f7945-140">Enable sender authentication (SPF, DMARC and DKIM).</span></span>
- <span data-ttu-id="f7945-141">Configurer Microsoft Defender pour Office 365 stratégies anti-hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="f7945-141">Set up Microsoft Defender for Office 365 anti-phishing policies.</span></span>
- <span data-ttu-id="f7945-142">Implémenter les pièces jointes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="f7945-142">Implement Safe Attachments.</span></span>
- <span data-ttu-id="f7945-143">Implémenter des liens sécurisés.</span><span class="sxs-lookup"><span data-stu-id="f7945-143">Implement Safe Links.</span></span>
- <span data-ttu-id="f7945-144">Implémenter des stratégies de détection et de réponse aux programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="f7945-144">Implement malware detection and response policies.</span></span>
- <span data-ttu-id="f7945-145">Implémenter des stratégies de courrier indésirable sortant et entrant.</span><span class="sxs-lookup"><span data-stu-id="f7945-145">Implement outbound and inbound spam policies.</span></span>

### <a name="references"></a><span data-ttu-id="f7945-146">Références :</span><span class="sxs-lookup"><span data-stu-id="f7945-146">References:</span></span>

- [<span data-ttu-id="f7945-147">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="f7945-147">Common identity and device access policies</span></span>](../security/office-365-security/identity-access-policies.md)
- [<span data-ttu-id="f7945-148">Se protéger contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f7945-148">Protect against threats in Office 365</span></span>](https://support.office.com/article/protect-against-threats-in-office-365-b10023f6-f30f-45d3-b3ad-b71aa4aa0d58)
- [<span data-ttu-id="f7945-149">Pièces jointes fiables</span><span class="sxs-lookup"><span data-stu-id="f7945-149">Safe Attachments</span></span>](../security/office-365-security/safe-attachments.md)
- [<span data-ttu-id="f7945-150">Liens fiables</span><span class="sxs-lookup"><span data-stu-id="f7945-150">Safe Links</span></span>](../security/office-365-security/safe-links.md)
- [<span data-ttu-id="f7945-151">Documents sécurisés</span><span class="sxs-lookup"><span data-stu-id="f7945-151">Safe Documents</span></span>](../security/office-365-security/safe-docs.md)
