---
title: Gestion des appareils mobiles pour Contoso
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Comprendre comment Contoso utilise Microsoft Intune dans Microsoft 365 entreprise pour gérer ses appareils et les applications qui s’exécutent sur ces appareils.
ms.openlocfilehash: 6d7783e8c2d9b78b63bf9eefe761fbc52d0b280f
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48753992"
---
# <a name="mobile-device-management-for-contoso"></a><span data-ttu-id="48176-103">Gestion des appareils mobiles pour Contoso</span><span class="sxs-lookup"><span data-stu-id="48176-103">Mobile device management for Contoso</span></span>

<span data-ttu-id="48176-104">Microsoft 365 entreprise inclut Intune et un ensemble de services Azure qui prise en charge la gestion et la sécurité des appareils mobiles et des applications.</span><span class="sxs-lookup"><span data-stu-id="48176-104">Microsoft 365 for enterprise includes Intune and a set of Azure services that support mobile device and application management and security.</span></span>

<span data-ttu-id="48176-105">Contoso compte de nombreux employés à mobilité fixe.</span><span class="sxs-lookup"><span data-stu-id="48176-105">Contoso has many mobile-enabled employees.</span></span> <span data-ttu-id="48176-106">Certains ont des bureaux à Contoso et d’autres n’ont pas de bureau.</span><span class="sxs-lookup"><span data-stu-id="48176-106">Some have offices in Contoso locations, and some have no offices.</span></span> <span data-ttu-id="48176-107">Contoso avait besoin d’un moyen pour activer la productivité des employés, tout en maintenant les appareils, les données Contoso stockées sur ces appareils et le comportement des applications sécurisés.</span><span class="sxs-lookup"><span data-stu-id="48176-107">Contoso needed a way to enable employee productivity but keep the devices, the Contoso data stored on those devices, and application behavior secure.</span></span>

## <a name="plan"></a><span data-ttu-id="48176-108">Prévision</span><span class="sxs-lookup"><span data-stu-id="48176-108">Plan</span></span>

<span data-ttu-id="48176-109">Contoso a identifié les cas d’utilisation Intune suivants de la gestion des appareils mobiles pour Microsoft 365 entreprise :</span><span class="sxs-lookup"><span data-stu-id="48176-109">Contoso identified the following Intune use cases of mobile device management for Microsoft 365 for enterprise:</span></span>

- <span data-ttu-id="48176-110">Protégez Exchange Online courrier électronique et les données afin qu’ils soient accessibles en toute sécurité par les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="48176-110">Protect Exchange Online email and data so it can be safely accessed by mobile devices.</span></span>
- <span data-ttu-id="48176-111">Implémentez un programme BYOD (Bring-your-own-device) pour les employés de Contoso.</span><span class="sxs-lookup"><span data-stu-id="48176-111">Implement a bring-your-own-device (BYOD) program for Contoso employees.</span></span>
- <span data-ttu-id="48176-112">Émettre des téléphones et des tablettes partagées à usage limité pour les employés de Contoso.</span><span class="sxs-lookup"><span data-stu-id="48176-112">Issue organization-owned phones and limited-use shared tablets to Contoso employees.</span></span>

<span data-ttu-id="48176-113">Contoso n’utilise pas Intune pour :</span><span class="sxs-lookup"><span data-stu-id="48176-113">Contoso doesn't use Intune to:</span></span>

- <span data-ttu-id="48176-114">Autoriser les employés à accéder en toute sécurité Microsoft 365 à partir d’une borne publique non sécurisée.</span><span class="sxs-lookup"><span data-stu-id="48176-114">Allow employees to securely access Microsoft 365 from an unmanaged public kiosk.</span></span>
- <span data-ttu-id="48176-115">Protégez le courrier électronique et les données locaux afin qu’ils soient accessibles en toute sécurité par les appareils mobiles, car il n’existe aucun serveur Microsoft Exchange local.</span><span class="sxs-lookup"><span data-stu-id="48176-115">Protect on-premises email and data so it can be safely accessed by mobile devices, because there are no on-premises Microsoft Exchange servers.</span></span>

## <a name="deploy"></a><span data-ttu-id="48176-116">Déployer</span><span class="sxs-lookup"><span data-stu-id="48176-116">Deploy</span></span>

<span data-ttu-id="48176-117">Voici la configuration de l’infrastructure de gestion des appareils mobiles de Contoso :</span><span class="sxs-lookup"><span data-stu-id="48176-117">This is how Contoso set up their mobile device management infrastructure:</span></span>

- <span data-ttu-id="48176-118">Définir Intune comme autorité de gestion des périphériques mobiles (MDM) et utiliser Intune sur Azure pour administrer le contenu et gérer les appareils</span><span class="sxs-lookup"><span data-stu-id="48176-118">Set Intune as the Mobile Device Management (MDM) authority, and use Intune on Azure to administer content and manage the devices</span></span>
- <span data-ttu-id="48176-119">Création Azure Active Directory groupes (Azure AD) pour les appareils pour l’inscription, les paramètres Intune et les stratégies d’accès conditionnel basé sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="48176-119">Created Azure Active Directory (Azure AD) groups for devices for enrollment and Intune settings and device-based Conditional Access policies</span></span>

  <span data-ttu-id="48176-120">Pour plus d’informations, voir [Stratégies d’accès conditionnel Contoso.](contoso-identity.md#conditional-access-policies-for-identity-and-device-access)</span><span class="sxs-lookup"><span data-stu-id="48176-120">For more information, see [Contoso Conditional Access policies](contoso-identity.md#conditional-access-policies-for-identity-and-device-access).</span></span>

- <span data-ttu-id="48176-121">A activé la plateforme d’appareils Apple pour prendre en charge les employés avec des iPad, des iMacs et des iPhone, ainsi que des iPhones d’entreprise</span><span class="sxs-lookup"><span data-stu-id="48176-121">Enabled the Apple device platform to support employees with iPads, iMacs, and iPhones, and corporate-owned iPhones</span></span>
- <span data-ttu-id="48176-122">Les politiques de conditions générales de Contoso ont été créées. Elles sont affichées pendant l’installation du portail de l’entreprise sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="48176-122">Created Contoso-specific terms and conditions policies, which are seen during the installation of the Company Portal for Contoso on mobile devices</span></span>
- <span data-ttu-id="48176-123">Pour les appareils qui ne sont pas inscrits, implémenté un ensemble de stratégies de gestion des applications mobiles (MAM) pour exiger l’authentification pour l’accès Microsoft 365 services</span><span class="sxs-lookup"><span data-stu-id="48176-123">For devices that aren't enrolled, implemented a set of Mobile Application Management (MAM) policies to require authentication for access to Microsoft 365 services</span></span>
- <span data-ttu-id="48176-124">Des stratégies Intune ont été créées pour appliquer :</span><span class="sxs-lookup"><span data-stu-id="48176-124">Created Intune policies that enforce:</span></span>
  - <span data-ttu-id="48176-125">Applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="48176-125">Allowed apps.</span></span>
  - <span data-ttu-id="48176-126">Chiffrement de l’appareil pour empêcher l’accès non autorisé.</span><span class="sxs-lookup"><span data-stu-id="48176-126">Device encryption to help prevent unauthorized access.</span></span>
  - <span data-ttu-id="48176-127">Code confidentiel ou mot de passe à six chiffres.</span><span class="sxs-lookup"><span data-stu-id="48176-127">A six-digit PIN or password.</span></span>
  - <span data-ttu-id="48176-128">Période d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="48176-128">An inactivity-timeout period.</span></span>
  - <span data-ttu-id="48176-129">Protection antivirus et programmes malveillants, et mises à jour de signatures Windows Defender sur Windows 10 appareils.</span><span class="sxs-lookup"><span data-stu-id="48176-129">Antivirus and malware protection, and signature updates with Windows Defender on Windows 10 devices.</span></span>
  - <span data-ttu-id="48176-130">Les mises à jour automatiques Windows 10 appareils qui incluent les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="48176-130">Automatic updates on Windows 10 devices that include the latest security updates.</span></span>
  - <span data-ttu-id="48176-131">Le fait de pousser des certificats vers des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="48176-131">Pushing certificates to managed devices.</span></span>
  - <span data-ttu-id="48176-p102">Une séparation claire des données professionnelles et personnelles. Les utilisateurs ou les administrateurs peuvent effacer de l’appareil les données d’entreprise sélectionnées, tout en conservant des données personnelles telles que des images, des comptes de messagerie personnels et des fichiers personnels.</span><span class="sxs-lookup"><span data-stu-id="48176-p102">A clear separation of business and personal data. Users or admins can selectively wipe corporate data from the device, while leaving personal data such as pictures, personal email accounts, and personal files untouched.</span></span>

<span data-ttu-id="48176-134">Contoso a inscrit les PC déployés et les smartphones et tablettes d’entreprise en les ajoutant aux groupes d’appareils Intune appropriés.</span><span class="sxs-lookup"><span data-stu-id="48176-134">Contoso enrolled deployed PCs and company-owned smartphones and tablets by adding them to the appropriate Intune device groups.</span></span> <span data-ttu-id="48176-135">Ils ont également mis en place un programme BYOD pour que les employés inscrivent leurs appareils personnels.</span><span class="sxs-lookup"><span data-stu-id="48176-135">They also established a BYOD program for employees to enroll their personal devices.</span></span> <span data-ttu-id="48176-136">Les appareils inscrits reçoivent des stratégies Intune, ce qui entraîne la gestion et la sécurisation des appareils et de leurs applications.</span><span class="sxs-lookup"><span data-stu-id="48176-136">Enrolled devices receive Intune policies, which results in managed and secured devices and their applications.</span></span> <span data-ttu-id="48176-137">Les appareils qui ne sont pas inscrits ont des stratégies de gestion des applications mobiles (MAM) qui spécifient les applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="48176-137">Devices that aren't enrolled have Mobile Application Management (MAM) policies that specify allowed applications.</span></span>

<span data-ttu-id="48176-138">Voici l’architecture de déploiement de la gestion des appareils mobiles Contoso.</span><span class="sxs-lookup"><span data-stu-id="48176-138">Here is the Contoso mobile device management deployment architecture.</span></span>

![Infrastructure de déploiement de la gestion des appareils mobiles Contoso](../media/contoso-mdm/contoso-mdm-fig1.png)

## <a name="next-step"></a><span data-ttu-id="48176-140">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="48176-140">Next step</span></span>

<span data-ttu-id="48176-141">Découvrez comment Contoso utilise les fonctionnalités de [protection](contoso-info-protect.md) des informations de Microsoft 365 entreprise pour classifier, identifier et protéger les biens numériques essentiels au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="48176-141">Learn how Contoso uses the [information protection capabilities](contoso-info-protect.md) of Microsoft 365 for enterprise to classify, identify, and protect crucial digital assets across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="48176-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48176-142">See also</span></span>

[<span data-ttu-id="48176-143">Gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="48176-143">Device management for Microsoft 365</span></span>](device-management-roadmap-microsoft-365.md)

[<span data-ttu-id="48176-144">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="48176-144">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="48176-145">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="48176-145">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)

