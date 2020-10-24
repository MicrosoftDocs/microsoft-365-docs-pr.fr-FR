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
description: Découvrez comment Contoso utilise Microsoft Intune dans Microsoft 365 pour entreprise pour gérer ses appareils et les applications qui s’y exécutent.
ms.openlocfilehash: 6d7783e8c2d9b78b63bf9eefe761fbc52d0b280f
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48753992"
---
# <a name="mobile-device-management-for-contoso"></a><span data-ttu-id="ef231-103">Gestion des appareils mobiles pour Contoso</span><span class="sxs-lookup"><span data-stu-id="ef231-103">Mobile device management for Contoso</span></span>

<span data-ttu-id="ef231-104">Microsoft 365 pour Enterprise inclut Intune et un ensemble de services Azure qui prennent en charge la gestion et la sécurité des applications et des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ef231-104">Microsoft 365 for enterprise includes Intune and a set of Azure services that support mobile device and application management and security.</span></span>

<span data-ttu-id="ef231-p101">Contoso possède un grand nombre d’employés à extension mobile. Certains d’entre eux ont des bureaux dans contoso et d’autres n’ont pas de bureau. Contoso a nécessité un moyen d’activer la productivité des employés tout en conservant les appareils, les données Contoso stockées sur ces appareils et le comportement de l’application sécurisé.</span><span class="sxs-lookup"><span data-stu-id="ef231-p101">Contoso has many mobile-enabled employees. Some have offices in Contoso locations, and some have no offices. Contoso needed a way to enable employee productivity but keep the devices, the Contoso data stored on those devices, and application behavior secure.</span></span>

## <a name="plan"></a><span data-ttu-id="ef231-108">Prévision</span><span class="sxs-lookup"><span data-stu-id="ef231-108">Plan</span></span>

<span data-ttu-id="ef231-109">Contoso a identifié les cas d’utilisation Intune suivants de la gestion des appareils mobiles pour Microsoft 365 pour les entreprises :</span><span class="sxs-lookup"><span data-stu-id="ef231-109">Contoso identified the following Intune use cases of mobile device management for Microsoft 365 for enterprise:</span></span>

- <span data-ttu-id="ef231-110">Protégez les messages électroniques et les données Exchange Online afin qu’ils puissent être utilisés en toute sécurité par les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ef231-110">Protect Exchange Online email and data so it can be safely accessed by mobile devices.</span></span>
- <span data-ttu-id="ef231-111">Implémentez un programme de mise à BYOD pour les employés de contoso.</span><span class="sxs-lookup"><span data-stu-id="ef231-111">Implement a bring-your-own-device (BYOD) program for Contoso employees.</span></span>
- <span data-ttu-id="ef231-112">Émettre des téléphones appartenant à l’organisation et des tablettes partagées à usage limité aux employés de contoso.</span><span class="sxs-lookup"><span data-stu-id="ef231-112">Issue organization-owned phones and limited-use shared tablets to Contoso employees.</span></span>

<span data-ttu-id="ef231-113">Contoso n’utilise pas Intune pour :</span><span class="sxs-lookup"><span data-stu-id="ef231-113">Contoso doesn't use Intune to:</span></span>

- <span data-ttu-id="ef231-114">Autoriser les employés à accéder en toute sécurité à Microsoft 365 à partir d’un kiosque public non géré.</span><span class="sxs-lookup"><span data-stu-id="ef231-114">Allow employees to securely access Microsoft 365 from an unmanaged public kiosk.</span></span>
- <span data-ttu-id="ef231-115">Protégez les données et les messages électroniques sur site afin qu’ils puissent être utilisés en toute sécurité par les appareils mobiles, car il n’existe pas de serveurs Microsoft Exchange locaux.</span><span class="sxs-lookup"><span data-stu-id="ef231-115">Protect on-premises email and data so it can be safely accessed by mobile devices, because there are no on-premises Microsoft Exchange servers.</span></span>

## <a name="deploy"></a><span data-ttu-id="ef231-116">Déployer</span><span class="sxs-lookup"><span data-stu-id="ef231-116">Deploy</span></span>

<span data-ttu-id="ef231-117">Voici la configuration de l’infrastructure de gestion des appareils mobiles de Contoso :</span><span class="sxs-lookup"><span data-stu-id="ef231-117">This is how Contoso set up their mobile device management infrastructure:</span></span>

- <span data-ttu-id="ef231-118">Définir Intune en tant qu’autorité de gestion des appareils mobiles (MDM) et utiliser Intune sur Azure pour administrer le contenu et gérer les appareils</span><span class="sxs-lookup"><span data-stu-id="ef231-118">Set Intune as the Mobile Device Management (MDM) authority, and use Intune on Azure to administer content and manage the devices</span></span>
- <span data-ttu-id="ef231-119">Les groupes Azure Active Directory (Azure AD) créés pour les paramètres d’enregistrement et d’Intune et les stratégies d’accès conditionnel basées sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="ef231-119">Created Azure Active Directory (Azure AD) groups for devices for enrollment and Intune settings and device-based Conditional Access policies</span></span>

  <span data-ttu-id="ef231-120">Pour plus d’informations, consultez la rubrique [stratégies d’accès conditionnel contoso](contoso-identity.md#conditional-access-policies-for-identity-and-device-access).</span><span class="sxs-lookup"><span data-stu-id="ef231-120">For more information, see [Contoso Conditional Access policies](contoso-identity.md#conditional-access-policies-for-identity-and-device-access).</span></span>

- <span data-ttu-id="ef231-121">Activation de la plateforme d’appareils Apple pour prendre en charge les employés avec iPad, iMac et iPhone, ainsi que les iPhone appartenant à l’entreprise</span><span class="sxs-lookup"><span data-stu-id="ef231-121">Enabled the Apple device platform to support employees with iPads, iMacs, and iPhones, and corporate-owned iPhones</span></span>
- <span data-ttu-id="ef231-122">Les politiques de conditions générales de Contoso ont été créées. Elles sont affichées pendant l’installation du portail de l’entreprise sur les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ef231-122">Created Contoso-specific terms and conditions policies, which are seen during the installation of the Company Portal for Contoso on mobile devices</span></span>
- <span data-ttu-id="ef231-123">Pour les appareils qui ne sont pas déployés, implémentez un ensemble de stratégies de gestion des applications mobiles (MAM) pour exiger l’authentification pour l’accès aux services Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ef231-123">For devices that aren't enrolled, implemented a set of Mobile Application Management (MAM) policies to require authentication for access to Microsoft 365 services</span></span>
- <span data-ttu-id="ef231-124">Des stratégies Intune ont été créées pour appliquer :</span><span class="sxs-lookup"><span data-stu-id="ef231-124">Created Intune policies that enforce:</span></span>
  - <span data-ttu-id="ef231-125">Applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="ef231-125">Allowed apps.</span></span>
  - <span data-ttu-id="ef231-126">Chiffrement de l’appareil pour empêcher les accès non autorisés.</span><span class="sxs-lookup"><span data-stu-id="ef231-126">Device encryption to help prevent unauthorized access.</span></span>
  - <span data-ttu-id="ef231-127">Un code confidentiel ou un mot de passe à six chiffres.</span><span class="sxs-lookup"><span data-stu-id="ef231-127">A six-digit PIN or password.</span></span>
  - <span data-ttu-id="ef231-128">Période d’inactivité-délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="ef231-128">An inactivity-timeout period.</span></span>
  - <span data-ttu-id="ef231-129">Protection antivirus et programmes malveillants et mises à jour de signature avec Windows Defender sur les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ef231-129">Antivirus and malware protection, and signature updates with Windows Defender on Windows 10 devices.</span></span>
  - <span data-ttu-id="ef231-130">Mises à jour automatiques sur les appareils Windows 10 qui incluent les dernières mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ef231-130">Automatic updates on Windows 10 devices that include the latest security updates.</span></span>
  - <span data-ttu-id="ef231-131">Envoi de certificats à des appareils gérés.</span><span class="sxs-lookup"><span data-stu-id="ef231-131">Pushing certificates to managed devices.</span></span>
  - <span data-ttu-id="ef231-p102">Une séparation claire des données professionnelles et personnelles. Les utilisateurs ou les administrateurs peuvent effacer de l’appareil les données d’entreprise sélectionnées, tout en conservant des données personnelles telles que des images, des comptes de messagerie personnels et des fichiers personnels.</span><span class="sxs-lookup"><span data-stu-id="ef231-p102">A clear separation of business and personal data. Users or admins can selectively wipe corporate data from the device, while leaving personal data such as pictures, personal email accounts, and personal files untouched.</span></span>

<span data-ttu-id="ef231-134">Contoso a déployé des PC et des smartphones et tablettes appartenant à la société en les ajoutant aux groupes d’appareils Intune appropriés.</span><span class="sxs-lookup"><span data-stu-id="ef231-134">Contoso enrolled deployed PCs and company-owned smartphones and tablets by adding them to the appropriate Intune device groups.</span></span> <span data-ttu-id="ef231-135">Ils ont également établi un programme BYOD pour les employés afin d’inscrire leurs appareils personnels.</span><span class="sxs-lookup"><span data-stu-id="ef231-135">They also established a BYOD program for employees to enroll their personal devices.</span></span> <span data-ttu-id="ef231-136">Les périphériques apportés reçoivent des stratégies Intune, qui génèrent des appareils gérés et sécurisés, ainsi que leurs applications.</span><span class="sxs-lookup"><span data-stu-id="ef231-136">Enrolled devices receive Intune policies, which results in managed and secured devices and their applications.</span></span> <span data-ttu-id="ef231-137">Les appareils qui ne sont pas s’inscrivent ont des stratégies de gestion des applications mobiles (MAM) qui spécifient les applications autorisées.</span><span class="sxs-lookup"><span data-stu-id="ef231-137">Devices that aren't enrolled have Mobile Application Management (MAM) policies that specify allowed applications.</span></span>

<span data-ttu-id="ef231-138">Voici l’architecture de déploiement de la gestion des appareils mobiles contoso.</span><span class="sxs-lookup"><span data-stu-id="ef231-138">Here is the Contoso mobile device management deployment architecture.</span></span>

![Infrastructure de déploiement de la gestion des appareils mobiles contoso](../media/contoso-mdm/contoso-mdm-fig1.png)

## <a name="next-step"></a><span data-ttu-id="ef231-140">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ef231-140">Next step</span></span>

<span data-ttu-id="ef231-141">Découvrez comment Contoso utilise les [fonctionnalités de protection des informations](contoso-info-protect.md) de Microsoft 365 pour Enterprise pour classer, identifier et protéger les biens numériques stratégiques au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="ef231-141">Learn how Contoso uses the [information protection capabilities](contoso-info-protect.md) of Microsoft 365 for enterprise to classify, identify, and protect crucial digital assets across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef231-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef231-142">See also</span></span>

[<span data-ttu-id="ef231-143">Gestion des appareils pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ef231-143">Device management for Microsoft 365</span></span>](device-management-roadmap-microsoft-365.md)

[<span data-ttu-id="ef231-144">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="ef231-144">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="ef231-145">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="ef231-145">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)

