---
title: Gestion des appareils mobiles pour Contoso
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso utilise Microsoft Intune dans Microsoft 365 pour entreprise pour gérer ses appareils et les applications qui s’y exécutent.
ms.openlocfilehash: 40d9473bcadfa636f6fd2b2c6c861c27dae8497c
ms.sourcegitcommit: 79065e72c0799064e9055022393113dfcf40eb4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2020
ms.locfileid: "46685841"
---
# <a name="mobile-device-management-for-contoso"></a><span data-ttu-id="5db71-103">Gestion des appareils mobiles pour Contoso</span><span class="sxs-lookup"><span data-stu-id="5db71-103">Mobile device management for Contoso</span></span>

<span data-ttu-id="5db71-104">Microsoft 365 pour Enterprise inclut Intune et un ensemble de services Azure pour la prise en charge de la gestion et de la sécurité des appareils mobiles et des applications.</span><span class="sxs-lookup"><span data-stu-id="5db71-104">Microsoft 365 for enterprise includes Intune and a set of Azure services to support mobile device and application management and security.</span></span>

<span data-ttu-id="5db71-p101">Chez Contoso, de nombreux employés sont équipés d’appareils mobiles. Certains d’entre eux ont leur bureau sur les sites de Contoso et d’autres n’ont pas de bureau. Contoso cherchait une solution pour renforcer la productivité des employés, tout en garantissant la sécurité des appareils, des données Contoso stockées sur ces appareils et du comportement des applications.</span><span class="sxs-lookup"><span data-stu-id="5db71-p101">Contoso has many mobile-enabled employees, some of which have offices in Contoso locations and some of which have no offices. Contoso needed a way to enable employee productivity but keep the devices, the Contoso data stored on those devices, and application behavior secure.</span></span>

## <a name="plan"></a><span data-ttu-id="5db71-107">Prévision</span><span class="sxs-lookup"><span data-stu-id="5db71-107">Plan</span></span>

<span data-ttu-id="5db71-108">Au début de l’analyse de la gestion des appareils mobiles pour Microsoft 365 pour les entreprises, Contoso a identifié les cas d’utilisation Intune suivants :</span><span class="sxs-lookup"><span data-stu-id="5db71-108">Early in the analysis of mobile device management for Microsoft 365 for enterprise, Contoso identified the following Intune use cases:</span></span>

- <span data-ttu-id="5db71-109">Protection des données et des e-mails Exchange Online pour y accéder en toute sécurité sur les appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="5db71-109">Protect Exchange Online email and data so it can be safely accessed by mobile devices</span></span>
- <span data-ttu-id="5db71-110">Implémentation d’un programme BYOD (Apportez votre propre appareil) destiné aux employés de Contoso</span><span class="sxs-lookup"><span data-stu-id="5db71-110">Implement a bring your own device (BYOD) program for Contoso employees</span></span>
- <span data-ttu-id="5db71-111">Fourniture de téléphones appartenant à l’organisation et de tablettes partagées à usage limité aux employés de Contoso</span><span class="sxs-lookup"><span data-stu-id="5db71-111">Issue organization-owned phones and limited-use shared tablets to Contoso employees</span></span>

<span data-ttu-id="5db71-112">Contoso n’utilise pas Intune pour :</span><span class="sxs-lookup"><span data-stu-id="5db71-112">Contoso is not using Intune to:</span></span>

- <span data-ttu-id="5db71-113">Autoriser les employés à accéder en toute sécurité à Microsoft 365 à partir d’un kiosque public non géré</span><span class="sxs-lookup"><span data-stu-id="5db71-113">Allow employees to securely access Microsoft 365 from an unmanaged public kiosk</span></span>
- <span data-ttu-id="5db71-114">Protéger les données et les e-mails dans l’environnement local pour pouvoir y accéder en toute sécurité sur les appareils mobiles, car il n’y a plus de serveurs Microsoft Exchange locaux.</span><span class="sxs-lookup"><span data-stu-id="5db71-114">Protect on-premises email and data so it can be safely accessed by mobile devices, because there are no longer on-premises Microsoft Exchange servers.</span></span>

## <a name="deploy"></a><span data-ttu-id="5db71-115">Déployer</span><span class="sxs-lookup"><span data-stu-id="5db71-115">Deploy</span></span>

<span data-ttu-id="5db71-116">Voici la configuration de l’infrastructure de gestion des appareils mobiles de Contoso :</span><span class="sxs-lookup"><span data-stu-id="5db71-116">This is how Contoso set up their mobile device management infrastructure:</span></span>

- <span data-ttu-id="5db71-117">Intune est devenu l’autorité de gestion des appareils mobiles (GAM). Il est utilisé sur Azure pour administrer le contenu et gérer les appareils.</span><span class="sxs-lookup"><span data-stu-id="5db71-117">Set Intune as the Mobile Device Management (MDM) authority and are using Intune on Azure to administer content and manage the devices</span></span>
- <span data-ttu-id="5db71-118">Des groupes Azure AD ont été créés pour inscrire des groupes d’appareil, pour les paramètres Intune et pour les stratégies d’accès conditionnel.</span><span class="sxs-lookup"><span data-stu-id="5db71-118">Created Azure AD groups for devices for enrollment and Intune settings and device-based Conditional Access policies</span></span>

  <span data-ttu-id="5db71-119">Pour plus d’informations, consultez [Stratégies d’accès conditionnel personnalisées de Contoso](contoso-identity.md#conditional-access-policies-for-identity-and-device-access).</span><span class="sxs-lookup"><span data-stu-id="5db71-119">See [Contoso's Conditional Access policies](contoso-identity.md#conditional-access-policies-for-identity-and-device-access) for more information.</span></span>

- <span data-ttu-id="5db71-120">Une plateforme d’appareils Apple a été mise en place pour prendre en charge les employés équipés d’appareils Apple (iPad, iMac, iPhone) et pour les téléphones de type iPhone appartenant à l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="5db71-120">Enabled the Apple device platform to support employees with iPads, iMacs, iPhones, and for iPhone-based corporate-owned phones</span></span>
- <span data-ttu-id="5db71-121">Les politiques de conditions générales de Contoso ont été créées. Elles sont affichées pendant l’installation du portail de l’entreprise sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="5db71-121">Created Contoso-specific terms and conditions policies, which are seen during the installation of the Company Portal for Contoso on mobile devices</span></span>
- <span data-ttu-id="5db71-122">Pour les appareils qui ne sont pas déployés, un ensemble de stratégies de gestion des applications mobiles (MAM) pour exiger l’authentification pour l’accès aux services Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5db71-122">For devices that are not enrolled, a set of Mobile Application Management (MAM) policies to require authentication for access to Microsoft 365 services</span></span>
- <span data-ttu-id="5db71-123">Des stratégies Intune ont été créées pour appliquer :</span><span class="sxs-lookup"><span data-stu-id="5db71-123">Created Intune policies that enforce:</span></span>
  - <span data-ttu-id="5db71-124">Des applications autorisées</span><span class="sxs-lookup"><span data-stu-id="5db71-124">Allowed apps</span></span>
  - <span data-ttu-id="5db71-125">Le chiffrement de l’appareil pour empêcher tout accès non autorisé</span><span class="sxs-lookup"><span data-stu-id="5db71-125">Device encryption to help prevent unauthorized access</span></span>
  - <span data-ttu-id="5db71-126">Un code confidentiel ou un mot de passe à six chiffres</span><span class="sxs-lookup"><span data-stu-id="5db71-126">A six-digit PIN or password</span></span>
  - <span data-ttu-id="5db71-127">Un délai d’inactivité</span><span class="sxs-lookup"><span data-stu-id="5db71-127">An inactivity timeout period</span></span>
  - <span data-ttu-id="5db71-128">Une protection antivirus et contre les programmes malveillants et des mises à jour de signature avec Windows Defender sur les appareils Windows 10</span><span class="sxs-lookup"><span data-stu-id="5db71-128">Antivirus and malware protection, and signature updates with Windows Defender on Windows 10 devices</span></span>
  - <span data-ttu-id="5db71-129">Des mises à jour automatiques sur les appareils Windows 10 qui incluent les dernières mises à jour de sécurité</span><span class="sxs-lookup"><span data-stu-id="5db71-129">Automatic updates on Windows 10 devices that include the latest security updates</span></span>
  - <span data-ttu-id="5db71-130">L’envoi de certificats aux appareils gérés</span><span class="sxs-lookup"><span data-stu-id="5db71-130">Pushing certificates to managed devices</span></span>
  - <span data-ttu-id="5db71-p102">Une séparation claire des données professionnelles et personnelles. Les utilisateurs ou les administrateurs peuvent effacer de l’appareil les données d’entreprise sélectionnées, tout en conservant des données personnelles telles que des images, des comptes de messagerie personnels et des fichiers personnels.</span><span class="sxs-lookup"><span data-stu-id="5db71-p102">A clear separation of business and personal data. Users or admins can selectively wipe corporate data from the device, while leaving personal data such as pictures, personal email accounts, and personal files untouched.</span></span>

<span data-ttu-id="5db71-p103">Une fois l’infrastructure déployée, Contoso a inscrit les PC et les smartphones et tablettes appartenant à l’entreprise en les ajoutant aux groupes d’appareils Intune appropriés et a déployé un programme BYOD pour que les employés inscrivent leurs appareils personnels. Les appareils inscrits ont reçu les stratégies Intune pour gérer et sécuriser les appareils et leurs applications. Les appareils qui ne sont pas inscrits ont des stratégies de gestion des applications mobiles (GAM) qui spécifient les applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="5db71-p103">Once deployed, Contoso enrolled PCs and company-owned smartphones and tablets by adding them to the appropriate Intune device groups and rolled out a BYOD program for employees to enroll their personal devices. Enrolled devices received Intune policies, resulting in managed and secured devices and their applications. Devices that are not enrolled have Mobile Application Management (MAM) policies that specify allowed applications.</span></span>

<span data-ttu-id="5db71-136">Voici l’architecture de déploiement de la gestion des appareils mobiles de Contoso.</span><span class="sxs-lookup"><span data-stu-id="5db71-136">Here is Contoso's mobile device management deployment architecture.</span></span>

![Infrastructure de déploiement de la gestion des appareils mobiles de Contoso](../media/contoso-mdm/contoso-mdm-fig1.png)

## <a name="next-step"></a><span data-ttu-id="5db71-138">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5db71-138">Next step</span></span>

<span data-ttu-id="5db71-139">[Découvrez](contoso-info-protect.md) comment Contoso utilise les fonctionnalités de protection des informations de Microsoft 365 pour Enterprise pour classer, identifier et protéger les biens numériques stratégiques au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="5db71-139">[Learn](contoso-info-protect.md) how Contoso uses the information protection capabilities of Microsoft 365 for enterprise to classify, identify, and protect crucial digital assets across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="5db71-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5db71-140">See also</span></span>

[<span data-ttu-id="5db71-141">Gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="5db71-141">Device management for Microsoft 365</span></span>](device-management-roadmap-microsoft-365.md)

[<span data-ttu-id="5db71-142">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="5db71-142">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="5db71-143">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="5db71-143">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)

