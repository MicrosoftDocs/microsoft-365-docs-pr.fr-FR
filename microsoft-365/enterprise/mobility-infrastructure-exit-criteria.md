---
title: Critères de sortie de l’infrastructure de gestion des appareils mobiles
description: Microsoft 365 Enterprise inclut la gestion des appareils mobiles à l’aide de Microsoft Intune. Passez en revue les conditions requises et les conditions préalables, configurez Intune à l’aide de votre ressource Azure Active Directory, inscrivez iOS, macOS, Android et appareils Windows, déployer des applications, créer un profil, utiliser une stratégie de conformité et activer l’accès conditionnel pour les appareils mobiles gestion des appareils avec Microsoft 365 Enterprise.
keywords: Microsoft 365, Microsoft 365 entreprise, documentation Microsoft 365, gestion des appareils mobiles, Intune
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/03/2019
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.service: ''
ms.technology: ''
ms.assetid: fb4182e6-5e78-45d0-9641-d791c4519441
audience: ITPro
ms.custom: microsoft-intune
ms.openlocfilehash: e8f8f53224b334f92142e2c03ed05eaa9e38787a
ms.sourcegitcommit: d4aa94716b33e6c270ae7adfbdc4c19cf4a0087d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/03/2019
ms.locfileid: "37385721"
---
# <a name="mobile-device-management-infrastructure-exit-criteria"></a><span data-ttu-id="7a943-105">Critères de sortie de l’infrastructure de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="7a943-105">Mobile device management infrastructure exit criteria</span></span>

![Phase 5 : gestion des appareils mobiles](./media/deploy-foundation-infrastructure/mobiledevicemgmt_icon-small.png)

<span data-ttu-id="7a943-107">*Cela s’applique aux versions E3 et E5 de Microsoft 365 entreprise*</span><span class="sxs-lookup"><span data-stu-id="7a943-107">*This applies to the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="7a943-108">Assurez-vous que votre configuration remplit les conditions suivantes pour l’infrastructure de gestion des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7a943-108">Ensure that your configuration meets the following requirements for mobile device management infrastructure.</span></span>

- <span data-ttu-id="7a943-109">Intune est configuré, y compris la création d’utilisateurs et de groupes Azure Active Directory (Azure AD) pour appliquer les règles de votre organisation aux appareils.</span><span class="sxs-lookup"><span data-stu-id="7a943-109">Intune is set up, including the creation of Azure Active Directory (Azure AD) users and groups to apply your organization's rules for devices.</span></span>
- <span data-ttu-id="7a943-110">Vous avez inscrit des appareils dans Intune pour qu’ils reçoivent les stratégies que vous créez.</span><span class="sxs-lookup"><span data-stu-id="7a943-110">You have enrolled devices in Intune so that the devices can receive the policies you create.</span></span>
- <span data-ttu-id="7a943-111">Les applications sont ajoutées aux appareils pour permettre à vos utilisateurs d’accéder aux services cloud Microsoft 365 de votre organisation, comme Exchange Online et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="7a943-111">Apps are added to devices so your users get access to your organization's Microsoft 365 cloud services, such as Exchange Online and SharePoint Online.</span></span>
- <span data-ttu-id="7a943-112">Les fonctionnalités et les paramètres sont configurés et appliqués à vos appareils à l’aide des utilisateurs et des groupes Azure AD créés. Parmi ces fonctionnalités et paramètres peuvent figurer l’activation de l’antivirus et la limitation de certaines applications.</span><span class="sxs-lookup"><span data-stu-id="7a943-112">Features and settings are configured and applied to your devices using the Azure AD users and groups you create, which might include enabling anti-virus and restricting specific apps.</span></span>
- <span data-ttu-id="7a943-113">Des stratégies de conformité sont en place pour exiger un pare-feu ou une longueur de mot de passe sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="7a943-113">Compliance policies are in place to require a firewall or a password length on a device.</span></span> <span data-ttu-id="7a943-114">Si les appareils ne sont pas conformes, l’accès conditionnel bloque l’accès aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7a943-114">If devices aren't compliant, Conditional Access blocks access to your organization's data.</span></span>

## <a name="results-and-next-steps"></a><span data-ttu-id="7a943-115">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7a943-115">Results and next steps</span></span>

<span data-ttu-id="7a943-116">Vos appareils sont intégrés dans Intune et configurés avec les stratégies appropriées.</span><span class="sxs-lookup"><span data-stu-id="7a943-116">Your devices are enrolled in Intune and configured with the appropriate policies.</span></span>

|||
|:-------|:-----|
|![Phase 6 : Protection des informations](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)| <span data-ttu-id="7a943-118">Si vous suivez les phases du déploiement de bout en bout de Microsoft 365 entreprise, votre phase suivante est la protection des [informations](infoprotect-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="7a943-118">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [information protection](infoprotect-infrastructure.md).</span></span> |
