---
title: Critères de sortie de l'infrastructure de gestion des appareils mobiles
description: Microsoft 365 Enterprise inclut la gestion des appareils mobiles à l'aide de Microsoft Intune. Passez en revue les conditions requises et les conditions préalables, configurez Intune à l'aide de votre ressource Azure Active Directory, inscrivez iOS, macOS, Android et appareils Windows, déployer des applications, créer un profil, utiliser une stratégie de conformité et activer l'accès conditionnel pour les appareils mobiles gestion des appareils avec Microsoft 365 Enterprise.
keywords: Microsoft 365, Microsoft 365 entreprise, documentation Microsoft 365, gestion des appareils mobiles, Intune
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 03/05/2019
ms.topic: article
ms.prod: microsoft-365-enterprise
ms.service: ''
ms.technology: ''
ms.assetid: fb4182e6-5e78-45d0-9641-d791c4519441
audience: ITPro
ms.custom: microsoft-intune
ms.openlocfilehash: 14f216fe352d9108fe69028731f4c94dfb9d19f7
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291231"
---
# <a name="mobile-device-management-infrastructure-exit-criteria"></a><span data-ttu-id="68eee-105">Critères de sortie de l'infrastructure de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="68eee-105">Mobile device management infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/mobiledevicemgmt_icon-small.png)

<span data-ttu-id="68eee-106">*Cela s'applique aux versions E3 et E5 de Microsoft 365 entreprise*</span><span class="sxs-lookup"><span data-stu-id="68eee-106">*This applies to the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="68eee-107">Assurez-vous que votre configuration remplit les conditions suivantes pour l'infrastructure de gestion des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="68eee-107">Ensure that your configuration meets the following requirements for mobile device management infrastructure.</span></span>

- <span data-ttu-id="68eee-108">Intune est configuré, y compris la création des utilisateurs et des groupes Azure AD, pour appliquer les règles de votre organisation à vos appareils.</span><span class="sxs-lookup"><span data-stu-id="68eee-108">Intune is set up, including the creation of Azure AD users and groups to apply your organization's rules for devices.</span></span>
- <span data-ttu-id="68eee-109">Vous avez inscrit des appareils dans Intune pour qu’ils reçoivent les stratégies que vous créez.</span><span class="sxs-lookup"><span data-stu-id="68eee-109">You have enrolled devices in Intune so that the devices can receive the policies you create.</span></span>
- <span data-ttu-id="68eee-110">Les applications sont ajoutées aux appareils pour permettre à vos utilisateurs d’accéder aux services cloud Microsoft 365 de votre organisation, comme Exchange Online et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="68eee-110">Apps are added to devices so your users get access to your organization's Microsoft 365 cloud services, such as Exchange Online and SharePoint Online.</span></span>
- <span data-ttu-id="68eee-111">Les fonctionnalités et les paramètres sont configurés et appliqués à vos appareils à l’aide des utilisateurs et des groupes Azure AD créés. Parmi ces fonctionnalités et paramètres peuvent figurer l’activation de l’antivirus et la limitation de certaines applications.</span><span class="sxs-lookup"><span data-stu-id="68eee-111">Features and settings are configured and applied to your devices using the Azure AD users and groups you create, which might include enabling anti-virus and restricting specific apps.</span></span>
- <span data-ttu-id="68eee-p102">Des stratégies de conformité sont implémentées pour exiger un pare-feu ou une longueur de mot de passe sur un appareil. Si des appareils ne sont pas conformes, l’accès conditionnel bloque l’accès aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="68eee-p102">Compliance policies are in place to require a firewall or a password length on a device. If devices aren't compliant, conditional access blocks access to your organization's data.</span></span>



## <a name="results-and-next-steps"></a><span data-ttu-id="68eee-114">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="68eee-114">Results and next steps</span></span>

<span data-ttu-id="68eee-115">Vos appareils sont intégrés dans Intune et configurés avec les stratégies appropriées.</span><span class="sxs-lookup"><span data-stu-id="68eee-115">Your devices are enrolled in Intune and configured with the appropriate policies.</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)| <span data-ttu-id="68eee-116">Si vous suivez les phases du déploiement de bout en bout de Microsoft 365 entreprise, votre phase suivante est la protection des [informations](infoprotect-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="68eee-116">If you're following the phases for the end-to-end deployment of Microsoft 365 Enterprise, your next phase is [information protection](infoprotect-infrastructure.md).</span></span> |
