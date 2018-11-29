---
title: Critères de sortie de l’infrastructure de gestion appareil mobile
description: Microsoft 365 entreprise inclut la gestion des appareils mobiles à l’aide de Microsoft Intune. Passez en revue les exigences et les conditions préalables, configurer Intune à l’aide de vos ressources Azure Active Directory, inscrivez iOS, Mac OS, Android et Windows appareils, déployer des applications, créer un profil de configuration, utilisez une stratégie de conformité et activer l’accès mobile conditionnelle gestion des périphériques avec Microsoft 365 pour entreprises.
keywords: Documentation Microsoft 365, Microsoft 365 pour entreprises, Microsoft 365, gestion des appareils mobiles, Intune
author: MandiOhlinger
ms.author: mandia
manager: dougeby
ms.date: 08/10/2018
ms.topic: article
audience: ITPro
ms.prod: microsoft-365-enterprise
ms.service: ''
ms.technology: ''
ms.assetid: fb4182e6-5e78-45d0-9641-d791c4519441
ms.custom: microsoft-intune
ms.openlocfilehash: b511052698f42a07df5fc25aeaad7fc7f00c2a6e
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867010"
---
# <a name="mobile-device-management-infrastructure-exit-criteria"></a><span data-ttu-id="6676b-105">Critères de sortie de l’infrastructure de gestion appareil mobile</span><span class="sxs-lookup"><span data-stu-id="6676b-105">Mobile device management infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/mobiledevicemgmt_icon-small.png)

<span data-ttu-id="6676b-106">*Cela s’applique aux versions de Microsoft 365 entreprise E3 et E5*</span><span class="sxs-lookup"><span data-stu-id="6676b-106">*This applies to the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

<span data-ttu-id="6676b-107">Avant de passer à la phase suivante du processus de déploiement, assurez-vous que votre configuration remplit les conditions suivantes pour l’infrastructure de gestion des appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="6676b-107">Before you move on to the next phase in the deployment process, ensure that your configuration meets the following requirements for mobile device management infrastructure.</span></span>

- <span data-ttu-id="6676b-108">Intune est configuré, y compris la création des utilisateurs et des groupes Azure AD, pour appliquer les règles de votre organisation à vos appareils.</span><span class="sxs-lookup"><span data-stu-id="6676b-108">Intune is set up, including the creation of Azure AD users and groups to apply your organization's rules for devices.</span></span>
- <span data-ttu-id="6676b-109">Vous avez inscrit des appareils dans Intune pour qu’ils reçoivent les stratégies que vous créez.</span><span class="sxs-lookup"><span data-stu-id="6676b-109">You have enrolled devices in Intune so that the devices can receive the policies you create.</span></span>
- <span data-ttu-id="6676b-110">Les applications sont ajoutées aux appareils pour permettre à vos utilisateurs d’accéder aux services cloud Microsoft 365 de votre organisation, comme Exchange Online et SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="6676b-110">Apps are added to devices so your users get access to your organization's Microsoft 365 cloud services, such as Exchange Online and SharePoint Online.</span></span>
- <span data-ttu-id="6676b-111">Les fonctionnalités et les paramètres sont configurés et appliqués à vos appareils à l’aide des utilisateurs et des groupes Azure AD créés. Parmi ces fonctionnalités et paramètres peuvent figurer l’activation de l’antivirus et la limitation de certaines applications.</span><span class="sxs-lookup"><span data-stu-id="6676b-111">Features and settings are configured and applied to your devices using the Azure AD users and groups you create, which might include enabling anti-virus and restricting specific apps.</span></span>
- <span data-ttu-id="6676b-p102">Des stratégies de conformité sont implémentées pour exiger un pare-feu ou une longueur de mot de passe sur un appareil. Si des appareils ne sont pas conformes, l’accès conditionnel bloque l’accès aux données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6676b-p102">Compliance policies are in place to require a firewall or a password length on a device. If devices aren't compliant, conditional access blocks access to your organization's data.</span></span>

## <a name="next-phase"></a><span data-ttu-id="6676b-114">Phase suivante</span><span class="sxs-lookup"><span data-stu-id="6676b-114">Next phase</span></span>

|||
|:-------|:-----|
|![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)| <span data-ttu-id="6676b-115">La phase suivante du processus de déploiement de bout en bout Microsoft 365 entreprise est [la protection des informations](infoprotect-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="6676b-115">Your next phase in the end-to-end deployment process for Microsoft 365 Enterprise is [information protection](infoprotect-infrastructure.md).</span></span> |
