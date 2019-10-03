---
title: Gestion des appareils mobiles pour Contoso
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso utilise Microsoft Intune dans Microsoft 365 Entreprise pour gérer ses appareils et les applications exécutées sur ces derniers.
ms.openlocfilehash: b083b7fed67eb08b47daf70c3fd22c181f5a8f77
ms.sourcegitcommit: 8bcd76e5c8749a5670fbc3356957a089454c03d1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2019
ms.locfileid: "37370481"
---
# <a name="mobile-device-management-for-contoso"></a><span data-ttu-id="62a6d-103">Gestion des appareils mobiles pour Contoso</span><span class="sxs-lookup"><span data-stu-id="62a6d-103">Mobile device management for Contoso</span></span>

<span data-ttu-id="62a6d-104">**Résumé :** Découvrez comment Contoso utilise Microsoft Intune dans Microsoft 365 Entreprise pour gérer ses appareils et les applications exécutées sur ces derniers.</span><span class="sxs-lookup"><span data-stu-id="62a6d-104">**Summary:** Understand how Contoso uses EMS in Microsoft 365 Enterprise to manage its devices and the apps that run on them.</span></span>

<span data-ttu-id="62a6d-105">Microsoft 365 Entreprise comprend Intune et un ensemble de services Azure pour prendre en charge la gestion et la sécurité des appareils mobiles et des applications.</span><span class="sxs-lookup"><span data-stu-id="62a6d-105">Enterprise Mobility + Security (EMS) in Microsoft 365 Enterprise consists of Microsoft Intune and a set of Azure services to support mobile device and application management and security.</span></span>

<span data-ttu-id="62a6d-p101">Chez Contoso, de nombreux employés sont équipés d’appareils mobiles. Certains d’entre eux ont leur bureau sur les sites de Contoso et d’autres n’ont pas de bureau. Contoso cherchait une solution pour renforcer la productivité des employés, tout en garantissant la sécurité des appareils, des données Contoso stockées sur ces appareils et du comportement des applications.</span><span class="sxs-lookup"><span data-stu-id="62a6d-p101">Contoso has many mobile-enabled employees, some of which have offices in Contoso locations and some of which have no offices. Contoso needed a way to enable employee productivity but keep the devices, the Contoso data stored on those devices, and application behavior secure.</span></span>

## <a name="plan"></a><span data-ttu-id="62a6d-108">Prévision</span><span class="sxs-lookup"><span data-stu-id="62a6d-108">Plan</span></span>

<span data-ttu-id="62a6d-109">Dès le début de l’analyse de la gestion des appareils mobiles pour Microsoft 365 Entreprise, Contoso a identifié les cas d’utilisation Intune suivants :</span><span class="sxs-lookup"><span data-stu-id="62a6d-109">Early in the analysis of mobile device management for Microsoft 365 Enterprise, Contoso identified the following Intune use cases:</span></span>

- <span data-ttu-id="62a6d-110">Protection des données et des e-mails Exchange Online pour y accéder en toute sécurité sur les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="62a6d-110">Protect Exchange Online email and data so it can be safely accessed by mobile devices</span></span>
- <span data-ttu-id="62a6d-111">Implémentation d’un programme BYOD (Apportez votre propre appareil) destiné aux employés de Contoso</span><span class="sxs-lookup"><span data-stu-id="62a6d-111">Implement a bring your own device (BYOD) program for Contoso employees</span></span>
- <span data-ttu-id="62a6d-112">Fourniture de téléphones appartenant à l’organisation et de tablettes partagées à usage limité aux employés de Contoso</span><span class="sxs-lookup"><span data-stu-id="62a6d-112">Issue organization-owned phones and limited-use shared tablets to Contoso employees</span></span>

<span data-ttu-id="62a6d-113">Contoso n’utilise pas Intune pour :</span><span class="sxs-lookup"><span data-stu-id="62a6d-113">Contoso is not using Intune to:</span></span>

- <span data-ttu-id="62a6d-114">Permettre aux employés d’accéder en toute sécurité à Office 365 depuis un lieu public non géré</span><span class="sxs-lookup"><span data-stu-id="62a6d-114">Allow employees to securely access Office 365 from an unmanaged public kiosk</span></span>
- <span data-ttu-id="62a6d-115">Protéger les données et les e-mails dans l’environnement local pour pouvoir y accéder en toute sécurité sur les appareils mobiles, car il n’y a plus de serveurs Microsoft Exchange locaux.</span><span class="sxs-lookup"><span data-stu-id="62a6d-115">Protect on-premises email and data so it can be safely accessed by mobile devices, because there are no longer on-premises Microsoft Exchange servers.</span></span>

## <a name="deploy"></a><span data-ttu-id="62a6d-116">Déployer</span><span class="sxs-lookup"><span data-stu-id="62a6d-116">Deploy</span></span>

<span data-ttu-id="62a6d-117">Voici la configuration de l’infrastructure de gestion des appareils mobiles de Contoso :</span><span class="sxs-lookup"><span data-stu-id="62a6d-117">This is how Contoso set up their mobile device management infrastructure:</span></span>

- <span data-ttu-id="62a6d-118">Intune est devenu l’autorité de gestion des appareils mobiles (GAM). Il est utilisé sur Azure pour administrer le contenu et gérer les appareils.</span><span class="sxs-lookup"><span data-stu-id="62a6d-118">Set Intune as the Mobile Device Management (MDM) authority and are using Intune on Azure to administer content and manage the devices</span></span>
- <span data-ttu-id="62a6d-119">Des groupes Azure AD ont été créés pour inscrire des groupes d’appareil, pour les paramètres Intune et pour les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="62a6d-119">Created Azure AD groups for devices for enrollment and Intune settings and device-based conditional access policies</span></span>

  <span data-ttu-id="62a6d-120">Pour plus d’informations, consultez [Stratégies d’accès conditionnel personnalisées de Contoso](contoso-identity.md#conditional-access-policies-for-identity-and-device-access).</span><span class="sxs-lookup"><span data-stu-id="62a6d-120">See [Contoso's conditional access policies](contoso-identity.md#conditional-access-policies-for-identity-and-device-access) for more information.</span></span>

- <span data-ttu-id="62a6d-121">Une plateforme d’appareils Apple a été mise en place pour prendre en charge les employés équipés d’appareils Apple (iPad, iMac, iPhone) et pour les téléphones de type iPhone appartenant à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="62a6d-121">Enabled the Apple device platform to support employees with iPads, iMacs, iPhones, and for iPhone-based corporate-owned phones</span></span>
- <span data-ttu-id="62a6d-122">Les politiques de conditions générales de Contoso ont été créées. Elles sont affichées pendant l’installation du portail de l’entreprise sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="62a6d-122">Created Contoso-specific terms and conditions policies, which are seen during the installation of the Company Portal for Contoso on mobile devices</span></span>
- <span data-ttu-id="62a6d-123">Pour les appareils qui ne sont pas inscrits, un ensemble de stratégies de gestion des applications mobiles (GAM) ont été instaurées pour imposer la procédure d’authentification pour accéder aux services Office 365.</span><span class="sxs-lookup"><span data-stu-id="62a6d-123">For devices that are not enrolled, a set of Mobile Application Management (MAM) policies to require authentication for access to Office 365 services</span></span>
- <span data-ttu-id="62a6d-124">Des stratégies Intune ont été créées pour appliquer :</span><span class="sxs-lookup"><span data-stu-id="62a6d-124">Created Intune policies that enforce:</span></span>
  - <span data-ttu-id="62a6d-125">Des applications autorisées</span><span class="sxs-lookup"><span data-stu-id="62a6d-125">Allowed apps</span></span>
  - <span data-ttu-id="62a6d-126">Le chiffrement de l’appareil pour empêcher tout accès non autorisé</span><span class="sxs-lookup"><span data-stu-id="62a6d-126">Device encryption to help prevent unauthorized access</span></span>
  - <span data-ttu-id="62a6d-127">Un code confidentiel ou un mot de passe à six chiffres</span><span class="sxs-lookup"><span data-stu-id="62a6d-127">A six-digit PIN or password</span></span>
  - <span data-ttu-id="62a6d-128">Un délai d’inactivité</span><span class="sxs-lookup"><span data-stu-id="62a6d-128">An inactivity timeout period</span></span>
  - <span data-ttu-id="62a6d-129">Une protection antivirus et contre les programmes malveillants et des mises à jour de signature avec Windows Defender sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="62a6d-129">Antivirus and malware protection, and signature updates with Windows Defender on Windows 10 devices</span></span>
  - <span data-ttu-id="62a6d-130">Des mises à jour automatiques sur les appareils Windows 10 qui incluent les dernières mises à jour de sécurité</span><span class="sxs-lookup"><span data-stu-id="62a6d-130">Automatic updates on Windows 10 devices that include the latest security updates</span></span>
  - <span data-ttu-id="62a6d-131">L’envoi de certificats aux appareils gérés</span><span class="sxs-lookup"><span data-stu-id="62a6d-131">Pushing certificates to managed devices</span></span>
  - <span data-ttu-id="62a6d-p102">Une séparation claire des données professionnelles et personnelles. Les utilisateurs ou les administrateurs peuvent effacer de l’appareil les données d’entreprise sélectionnées, tout en conservant des données personnelles telles que des images, des comptes de messagerie personnels et des fichiers personnels.</span><span class="sxs-lookup"><span data-stu-id="62a6d-p102">A clear separation of business and personal data. Users or admins can selectively wipe corporate data from the device, while leaving personal data such as pictures, personal email accounts, and personal files untouched.</span></span>

<span data-ttu-id="62a6d-p103">Une fois l’infrastructure déployée, Contoso a inscrit les PC et les smartphones et tablettes appartenant à l’entreprise en les ajoutant aux groupes d’appareils Intune appropriés et a déployé un programme BYOD pour que les employés inscrivent leurs appareils personnels. Les appareils inscrits ont reçu les stratégies Intune pour gérer et sécuriser les appareils et leurs applications. Les appareils qui ne sont pas inscrits ont des stratégies de gestion des applications mobiles (GAM) qui spécifient les applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="62a6d-p103">Once deployed, Contoso enrolled PCs and company-owned smartphones and tablets by adding them to the appropriate Intune device groups and rolled out a BYOD program for employees to enroll their personal devices. Enrolled devices received Intune policies, resulting in managed and secured devices and their applications. Devices that are not enrolled have Mobile Application Management (MAM) policies that specify allowed applications.</span></span>

<span data-ttu-id="62a6d-137">Voici l’architecture de déploiement de la gestion des appareils mobiles de Contoso.</span><span class="sxs-lookup"><span data-stu-id="62a6d-137">Here is Contoso's mobile device management deployment architecture.</span></span>

![Infrastructure de déploiement de la gestion des appareils mobiles de Contoso](./media/contoso-mdm/contoso-mdm-fig1.png)

## <a name="next-step"></a><span data-ttu-id="62a6d-139">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="62a6d-139">Next step</span></span>

<span data-ttu-id="62a6d-140">[Découvrez](contoso-info-protect.md) comment Contoso utilise les fonctionnalités de protection des informations de Microsoft 365 Entreprise pour classer, identifier et protéger les actifs numériques au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="62a6d-140">[Learn](contoso-info-protect.md) how Contoso uses the information protection capabilities of Microsoft 365 Enterprise to classify, identify, and protect crucial digital assets across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="62a6d-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62a6d-141">See also</span></span>

[<span data-ttu-id="62a6d-142">Gestion des appareils mobiles pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="62a6d-142">Mobile device management for Microsoft 365 Enterprise</span></span>](mobility-infrastructure.md)

[<span data-ttu-id="62a6d-143">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="62a6d-143">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="62a6d-144">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="62a6d-144">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)

